## Installation Guide for Blufin

- Create a new folder where you will house your toolbox
    
    ```bash
    mkdir Antigravity
    ```
- Create a toolbox enviroment same name as the directory you just made
    ```bash
    cd Antigravity
    toolbox create Antigravity
    ```
- Enter the toolbox and download mozila 
    ```bash
    toolbox enter Antigravity
    sudo dnf install firefox
    ```
- Install Antigravity
    - Add the repository to /etc/yum.repos.d
        ```
        sudo tee /etc/yum.repos.d/antigravity.repo << EOL
        [antigravity-rpm]
        name=Antigravity RPM Repository
        baseurl=https://us-central1-yum.pkg.dev/projects/antigravity-auto-updater-dev/antigravity-rpm
        enabled=1
        gpgcheck=0
        EOL
        ```
    - Update the package cache
        ```
        sudo dnf makecache
        ```
    - Install the package
        ```
        sudo dnf install antigravity
        ```
- Open the IDE
    ```
    antigravity
    ```

### Remenber every time you want to lanch the app you have to enter your toolbox you just created and when you are done using it close it again don't keep it open don't waste resources.