# Intelec AI - Automated machine learning platform with GPU support free to download

This repository is intended to help people set up Intelec AI on their computer or server. Please note that Intelec AI works on [Docker](https://www.docker.com/). Hence, please download and install docker before starting to set up Intelec AI.

## About Intelec AI

Intelec AI is a zero code machine learning platform. It can help you automate building and deploying machine learning models.

[![Intelec AI Demo](https://github.com/intelec-ai/intelecai-installation/raw/master/img/demo_image.png)](https://www.youtube.com/watch?v=klv_3L68MJ0)

## Setting up Intelec AI in Windows

0. Download, install and start docker in your machine, if you haven't done it so far. You can install Docker Desktop for Windows following this link https://docs.docker.com/docker-for-windows/install/ and clicking on "Download from Docker Hub". 
1. Download the required files for Intelec AI set up from Github. You can do it either of the following 2 ways:
   * download them as a zip file from here https://github.com/intelec-ai/intelecai-installation/archive/master.zip and unzip it (right click on the zip file and choose "Extract All...")
   * or clone the git repository like this `git clone https://github.com/intelec-ai/intelecai-installation.git`
2. Start Intelec AI by clicking on `start_servers.bat`.
3. Visit http://localhost:7700 to open Intelec AI.
4. You can stop Intelec AI by clicking on `stop_servers.bat`.

## Installation in Linux and Mac

0. Download, install and start docker in your machine, if you haven't done it so far. You can [install Docker Desktop for Mac](https://docs.docker.com/docker-for-mac/install/) or [Docker Community Edition for Linux](https://docs.docker.com/install/linux/docker-ce/ubuntu/) (choose the appropriate linux distribution from the left hand side).
1. Download the required files for Intelec AI set up from Github. You can do it either of the following 2 ways:
   * download them as a zip file from here https://github.com/intelec-ai/intelecai-installation/archive/master.zip and unzip it. For example,
      * `wget https://github.com/intelec-ai/intelecai-installation/archive/master.zip`
      * `unzip intelecai-installation-master.zip`
   * or clone the git repository like this `git clone https://github.com/intelec-ai/intelecai-installation.git`
2. Go to the downloaded folder and give 'executable' permission to the required files: 
   * `cd intelecai-installation`
   * `chmod +x *.sh`
3. Now you can start Intelec AI by running `./start_servers.sh`.
4. Visit http://localhost:7700 to open Intelec AI.
5. You can stop Intelec AI by running `./stop_servers.sh`.

## GPU support

You need to have Linux operating system and an Nvidia GPU in order to add GPU support to your Intelec AI installation. If you have them, please go ahead and install Nvidia drivers and [nvidia-container-toolkit](https://github.com/NVIDIA/nvidia-docker). You will also need to set nvidia as default runtime in `/etc/docker/daemon.json`:

```
{
    "default-runtime":"nvidia",
    "runtimes": {
        "nvidia": {
            "path": "nvidia-container-runtime",
            "runtimeArgs": []
        }
    }
}
```

Then, after installing Intelec AI, you can start it with GPU support by running `./start_servers_gpu.sh`

## Report a problem or give a feedback

Please write to [info@intelec.ai](mailto://info@intelec.ai) or fill [this form](https://forms.gle/tcWBTaGUnJJGpJVd8) to report a problem or give a feedback.