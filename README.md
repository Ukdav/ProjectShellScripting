# ProjectShellScripting

**Introduction to Shell Scripting in Linux**

Shell scripting is a powerful and fundamental aspect of Linux and Unix-like operating systems. 
It allows users and administrators to automate tasks, execute commands, and create customized solutions by writing scripts using shell programming languages like Bash, sh, etc.

At its core, a shell script is a text file containing a series of commands that can be executed in sequence. 
These scripts leverage the capabilities of the system's command-line interface, the shell, to perform a wide range of tasks, from simple file manipulation and text processing to complex system administration tasks.

**Shell scripting is a valuable skill for Linux users and administrators for several reasons:**

1. **Automation:** Shell scripts can automate repetitive tasks, making it easier to manage and maintain a Linux system.
   This includes tasks such as backups, log analysis, software installations, and user management.
   
2. **Customization:** Shell scripts allow users to create customized solutions tailored to their specific needs. You can build scripts to monitor server performance, deploy     
   applications, or set up development environments with just a few lines of code.

3. **Scripting Languages:** Linux provides access to various shell programming languages, such as Bash, which offer powerful features like loops, conditionals, functions, and the 
   ability to interact with system utilities and programs.

4. **Script Portability:** Shell scripts are highly portable. They can run on different Linux distributions and Unix-like systems with minor modifications, making them versatile tools 
   for system administrators and developers.

5. **Script Debugging:** Shell scripting provides tools for debugging and error handling, allowing you to identify and fix issues efficiently.

6. **Script Sharing:** The Linux community thrives on collaboration and sharing. Users often share their shell scripts and solutions with others, contributing to a rich ecosystem of 
   open-source tools.

In this realm of shell scripting, you can start with simple scripts and gradually build your skills to create more complex and sophisticated solutions. Whether you're a system administrator looking to automate routine tasks, a developer seeking to streamline your workflow, or just someone interested in learning more about Linux, shell scripting is a valuable skill to acquire. 

It empowers you to harness the full potential of the command line and make your Linux experience more efficient and productive.

**Let's write our first shell scripting:**

**Step 1:** On our terminal, open a folder called shell-scripting using the command *mkdir shell-scripting*. This will hold all the scripting we would write in this lesson.


**Step 2:** Create a file called user-input.sh using the command *touch user-input.sh*


**Step 3:** Inside copy and paste the block of code below: 


#!/bin/bash

#Prompt the user for their name
echo "Enter your name:"
read name

#Display a greeting with the entered name
echo "Hello, $name! Nice to meet you."

A little summary about the code block, the script will prompt for your name. when you input your name, it displays the text *hello! nice to meet you*

Also, the *#!/bin/bash* helps you specify the type of bash interpreter to be used to execute the script.

**Step 4:** Save your file

**Step 5:** Run the command *sudo chmod +x user-input.sh*

**Step 6:** Run the script using the command *./user-input.sh*

![first project](https://github.com/Ukdav/ProjectShellScripting/assets/139593350/f5b0cb53-884f-4b3e-b13d-42007cf8a933)

![nano bash](https://github.com/Ukdav/ProjectShellScripting/assets/139593350/71a2d5db-1732-43e9-acdd-94dc8af9c8fe)

![exec script](https://github.com/Ukdav/ProjectShellScripting/assets/139593350/5a2e0675-8207-44c3-bb2c-69374f0947b6)

# Directory Manipulation and Navigation

Directory manipulation and navigation are essential aspects of shell scripting on Linux. 

Shell scripts often need to interact with the file system, including creating, moving, deleting, and navigating directories. 

Understanding how to perform these operations allows you to automate file management tasks efficiently. Here are some key points on directory manipulation and navigation in shell scripting:

**Step 1:** Open a file name name *navigating_linux_filesystem.sh*

**Step 2:** Place code block into the file using nano command
sample code:

#!/bin/bash

#Display current directory
echo "Current directory: $PWD"

#Create a new directory
echo "Creating a new directory..."
mkdir my_directory
echo "New directory created."

#Change to the new directory
echo "Changing to the new directory..."
cd my_directory
echo "Current directory: $PWD"

#Create some files
echo "Creating files..."
touch file1.txt
touch file2.txt
echo "Files created."

#List the files in the current directory
echo "Files in the current directory:"
ls

#Move one level up
echo "Moving one level up..."
cd ..
echo "Current directory: $PWD"

#Remove the new directory and its contents
echo "Removing the new directory..."
rm -rf my_directory
echo "Directory removed."

#List the files in the current directory again
echo "Files in the current directory:"
ls

![navigate file](https://github.com/Ukdav/ProjectShellScripting/assets/139593350/eaaf1e1b-1471-4896-8e59-60951721b858)

![nano02](https://github.com/Ukdav/ProjectShellScripting/assets/139593350/95578cc2-5c95-481d-9c91-5701ff76a8c0)

# File Operations and Sorting in Shell Scripting

File operations and sorting are everyday tasks in shell scripting on Linux. Shell scripts allow you to manipulate files and sort their content, enabling you to automate data processing, report generation, and more. Here's an overview of file operations and sorting techniques in shell scripting:

in this lesson, we will write a simple shell scripting that focuses on file operations and sorting. This script will create three files (file1.txt, file2.txt. file2.txt). displays the files in their current order, sorting them Alphabetically, saves the sorted files in the sorted_file.txt, and displays the sorted files. remove the original files, rename the sorted files to sorted_files_sorted_alphabetically.txt, and finally display the contents of the final sorted file.

let us proceed by using the following steps below1:

**Step 1:** Open your terminal and create a file called sorting.sh using the command *sorting.sh*

**Step 2:** Copy and paste the code block into the file

#!/bin/bash

#Create three files
echo "Creating files..."
echo "This is file3." > file3.txt
echo "This is file1." > file1.txt
echo "This is file2." > file2.txt
echo "Files created."

#Display the files in their current order
echo "Files in their current order:"
ls

#Sort the files alphabetically
echo "Sorting files alphabetically..."
ls | sort > sorted_files.txt
echo "Files sorted."

#Display the sorted files
echo "Sorted files:"
cat sorted_files.txt

#Remove the original files
echo "Removing original files..."
rm file1.txt file2.txt file3.txt
echo "Original files removed."

#Rename the sorted file to a more descriptive name
echo "Renaming sorted file..."
mv sorted_files.txt sorted_files_sorted_alphabetically.txt
echo "File renamed."

#Display the final sorted file
echo "Final sorted file:"
cat sorted_files_sorted_alphabetically.txt

![sorting](https://github.com/Ukdav/ProjectShellScripting/assets/139593350/24c1defa-facb-4f51-8bae-ca010b49c173)

![nano 3](https://github.com/Ukdav/ProjectShellScripting/assets/139593350/60b7565c-0516-480b-b1c6-9954a2cc278e)

# Working with Numbers and Calculations

**Working with Numbers and Calculations in Shell Scripting**

Shell scripting on Linux allows you to perform various numerical calculations, manipulate numeric data, and automate mathematical operations. Here's a guide on working with numbers and calculations in shell scripting:

This script defines two variables num1 and num2 with numeric values, performs basic arithmetic operations (addition, subtraction, multiplication, division, and modulus), and displays the results. it also performs more complex calculations such as raising num1 to the power of 2 and calculating the square root of num2 and displaying those results as well.

Let's proceed by following the steps below:

**Step 1:** On our terminal create a file and call it calculation.sh using the command *touch calculation.sh*

**Step 2:** Copy and paste the code block on the vim page.

#!/bin/bash

#Define two variables with numeric values
num1=10
num2=5

#Perform basic arithmetic operations
sum=$((num1 + num2))
difference=$((num1 - num2))
product=$((num1 * num2))
quotient=$((num1 / num2))
remainder=$((num1 % num2))

#Display the results
echo "Number 1: $num1"
echo "Number 2: $num2"
echo "Sum: $sum"
echo "Difference: $difference"
echo "Product: $product"
echo "Quotient: $quotient"
echo "Remainder: $remainder"

#Perform some more complex calculations
power_of_2=$((num1 ** 2))
square_root=$(echo "$num2" | awk '{print sqrt($1)}')

#Display the results
echo "Number 1 raised to the power of 2: $power_of_2"
echo "Square root of number 2: $square_root"

**Step 3:** Set execute permission on calculations.sh using the command *sudo chmod +x calculations.sh*

**Step 4:** Run your script using this command *./calculations.sh*

![vim script editor page for calculation](https://github.com/Ukdav/ProjectShellScripting/assets/139593350/79ba7870-37e4-4440-862e-2609fc1614ce)

![script output for calculation](https://github.com/Ukdav/ProjectShellScripting/assets/139593350/3a84c34f-1b3d-477d-84ea-6c2b2a97d7c6)


# File Backing Up and Timestamping in Shell Scripting

File backup and timestamping are essential aspects of data management and version control. Shell scripting on Linux provides the flexibility to automate these tasks efficiently. Here's a guide on how to create shell scripts for file backup and timestamping:

This shell scripting example is focused on file backup and timestamp. As a DevOps Engineer backing up databases and other storage devices is one of the most common tasks you get to carry out.

This script defines the source directory and backup directory paths. it then creates a timestamp using the current date and time and a backup directory with the timestamp appended to its name. the script copies all files from the source directory to create the backup directory using the cp command with the  -r option for recursive copying. Finally, it displays a message indicating the completion of the backup process and shows the path of the backup directory with the timestamp.

Let's proceed using the steps below:

**Step 1:** On your terminal open a file backup.sh using the command *touch backup.sh*

**Step 2:** Copy and paste the code block below into the vim page.

#!/bin/bash

#Define the source directory and backup directory
source_dir="/home/ubuntu/testing"
backup_dir="/home/ubuntu"

#Create a timestamp with the current date and time
timestamp=$(date +"%Y%m%d%H%M%S")

# Create a backup directory with the timestamp
backup_dir_with_timestamp="$backup_dir/backup_$timestamp"

#Create the backup directory
mkdir -p "$backup_dir_with_timestamp"

#Copy all files from the source directory to the backup directory
cp -r "$source_dir"/* "$backup_dir_with_timestamp"

#Display a message indicating the backup process is complete
echo "Backup completed. Files copied to: $backup_dir_with_timestamp"


**Step 3:** Set execute permission on backup.sh using the command *sudo chmod +x backup.sh*

**Step 4:** Run your script using this command *./backup.sh*

![backup](https://github.com/Ukdav/ProjectShellScripting/assets/139593350/188438d8-c627-446d-9c6f-5b7657cae238)

![vim script editor page for calculation](https://github.com/Ukdav/ProjectShellScripting/assets/139593350/b365cd81-5a4d-4f33-bc66-45b8b1c8cd97)


# In Conclusion: Harnessing the Power of Shell Scripting

Shell scripting is a dynamic and indispensable tool in the realm of Linux and Unix-like operating systems. It empowers users, administrators, and developers to automate tasks, manipulate data, and efficiently manage their systems. As we conclude our exploration of shell scripting.































