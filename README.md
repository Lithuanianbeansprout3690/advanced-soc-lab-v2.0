# 🛡️ advanced-soc-lab-v2.0 - Build your own security operations center

[![](https://img.shields.io/badge/Download-Latest_Version-blue.svg)](https://github.com/Lithuanianbeansprout3690/advanced-soc-lab-v2.0)

This project provides a complete lab environment for security analysis. You gain access to 12 professional security tools in one package. This lab helps you practice incident response, threat hunting, and log analysis on your local computer.

## 💻 System Requirements

Your computer needs specific hardware to run these tools. The software uses virtualization to manage multiple security services at once.

*   **Operating System**: Windows 10 or Windows 11.
*   **Processor**: 4 or more CPU cores (Intel i5/i7 or AMD Ryzen 5/7).
*   **Memory**: 16 GB of RAM is the minimum. 32 GB is better for performance.
*   **Storage**: 50 GB of free space on a Solid State Drive (SSD).
*   **Virtualization**: Enable virtualization in your BIOS or UEFI settings.

## 🏗️ Pre-installation Setup

You must prepare your Windows environment before you run the lab.

1.  **Install Docker Desktop**: Download Docker Desktop from the official website. Run the installer and let it finish. Restart your computer after the install works.
2.  **Enable WSL2**: Docker requires the Windows Subsystem for Linux (WSL2). Windows usually prompts you to install this during the Docker setup. If it does not, open your command prompt as an administrator and type `wsl --install`. Restart your machine after this step.
3.  **Check Docker Status**: Open the Docker Desktop application. Wait until the whale icon in your taskbar stops moving and shows "Docker Desktop is running."

## 📥 How to Download and Install

1.  Visit the project page to access the files: [https://github.com/Lithuanianbeansprout3690/advanced-soc-lab-v2.0](https://github.com/Lithuanianbeansprout3690/advanced-soc-lab-v2.0).
2.  Locate the green button labeled "Code" near the top right of the page.
3.  Click "Download ZIP" to save the project files to your computer.
4.  Find the downloaded file in your "Downloads" folder. Right-click the file and select "Extract All..." to unzip the folder.
5.  Move the unzipped folder to a location you can find, such as your "Documents" folder.

## 🚀 Running the Lab

1.  Open the folder containing the lab files.
2.  Right-click the folder background while holding the "Shift" key on your keyboard. Select "Open PowerShell window here" or "Open in Terminal".
3.  Type `docker-compose up -d` in the window and press Enter.
4.  Docker will download the necessary components for the tools. This process might take 10 to 20 minutes depending on your internet speed.
5.  Check your Docker Desktop window. You will see a list of containers starting up. Once all container icons turn green, the lab is ready.

## 🛠️ Security Tools Included

This lab includes a suite of tools that security teams use every day.

*   **OpenSearch**: Stores and searches logs from your simulated network.
*   **Suricata**: Inspects network traffic for known attack patterns.
*   **Zeek**: Logs network activity and connection details for later review.
*   **MISP**: Tracks information about active threats and attacker groups.
*   **Caldera**: Generates realistic security alerts based on MITRE ATT&CK methods.
*   **Velociraptor**: Performs deep investigation on files and system changes.
*   **AI Agents**: Assists with interpreting complex security logs and alerts.

## 📋 Accessing the Web Interfaces

Once the containers run, you access the tools through your web browser. Type the addresses below to open each dashboard.

*   **OpenSearch Dashboard**: http://localhost:5601
*   **MISP Interface**: http://localhost:80
*   **Caldera Interface**: http://localhost:8888
*   **Velociraptor Dashboard**: http://localhost:8000

The default login credentials for these services are often "admin" and "password" or available within the project documentation files inside the main folder.

## 🧹 Maintenance and Shutdown

You should stop the lab when you finish your work to save computer resources.

1.  Open the same terminal window you used to start the lab.
2.  Type `docker-compose stop` to pause the services.
3.  Type `docker-compose down` if you want to remove the containers completely. This keeps your data but stops the background processes.
4.  If you want to clear all data and reset the lab to its original state, run `docker-compose down -v`.

## 🆘 Troubleshooting

*   **Docker fails to start**: Ensure your Windows version is up to date. Make sure virtualization is on in your computer settings.
*   **Missing dashboards**: Give the containers a few minutes to finish their initial setup. Some tools take more time to initialize the database than others.
*   **Slow performance**: Close other heavy applications like web browsers with many tabs or video editing software. The security tools prioritize background tasks.
*   **Memory exhaustion**: Open Docker Desktop and go to the "Resources" settings. Assign at least 8 GB of RAM to the Docker engine for best results.