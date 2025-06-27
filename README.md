# MOVING - Software AG Mainstream DevOps Example: API Gateway 10.7 Custom Image Multi Stage Build Pipeline

# This repo will be moved away from the Software AG organization

## Prerequisites

This pipeline is an example of the second tier pipelines in the overall Software AG mainstream DevOps framework.
It requires the Azure [prerequisites](https://github.com/SoftwareAG/sag-mainstream-devops-az-00-prerequisites) to be satisfied and a [tier one zip images pipeline](https://github.com/SoftwareAG/sag-mainstream-devops-az-01-product-fix-images) to have produced the following input files in the shared folder in the framework's storage account:

- `/products/APIGateway/1007/default/products.zip`
- `/fixes/APIGateway/1007/default/<YY-MM-DD>/fixes.zip`
- Optionally `/bin/installer.bin`
- Optionally `/bin/sum-bootstrap.bin`

Also, the Azure DevOps project must have a secure file called `yai-license.xml` containing a valid API Gateway license.

## Quick Start

- use this template repository to create your own
- clone it on your machine and alter the following files according to your project specifics
  - `setEnv.sh`
  - `azure-pipelines.yml`, if needed
    - for example change the agents pool name to match what you provisioned
- Save, commit and push your changes
- Generate a new pipeline in Azure DevOps pointing to your generated repository

## Constraints

- Even if SUIF admits the installation to be done without fixes, the used dockerfile always requires the fixes zip file to be available

------------------------------

These tools are provided as-is and without warranty or support. They do not constitute part of the webMethods product suite. Users are free to use, fork and modify them, subject to the license agreement. While we welcome contributions, we cannot guarantee to include every contribution in the master project.
