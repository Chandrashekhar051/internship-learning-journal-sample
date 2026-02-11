# Week 1 – Session 3
## WSL, Linux File System and LLM Tool Setup

### Overview

In this session, I learned how WSL works internally, how Linux integrates with Windows, and how to efficiently use the terminal inside VS Code. The session also covered installing development tools like UV and configuring the LLM CLI to interact with GPT and Gemini models directly from the terminal.

---

## 1. WSL and System Architecture

- Understood the computer boot process.
- Learned how WSL2 uses lightweight virtualization.
- Studied the role of hypervisors in running multiple operating systems.
- Compared traditional virtual machines with WSL.
- Understood why WSL is efficient for development purposes.

---

## 2. Linux File System in WSL

### Key Directories

/        - Root directory  
/home    - User directories  
/etc     - Configuration files  
/var     - Logs and variable data  
/bin     - Essential system binaries  
/mnt     - Mounted Windows drives  

Accessing Windows drive from WSL:

cd /mnt/c

Learned that Linux follows a hierarchical structure starting from root (/), unlike Windows which uses drive letters.

---

## 3. Absolute and Relative Paths

Absolute Path Example:

cd /home/username/Documents

Relative Path Example:

cd Documents

Special symbols used:

.   - Current directory  
..  - Parent directory  
~   - Home directory  

---

## 4. Working in VS Code with WSL

Opened WSL:

wsl

Navigated to home directory:

cd ~

Created project folder:

mkdir session3  
cd session3  

Opened folder in VS Code:

code .

---

## 5. Linux Commands Practiced

pwd  
ls  
ls -la  
cd foldername  
cd ..  
mkdir project  
touch notes.txt  
rm notes.txt  
rm -r project  
clear  

Practiced file and directory operations inside the WSL terminal.

---

## 6. Installing and Using UV Tool

Updated system packages:

sudo apt update  
sudo apt upgrade -y  

Installed UV:

pip install uv 
or
curl -LsSf https://astral.sh/uv/install.sh | sh

Verified installation:

uv --version  

Created virtual environment:

uv venv  
source .venv/bin/activate  

Deactivated environment:

deactivate  

---

## 7. Installing LLM CLI Tool

Installed LLM using UV:

uv tool install llm  

Verified installation:

llm --version 

Checked plugins:

llm plugins  

---

## 8. Setting API Keys

Installs llm-gemini:

llm install llm-gemini

Set Gemini API key:

export GEMINI_API_KEY="your_api_key_here"  

Set OpenAI API key:

export OPENAI_API_KEY="your_api_key_here"  

Verified:

echo $OPENAI_API_KEY  

Made environment variable permanent:

nano ~/.bashrc  
source ~/.bashrc  

---

## 9. Running LLM Commands

Using GPT model:

llm -m gpt-4 "Explain Linux file system"  

Using Gemini model:

llm -m gemini-pro "What is WSL?"  

Interactive chat mode:

llm chat -m gpt-4  

---

## Key Learning Outcomes

- Understood WSL architecture and virtualization.
- Gained hands-on experience with Linux file system navigation.
- Practiced absolute and relative paths.
- Integrated VS Code with WSL environment.
- Installed and used UV package manager.
- Created Python virtual environments.
- Installed and configured LLM CLI.
- Set up API keys securely.
- Executed GPT and Gemini models from the terminal.

