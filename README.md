# Use Action As Remote Using SSH

## How to Use
1. [Fork this repository.](https://github.com/lazycodebuilder/Ubuntu-Server.git)

2. Creating/Adding SSH Keys
    - open termux app and type: `pkg install openssh`
    - `ssh-keygen -t ed25519 -C "git@github.com:owner/Action-Remotely-Access.git"`
    - `cd /data/data/com.termux/files/usr/etc/ssh`
    - paste this line on termux `cat ssh_host_ed25519_key.pub` 
    - Select and copy the public key and paste (follow 2.1 steps)
    
2.1. [Adding a new Public SSH key to your GitHub account:](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?platform=windows)
     - In the upper-right corner of any page, click your profile photo, then click Settings.
     - In the "Access" section of the sidebar, click  SSH and GPG keys.
     - Click New SSH key or Add SSH key.
     
2.3. (Add the private SSH key to the repository triggering the Github Action:)[https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions]
     - paste this line on termux `cat ssh_host_ed25519_key` Now to add your private ssh key
     - In this repository, go to the `Settings` > `secrets and variables` > `action`
     - click on New repository secret
     - on name* section add `SSH_PRIVATE_KEY`. and on secret* section Add your ssh private key

3. Now You Can Operate Remotely
     - Go `Action` > `All workflows` > Click on Ubuntu-Server > click on `run workflow`
     - click on `running workflow` > `initializing environment`
     - tap > `Setup tmate session` scroll down little bit and copy `ssh htY8ttTpbANJtFwgHvK9NX5Sd@nyc1.tmate.io`
     - open termux app and paste
     - click 0 then q