# Cyber and Fraud Centre Scotland - Testing Laptop / Testing VM Playbook

This ansible playbook was created with the original purpose of reworking the
Testing Laptop used by Cyber and Fraud Centre Scotland. However, it has now became
a streamlined way for the hackers to spin up a completely fresh Kali Linux virtual
machine for each engagement, ensuring that there are no overlaps in data between
tests and clients.

## Table of Contents

1. [Prerequisites](#prerequisites)
1. [Usage](#usage)

## Prerequisites

The only requirement to use this playbook is the ansible-core package, this contains
everything needed by ansible to successfully execute the playbook. The following
command can be used to download the package.

```bash
sudo apt update -y && sudo apt update -y && \ 
sudo apt install ansible-core -y
```

## Usage

### Creating a new Kali Virtual Machine

The first step in using this playbook is creating a fresh Kali virtual machine.
An ISO file for Kali can be downloaded from [here](https://www.kali.org/get-kali/#kali-installer-images)
and installation guidance can be found [here](https://www.kali.org/docs/installation/hard-disk-install/).

### Using the Playbook

Once Kali is installed the next step is to clone the GitHub repository containing
the playbook. To do this open a terminal and type the following.

```bash
git clone https://github.com/CyberFraudCentre/Hacker-Playbook.git
```

To then install the playbook change into the newly created directory for the repo
(`cd Hacker-Playbook`) and run the following command, entering the password for
your user account when prompted.

```bash
ansible-playbook main.yml -K
```

The playbook will then install the extra tools used by Cyber and Fraud Centre hackers
alongside making a few QOL changes to software such as burpsuite and firefox.

