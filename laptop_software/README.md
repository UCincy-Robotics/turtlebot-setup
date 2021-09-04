This folder contains instructions for how to install necessary software on your laptop. After running these scripts, your laptop will be ready to interface with the TurtleBots. We are assuming you will run this on Ubuntu 18.04. YMMV on other distros.

### Step 1
Open up a new terminal. You can do this my pressing `ctrl` + `shift` + `+` or `windows key` (`cmd` on a Mac) + `space` and searching for 'Terminal' . Run the following by typing each line in and hitting enter, one at a time.

* The following make sure your operating system is up to date. You'll want to run both of them.

```
sudo apt-get update
sudo apt-get upgrade
```

* This next line uses a tool called wget. It's popular tool for Unix-based systems. It was first released in 1996 and is part of the GNU project. You can read more about it [here](https://en.wikipedia.org/wiki/Wget). We use it to copy a file in this repository onto your computer.
```
wget https://raw.githubusercontent.com/UCincy-Robotics/turtlebot-setup/main/laptop_software/install_ros_melodic.sh
```

* chmod is a popular command for Unix-based systems. It was invented in 1971, and lets you change which users have access to a certain file. The term chmod comes from 'change mode'. You can read more about it [here](https://en.wikipedia.org/wiki/Chmod). Each 7 indicates someone who is receiving full access to read, write, and execute the file. In this case, the file owner, member's of the file's group, and all others are given full access to the file.
```
chmod 755 ./install_ros_melodic.sh
```

* This last step actually runs (or "executes") the code in the file we just downloaded using wget. bash is the name of the shell most commonly used in Unix-based operating systems. It's name is an acronym standing for 'Bourne Again Shell', and replaced the Bourne Shell in 1989. You can read more about it [here](https://en.wikipedia.org/wiki/Bash_(Unix_shell)).
```
bash ./install_ros_melodic.sh
```
