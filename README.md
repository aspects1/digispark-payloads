# wifi password grabber 
grabs saved wifi passwords using the "netsh wlan show profile NetworkName key=clear" command and sends formatted xml containing passwords to hosted domain on the "webhook.site"
note - please use your own self hosted webhook domain and replace link in code
# reverse shell 
the victim windows machine initiates a connection to the host's linux machine, allowing the linux machine to execute commands on the windwos machine remotely with adminstrator rights, code has 192.168.1.51 as forward to IP address [linux machine's IP] and is transmitted through port 44
note - reconvert this code to a badUSB script, edit the ip address and port to desired and convert back to .ino file to upload to digispark
