## About Me - My Hobbies

### DJing 🎧

I have a deep passion for music, particularly in **DJing**. It's not just about playing tracks; it's an art of blending rhythms, creating a journey through soundscapes, and connecting with the audience. Here's what I love about DJing:

- **Creating Mixes**: Crafting seamless transitions between tracks, maintaining energy flow, and exploring various genres.
- **Engaging with Music**: DJing allows me to explore music deeply, understanding nuances and appreciating the craft behind each track.
- **Sharing Vibes**: There's nothing like seeing a crowd groove to the beats I play. It's a shared experience of joy and excitement.

### Drumming 🥁

Another hobby I'm deeply involved in is **drumming**. It's a physical, energetic, and expressive way to engage with music. Here's why I love it:

- **Rhythmic Foundation**: As a drummer, I enjoy being the backbone of the music, providing the rhythm that guides the other instruments.
- **Physical Activity**: Drumming is not just about rhythm; it's a physically engaging activity that requires coordination and energy.
- **Expressiveness**: Through drumming, I can express emotions non-verbally. It's a powerful way to communicate feelings through music.

---

These hobbies reflect my love for music and rhythm. They're not just pastimes; they're integral parts of who I am, providing a creative outlet and a way to connect with others.


## Class Accomplishments so far

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

#To Run Tests:

`npm run test`