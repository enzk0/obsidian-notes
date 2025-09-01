
Tasks:
- [x] Python Bootcamp Course
	- Completed on September 1, 2025 10:10am

- [ ] Install Frappe Framework using Frappe Docker

**Important Note:**

**Use this guide for this Training Course ONLY. There’s a dedicated Frappe Docker guide for the development of Wela Apps.**

**Pre-requisite:**

- Install Ubuntu into your machine (Sub-system or Dual-boot)
- Install Docker and Docker Compose
    - curl -sSL [https://get.docker.com/](https://get.docker.com) | sh
    - [Install Docker Compose](https://docs.docker.com/compose/install/linux/#install-the-plugin-manually)

**Steps :**

1. **Bootstrap Containers for development**
    1. **Clone Repository**

```
git clone https://github.com/frappe/frappe_docker.git
cd frappe_docker
```

1. [x] 1. Copy example devcontainer config from devcontainer-example to .devcontainer
        - cp -R devcontainer-example/ .devcontainer/
    2. [x] Copy example vscode config for devcontainer from development/vscode-example to development/.vscode. This will setup basic configuration for debugging.
        - cp -R development/vscode-example development/.vscode
    3. [ ] **Manually start containers**
        1. [x] enable permission
            1. sudo usermod -aG docker ${USER}
        2. Running the containers
            - docker compose -f .devcontainer/docker-compose.yml up -d
        3. And enter the interactive shell for the development container with the following command:
            - docker exec -e "TERM=xterm-256color" -w /workspace/development -it devcontainer-frappe-1 bash
    4. **Use VSCode Remote Containers extension (Optional)**
        1. Install [Dev Container](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) in your VS Code
        2. Install Remote - Containers for VSCode
            1. through command line code --install-extension ms-vscode-remote.remote-containers
            2. clicking on the Install button in the Vistual Studio Marketplace: [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
            3. View: Extensions command in VSCode (Windows: Ctrl+Shift+X; macOS: Cmd+Shift+X) then search for extension ms-vscode-remote.remote-containers
        3. After the extensions are installed, you can:
            1. Open frappe_docker folder in VS Code.
                1. code .
            2. Launch the command, from Command Palette (Ctrl + Shift + P) Remote-Containers: Reopen in Container. You can also click in the bottom left corner to access the remote container menu.
        4. Notes:
            1. The development directory is ignored by git. It is mounted and available inside the container. Create all your benches (installations of bench, the tool that manages frappe) inside this directory.
            2. Node v14 and v10 are installed. Check with nvm ls. Node v14 is used by default.