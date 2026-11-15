# Mission 2 – Become Comfortable with the Terminal

## Mission Objective

The objective of this mission was to learn how to use the Terminal to navigate folders, manage files, understand command options and pipes, and learn about package managers.

## Task 2.1 – Explore Basic Terminal Operations

| Operation / Command | What it does | What I observed |
|---|---|---|
| `pwd` – Current-directory display | Displays the full path of the current working directory. | It displayed the path of my project folder. |
| `ls` – Directory listing | Lists files and folders in the current location. | It showed the files and folders available in the directory. |
| `ls -l` – Detailed listing | Displays files with details such as permissions, size and modification date. | It displayed more details than the normal listing. |
| `cd ..` – Change directory | Moves to the parent directory. | My location changed to the folder one level above. |
| `mkdir terminal-practice` – Create directory | Creates a new folder. | A new folder named terminal-practice was created. |
| `touch terminal-practice/notes.txt` – Create empty file | Creates an empty text file. | The notes.txt file was created inside the practice folder. |
| `cp terminal-practice/notes.txt terminal-practice/copy.txt` – Copy file | Creates a copy of an existing file. | A separate copy named copy.txt appeared. |
| `mv terminal-practice/copy.txt terminal-practice/renamed.txt` – Move / rename file | Moves or renames a file. | The copied file was renamed to renamed.txt. |
| `cat terminal-practice/notes.txt` – Display file contents | Displays the contents of a text file. | It displayed the text stored in the original file. |

## Task 2.2 – Practise File Changes Safely

I created a folder named terminal-practice and worked inside it.
I created a text file, added two lines without removing the first line, displayed its contents, created a backup and renamed the backup.

**Commands used:**

```bash
echo "This is my first line." > terminal-practice/notes.txt
echo "This is my second line." >> terminal-practice/notes.txt
cat terminal-practice/notes.txt
cp terminal-practice/notes.txt terminal-practice/backup.txt
mv terminal-practice/backup.txt terminal-practice/notes-backup.txt
```

### Answers to the questions

**1. What is the difference between replacing a file's contents and adding text to the end?**

The `>` operator replaces the existing contents of a file, while `>>` adds new text at the end without removing the previous content.

**2. What is the difference between copying a file and moving a file?**

Copying creates a separate duplicate while keeping the original file. Moving transfers the file to another location or changes its name.

**3. What information does the current-directory display provide?**

It shows the full path of the directory I am currently working in.

**4. Why is a directory-listing operation useful?**

It helps me see the files and folders available in a directory and find the files I need.

## Task 2.3 – Understand Flags and Pipes

I compared normal and detailed directory listings using the following commands:

```bash
ls
ls -lah
ls -lah | head -n 5
```

### What I understood

- `-l` displays detailed file information.
- `-a` includes hidden files and directories.
- `-h` displays file sizes in a human-readable format.
- The pipe symbol (`|`) passes the output of one command to another.
- `head -n 5` displays only the first five lines of the output.

The normal listing showed visible files and folders, while the detailed listing provided additional information and included hidden files. Using the pipe helped limit the output to the first five lines.

## Task 2.4 – Understand Package Managers

A package manager is a tool used to install, update and remove software.

On macOS, Homebrew is a commonly used package manager. It helps manage software packages and their dependencies through Terminal.

**Commands used to check Homebrew:**

```bash
brew --version
brew list
```

**My observation:** 

Homebrew was installed, its version was 7.0.9 and I could see the different packages installed on my system, including Git, Python, NumPy, FFmpeg and Vim.

## Tools Used

- Terminal – To execute commands and manage files.
- Visual Studio Code – To write and organise documentation.
- Git – To track and commit changes.
- GitHub – To store the completed project.

## What I Understood

This mission helped me understand basic Terminal commands, file operations, command flags, pipes and the purpose of package managers. I also learned the difference between copying and moving files and between replacing and appending text.

## Difficulties Faced

I did not face any major difficulties while completing this mission. All the commands worked as expected, and I was able to complete the tasks successfully.

## Conclusion

I learned basic Terminal commands and how to manage files and folders more easily.