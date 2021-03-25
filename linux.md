# Linux

## Q & A

Q1: What is the difference between the GUI and the CLI?\
A1: The GUI is the Graphical User Interface. That is where one can interact with the OS in a graphical way. The CLI is the Command Line Interface. That is where one can interact with the OS in the Terminal and can navigate with commands.

Q2: What is the difference between the **"ls"** and **"ll"** commands?\
A2: The terminal only lists the names of the folders and files, when we use **"ls"**, but when we use **"ll"** then then these are also listed: Permission, date, time and size.

Q3: How do we delete directories, that contain files/folders?\
A3: The "rm" only deletes files and **"rmdir"** only deletes empty folders, so we use the **"rm -r"** command.

Q4: How can we restore deleted files?\
A4: There is **NO** way of recovering files, that are deleted in the CLI.

Q5: What is the difference between **">"** and **">>"**?\
A5: **">"** completely replaces/overwrites the content of a file, while **">>"** pushes the new information below the content of the target file.

Q6: What is the difference between **"&&"** and **"||"**?\
A6: When **"&&"** is between commands, the next one will only execute while the one before runs, while using **"||"**, the next command will only run, if the previous one does **NOT** execute.

Q7: How can we view the content of multiple files in the same time?\
A7: With the **"cat"** command, like this: **"cat test.txt test_2.txt"**.

Q8: How do we create a file?\
A8: With the **"touch"** command, like this: **"test_file.md"**.

## Notes

21.03.24.

I managed to auto-hide the top bar. Turned out only a pc restart was needed, so the Tweak app would initialize the auto-hide feature. Wohoo! I wouldn't think a restart would be needed for such a minor change, but now I know.

**Some Terminal commands:**

- Terminal can be opened with Ctrl+Alt+T.

- Terminal can be cleared with "clear" or Ctrl+L.

- With the up arrow we can acces the last command we used. We can press it several times.

- Tab autofills commands.

- "pwd" prints the current working directory.

- "ls" lists what folders and files are in the current directory. "ls mrdanielharka/Documents" can be used to list files in a different directory.

- "ll" is similar to "ls", but give a more detailed list of items in the directory. Lists names, permission, date, time and size.


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
    - "mkdir "dir 1"" or "mkdir 'dir 1'" for a folder with a space.
- "touch" works similar to "mkdir", but creates a file.

- "whoami" tells us the username. Specially useful if we are using a different pc.

- "cat" Con**cat**enate (to link together) lets us see the content of a single or multiple files.
    - "cat test.m<span>d" or "cat test.m<span>d test_2.m<span>d"
    - ? and * are wildcard characters. Can be used on multiple files. These will achieve the same result:\
    cat test_1.txt test_2.txt\
    cat test_?.txt\
    cat test_*
- "less" works as a pager and helps us view bigger files. We can use the navigation keys, to go up and down. We quit with "q".
- "mv file.txt to_this_dir1" Moves a file to a different directory.
    - "mv file.txt test_1.txt dir1 dir1" The last argument is where the files will be moved.
    - "mv file_1.txt file_2.txt" renames the first file to the 2nd and keeps it in the same directory.
    - This works also on directories.
- "cp" is almost identical to "mv", but keeps a file in the source directory.
    - "cp file_1.md file_2.md" creates a copy in the same directory.
- "rm" removes files and "rmdir" removes empty directories. "rm -r" also removes directories, that have files or other directories within. **No "trash" folder in CLI!**
- ">" Redirection operator inputs (redirects) the content of a command or file to an other one.
- ">>" appends (adds) the content of a command or file to an other one.
- | or pipe helps us chain commands together, to use multiple ones at the same time.
- "&&" between commands runs the next n-th command if the one before does run.
- "||" between commands runs the next n-th command if the one before does NOT run.
- ";" between commands runs the next n-th command if the one before does or does NOT run.
- "man" followed by a command, give us a thorough desription of the chosen command. We exit with "q".
- "chmod" is used to change the mode (permissions) of a file/directory, by the item owner or the superuser. The two ways of specifying the mode are octal number representation and symbolic representation.
- "vi" lets us edit text files in Terminal. We save and quit by pressing ESC + ":wq" or NOT save and quit ESC + ":q".
- "sudo gedit file.m<span>d" lets us open a file outside of the Terminal.
- "sudo" lets us perform commands as a root/super user. We need to be cautious about what we run!
- Ctrl+D or "logout" to close the Terminal.

21.03.22.

The installation was pretty straightforward. My older PC seems to run Ubuntu 20.04.2.0 LTS without any issues. I installed VSCode and GitHub Desktop. The OS seems fine, but I don't like how I lose screen real estate due to the "useless" top bar. I prefer the Windows way of doing it, where all the programs, the date and the volume was at the same place. At least I could set the docker to auto-hide, so it's something.
