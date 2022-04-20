![image](https://user-images.githubusercontent.com/80892763/164226092-95ce6a2e-08fc-46ee-ae80-3c702c26e9ce.png)

### Prerequisites
-   Ubuntu 20.04 or Ubuntu 20.10
-   1024MB or above Ram.
-   10GB Disk Space.
-   1 vCPU or above CPU.
-   root privileges

## Step 1 - connect to SSH if usued

Use the following command to log in to your server on SSH:
```
ssh root@server_ip
```
Also, check if your system package database is up to date before continuing this tutorial.

## Step 2 - Update Ubuntu

Log in to your server via SSH and before starting the installation of  **MkDocs**, it is always recommended updating the system packages.

So let's go to the command:

```bash
sudo apt update
```

Ensuite :

```bash
sudo apt upgrade
```

## Step 3 - Install Python 3 or plus

Verify Python 3 is installed

```bash
sudo apt-get install software-properties-common
python3 --version
Python 3.8
```

You need Python 3 or more for this installation!

## Step 4 - Install MkDocs

```bash
sudo apt install mkdocs
```

```bash
mkdocs --version
mkdocs, version 1.0.4 from /usr/lib/python3/dist-packages/mkdocs (Python 3.7)
```

## Step 5 - Create a new project called mkdocs and build a new site

```bash
sudo mkdocs new mkdocs
```

```bash
cd mkdocs
```

```bash
sudo mkdocs build
```

## Step 6 - Verify the following files are created successfully

```bash
ls -la /mkdocs

docs  mkdocs.yml  site  ssl

ls -la /mkdocs/site

404.html  css  fonts  img  index.html  js  search  sitemap.xml  sitemap.xml.gz
```

## Step 7 - Install Python PIP and mkdocs-meterial theme

```bash
sudo apt install python3-pip
```

```bash
pip3 install mkdocs-material
```

## Step 8 - Modify  **/mkdocs/mkdocs.yml**  to use mkdocs-material theme
```bash
sudo apt-get install nano
```
```bash
sudo nano /mkdocs/mkdocs.yml
```

```bash
site_name: My Docs
theme:
  name: material
```

## Step 9 - Start mkdocs

IP Address =  **0.0.0.0**  and listening on  **Port 8000**

```bash
mkdocs serve -a 0.0.0.0:8000
```

```bash
INFO    -  Building documentation...
INFO    -  Cleaning site directory
[I 210201 01:03:15 server:298] Serving on http://0.0.0.0:8000
[I 210201 01:03:15 handlers:59] Start watching changes
[I 210201 01:03:19 handlers:132] Browser Connected: http://0.0.0.0:8000



