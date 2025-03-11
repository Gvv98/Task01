# Install AlmaLinux 9 on Windows using Docker


This guide explains how to install and use **AlmaLinux 9** on Windows via **Docker**.

1. **Install Docker Desktop**
   - Download and install **[Docker Desktop for Windows](https://www.docker.com/products/docker-desktop/)**.
   - Make sure Docker is running and active (open the Desktop application and check if something happens).


2. **Pull the AlmaLinux image**
   - Open **Terminal** and type:
     ```powershell
     docker pull almalinux:9
     ```
     This command pulls the latest version of **AlmaLinux 9** from **Docker Hub**.

3. **Create and run an AlmaLinux container**
   - Run the following command to create and start an interactive container:
     ```powershell
     docker run -it --name almalinux9 almalinux:9 /bin/bash
     ```
     - `-it`     Runs the container in interactive mode.
     - `--name almalinux9`   Assigns a custom name to the container.
     - `/bin/bash`    Starts a **Bash shell** inside the container.

4. **Verify the installation**
   - Inside the container, check the AlmaLinux version with:
     ```bash
     cat /etc/os-release
     ```
     You should see an output like this:
     ```
     NAME="AlmaLinux"
     VERSION="9.x (Blue Onyx)"
     ID="almalinux"
     ```

---
