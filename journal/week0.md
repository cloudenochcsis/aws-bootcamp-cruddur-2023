# Week 0 — Billing and Architecture

Set Up a Cost Budget to make sure I do not exceed the free tier. 

This guide was used to install the aws cli in our environment 

https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

Update our .gitpod.yml to include the following task.



tasks:
  - name: aws-cli
    env:
      AWS_CLI_AUTO_PROMPT: on-partial
    init: |
      cd /workspace
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install
      cd $THEIA_WORKSPACE_ROOT
