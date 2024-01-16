## Accomplishments

1. **Create a GitHub Repository**
    - Created a remote Git repository on GitHub.
    - The repository is initially empty, serving as a place to keep and share code.

2. **Set Repository to Public**
    - Configured the repository visibility to public.

3. **Generating a New SSH Key**
    - Generated a new SSH key on the local machine.
    - Added the public key to GitHub account for SSH authentication.
    - Note: Post March 15, 2022, GitHub no longer supports DSA keys (ssh-dss). RSA keys must use a SHA-2 signature algorithm.

    **Steps:**
    - Open Git Bash.
    - Run `ssh-keygen -t ed25519 -C "your_email@example.com"`.
    - For legacy systems: `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`.
    - Follow prompts to generate public/private key pair.

4. **Adding SSH Key to ssh-agent**
    - Checked for existing SSH keys and generated a new one.
    - For GitHub Desktop users, cloning repositories does not require dealing with SSH keys.

    **Steps:**
    - Start ssh-agent in PowerShell: 
        ```
        Get-Service -Name ssh-agent | Set-Service -StartupType Manual
        Start-Service ssh-agent
        ```
    - Add SSH private key to ssh-agent: `ssh-add c:\Users\YOU\.ssh\id_ed25519`.

5. **Adding New SSH Key to GitHub Account**
    - SSH keys can be used for authentication, commit signing, or both.
    - As of March 15, 2022, GitHub improved security measures.

    **Steps:**
    - Copy SSH public key to clipboard: `$ clip < ~/.ssh/id_ed25519.pub`.
    - For Windows Subsystem for Linux (WSL), use `clip.exe`. If `clip` isn't working, manually copy the key.
    - On Windows Terminal or PowerShell, use alternative command: `$ cat ~/.ssh/id_ed25519.pub | clip`.
    - Navigate to GitHub Settings → SSH and GPG keys → Add New SSH key.
    - Add a descriptive label for the key and paste your public key.
    - Click Add SSH key and confirm account access if prompted.
