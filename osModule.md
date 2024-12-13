Use Cases of os Module:
File and Directory Operations:

You can perform tasks like creating, removing, and manipulating files and directories.
Example: Listing files in a directory, checking if a file exists, renaming files, and removing files.
Working with Environment Variables:

You can access or modify environment variables, which is useful for configuring application settings or retrieving system-level information.
Example: Getting the current user's environment variables.
Path Operations:

The module provides functions to manipulate file paths in a platform-independent way, which is essential for ensuring that your code works on different operating systems.
Example: Joining paths, getting file extensions, or extracting filenames from paths.
Process Management:

You can interact with the system's processes, such as running shell commands, launching processes, and getting the process ID.
Example: Executing shell commands using os.system().
System Information:

The module allows you to query various system-related details, such as the operating system name, current working directory, etc.
Example: Retrieving the current working directory.
Common Functions in os Module:
File Operations:

os.remove(path) – Deletes a file.
os.rename(src, dst) – Renames a file or directory.
os.mkdir(path) – Creates a new directory.
os.rmdir(path) – Removes a directory.
Path Operations:

os.path.join(path, *paths) – Joins one or more path components.
os.path.exists(path) – Returns True if the path exists.
os.path.isfile(path) – Checks if the path is a file.
os.path.isdir(path) – Checks if the path is a directory.
os.path.abspath(path) – Returns the absolute path of the given path.
Working with Environment Variables:

os.environ – A dictionary representing the user's environment variables.
os.getenv(key) – Returns the value of the environment variable key.
os.putenv(key, value) – Sets an environment variable.
Process Management:

os.system(command) – Executes a system command (shell command).
os.getpid() – Returns the current process ID.
Working Directory:

os.getcwd() – Returns the current working directory.
os.chdir(path) – Changes the current working directory to path.
Example Code Snippets:
1. File Operations:
python
Copy code
import os

# Create a new directory
os.mkdir('new_folder')

# Check if a file exists
if os.path.exists('new_folder'):
    print("Directory created successfully!")

# Rename a directory
os.rename('new_folder', 'renamed_folder')

# Remove a directory
os.rmdir('renamed_folder')
2. Working with Environment Variables:
python
Copy code
import os

# Get the value of an environment variable
home_dir = os.getenv('HOME')
print("Home Directory:", home_dir)

# Set an environment variable
os.putenv('MY_VAR', '123')

# Access the updated environment variable
print("MY_VAR:", os.getenv('MY_VAR'))
3. Path Operations:
python
Copy code
import os

# Join paths
path = os.path.join('folder', 'subfolder', 'file.txt')
print("Joined Path:", path)

# Check if a path is a file
if os.path.isfile(path):
    print(f"{path} is a file.")

# Get the absolute path
abs_path = os.path.abspath(path)
print("Absolute Path:", abs_path)
4. System Information and Process Management:
python
Copy code
import os

# Get the current working directory
current_dir = os.getcwd()
print("Current Working Directory:", current_dir)

# Execute a shell command
os.system('echo Hello, World!')

# Get the current process ID
pid = os.getpid()
print("Current Process ID:", pid)
