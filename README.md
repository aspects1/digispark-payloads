# WiFi Password Grabber

Grabs saved WiFi passwords on a Windows machine and sends them to a hosted domain using a webhook. This is done using the following command:
  `
netsh wlan show profile NetworkName key=clear `

Key Features:
-------------

-   **Command**: `netsh wlan show profile NetworkName key=clear`
-   **Webhook**: Sends the retrieved passwords in XML format to a hosted domain via a webhook (use your own domain).

Usage:
------

1.  **Command Execution**: The command retrieves stored WiFi passwords on the machine.
2.  **Replace Webhook URL**: Replace the webhook URL in the code with your own self-hosted webhook domain.
3.  **Format**: Passwords are formatted into XML and sent to your hosted webhook.

### Important Notes:

-   Ensure to use your **own self-hosted webhook** to receive the WiFi password data.
-   This tool is intended for **legal use only** in environments where you have permission.

* * * * *

Reverse Shell
=============

The reverse shell allows a **Windows machine** to initiate a connection to a **Linux machine**, enabling the Linux machine to remotely execute commands on the Windows machine with **administrator rights**.

Key Features:
-------------

-   **IP Address**: The code is configured to forward the reverse shell to `192.168.1.51` (Linux machine IP address).
-   **Port**: The reverse shell uses port `44` to establish the connection.
-   **Connection Type**: The Windows machine initiates the connection to the Linux machine, allowing the Linux machine to execute commands remotely.

Usage:
------

1.  **Victim (Windows)**: The Windows machine connects to the Linux machine.
2.  **Host (Linux)**: The Linux machine receives the connection and can execute commands remotely on the Windows machine.

Steps to Modify:
----------------

1.  **Change IP Address**: Replace the `192.168.1.51` with the IP address of your Linux machine.
2.  **Change Port**: Replace `44` with the desired port for communication.

### Important Notes:

-   **Admin Rights**: The commands executed on the Windows machine will have administrator rights.
-   **Legal Use Only**: Ensure you have proper permission before using the reverse shell on any machine.

* * * * *

BadUSB Script
=============

The **BadUSB Script** can be used to deliver the reverse shell payload to a target machine through a **Digispark** device.

Steps to Convert to BadUSB Script:
----------------------------------

1.  **Modify the Reverse Shell Code**:

    -   Update the IP address (`192.168.1.51`) and port (`44`) to your desired values.
    -   Ensure the script is properly formatted for use as a BadUSB payload.
2.  **Convert to `.ino` File**:

    -   Once you've modified the reverse shell script, save it as an `.ino` file. This file format is necessary to upload the code to the **Digispark** device.
3.  **Upload to Digispark**:

    -   Use the **Arduino IDE** to upload the `.ino` file to the Digispark.
    -   After uploading, plug in the Digispark to the target machine, which will initiate the reverse shell payload.

How to Upload to Digispark:
---------------------------

1.  Open the **Arduino IDE**.
2.  Paste your modified BadUSB script into the IDE.
3.  Select **Tools > Board > Digispark**.
4.  Upload the code to the Digispark device.
5.  Plug the Digispark into the target machine to initiate the reverse shell.

### Important Notes:

-   **IP & Port Customization**: Remember to change the IP address and port to the appropriate values.
-   **Legal Use Only**: Use this script in environments where you have legal permission to test.
