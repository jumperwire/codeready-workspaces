# codeready-workspaces

Installation and Setup

Deploy CodeReady Workspaces Operator via OperatorHub

Create a new project “codeready-workspaces”
Navigate to Catalog -> OperatorHub
Click “Developer Tools”
Select “Red Hat CodeReady Workspaces” Operator
Click “Install”
Click “Subscribe”
Wait until “1 installed” link becomes active



Install CodeReady Workspaces Using Operator

Navigate to Catalog -> Operator Management
Click on “codeready-worspaces” link
Click on “1 installed” link
Under “Red Hat CodeReady Workspaces Cluster” box, click “Create New”
Review the YAML and click “Create” button
Navigate to Networking -> Routes
Click on URL under “codeready” route


Setting Up CodeReady Workspaces Environment

Go to the "swagger" page for CRW: http://<CHE_URL>/swagger
Expand the "Stacks" API definition, and look for the "POST /stacks" API.

Copy/paste the stack definition from https://raw.githubusercontent.com/RedHatWorkshops/quarkus-workshop/master/files/stack.json into the text box

Click "Try it!"

Now “Quarkus Java, CodeReady, odo” stack should appear as an option when you create a new workspace.

Import Quarkus Image:

oc create -n openshift -f https://raw.githubusercontent.com/RedHatWorkshops/quarkus-workshop/master/files/stack.imagestream.yaml

oc import-image --all quarkus-stack -n openshift

Create and start a new workspace based on custom stack

Import the "hello world" Quarkus app as a new Java project from https://github.com/RedHatWorkshops/quarkus-workshop-labs

