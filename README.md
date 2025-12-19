
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
  ```

* Server Adminstration

  [Fresh Ubuntu Server Installation](https://hackmd.io/@xtorker/Bk7b4jYKL)

  Docker User Namespace Remap Please read [this article](https://docs.docker.com/engine/security/userns-remap/) very carefully and understand everything in it. TLDR: We use `userns-remap` to avoid users (not a sudoer) to get the root permission on the host with commands executed inside the docker container.

  sodu command Audit (Installed on “teddy” only) We record all the commands executed begin with sudo. You can replay them via [this scripts](https://github.com/xtorker/replayUserAudit).

  [Firewall (ufw)](https://www.digitalocean.com/community/tutorials/ufw-essentials-common-firewall-rules-and-commands)
  [fail2ban](https://www.linode.com/docs/guides/using-fail2ban-to-secure-your-server-a-tutorial/)
  [Disk Management](https://blog.gtwang.org/linux/parted-command-to-create-resize-rescue-linux-disk-partitions/)

  * `df`
  * `lsblk`
  * `parted`
  * `mkfs`
  * `blkid`
  * `mount`

  NMSL Logo on teddy

  * `lolcat`
  * `motd`
  * put [this file](https://github.com/xtorker/Linux_server_motd_logo) under `/etc/update-motd.d/` (You can change the logo to whatever you want)
  * ASCII Generator

* x-window

  * Windows

    * Putty (Setup the x-client for you)
    * [VcXsrv](https://sourceforge.net/projects/vcxsrv/)

  put these line in your server `.bashrc` or `.zprofile`

  ```bash
  # YourIP:0.0 for default setting in VcXsrv
  # ‘0.0’ can be found in Windows system tray
  export DISPLAY=”140.114.xx.xx:0.0″
  ```

  replace with your public IP

  Remember to check the third option (Disable access control)

  ![](https://i.imgur.com/66aQuAe.png)

* bash, zsh

  * In case you forget what is shell, [this](https://www.tutorialspoint.com/unix/unix-what-is-shell.htm) is for you.
  * If you are familiar with bash (the default shell in Ubuntu) and wanna try something fancy to make your everyday life better, give zsh a try.
  * Personally, I recommend [zplug](https://github.com/zplug/zplug) as your first zsh framewrok.
  * [Here](https://github.com/xtorker/zsh_setting) is my own zsh setting if anyone want to get a quick start.
  * [ Rule of thumb ] Choose the plugin you need and make your own zsh setting

* screen, tmux
  [screen](https://linuxize.com/post/how-to-use-linux-screen/) Keep your command running in the background and control it whenever you want. Critical tool for your experiments that take long time to finish.
  tmux ([link1](https://linuxize.com/post/getting-started-with-tmux/), [link2](https://blog.gtwang.org/linux/linux-tmux-terminal-multiplexer-tutorial/)) Give you additional terminal within a single tab to make your life easier.

* Common issues on compiling

  * `$PATH`, `$LD_LIBRARY_PATH` is not correct
  * version mismatch on either linking library, compiler, driver, etc.
  * Files not found: make sure everything is in the right place.

* Debugging tool (gdb)

  [Good tutorial](https://developers.redhat.com/blog/2021/04/30/the-gdb-developers-gnu-debugger-tutorial-part-1-getting-started-with-the-debugger)

### Miscellaneous

* Slack

  * Professor will add you in our slack workspace, so you can use slack for communications
  * Download slack from their website according to your OS: [https://slack.com/downloads](https://slack.com/downloads)
  * Open the app and Enter the workspace: [https://aiinsnthu.slack.com](https://aiinsnthu.slack.com)
  * Use your formal name as the account name
  * Also download the mobile app from the app store

* Google Groups

  * Professor will add you in our google group, so you can send and receive mails and see all the group events
  * To send the mail to everyone, the address is [mailto:nmsl-all@googlegroups.com](mailto:nmsl-all@googlegroups.com)

  ![](https://i.imgur.com/9L63oPB.png)

* Google Calendar

  * Professor will add you in our google calendar, so you can check our lab events and book meeting time
  * Click the office hour event on google calendar will bring you to the reservation page

* How to write professional emails:

  * Check your emails often.

  * Include a clear, direct subject line.

  * Please use a professional email address. Here is a bad example: teddybear AT gmail.com .

  * Some of you may have more than one email account, please do forward all emails to your primary email account (so that you don’t check your account once per week).

  * Reply-all whenever possible. This will keep everyone in the loop (after all, we are a team).

  * Reply to your emails — even if (you think) the email wasn’t intended for you.

  * Be aware that people from different cultures speak and write differently.

  * Proofread every message (multiple times). For formal emails, run them by Grammarly.

  * Keep your fonts classic, or better make your email plain-text.

  * Double-check that you’ve selected the correct recipient.

  - Revised from an article@businessinsider

* 1-1 Meeting Reservation

  Step 1. Open your google calendar and click NMSL Office Hour (Graduate Students)

  ![](https://aiins.cs.nthu.edu.tw/wp-content/uploads/2021/11/1.png)

  Step 2. Click the appointment page

  ![](https://aiins.cs.nthu.edu.tw/wp-content/uploads/2021/11/2-1024x487.png)

  Step 3. Choose a time slot you want

  ![](https://aiins.cs.nthu.edu.tw/wp-content/uploads/2021/11/3-1024x480.png)

  Step 4. Click save

  ![](https://aiins.cs.nthu.edu.tw/wp-content/uploads/2021/11/5.png)

* Weekly reports

  You need to send weekly report to professor through email every Friday, the email name would be like: `[WR] Your Name`

  Here is the content format:

  ![](https://i.imgur.com/G7dfwAO.png)

  Examples of not-very-useful todo tasks:

  * Finish MM homework #2 <— has nothing or very little to do with your research
  * Write my paper <— take longer than 4 hours to complete, break it down
  * Read some papers <— tell me which papers you are reading
  * Read more papers <— define more

  Here are the more meaningful and get-to-the-points todo tasks:
  Todo:

  1. apply different numbers of features/factors
  2. add features as factors for IS
  3. add references to related work
  4. sec. 3.1 and results writeup

* How to use projector

  * Windows

    1. Connect to the projector’s Wi-Fi (Wi-Fi name and password will be displayed on the projection screen when no any device use it)
    2. Open setting `System/Display/Multiple Displays` **Connect to a wireless display**
       ![Screenshot 2023-12-14 163848](https://hackmd.io/_uploads/ryYDbBd8a.png)
       ![Screenshot 2023-12-14 163859](https://hackmd.io/_uploads/B15O-rdL6.png)
       ![Screenshot 2023-12-14 163905](https://hackmd.io/_uploads/By2dWSuL6.png)
    3. If the connection is successful, you can then change projection options and project the screen just like using a regular wired projector
       ![Screenshot 2023-12-14 165622](https://hackmd.io/_uploads/H1qHrHdIT.png)
  * Mac

* 研究生完全求生手冊

  * The purpose of reading this book is to help new students participate in the lab.
  * You can access this [book](https://nthu.primo.exlibrisgroup.com/discovery/fulldisplay?docid=alma990054645290206774&context=L&vid=886UST_NTHU:886UST_NTHU&lang=zh-tw&search_scope=NTHU_holding&adaptor=Local%20Search%20Engine&tab=LibraryCatalog&query=any,contains,%E7%A0%94%E7%A9%B6%E7%94%9F%E5%AE%8C%E5%85%A8%E6%B1%82%E7%94%9F%E6%89%8B%E5%86%8A&offset=0) through the NTHU library.
    ![](https://reading.udn.com/readingimg/covert_page/book/117715.jpg)

* Presentation slides

  For those who are going to present in the next week, you need to share with us your presentation topic in the last group meeting

  After presentation, please go to the second link and upload your presentation slides

  Group meeting presentation title and order:
  [https://docs.google.com/spreadsheets/d/1Nk8V5x8DWbpaQhKh91I0kbwN0Q7bTGSQV7qka4aVqMQ/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1Nk8V5x8DWbpaQhKh91I0kbwN0Q7bTGSQV7qka4aVqMQ/edit?usp=sharing)

  Group meeting presentation slides:
  [https://drive.google.com/drive/folders/1UejVCYAl_RIfriNZmQMx0F2hN1yuvfnw?usp=sharing](https://drive.google.com/drive/folders/1UejVCYAl_RIfriNZmQMx0F2hN1yuvfnw?usp=sharing)

  The file name of the slides would be like `NAME_YYDD`, for example, `TC_210623`

* How to create CV

  * reference to CV overleaf [template](https://www.overleaf.com/read/dprxndnfwrpc#08e4cf)
