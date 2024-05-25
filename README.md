# Stocks
Scripts for Stocks to Discord Tickers
Sure, I'll break down the steps to set up and use the provided Google Apps Script, including creating the necessary Gmail labels and configuring the script in Google Apps Script.
What you will need
A text editor
A gmail account.
https://script.google.com/ setup its free but needed)
A discord account that you admin, or have webhooks to use.
The script itself can be edited using the below direction to add or remove as you desire.


Step 1: Creating Gmail Labels
Open Gmail:

Go to your Gmail account.
Create the 'Discord' Label:

On the left sidebar, scroll down and click on "More."
Scroll down and click on "Create new label."
Enter "Discord" as the label name and click "Create."
Create the 'Processed' Label:
( Make sure the script uses the same label name)

Repeat the above steps to create another label named "Processed."
Step 2: Tagging Emails with the 'Discord' Label
Select Emails:

Go to your Gmail inbox.
Select the emails you want to tag with the 'Discord' label by checking the boxes next to them.
Apply the 'Discord' Label:
Or you can creat a filter that will automatically send the incoming mail to that label.
( example emails that have xyz.com will go to that lable.

Click on the "Label" icon at the top of the inbox.
Select "Discord" from the dropdown menu.
Step 3: Setting Up Google Apps Script
Open Google Apps Script:

Go to your Google Drive.
Click on "New" > "More" > "Google Apps Script."
Create a New Project:

In the Google Apps Script editor, click on "Untitled project" at the top and give your project a meaningful name, such as "Discord Email Processor."
Paste the Script:

Delete any default code in the script editor.
Copy and paste the provided script into the editor.

Step 4: Set Up Triggers
Save the Script:

Run the setupEnableDisableTriggers function by selecting it from the dropdown menu next to the run button (▶) and clicking the run button.
The script will ask for necessary permissions. Click "Review Permissions" and authorize the script.
Verify Triggers:

Click on the clock icon on the left sidebar (Triggers).
Ensure there are triggers set for enabling the main script at 6:00 AM and disabling it at 1:30 PM.
Summary
Create Gmail Labels:

Create 'Discord' and 'Processed' labels in Gmail.
Tag relevant emails with the 'Discord' label.
Set Up Google Apps Script:

Create a new project in Google Apps Script.
Paste the provided script into the editor and save it.
Run the setupEnableDisableTriggers function to set up the necessary triggers.
Authorize the script when prompted.
Verify:

Check the triggers to ensure they are set correctly.
The script should now run every 5 minutes between 6:00 AM and 1:30 PM.
This setup will process your tagged emails and send them to Discord within the specified time frame.

_____________________________________________________________________________________________________

To set up Discord for use with the Google Apps Script, you'll need to create a webhook in your Discord server. 
This webhook will be used by the script to send messages to a specific channel. Here are the steps to create a Discord webhook and configure it for use:

Step 1: Create a Discord Webhook
Open Discord:

Go to your Discord server where you want to receive the messages.
Navigate to Server Settings:

Click on the server name at the top of the channel list to open the dropdown menu.
Select "Server Settings."
Create a Webhook:

In the left sidebar, select "Integrations."
Click on "Webhooks."
Click on "New Webhook."
Configure the Webhook:

Give your webhook a name (e.g., "Gmail to Discord").
Choose the channel where you want the messages to be sent.
Click "Copy Webhook URL" to copy the webhook URL to your clipboard. You will use this URL in your Google Apps Script.
Save Changes:

Click "Save" to create the webhook.
Step 2: Integrate the Webhook URL into Google Apps Script
Open your Google Apps Script project:

Go to your Google Drive.
Open the project you created for the Gmail to Discord integration.
Paste the Webhook URL:

Find the line in your script where the webhookUrl is defined.
Replace the placeholder URL with the webhook URL you copied from Discord.
Example:

javascript
Copy code
var webhookUrl = "https://discord.com/api/webhooks/YOUR_WEBHOOK_ID/YOUR_WEBHOOK_TOKEN";

___________________________________________________________________________________________________________
Email: 
Think or swim as and examply can send and email notication. 
That email is then routed to a Label.
That Lable is used to run the script from Google Scripts
The Script thhen uses a webhook to display.
The script can be ajusted as follows.
Time, labels, hooks, Subject line and amount of line sets.
This script can be used for news of any kind that comes in a Gmail account.
Not the free script account allows a large frequency, but you can over use it and lose 
access for 24 hours. It is therefore suggested that 5min updates as the max and setting times
on and off are idea to elimiate reaching a limit.



EDIT: 5-25-2024


