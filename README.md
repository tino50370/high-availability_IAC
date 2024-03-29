# High Availability Infrastructure as Code

This repository contains Infrastructure as Code (IaC) scripts to deploy the necessary network infrastructure, server infrastructure, and jumpbox infrastructure for a dummy application, PhotoGram, on Amazon Web Services (AWS) using AWS CloudFormation. Checkout the infrastructure diagram in this repository for a visual representation of the infrastructure.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Deploy Network Infrastructure](#deploy-network-infrastructure)
- [Deploy Server Infrastructure](#deploy-server-infrastructure)

## Introduction

PhotoGram is an Instagram clone that aims to replicate the functionality and features of the popular social media platform. This repository provides the necessary IaC scripts to automate the provisioning of the underlying infrastructure required to deploy the PhotoGram application on AWS.

The infrastructure deployment is achieved using AWS CloudFormation, a service that allows you to create and manage AWS resources using declarative templates. The IaC scripts provided in this repository are designed to be deployed on AWS CloudFormation to automate the creation of network resources, server resources, and a jumpbox instance.

## Prerequisites

Before running the IaC scripts, ensure that you have the following prerequisites:

- An AWS account with sufficient permissions to create and manage resources.
- The AWS Command Line Interface (CLI) installed and configured on your local machine.
- Basic knowledge of AWS services and CloudFormation concepts.
- Familiarity with shell scripting (Bash) for executing the provided deployment scripts.

## Installation

To get started, follow these steps:

1. Clone this repository to your local machine:

``` bash
git clone https://github.com/tino50370/high-availability_IAC.git

```

2. Navigate to the project directory:

``` bash
cd high-availability_IAC

```

## Usage

This repository provides three IaC scripts for deploying different parts of the infrastructure. Each script can be executed using the provided bash files.

### Deploy Network Infrastructure

To deploy the network infrastructure, which includes Virtual Private Cloud (VPC), subnets, and security groups, follow these steps:

1. Open a terminal and navigate to the project directory.
2. Ensure that the AWS CLI is configured before running the commands below.
3. Check the region in the create.sh file if you are on a unix OS or create.bat if you are on windows
4. Execute the following command to create the network infrastructure using AWS CloudFormation:

Unix

``` bash
create.sh Network Network.yml NetworkParams.json

```

Windows

``` bash
create.bat Network Network.yml NetworkParams.json

```

### Deploy Server Infrastructure

To deploy the server infrastructure, which includes security groups, IAM resources, auto-scaling resources and load balancing resources, follow these steps:

1. Open a terminal and navigate to the project directory.
2. Ensure that the AWS CLI is configured before running the commands below.
3. Check the region in the create.sh file if you are on a unix OS or create.bat if you are on windows
4. Execute the following command to create the network infrastructure using AWS CloudFormation:

Unix

``` bash
create.sh Server Servers.yml ServersParams.json

```

Windows

``` bash
create.bat Server Servers.yml ServersParams.json

```

*Optional:* Follow the same instructions to deploy the Jumpbox server as well.


