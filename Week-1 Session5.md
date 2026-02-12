# Week 1 – Session 5  
## GitHub Setup, SSH Collaboration & Copilot Integration

This live session covered the complete setup of Git and GitHub for collaboration in the Data Science course. It included creating a GitHub repository, setting up SSH authentication to securely connect the local machine with the remote repository, cloning the repository, committing changes, troubleshooting push errors, and integrating GitHub Copilot with VS Code.

---

## 1.Git Installation and Configuration

Check if Git is installed:

```bash
git --version
```

If not installed (Linux/WSL):

```bash
sudo apt update
sudo apt install git
```

Configure Git identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

---

## 2.Creating a GitHub Repository

- Logged into GitHub  
- Created a new repository  
- Provided repository name and visibility  
- Repository created as the remote source  

---

## 3.SSH Setup for Secure Communication

Generate SSH key:

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

Start SSH agent and add the key:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

Copy the public key:

```bash
cat ~/.ssh/id_ed25519.pub
```

Add the copied key in GitHub under  
**Settings → SSH and GPG Keys → New SSH Key**

Test the connection:

```bash
ssh -T git@github.com
```

---

## 4.Cloning and Working with the Repository

Clone using SSH:

```bash
git clone git@github.com:username/repository-name.git
cd repository-name
```

Check status:

```bash
git status
```

Stage and commit changes:

```bash
git add .
git commit -m "Initial commit"
```

Push changes to GitHub:

```bash
git push origin main
```

If needed, verify remote:

```bash
git remote -v
```

---

## 5.Linux / WSL Discussion

Linux or WSL was recommended for better compatibility with development tools and smoother workflow in data science environments.

---

## 6.GitHub Copilot Integration

GitHub Copilot was introduced as an AI coding assistant in VS Code.

- Install the Copilot extension  
- Sign in with GitHub  
- AI suggestions appear while coding  

It helps speed up development but requires review of generated code.

---

## 7.Pushing Generated Code

After generating or modifying code (including Copilot-assisted code):

```bash
git status
git add .
git commit -m "Added generated code"
git push origin main
```

This completes the full workflow from setup to collaboration and pushing updates to the remote repository.
