# Building-a-DHCP-Server-on-Windows-Server-2022-A-Step-by-Step-Lab
#

This repository contains instructions and assets for standing up a **Dynamic Host Configuration Protocol (DHCP)** server on **Windows Server 2022** using the domain name `saimoon.local`.  The goal of this project is to build a small lab environment where Windows Server hands out IP addresses to clients automatically.

The project includes:

* **Documentation** – located under the [`docs/`](docs/) folder, the documentation explains how to install the DHCP role, configure the service and create an IPv4 scope.  Screenshots are included to illustrate each step.
* **Images** – the [`images/`](images/) folder contains screenshots of the installation wizard as well as diagrams of the scope‑configuration wizard.  These images are referenced from the documentation and are stored in the repository for offline viewing.

## Repository structure

```
dhcp_project/
│  README.md            – high level overview and repository description
│
├─docs/
│   └─setup_dhcp.md     – step‑by‑step guide for installing and configuring DHCP on Windows Server 2022
│
└─images/
    ├─step1.jpg         – opening **Server Manager** from the start menu
    ├─step2.jpg         – launching the **Add Roles and Features** wizard in Server Manager
    ├─step3.jpg         – **Before you begin** page of the wizard
    ├─step4.jpg         – selecting **Role‑based or feature‑based installation**
    ├─step5.jpg         – selecting the destination server
    ├─step7.jpg         – selecting the **DHCP Server** role (wizard prompts to add management tools)
    ├─step6.jpg         – confirming the addition of required management tools (DHCP Server Tools)
    ├─scope_step1.png   – conceptual diagram of the scope wizard’s **Name and description** page
    ├─scope_step2.png   – conceptual diagram of the **IP address range and exclusions** page
    └─scope_step3.png   – conceptual diagram of the **DHCP options** page (gateway, domain name and DNS servers)
```

## Quick start

1. Clone this repository to your local machine and open [`docs/setup_dhcp.md`](docs/setup_dhcp.md) in a Markdown viewer.
2. Follow the instructions to install the DHCP role, authorize the server in Active Directory, create a scope and configure DHCP options for the domain `saimoon.local`.
3. Review the screenshots in the `images/` folder if you need visual guidance.  Each image is referenced from the documentation.

If you wish to recreate the environment in a lab, ensure you have a Windows Server 2022 installation with a static IP address and that it is joined to the `saimoon.local` Active Directory domain.  The documentation assumes the server will hand out addresses in the `192.168.50.0/24` subnet, but you can adjust the scope to suit your environment.
