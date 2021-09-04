This folder contains instructions for how to install necessary software on your laptop. After running these scripts, your laptop will be ready to interface with the TurtleBots. We are assuming you will run this on Ubuntu 18.04. YMMV on other distros. We also assume that you've generated an SSH key and added it to GitHub. If you don't think you've done this yet, following the steps [here](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh).
 
### Step 1
Open up a new terminal. You can do this my pressing `ctrl` + `shift` + `+` or `windows key` (`cmd` on a Mac) + `space` and searching for 'Terminal' . Run the following by typing each line in and hitting enter, one at a time.

* The following make sure your operating system is up to date. You'll want to run both of them.

```
sudo apt-get update
sudo apt-get upgrade
```

* Now you're almost ready to download the code in this repository. You'll want to save the code to your Documents folder (folder="directory" in Linux-speak). You'll do this by first navigating to the Documents directory, then downloading the code. You can use the command `cd` ("change directory") to change your *working directory* (the directory you're currently working in) to the Documents directory. We let the computer know where the Documents directory is relative to home (home is represented by `~`). If you want to read more about `cd`, you can do that [here](https://en.wikipedia.org/wiki/Cd_(command)).
```
cd ~/Documents
```

* We'll use a tool called git to copy (or "clone") it to your computer. More on [git](https://en.wikipedia.org/wiki/Git).
```
git clone git@github.com:UCincy-Robotics/turtlebot-setup.git
```

* chmod is a popular command for Unix-based systems. It was invented in 1971, and lets you change which users have access to a certain file. The term chmod comes from 'change mode'. You can read more about it [here](https://en.wikipedia.org/wiki/Chmod). 7 indicates someone who is receiving full access to read, write, and execute the file. Each 5 indicates someone who is receiving access to read and execute - but not write to - the file. In this case, the file owner has access to read/write/execute and member's of the file's group and all others are given read/execute access to the file.
```
chmod 755 ./install_ros_melodic.sh
```

* This last step actually runs (or "executes") the code in the file we just downloaded using wget. bash is the name of the shell most commonly used in Unix-based operating systems. It's name is an acronym standing for 'Bourne Again Shell', and replaced the Bourne Shell in 1989. You can read more about it [here](https://en.wikipedia.org/wiki/Bash_(Unix_shell)).
```
bash ./install_ros_melodic.sh
```

### Step 2
ROS and the TurtleBot tutorials depend on certain packages in order to work. In this step, we'll install those dependencies. 

* You already downloaded a file containing the command to install the dependencies, you just need to give yourself permission to execute the code in the file. Go ahead and execute
```
chmod 755 ./step_2.sh
```

* Now that you have permission to run the file, go ahead and execute it. Although we used `bash ./<script_name>.sh` before, you can actually shorten this to just:
```
./step_2.sh
```


### Step 3
The TurtleBots themselves depend on another set of packages.

* You can install them changing the file permissions:
```
chmod 755 ./step_3.sh
```

* And executing the file:
```
./step_3.sh
```

