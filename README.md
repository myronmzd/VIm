Vim Quick Start Guide
This is a beginner-friendly guide to help you get started with Vim, a powerful text editor available on most Unix-based systems.

📦 Install Vim
To check if Vim is installed:

bash
Copy
Edit
vim --version
If not installed, you can install it using your package manager:

Ubuntu/Debian:

bash
Copy
Edit
sudo apt update && sudo apt install vim
RedHat/CentOS/Fedora:

bash
Copy
Edit
sudo yum install vim      # or
sudo dnf install vim
MacOS:

bash
Copy
Edit
brew install vim
📂 Open a File in Vim
bash
Copy
Edit
vim filename.txt
or

bash
Copy
Edit
vi filename.txt
If the file doesn't exist, Vim will create it upon saving.

✍️ Modes in Vim
Vim has several modes. The main ones:

Normal Mode (default when opening a file): navigate, delete, copy, etc.

Insert Mode (i, a, etc.): for typing/editing.

Visual Mode (v): for selecting text.

Command Mode (:): for running commands like :w, :q.

🔄 Switching to Insert Mode
To start editing a file:

Key	Action
i	Insert before the cursor
a	Insert after the cursor
I	Insert at the beginning of the line
A	Insert at the end of the line
o	Open a new line below cursor
O	Open a new line above cursor

❌ q or Q is not for editing! (It's used to record macros or enter Ex mode)

💾 Save & Exit
Inside Vim, press Esc and type:

Command	Description
:w	Save the file
:q	Quit (only if no changes made)
:wq	Save and quit
:x	Save and quit (like :wq)
:q!	Quit without saving

🔢 Enable Line Numbers
To show line numbers temporarily:

vim
Copy
Edit
:set number
To always enable it, add this to your ~/.vimrc file:

vim
Copy
Edit
set number
🔁 Undo and Redo
u — Undo last change

Ctrl + r — Redo (only in Normal mode)

📜 Visual Mode & Text Manipulation
Key	Action
v	Start visual mode
V	Line-wise visual mode
y	Copy (yank)
p	Paste after the cursor
P	Paste before the cursor
d	Delete selected text
dd	Delete the entire line
D	Delete from cursor to line end
r<char>	Replace character under cursor

🧭 Navigation
Key	Move...
h	Left
l	Right
j	Down
k	Up
w	Forward by word
b	Backward by word
0	To beginning of line
$	To end of line
gg	To beginning of file
G	To end of file
:n	To line number n

📁 Edit Vim Settings Permanently
Edit your ~/.vimrc file to configure Vim behavior:

bash
Copy
Edit
vim ~/.vimrc
Example config:

vim
Copy
Edit
set number
syntax on
set tabstop=4
set shiftwidth=4
set expandtab
✅ Tips
Always press Esc before issuing any command.

Use :help <command> in Vim to get help (e.g., :help :w).

Use ZZ to save and quit (:wq shortcut).

Use :!<shell command> to run shell commands from within Vim.
