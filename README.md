# Orientation Materials – AIINS@NTHU

## New Students Please Read the Following Information

- [How to Google](#how-to-google-google-just-google-it)
- [How to read and write papers](#how-to-read-and-write-papers)
- [Coding](#coding)
- [Linux](#linux)
- [Miscellaneous](#miscellaneous)

### How to Google (Google, just Google it)

Rule of thumb: Use ENGLISH to search everything, get rid of any Chinese keyword.

### How to read and write papers

- [How to read paper](http://ccr.sigcomm.org/online/files/p83-keshavA.pdf)

- Google scholar
  - Google Scholar provides a simple way to broadly search for scholarly literature. Search across a wide variety of disciplines and sources: articles, theses, books, …
  - <https://scholar.google.com/>

- Zotero
  - Help you manage your paper, you can put the paper your find in zotero to manage them
  - Please also install the Better Bibtex for Zotero extension (<https://retorque.re/zotero-better-bibtex/>) to automatically generate the citation keys. Please change the citation key foramt into: `[auth:lower][year][veryshorttitle:lower]`.
  - <https://www.zotero.org/>

  ![](https://i.imgur.com/g94itfE.png)

- Visual Studio Code
  - vscode is a text editor. You can use it to write your paper and code
  - Note that vscode is a text editor, so you need to install compiler for your code if you want to compile your code
  - <https://code.visualstudio.com/>

- LaTex / BibTex
  - latex is the language for writing paper. You can use overleaf to get used to it
  - overleaf: <https://www.overleaf.com/>
  - You need to install latex compiler if you want to compile your latex code on your computer
  - Latex compiler: <https://www.latex-project.org/get/>
  - For convince,
    - Windows, linux: TeX Live
    - Mac: MacTeX

- bib File Writing Toturial
  - Basic Information
    - bib file contains all he references cited by your manuscript, each are in different formats according to their types: e.g., Journal:

      ```bibtex
      @article{MEVS03,
        author = {Anirban Mahanti and Derek Eager and Mary Vernon and David Sundaram-Stukel},
        title = {Scalable On-demand Media Streaming with Packet Loss Recovery},
        journal = {ACM Transactions on Networking},
        volume = {11},
        number = {2},
        pages = {195–209},
        year = {2003}
      }
      ```

    - Where to find the information required for the bib entries
      - Find the bibtex entry first:  
        ![](https://aiins.cs.nthu.edu.tw/wp-content/uploads/2022/12/bibtex1-300x219.png)
      - Revise the entry
        - verify the information via Google scholar or the conference page, e.g., missing or wrong information
        - make each entry follow the same rule

  - Common Rules
    - Key: the first letter of each authorʼs last name + published year (ex. YFFH17)
      - if there are more than 4 authors: YFFH+17
      - key conflicts: YFFH17a, YFFH17b
    - authors: connected with “and”
      - Fan, Ching-Ling and Yen, Shou-Cheng and Hsu, Cheng-Hsin
      - Ching-Ling Fan and Shou-Cheng Yen and Cheng-Hsin Hsu
    - Initial-Capitalized in title (when writing in the bib file)
    - pages: 13–23
    - `{}` for special terms, e.g., Internet, 3D, HEVC
    - Use opt as prefix to comment out the entry
      - `optmonth={April}` <- wonʼt show up in the compiled paper

  - Samples for Each Reference Type
    - Journal

      ```bibtex
      @article{MEVS03,
        author = {Anirban Mahanti and Derek Eager and Mary Vernon and David SundaramStukel},
        title = {Scalable On-demand Media Streaming with Packet Loss Recovery},
        journal = {ACM Transactions on Networking},
        volume = {11},
        number = {2},
        pages = {195–209},
        month = {April},
        year = {2003}
      }
      ```

      - no publisher entry, instead, move publisher (e.g., IEEE, ACM) to the head of journal name
      - require volume and number (issue)

    - Conference/workshop papers

      ```bibtex
      @inproceedings{LLGC11,
        author = {Yao Liu and Fei Li and Lei Guo and Songqing Chen},
        title = {A Measurement Study of Resource Utilization in {Internet} Mobile Streaming},
        booktitle = {Proc. of ACM International Workshop on Network and Operating Systems Support for Digital Audio and Video (NOSSDAVʼ11)},
        pages = {33–38},
        month = {June},
        year = {2011},
        address = {Vancouver, Canada}
      }
      ```

      - Proc. of
      - no publisher entry, instead, move IEEE or ACM to the head of booktitle
      - address:
        - in USA: `[CITY], [STATE abbr.]` (ex. Los Angeles, CA)
        - otherwise: `[CITY], [COUNTRY]` (ex. Vancouver, Canada)

    - URL

      ```bibtex
      @online{cisco_news,
        author = {{Cisco Inc.}},
        title = {Cisco Visual Networking Index: Forecast and Methodology, 2016-2021},
        note ={https://www.cisco.com/c/en/us/solutions/collateral/service-provider/visualnetworking-index-vni/complete-white-paper-c11-481360.html},
        year = {2017},
        lastaccessed ={April 26, 2018}
      }
      ```

      or

      ```bibtex
      @misc{cisco_news,
        author = {{Cisco Inc.}},
        title = {Cisco Visual Networking Index: Forecast and Methodology, 2016-2021},
        key = {Cisco Visual Networking Index: Forecast and Methodology, 2016-2021},
        year = {2017},
        note = {\url{https://www.cisco.com/c/en/us/solutions/collateral/serviceprovider/visual-networking-index-vni/complete-white-paper-c11-481360.html}}
      }
      ```

    - Book chapter:

      ```bibtex
      @incollection{Rezaei09,
        author = {Mehdi Rezaei},
        booktitle = {Mobile Multimedia Broadcasting Standards},
        title = {Video Streaming over {DVB-H}},
        chapter = {4},
        publisher = {Springer US},
        year = {2009},
        pages = {109–131},
        month = {November},
        editor = {Fa-Long Luo}
      }
      ```

      - require chapter, publisher, and editor entry
      - if you want to cite the whole book, then no chapter

    - Tech Report

      ```bibtex
      @techreport{ITUTJ247,
        type = {Standard},
        key = {ITU-T J.247},
        year = {2008},
        title = {Objective Perceptual Multimedia Video Quality Measurement in the Presence of a Full Reference},
        institution = {ITU Telecommunication Standardization Sector}
      }
      ```

      - standard, supplementary document, or non-published document

    - Thesis

      ```bibtex
      @mastersthesis{Nordland16,
        author = {Atle Nordland},
        title = {Compression of {3D} Media for {Internet} Transmission},
        school = {University of Oslo},
        year = {2016}
      }
      ```

      - masthersthesis, phdthesis

- SVN
  - subversion (svn) is a version control software. In our lab, we use it to do the version control for data of papers.
  - our svn server: https://nmsl.cs.nthu.edu.tw/svn/nmsl/
  - you need to install svn client to access data on svn server
  - We recommend svn tortoise for windows. It have GUI, so you use it easily if you are a beginner
  - For mac and linux system, you can install svn using command line
  - [Tutorial](https://aiins.cs.nthu.edu.tw/wp-content/uploads/2021/09/svn-tutorial.pdf)
    - Linux: `sudo apt install subversion`
    - Mac: `brew install svn`

- Inkscape
  - <https://inkscape.org/>
  - We use inkscape to draw figures for papers.
  - The reason we don’t use inkscape rather than ppt is the output of inkscape is .svg or .eps, which are format of Vector graphics. The Vector graphic is better than normal figure because it can provide you high visual quality when you zoom in. (like the following figure)

  ![](https://i.imgur.com/MUkO04f.png)

- Evaluation guideline

  [The hint wrote by ChengHsin](https://drive.google.com/file/d/1iojCJ1nAp4cKFdaNHA9J1eYJ8ePIlUrv/view?usp=sharing)

  > The evaluation design is crucial for we systems folks. I used to teach each of you individually when you are working on your research papers.
  >
  > This morning, I planned to put up a more comprehensive evaluation design for a paper we submitted to ICDCS in January. I then decided to write down the hints and ask the student author to redo her evaluation design instead. 🙂
  >
  > Please find my notes attached. *This is a mandatory reading material; please finish it, and discuss with me if you don’t understand any parts of it.*
  >
  > Hopefully, we will save some trial-and-error time when you work on your papers shortly.

- Matlab
  - we use matlab to plot the chart for our experiments.
  - you can follow this [website](https://learning.site.nthu.edu.tw/p/405-1319-113887,c11954.php?Lang=zh-tw) to install Matlab
  - tutorial: <https://www.cyclismo.org/tutorial/matlab/>
  - an example of [plotting a figure with curves and errorbars](https://aiins.cs.nthu.edu.tw/wp-content/uploads/2021/09/example-of-plotting-a-figure-with-curves-and-errorbars.pdf)

- Spell checker
  - You need to install spell checker to check your write-up
  - If you use vscode, vscode have spell checker extension

  ![](https://i.imgur.com/RZfK3Hg.png)

- Grammarly
  - Help you check your grammar
  - <https://app.grammarly.com/>

- Turnitin
  - Help you detect plagiarism
  - Every thesis and paper submission should go through Turnitin
  - Make sure that you don’t index your own submission to Turnitin database
  - Apply for your account: [English](https://learning.site.nthu.edu.tw/p/412-1319-7120.php?Lang=en) / [Chinese (Traditional)](https://learning.site.nthu.edu.tw/p/412-1319-6168.php?Lang=zh-tw)
  - <https://www.turnitin.com/>

### Coding

- Python
  - Jupyter Notebook

    Jupyter Notebook is an open-source web application. You can program, apply all visualization package, and even make a tutorial documents on Jupyter Notebook as long as using Python. Jupyter Notebook is very convenient when you want to quickly realize and demo your code including data cleaning, numerical simulation, machine learning, etc.

    [Video](https://aiins.cs.nthu.edu.tw/wp-content/uploads/2021/07/jupyter.mov)

    **Installation & run:**

    ```bash
    pip install jupyter
    jupyter notebook
    ```

    The jupyter notebook will be launched on localhost by default.

    **How to use:**

    - We are coding in the cell, which is the selected box area in the following figure. We can run each cell separately. All the variables and functions all shared in across the cells.

      ![](https://i.imgur.com/mhKJxq6.png)

    - Basic command:
      - Run current cell: `ctrl+R`
      - Run current cell and jump to the next cell: `shift+R`
      - Add cell above/below: select cell & type `A` / `B`
      - Remove cell: select cell & type `x`
    - You can write markdown in the notebook. This is useful when you are making coding documents. Nav bar > Cell > Cell Type > Markdown

    **Remote access:**

    Running our experiments on the powerful servers, which usually don’t have GUI, is a common case. Thus, we need to launch jupyter notebooks and access them remotely. There are two ways to do that:

    - Port Forwarding with SSH Tunnel:

      First, launch jupyter notebook on the server side. Note that you can do it with session-based tool, e.g., session or tmux, so that the data would not vanish even if you closed the connection to the server. (server w/ tmux)

      ![](https://i.imgur.com/R6frE9i.png)

      Second, do port forwarding with ssh on the **client side**.

      ```bash
      ssh -L port:<host>:<host_port> user@<SSH server address>
      ```

      (client)

      ![](https://i.imgur.com/tYcaaTx.png)

      By doing so, we can access the jupyter notebook on the localhost of client side.

    - Port Forwarding with *vscode* entension

      Install the Jupyter extension in vscode and just open your `.ipynb`

      ![](https://i.imgur.com/589bjob.png)

      This extension will take over all the things.

  - Common packets
    - pandas
      - Pandas is a Python package that we often use to organize and analyze our data before trainning models, visualizing information.
      - You can follow the [10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html) to take a quick look at it.
    - multiprocess
      - Python package. Leverage it on your large scale experiments.
      - Official document: [link](https://docs.python.org/3/library/multiprocessing.html)
    - subprocess
      - When you want to run shell command in you Python code, the recommended approach is subprocesses module.
      - Official API document: [link](https://docs.python.org/3/library/subprocess.html) (`os.system()` is an alternative way, however, subprocess module is more comprehensive.)
    - pathlib
      - pathlib is an object-oriented filesystem paths module, which is simpler than os moudle when you try to manuiplate file path in you Pyhton code. It encapsulates some of modules from os

      For example, to get the parent directory, in os moudle, you need:

      ```python
      os.path.dirname(os.path.dirname(os.getcwd()))
      ```

      However, in pathlib, you only need:

      ```python
      pathlib.Path.cwd().parent
      ```

    - argparser
      - When you want to pass parameters to your program, you can use argparser, which is the officially recommended module. It helps you define the type, optional or not, the default value, and the description of the arguments( –help ).
      - Official tutorial: [link](https://docs.python.org/3/howto/argparse.html)
    - matplotlib.pyplot
      - Matplotlib is a Python plotting library. You can use matplotlib in Python scripts, the Python and IPython shells, the Jupyter notebook, web application servers, and four graphical user interface toolkits.
      - It is a good plot tool which allow quick visualize you experiment result in Python. However, please don’t use matplotlib to plot figure which will be used in your paper. Please Use matlab if possible.
    - matplotlib+LaTeX+Anaconda
      - Tutorial: [link](https://hackmd.io/@chenyuanjie/r1b38VEfq)

- Regular Expression

- Git & Github

  Git is a free and open-source distributed version control tool. No matter you project is small or large, version control is important to make your project more efficient. When you work with a team, you need to ensure that everyone would not ruin the project when he/she does any modification on project. Even if the error occur, unlucky, you can still recover the project by few command. That is the power of version control.

  Even if you work alone, you also need it to backup your source code. Suppose your deadline is only one day left, and you are quite busy on coding at your machine without any backup and version control. With the pressure from Bear, you accidentally remove a crucial script (it calls Murphy’s Law, you know). At this moment, a command “git pull” would save you life without any effort.

  Free Git & Github learning resource: [link](https://w3c.hexschool.com/git/cfdbd310)

- HackMD

  We often use Hackmd to write the document, tutorial, project issue, and solution note. Just like what you see now. Here is a nice [HackMD tutorial Book](https://hackmd.io/c/tutorials/%2Fs%2Ftutorials)

- Comment your code

  Always place some *human readable descriptions* when you are coding. Because you never know when will you or your labmates need to require them in the future (three months or one year, probably). Here is a nice [article](https://realpython.com/python-comments-guide/#python-commenting-worst-practices) that teaches you how to comment Python in a good manner.

- Modularization

  Modularization is a essential technique in software design. Porper modularization keeps your code maintainable, readable, reliable. Modular programming is a software design technique to split your code into separate parts. These parts are called modules. Note that the dependency between modules should be minimize so that they can work independent without lots of noisy binding. A good modulized system build by several modules with more and less dependency. The executable application will be created by putting them together.

### Linux

- SSH

  [Simple Connection Guide](https://phoenixnap.com/kb/ssh-to-connect-to-remote-server-linux-or-windows#ftoc-heading-6)  
  [Comprehensive Guideline](https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys)

- Basic commands

  [Linux Commands 101](https://hackr.io/blog/basic-linux-commands)  
  [File Permission and Ownership](https://www.thegeekdiary.com/understanding-basic-file-permissions-and-ownership-in-linux/)  
  [Inpu/Output Redirection](https://www.geeksforgeeks.org/input-output-redirection-in-linux/)

  - `|` (pipe)
  - `grep`
  - `sort`
  - `find`
  - `awk`
  - `sed`
  - `locate`
  - `ld`
  - `which`
  - `tee`
  - `readlink`
  - `ln`

- GPU driver & CUDA

  Follow the document: <https://hackmd.io/4t7SbwIcSwukksWngapc8A?view>  
  If you are using PC, the GPU is often plugged in PCI-E. Oh, you need to shutdown your PC first, right? Or BBQ will be held on your motherboard.

- Virtual env (docker, conda, venv, multi-pass)

  [Docker](https://docs.docker.com/get-started/)  
  [conda (both python package and parts of apt package)](https://conda.io/projects/conda/en/latest/user-guide/getting-started.html)  
  [venv (python package only)](https://docs.python.org/3/tutorial/venv.html)  
  [multipass (virtual Ubuntu instance)](https://multipass.run/docs/working-with-instances)

- Install Times New Roman(Ubuntu)

  ```bash
  sudo apt install msttcorefonts -qq
  rm ~/.cache/matplotlib -rf
