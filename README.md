# WiFi Password Grabber

Grabs saved WiFi passwords on a Windows machine and sends them to a hosted domain using a webhook. This is done using the following command:

```bash
netsh wlan show profile NetworkName key=clear
Key Features:
Command: netsh wlan show profile NetworkName key=clear
Webhook: Sends the retrieved passwords in XML format to a hosted domain via a webhook (use your own domain).
Usage:
Command Execution: The command retrieves stored WiFi passwords on the machine.
Replace Webhook URL: Replace the webhook URL in the code with your own self-hosted webhook domain.
Format: Passwords are formatted into XML and sent to your hosted webhook.
Important Notes:
Ensure to use your own self-hosted webhook to receive the WiFi password data.
This tool is intended for legal use only in environments where you have permission.
