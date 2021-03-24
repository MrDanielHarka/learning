# Linux

## Q & A

Q1: What is the difference between the GUI and the CLI?

A1: The GUI is the Graphical User Interface. That is where one can interact with the OS in an easy way. The CLI is the Command Line Interface. That is where one can interact with the OS in the Terminal.

Q2:

A2:

Q3:

A3:

Q4:

A4:

Q5:

A5:

## Notes

21.03.24.

I managed to auto-hide the top bar. Turned out only a pc restart was needed, so the Tweak app would initialize the auto-hide feature. Wohoo! I wouldn't think a restart would be needed for such a minor change, but now I know.

**Some Terminal commands:**

- Terminal can be opened with Ctrl+Alt+T.

- Terminal can be cleared with "clear" or Ctrl+L.

- "pwd" prints the current working directory.

- "ls" lists what folders and files are in the current directory. "ls mrdanielharka/Documents" can be used to list files in a different directory.

- "ll" 


- "cd" lets us change directory (navigate in the CLI). When used it takes us to the specified folder.
    - "cd example_document" moves the user to the example_document directory from the current one.
    - "cd .." takes us one directory up.
    - "cd /" takes us to the root directory.
    - It's possible to make multiple moves with one command. "cd mrdanielharka/Documents" or "cd ../.."
    - Only typing "cd" will take us to our user directory.

- "~" The tilde character uses our user directory for commands.

- "mkdir" makes a directory (creates a new folder). "mkdir mrdanielharka/new_dir" creates a new directory new_dir in mrdanielharka.
    - "mkdir dir1 dir2 dir3" creates 3 directories.
    - "mkdir -p dir4/dir5/dir6" is used to created sub-directories. ("-p" is an option/switch. These modify the way a command works.)
    - "mkdir "dir 1"" or "mkdir 'dor 1'" for a folder with a space.

- "whoami" tells us the username. Specially useful if we are using a different pc.

21.03.22.

The installation was pretty straightforward. My older PC seems to run Ubuntu 20.04.2.0 LTS without any issues. I installed VSCode and GitHub Desktop. The OS seems fine, but I don't like how I lose screen real estate due to the "useless" top bar. I prefer the Windows way of doing it, where all the programs, the date and the volume was at the same place. At least I could set the docker to auto-hide, so it's something.
