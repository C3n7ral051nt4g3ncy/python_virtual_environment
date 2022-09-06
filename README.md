# Python Virtual Environment (virtualenv) 
### Python 🐍 : Working in a Virtual Environment - macOS

<br>

<img width="633" src="https://user-images.githubusercontent.com/104733166/186441960-6769e6e7-dfcb-4835-afd4-4a9dff3a8939.png">

<br>

# What is a virtual environment?
An environment such that the Python interpreter, libraries and scripts installed into it are **isolated from those installed in other virtual environments**.
Meaning each tool you have will be isolated from each other and won't conflict with each other, as part of your OS (operating system).

<br>

# Why set up a virtual environment?
You really don't have to be a python expert or developper to use a virtual environment, even though all Python Devs use a VE.<br>

Think about this for a second, you do a lot of OSINT and you love using all the best python tools, the problem is that you have accumulated 30 or 40 tools that start to conflict with each other and you find yourself writing/starting an issue on Github because your awesome OSINT python tool is no longer operational.

One OSINT python tool may require of you to install Package A version 1.0 to your python lib (Library), another OSINT tool may require you to install Package A version 2.2, you install the requirements, and now you find that your tools stop working because of conflicting packages/python libs.
<br>
How about not having these issues by isolating the tools? 🧠

<br>

<img width="633" height="433" src="https://user-images.githubusercontent.com/104733166/186442442-d13b5671-f57b-414e-8a6c-0ea14df6d85a.png">

*Image Above: Piotr Płoński, https://mljar.com*

<br>

# Install a Virtual Environment using Venv
Requirements: First of all, you need to have Python installed: https://www.python.org/downloads/

Install Virtual Environment Command:
```
$ pip3 install virtualenv
```
<br>

Now let's create your project/tool folder: (`mkdir` stands for `make directory`)
```
$ mkdir project-Osint1
```

```
$ cd project-Osint1
```
`cd` command = `change directory`

Now that the the `project-osint1` folder has been created, we have the luxury of choosing what python version we want to use in our virtual environment, and the virtual environment name.
We can do this with the following command: 

```
$ python3.9 -m venv myvenv
```
You can choose any python version and any name for your virtual environment,**it is recommended to keep it short and simple**.<br>
Remember **KISS**:💋**K**eep **I**t **S**imple **S**tupid


<img width="333" alt="Screen Shot 2022-08-24 at 14 29 21" src="https://user-images.githubusercontent.com/104733166/186418585-c762775b-83ac-42b7-88e0-404665a03278.png">

<br>

# Virtual Environment Activation 
Everything needed has been created, but we need to activate the virtual environment in order for it to be useable.
Activation command:
```
$ source myvenv/bin/activate
```
recap: `source <your virtual environment name>/bin/activate`

Let's check the Python Version:
Command:
```
$ python --version
```
<br>

<img width="333" src="https://user-images.githubusercontent.com/104733166/186422952-5ebba067-43e5-4449-bf33-e2517b6a4da5.png">

Let's check if everything is working correctly with one commmand:

```
$ pip list
```
This is an example I am using with the OSINT python tool called [Twayback](https://github.com/Mennaruuk/twayback), after the `pip list` command, we can see all the libs and requirements that only concern Twayback, which is isolated from the rest of the libs on my system.

<br>


<img width="333" alt="Screen Shot 2022-08-24 at 15 01 40" src="https://user-images.githubusercontent.com/104733166/186425943-3b5ba95b-8235-4f5e-8846-63aa43c3d761.png">

You may want to check the current version of virtualenv:

<br>

```
$ virtualenv --version
```

# Another way of creating a Virtual Environment:

Make sure Pip is up to date:

```
$ python3 -m pip install --upgrade pip
```

```
$ pip3 install virtualenv
```
```
$ virtualenv venv 
```
(or the name you choose instead of venv)

```
$ source venv/bin/activate 
```

# All is now ready for take-off 🚀
Success! ✅, your Virtual Environment has been created and is now activated, you can make the checks with the check commands given above, now install your python OSINT tools (git clone) , dependencies, requirements, libs etc..
You now have a much higher success rate with your OSINT Python tools and less chance of having to open an issue on Github , most of the issues that OSINT Analysts have is due to a lack of knowledge with Python, they keep adding dozens and dozens of tools on top of each other without isolating them, so the tools all conflict with each other, thus, creating a big messy salad of packages/libs all conflicting with one another. 


# Deactivation 
To Deactivate and return to the default sys environment, the command is KISS, I bet you can guess what the command is right? 🤔

```
$ deactivate
```

Enjoy using your Python 🐍 Virtual Environment ! 

