**Arthor**: Hao Zhu

Latest update: 03/22/2024

---

# TianLab Server Tutorial

Welcome to the TianLab Server! As of 2024, our server has been upgraded to the Ubuntu 22.04 LTS system. This guide will help you get started, install essential software, and troubleshoot common issues.

**Note**: Due to the upgrade, all user accounts and home directory files have been reset. Legacy data is now stored in `/Data`.

## Getting Started

#### Access Requirements
 
Access to the NYU Network is **required**. Use the `nyu` WiFi on campus or the Cisco Anyconnect VPN off-campus with the address: `vpn.shanghai.nyu.edu`.
[Download VPN here](https://shanghai.nyu.edu/it/vpn)

#### Server Hardware Specifications

|Hardware|Information|
|-----|--------|
|Model|Dell PowerEdge R730|
|CPU  |Intel Xeon E5-2667 v4 3.2Ghz 16C32T|
|RAM  |256G|
|DISK |30T|
|OS   |Ubuntu 22.04.4 LTS 64-bit|

#### Account Setup

**Contact the server administrator to create your account**. Your default password will be `!QAZ2wsx`. Be sure to change it upon your first login.

## Connecting to the Server

#### Using Windows Remote Desktop

1. Search for and open `mstsc` from the start menu.
2. Enter the server IP: `10.208.17.131`.
3. Login with your username and the provided default password.
4. Click `OK` to connect.

#### Using SSH (macOS/Ubuntu)

1. Before connecting, ensure you remove any existing entries for `10.208.17.131` from your `~/.ssh/known_hosts` file to avoid errors.
2. Open a `terminal` and type `ssh username@10.208.17.131`.
3. Enter your password when prompted.


## Setting Up Your Work Environment

We encourage users to install their environments in their home directories to prevent conflicts and enhance efficiency. The `/Share` folder contains installers and zip files for many common applications.

#### Anaconda (Python)

1. Locate the Anaconda installer at `/Share/Anaconda3-2024.02-1-Linux-x86_64.sh` or download the latest version from the [Anaconda website](https://www.anaconda.com/download).
2. Copy the installer to your home directory (e.g., `/home/username/Desktop`).
3. Open a `terminal`, navigate to the directory containing the installer, and run `bash Anaconda3-2024.02-1-Linux-x86_64.sh`. Follow the on-screen instructions, accepting the default options (type `yes` when prompted).
4. After installation, restart your terminal and type `conda` to verify the installation.

#### MATLAB

1. The MATLAB R2024a installer can be found at `/Share/matlab_R2024a_Linux.zip`.
2. Copy the installer to your home directory and unzip it.
3. Follow the installation prompts, selecting the necessary toolboxes. Installation time varies based on the selected components.
4. For additional toolboxes or software (e.g., SPM, Brainstorm), refer to their official websites for installation instructions.

#### FTP file Transfer

1. We recommend using FileZilla for file transfers. Download it from the [official website](https://filezilla-project.org/).
2. Enter `10.208.17.131` in the Host field and your username and password. Leave the Port field blank and click `Quickconnect`.
3. The interface shows your local files on the left and your server home directory on the right. Drag and drop files between these areas to transfer them. Transfers are bi-directional.

## Troubleshooting

 1. Keyboard malfunction in Firefox web browser.

 - open `terminal`, type `ibus exit`.