DevOps Lifecycle Implementation – Abode Software
This project implements a complete DevOps lifecycle for the Abode Software product available at GitHub - hshar/website.

Lifecycle Overview
Configuration Management

Use tools like Ansible, Puppet, or Chef to install and configure required software on all machines.

Git Workflow

Implement a standard Gitflow branching strategy.

Monitor master and develop branches for triggering CI/CD pipelines.

CI/CD with Jenkins and CodeBuild

Jenkins is used to automate the pipeline:

Master branch:

Run tests

Deploy to production

Develop branch:

Run tests only

Containerization

Application is containerized using Docker.

Base image: hshar/webapp

App code copied to /var/www/html

Docker image is rebuilt on every commit to GitHub.

Jenkins Pipeline Jobs

Job 1: build

Clone repo

Build Docker image

Job 2: test

Run application tests

Job 3: prod

Deploy to production (only for master branch)
