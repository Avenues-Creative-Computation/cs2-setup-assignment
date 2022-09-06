# 💻 Workstation and GitHub Setup

## 🤓 Course overview and learning outcomes 

The goal of this assignment is to get your MacBook setup to write and run Python code and to give you a brief introduction to GitHub which we will be using to submit projects and assignments. 🚀

## Python

For the first half of the year, your work for this class will be written in Python.  We've chosen Python because you are already familiar with it. Instead of focusing on learning a new language, you will focus on deepening your knowledge of programming strategies and algorithms.

- [ ] Install the latest stable release of Python by clicking on this link and following the installer instructions: https://www.python.org/ftp/python/3.10.6/python-3.10.6-macos11.pkg

On Mac OS X, the default version of Python is Python 2.  Since Python 2 is soon to be deprecated, you will likely never need to run Python 2 (unless you are working on some old code).  We will use Python 3 for everything in this class.  Follow the instructions below to change your system's default to Python 3.

- [ ] Open a new Terminal
- [ ] Type the following into the command line to open the file `.zshrc` in TextEditor:
    ```
    open -e ~/.zshrc
    ```
- [ ] Add the following line to the bottom of the `.zshrc` file.
    ```
    alias python=/usr/local/bin/python3
    ```
- [ ] Save the file (`command+s`) and close TextEditor.
- [ ] Quit Terminal, then open a new Terminal.
- [ ] Type the following into the command line:
    ```
    python --version
    ```
    You should see `Python 3.10.6`.


## Visual Studio Code

We will use [Visual Studio Code (VSCode)](https://code.visualstudio.com/) as our IDE (interactive coding environment).  VSCode has a built-in terminal, debugging tools, and extensions that make completing and submitting your assignments easy.

- [ ] **Download and install Visual Studio Code from Self-Service**

### VSCode Extensions

Open VSCode and click on the extensions tab on the far left of your screen. Use the search bar to find and install the following extensions:
- [ ] **Python** (from Microsoft)
- [ ] **GitHub Classroom** (from GitHib)
- [ ] **Jupyter** (from Microsoft)

Once you have installed these extensions, quit Visual Studio Code and relaunch the app.


## :octocat: Git and GitHub

Git is a **distributed Version Control System (VCS)**, which means it is a useful tool for easily tracking changes to your code, collaborating, and sharing. With Git you can track the changes you make to your project so you always have a record of what you’ve worked on and can easily revert back to an older version if need be (like Version History in Google Docs). It also makes working with others easier—groups of people can work together on the same project and merge their changes into one final source!

GitHub is a way to use the same power of Git all online with an easy-to-use interface. It’s used across the software world and beyond to collaborate and maintain the history of projects.

## :octocat: Understanding the GitHub flow 

The GitHub flow is a lightweight workflow that allows you to experiment and collaborate on your projects easily, without the risk of losing your previous work.

### Repositories

A repository is where your project work happens--think of it as your project folder. It contains all of your project’s files and revision history.  You can work within a repository alone or invite others to collaborate with you on those files.

**:books: Each of your assignment and projects for Computer Science 2 will have its own repository.**

### Cloning 

When a repository is created with GitHub, it’s stored remotely in the ☁️. You can clone a repository to create a local copy on your computer and then use Git to sync the two. This makes it easier to fix issues, add or remove files, and push larger commits. You can also use the editing tool of your choice as opposed to the GitHub UI. Cloning a repository also pulls down all the repository data that GitHub has at that point in time, including all versions of every file and folder for the project! This can be helpful if you experiment with your project and then realize you liked a previous version more. 

**:books: When you start a project or assignment for class you will use GitHib Classroom to clone a template repository that contains instructions and all of the files needed for the project.**

To learn more about cloning, read ["Cloning a Repository"](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository). 

### Committing and pushing
**Committing** and **pushing** are how you can add the changes you made on your local machine to the remote repository in GitHub. That way your instructor and/or teammates can see your latest work when you’re ready to share it. You can make a commit when you have made changes to your project that you want to “checkpoint.” You can also add a helpful **commit message** to remind yourself or your teammates what work you did (e.g. “Added a README with information about our project”).

Once you have a commit or multiple commits that you’re ready to add to your repository, you can use the push command to add those changes to your remote repository. Committing and pushing may feel new at first, but we promise you’ll get used to it 🙂

**:books: When you are ready to submit an assignment or project you will commit and push your work to the GitHub repository.  GitHib classroom will notify me of your submission as well as tell us both whether your code has passed any tests I might setup for the assignment.**


## Setup your GitHib and GitHub Classroom account

- [ ] You will need a GitHib account associated with your Avenues Gmail account for this class.  Go to [github.com](https://github.com) and click `Sign up`.  Enter your Avenues Gmail address, then follow the on-screen instructions to finish setting up your account.
- [ ] Link your GitHub account to GitHub Classroom by following this link: https://classroom.github.com/a/RyX7DTSH and selecting your name from the class roster.
- [ ] In Visual Studio Code, click on the GitHub tab :octocat: in the sidebar.
- [ ] Under `CLASSROOMS` click `Sign In` and follow the on-screen instructions.
- [ ] You should see this assignment appear under the `CLASSROOMS` menu.  Click the folder icon to the right of the assignment to clone the assignment repository to your computer and open the repository folder in Visual Studio Code.

**Now you are ready to write some code!**


## Three ways to execute code in Visual Studio Code

There are three ways to execute Python code in Visual Studio Code.  Each way has its uses.  For this assignment you will write and execute the some simple programs all three ways.

### 1. Terminal-based REPL (read-evaluate-print-loop)
   
- [ ] In Visual Studio Code, open a new Terminal from the Terminal menu.
- [ ] On the command line type: `python`, and you will see the version of Python you are running followed by the `>>>` prompt.
- [ ] You can type any single line of valid Python code at the prompt and see the results printed beneath.  Try it...
    - Type `4 + 5` and press enter.
    - Type `[i for i in range(0,100) if i % 2 != 0]` and press enter.
- [ ] To exit the REPL environment you can press `command+z` or close the terminal.

### 2. Jupyter Notebook

Jupyter Notebooks are interactive notebooks designed for sharing computational documents on the web.  You may have seen Jupyter Notebooks on Google's CoLab.  They are also convenient places to write and execute short programs.

- [ ] Open the command pallet in Visual Studio Code by pressing `command+shift+p`.
- [ ] Type `Jupyter` into the search bar.
- [ ] Select `Create: New Jupyter Notebook`
- [ ] Save the Notebook as `test_jupyter.ipynb`
- [ ] You will see a single "cell" where you can type some code and run it independently of the rest of cells in the notebook.  Try it.  Paste the following code into the notebook cell.

    ```
    odds = [i for i in range(0,25) if i % 2 != 0]
    print('Printing even numbers...')
    for number in odds:
        print(number + 1, end=' ')
    ```
- [ ] You can create a new code cell by clicking the `+ Code` button at the top of the screen.  

I ofter use a Jupyter Notebook like a piece of scratch paper when I want to test out little bits of code before I include them in a larger project.

### 3. Run Python Files

The most common way you will execute code for this class is by executing a `.py` file.  Visual Studio Code includes a file browser that allows you to manage multiple files simultaneously while working on big projects.

- [ ] You should see the file explorer sidebar on the left of your screen.  If not, click on the file explorer tab (the top one).  It should be open to the `setup-your-name` folder.
- [ ] Click `File >> New File...` or press `command+n`.
- [ ] Save the file as `add2.py`.
- [ ] Write the following simple program in the new file:

    ```
    print('Enter two integers and I will tell you their sum.')
    a = int(input('Enter the first integer '))
    b = int(input('Enter the second integer '))
    print('The sum of', a, 'and', b, 'is', a + b)
    ```

- [ ] You can run the file by clicking the run button :arrow_forward:.  This will open a new Terminal and show you the output of your program.
- [ ] You can also run the program from a Terminal by typing `python add2.py`.

### Debugging

Visual Studio Code also provides you with a debugging interface.

- [ ] With your `add.py` file open, hover your mouse to the left of line 4 (the second `print` statement).
- [ ] Click on the red dot that appears to add a **breakpoint**.
- [ ] Click the dropdown next to the run button and select `Debug Python File`.  
This will run your code, but before executing the last `print` the program will pause and the sidebar will show you the current value of each variable.  Clever debugging can be a huge help when trying to hunt down errors in your code.
- [ ] Click the blue `Continue` button on the debug toolbar at the top of the screen to continue execution.  You can also stop or restart execution using the other tools on the debug toolbar.

## Submitting Projects and Assignments
You will submit assignments by **committing and pushing** your work to GitHub.

- [ ] In Visual Studio, click on the Source Control tab on the sidebar.  You will see a place to enter a message and a list of the changes you have made since cloning the repository or since your last commit.
- [ ] Next to your file `add2.py` click the `+` button to "stage" the changes in that file.
- [ ] In the message box, type `Completed assignment`
- [ ] Press the `Commit` button.  Your changes are now saved in the version history on your computer, but have **NOT** been pushed to GitHub.
- [ ] Click on the `•••` menu at the top of the source control sidebar.  Select `Pull, Push` then `Push`.  This will upload your committed changes to the remote GitHub repository and notify me that you have submitted the assignment.  You can also **push** from the command palette by pressing `command+shift+p`, typing `push`, then selecting `Git: Push`.


## 📚  Resources 
* [A short video explaining what GitHub is](https://www.youtube.com/watch?v=w3jLJU7DT5E&feature=youtu.be) 
* [Git and GitHub learning resources](https://docs.github.com/en/github/getting-started-with-github/git-and-github-learning-resources) 
* [Understanding the GitHub flow](https://guides.github.com/introduction/flow/)
* [Interactive Git training materials](https://githubtraining.github.io/training-manual/#/01_getting_ready_for_class)

