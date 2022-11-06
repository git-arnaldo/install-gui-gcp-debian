# install-gui-gcp-debian
## My Primary Goal:
- Log in to a linux GCP VM from a Windows local machine via remote desktop
## What do I know:
- (really) basic sh knowledge
- GCP Linux VMs come without Graphical User Interfaces (GUI).
- I need a RDP connection

I am not a linux person, so I made this repo to save infos that I'll forget soon.
## Let's go

### How to Install a GUI on a Google Cloud Platform Debian 11 VM

**I followed this tutorial:**
<https://techviewleo.com/install-lxqt-desktop-environment-on-debian/>

**always exec this command, because yes:**
```sh
sudo apt update
```

**install a gui of your choice:**
```sh
sudo apt install task-lxqt-desktop -y
```

### how to Install a RDP to access the VM through Windows
**installing xRDP:**
```sh
sudo apt -y install xrdp
```

**Exec this commands to make xrdp not user dependent:**
```sh
sudo systemctl enable xrdp
sudo systemctl restart xrdp
```

**Know issues:**
- Only connects to root user. Don't ask me why. I Appreciate any help
