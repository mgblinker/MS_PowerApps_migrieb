# MS_PowerApps_migrieb
PowerApps demo packages for demo and quick start purposes #MSFTAdvocate

What you need
- PowerApps and Microsoft Flow license (part of Office E3/E5, PowerApps P1/P2 license, Dynamics 365 license)
- Office 365 tenant including Azure Active Directory (AAD)
- Dynamics 365 paid or trial subscription
- Microsoft Azure subscription including Cognitive Services license

Package (downloadable ZIP file) content
- PowerApp
- Flow import template

How to set up
1) Set up Azure Cognitive Services
- Select Location "West US"
- If not existing, create a new Resource group, e.g. "PACogVis"

2) Download PowerApps ZIP File

3) Log on to https://web.powerapps.com

4) Select the environment you want to install the app into from the environment picker top right

5) From the navigation, select "Apps"

6) Click "Import package (preview)" from the menu bar, select the PowerApps ZIP package
- This will automatically create the App and the Flow
- In the section "Review Package Content", hit the wrench icon for every line indicating required configurations
* For the PowerApp itself, select "Create as new" and give it a memorizable name
* For the Cognitive Services API, select "Create New", create a new connection of type "Computer Vision API", and enter the following values:
+ Account key: Copy from your Azure resource ("Grab your keys")
+ Site URL: "https://westus.api.cognitive.microsoft.com/vision/v1.0"
NOTE: Currently, you can only use the West US API in conjunction with Microsoft Flow
* For the Flow, select "Create as new", give it a name of your choice
* For the Dynamics 365 connection, click "Create new", then link to a Dynamics 365 instance your an administrator of (if you don't have one, feel free to create a trial via https://trials.dynamics.com)

7) Click "Import"
