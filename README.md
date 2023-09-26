# intro-bash-conda-git-linux-shell

Intro to Bash, Conda Git, Linux, and Shell

Theodore Nelson
 

1. **Bash:**
   - Bash stands for "Bourne Again Shell." It is a widely used command-line interface (CLI) and scripting language for Unix-based operating systems. Bash is the default shell for most Linux distributions and macOS. It provides a text-based interface for users to interact with the operating system, execute commands, and automate tasks through scripts.

2. **Conda:**
   - Conda is an open-source package management and environment management system that runs on Windows, macOS, and Linux. It is commonly used in the field of data science and scientific computing. Conda allows users to easily install, manage, and organize software packages and their dependencies, making it particularly useful for setting up isolated computing environments with specific software configurations.

3. **Git:**
   - Git is a distributed version control system designed for tracking changes in source code during software development. It allows multiple developers to collaborate on a project, each working on their own local copy of the code, and then merge their changes seamlessly. Git records a history of all changes, making it possible to revert to earlier versions if needed. It is widely used in the software development industry.

4. **Linux:**
   - Linux is a family of open-source Unix-like operating systems based on the Linux kernel. It is known for its stability, security, and flexibility. Linux provides a robust platform for a wide range of computing tasks, from servers and embedded systems to desktops and mobile devices. There are various distributions (distros) of Linux, such as Ubuntu, Fedora, and CentOS, each with its own package management system and user interface.

5. **Shell:**
   - In computing, a shell is a user interface that provides access to an operating system's services and resources. It allows users to interact with the system by entering commands, which are then executed by the operating system. Shells can be command-line interfaces (CLI) where commands are typed as text, or they can have graphical user interfaces (GUI) that provide a visual way to interact with the system. Bash, mentioned earlier, is an example of a popular command-line shell.


### Opening Terminal on Windows:

**Using Command Prompt:**
1. Press `Win + R` on your keyboard. This will open the "Run" dialog box.
2. Type `cmd` or `cmd.exe` and press Enter. This will open the Command Prompt, which is the default terminal on Windows.

**Using PowerShell:**
1. Press `Win + X` on your keyboard.
2. Select "Windows PowerShell" from the menu.

**Using Windows Terminal (if installed):**
1. You can search for "Windows Terminal" in the Start menu or search bar and click on it to open.

### Opening Terminal on macOS:

**Using Spotlight Search:**
1. Press `Cmd + Space` on your keyboard to open Spotlight Search.
2. Type "Terminal" and press Enter. This will open the Terminal app.

**Using Finder:**
1. Open the "Finder" application.
2. Go to the "Applications" folder.
3. Inside "Applications," find and open the "Utilities" folder.
4. Double-click on "Terminal" to open it.

**Using Launchpad:**
1. Open Launchpad from the Dock or by pressing `F4` on your keyboard (if available).
2. Find and click on the "Terminal" icon.

**Using Siri (macOS Catalina and later):**
1. Activate Siri by clicking the Siri icon in the menu bar or using a keyboard shortcut if enabled.
2. Say "Open Terminal" to Siri.


### 1. **ls** (List Files)

- **Basic Command**: Lists files and directories in the current directory.
- **With Parameters**:

	- `ls -l`: Provides a detailed listing with additional information like permissions, owner, size, and modification time.
    
	- `ls -a`: Lists all files, including hidden files (those starting with a dot).
    
	- `ls -h`: Makes file sizes human-readable (e.g., KB, MB).
    
	- `ls -t`: Sorts files by modification time, newest first.

### 2. **cd** (Change Directory)

- **Basic Command**: Allows you to change the current directory.
- **With Parameters**:

	- `cd ..`: Moves up one directory level.
    
	- `cd /path/to/directory`: Changes to a specific directory (replace `/path/to/directory` with the actual path).
    
	- `cd ~`: Changes to the user's home directory.

### 3. **mkdir** (Make Directory)

- **Basic Command**: Creates a new directory.
- **With Parameters**:

	- `mkdir directory_name`: Creates a directory with the specified name.
    
	- `mkdir -p /path/to/directory`: Creates directories recursively if they do not exist.

### 4. **touch** (Create Empty File)

- **Basic Command**: Creates a new, empty file.
- **With Parameters**:

	- `touch filename`: Creates a file with the specified name.
    
	- `touch file1 file2 file3`: Creates multiple files at once.

### 5. **rm** (Remove)

- **Basic Command**: Deletes files or directories.
- **With Parameters**:

	- `rm filename`: Deletes a file.
    
	- `rm -r directory_name`: Recursively deletes a directory and its contents.
    
	- `rm -rf directory_name`: Forcefully and recursively deletes a directory (use with caution).

### 6. **cp** (Copy)

- **Basic Command**: Copies files or directories.
- **With Parameters**:

	- `cp source destination`: Copies a file or directory from the source to the destination.
    
	- `cp -r source_directory destination_directory`: Copies a directory and its contents recursively.

### 7. **mv** (Move/Rename)

- **Basic Command**: Moves or renames files or directories.
- **With Parameters**:

	- `mv source destination`: Moves a file or directory from the source to the destination.
    
	- `mv old_name new_name`: Renames a file or directory.

### 8. **cat** (Concatenate and Display)

- **Basic Command**: Displays the contents of a file.
- **With Parameters**:

	- `cat filename`: Outputs the contents of the file to the terminal.
    
	- `cat file1 file2 > newfile`: Concatenates the contents of `file1` and `file2` into `newfile`.

### 9. **grep** (Global Regular Expression Print)

- **Basic Command**: Searches for patterns in files.
- **With Parameters**:

	- `grep pattern filename`: Searches for a specific pattern in a file.
    
	- `grep -r pattern /path/to/directory`: Searches for a pattern recursively in files within a directory.

### 10. **head/tail** (Display the Beginning/End of a File)

- **Basic Command**:

	- `head filename`: Displays the first few lines of a file.
    
	- `tail filename`: Displays the last few lines of a file.
    
- **With Parameters**:

	- `head -n 10 filename`: Displays the first 10 lines.
    
	- `tail -n 20 filename`: Displays the last 20 lines.



Install Conda: https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html 

1. **Open Terminal/Command Prompt:**
   - Open your terminal or command prompt window.

2. **Add Bioconda Channel:**
   - Use the following command to add the Bioconda channel to Conda:

   ```bash
    conda config --add channels defaults
    conda config --add channels bioconda
    conda config --add channels conda-forge
    conda config --set channel_priority strict
   ```

   This command adds Bioconda as a channel along with the default and Conda-Forge channels.

3. **Verify Channels:**
   - You can verify that the channels have been added by running:

   ```bash
   conda config --show channels
   ```

   It should display a list of channels including `defaults`, `bioconda`, and `conda-forge`.

4. **Update Channels (Optional):**
   - It's a good practice to update the channels to ensure you have the latest package information. You can do this with:

   ```bash
   conda update --all
   ```

5. **Verify Installation:**
   - You can verify that Bioconda is available by searching for a package that is commonly found in the Bioconda channel. For example, you can check for the package `samtools`:

   ```bash
   conda search samtools
   ```

   If the search results include `bioconda::samtools`, then Bioconda has been successfully added.

*RNA-Seq Program Installation*

```bash
#!/bin/bash

# Define base path
BASE_PATH="/Users/$USER/miniconda3/envs/"

# Create and activate sra-toolkit environment
conda create --name sra-toolkit -y
conda activate $BASE_PATH"sra-toolkit"
conda install sra-tools -y
conda deactivate

# Create and activate ascp environment
conda create --name ascp -y
conda activate $BASE_PATH"ascp"
conda install -c hcc aspera-cli -y
conda deactivate

# Create and activate fastqc environment
conda create --name fastqc -y
conda activate $BASE_PATH"fastqc"
conda install fastqc -y
conda deactivate

# Create and activate fastp environment
conda create --name fastp -y
conda activate $BASE_PATH"fastp"
conda install fastp -y
conda deactivate

# Create and activate aligners environment
conda create --name aligners -y
conda activate $BASE_PATH"aligners"
conda install star -y
conda deactivate

# Create and activate samtools environment
conda create --name samtools -y
conda activate $BASE_PATH"samtools"
conda install -c bioconda samtools -y
conda deactivate

# Create and activate featureCounts environment
conda create --name featureCounts -y
conda activate $BASE_PATH"featureCounts"
conda install -c bioconda subread -y
conda deactivate

# Create and activate multiqc environment
conda create --name multiqc -y
conda activate $BASE_PATH"multiqc"
conda install multiqc -y
conda deactivate
```
