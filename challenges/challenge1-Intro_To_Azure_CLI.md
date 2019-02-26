# Intro to Azure CLI

## Expected outcome

In this lab, you will prepare your workstation VM for using the Azure CLI, sign in, and utilize the Azure CLI to deploy basic Azure resources. You will need to have a browser client on your local PC and access to the web to launch our Hackfest Workstation VM.

## How to 

1. <strong>Using your browser go to the Registration Site listed in your classroom.</strong>
    * Please make sure you use a valid work email as it will not allow for commercial e-mail domains.

![SignUp](./images/signup.png)

 * Once you select submit, **DO NOT CLOSE THE BROWSER**.
 * On the Lab and Overview page, navigate to the Lab tab and then select Launch Lab

![Launch Lab](./images/launch2.png)

 * The Lab will begin to deploy. **DO NOT CLOSE THE BROWSER**. This will take some time but the needed credentials will be presented on the page when the provisioning is complete.

![Preparing Lab](./images/preparing.png)

 * Your credentials will be emails to your signup email address as well as presented on the screen

![Credentials](./images/labready.png)

<hr>
2. <strong>Launch your web browser of choice and enter the url for the VNC server provided for you. Use the password provided to you in email or on the screen to login.</strong>

![noVNC Server](./images/vncserver.png)

 * It may take a minute or so at first launch to get the desktop to present. This is normal at first log in.
 * Mozilla Firefox, Edge, and Internet Explorer have all been tested; Google Chrome has been tested but is buggy.
 * Once this is completed, go to the terminal and you should be ready to start with the Azure CLI instructions below.

![noVNC Terminal](./images/vncterminal.png)

<hr>
3. <strong>Install Azure CLI (AZ CLI) on your workstation</strong>

 * Azure CLI is available for Mac, Windows and Linux.
 * You will need administrator access to install Azure CLI. You can switch user to root with ``su``. The password is the same as you used to login to the VNC environment.
 * You can find installation instructions here: [Install Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-yum?view=azure-cli-latest)
 * It is recommended you open reference material like the Azure CLI reference within your VNC environment so you can easily copy/paste commands.
 * Alternatively, you could use Azure Cloudshell from the Azure Portal. 

<hr>
4. <strong>Log in to your student Azure account via the CLI</strong>

 * Use ``az login`` to login to your lab Azure Account. You will be asked to visit ``https://aka.ms/devicelogin`` and use the provided code to authenticate. On your desktop, open the credentials.txt file to obtain the list of credentials which have been assigned to you.

![Azure Credentials](./images/azcred2.png)

 * The password is a onetime password and must be changed at first signing in
 * Your terminal windows will update with a JSON output of your subscription confirming the login has worked

<hr>
5. <strong>Navigate the portal and find Azure resources</strong>

   * Go to ``https://portal.azure.com`` and sign in using your credentials provided
   * Navigate to resource groups on the left hand side, and locate the resource group previously created for you or display them through your shell window
   * Note the region in which the resource group is located
 
   ![Azure Portal](./images/portalrg.png)

<hr>
6. <strong>Configure Azure CLI Defaults</strong>

 * Run ``az vm list -d`` to verify that your output is currently using JSON
 * Configure AZ CLI to default to table output
 * Run ``az vm list -d`` again to check that the output is now using the table format
 * Configure AZ CLI to use the same default location as your resource groups and verify

      ![Default Location](./images/defaultloc.png)

<hr>
7. <strong>Determine the commands for creating storage accounts using the AZ CLI find command</strong>

 * Use the ``az find`` command along with the necessary options to understand how to create a az storage command
 * Use the --search-query option to help in your search
 
 ![azfind](./images/azfind.png)

<hr>
8. <strong>Log into interactive mode and create a new Azure storage account using the AZ CLI</strong>

 * Make the storage account use Standard Locally Rundandant Storage
 * Name the storage account in the following format:   "firstnamelastnamebirthyear", example, "stuartkirk1975"
 * Create the storage account in the resource group you previously identified
 * Create a blob container within this storage account
 
 ![azinteractive](./images/azinteractive.png)

<hr>
9. <strong>Verify you have now created the storage account in the portal</strong>

 * If not done so already, visit ``https://portal.azure.com``

## Advanced areas to explore

1. If you have time, explore using the Azure Cloud Shell [Azure Portal](https://portal.azure.com). 
2. Try creating your own Azure virtual network using the Azure CLI Cloud Shell
