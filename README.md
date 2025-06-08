# DevOps Lifecycle Implementation – Abode Software

This project implements the DevOps lifecycle for Abode Software using the GitHub repository: [https://github.com/hshar/website.git](https://github.com/hshar/website.git)

## Project Summary

1. **Configuration Management**
   - Installed required software using a configuration management tool (e.g., Ansible).

2. **Git Workflow**
   - Implemented Git branching strategy:
     - `master` – production deployment
     - `develop` – testing only

3. **CI/CD Automation**
   - CodeBuild triggered automatically on push:
     - **master**: test and deploy to production
     - **develop**: test only (no deployment)

4. **Containerization**
   - Application containerized using Docker.
   - Used pre-built image: `hshar/webapp`
   - App code resides in `/var/www/html`
   - Docker image rebuilt on each GitHub push.

5. **Jenkins Pipeline Structure**
   - **Job1: build** – Clone repo and build Docker image
   - **Job2: test** – Run tests
   - **Job3: prod** – Deploy to production (only on master branch)

