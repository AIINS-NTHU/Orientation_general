
# Guidelines for sharing NVIDIA GPUs

> 共用顯卡注意事項  
> These guidelines apply to machines with NVIDIA GPUs using CUDA.



## General Principle

Before starting a long training / inference job, or any experiments in general:

- Always check current GPU usage (GPU memory / VRAM + utilization).
- Prefer using free or lightly loaded GPUs.
- If all GPUs are busy, coordinate with current users (e.g., lab chat) instead of killing processes blindly (which is rude).
- If you must stop a runaway job, try to contact the process owner first and kill only the specific process, not the entire machine.
- If you think you need a different CUDA / driver setup, use a container or virtual environment (e.g., Conda, Docker) and do **not** change the system-wide driver or CUDA installation, as it may affect all users.


## Basics

### Check Current GPU Usage

```bash
nvidia-smi
```

### Periodically Monitor GPU Usage

```bash
watch -n 1 nvidia-smi  # refresh every 1 second
```

(`nvidia-smi dmon` also does the job but is more cumbersome to use.)

### Check Who's Using the GPUs

```bash
sudo fuser -v /dev/nvidia*
```

---

### Pin Your Job to Specific GPUs

```bash
CUDA_VISIBLE_DEVICES=0,1 python train.py
```

(or equivalently, put `export CUDA_VISIBLE_DEVICES=0,1` in your shell script for running jobs)

---

### Killing Zombie / Runaway Processes

1. Find the PID via `nvidia-smi` or `sudo fuser -v /dev/nvidia*`.
    
2. Confirm it with:
    
    ```bash
    ps -p PID -o pid,user,stime,cmd
    ```
    
3. Kill it:
    
    ```bash
    kill 12345      # polite attempt
    kill -9 12345   # only if the above does not work
    ```
    

---

### Getting CUDA & PyTorch Working

Please refer to:  
[https://syjintw.github.io/posts/cuda-and-pytorch/](https://syjintw.github.io/posts/cuda-and-pytorch/)
