# Build AI Solution with Edge Agent

Welcome to the session! Let's learn about Advantech Edge Agent 🚀

- **Speaker**: Chun-Yu Chen, Edge AI Senior Solution Engineer
- **Organization**: Edge Server Group, IIoT, Advantech
- **Time**: 10:10 ~ 11:10, 13th May, 2025

## Advantech Edge Agent GitHub

Edge Agent [Github](https://github.com/advantech-EdgeAI/edge_agent) is the place where everything is included for installing and understanding Edge Agent. The best practices to follow for using the repo are:

- **Take an overview on README file, Issues, and Wiki**
- **Watch YouTube videos in the repo**
  - [Promotion Video of Edge Agent](https://www.youtube.com/watch?v=xsvGXlDslf0)
  - [Quick Introduction to Edge Agent](https://www.youtube.com/watch?v=P6T5xecStjk)
  - [Short Installation Walkthrough Video of Edge Agent](https://www.youtube.com/watch?v=zIH040_c2yg)
  - [Start a Short Demo Project on Edge Agent](https://www.youtube.com/watch?v=XNr-aNQwoPc)
- **Star the repo for quick referencing** ⭐
- **Try to follow the instructions to install Edge Agent**  
  👉 Tips and Pitfalls for Installing Edge Agent
- **Try preset projects in Edge Agent with the guidance in Wiki**  
  👉 Factory Outfit Detection  
  👉 Clearance Space Detection

- **Ask your question by creating an issue**  
  👉 How to Ask Questions on Edge Agent GitHub

## Tips and Pitfalls for Installing Edge Agent

### Before Installation…

- Check BSP version of your MIC-733
  - Only JetPack 6.0 is verified
- Prepare at least 200 GB NVMe SSD and install it on MIC-733
- Connect your MIC-733 with Internet

### During Installation…

- Why we need to install Docker?
  - Edge Agent and most of its components are running in Docker containers.
- Why we need to migrate Docker directory to SSD?
  - Models will be downloaded to Docker directory while using Edge Agent. We use extra SSD to hold the storage-demanding Docker directory.
- [Highly recommended verifying Docker directory is moving to SSD](https://github.com/advantech-EdgeAI/edge_agent/wiki/Test-Docker-on-SSD)
- "Download Essential Data" will take 5 to 10 minutes, be patient.
- Essential Data includes:
  - Demo data (images, videos, etc.)
  - Preset projects
  - Entire Edge Agent service (approx. 30 GB)

### After Installation…

- If you find MIC-737 entering emergency mode after rebooting…
  - Press "Ctrl + D" to continue entering system
  - Remove a redundant file (`sudo rm -rf /etc/udev/rules.d/70-nvme.rules`)
- To start Edge Agent:
  - By script: `bash startEA.sh`
  - [Manually](https://github.com/advantech-EdgeAI/edge_agent?tab=readme-ov-file#optional-start-edge-agent-manually)
- Plug in your USB camera before you start the Edge Agent.
- Use Chrome (or Chromium) to run Edge Agent

## Quick Demo Projects

- [Factory Outfit Detection](https://github.com/advantech-EdgeAI/edge_agent/wiki/Factory-Outfit-Detection)
- [Clearance Space Detection](https://github.com/advantech-EdgeAI/edge_agent/wiki/Clearance-Space-Detection)

## How to Ask Questions on Edge Agent GitHub

- We use [GitHub Issues](https://github.com/advantech-EdgeAI/edge_agent/issues) to track questions.
- Before creating an issue…
  - You must sign in your GitHub account.
  - Try to find the answer in [FAQ](https://github.com/advantech-EdgeAI/edge_agent/issues?q=is%3Aissue%20state%3Aclosed%20label%3AFAQ) first.
- When you are creating a new issue…
  - Specify which BSP you are using.
  - Describe your question with details.
  - Always consider to upload supportive materials (e.g. screenshots, logs, etc.).
- After you submit an issue…
  - We will tag your issue with a label (e.g. bug, enhancement, question, etc.).
  - We will reply to your issue ASAP (you will be notified automatically by email).
