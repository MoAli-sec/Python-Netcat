# NetCat Tool in Python
This Python script is a simple implementation of the NetCat tool that allows communication over TCP/IP networks. It was inspired by the book "Black Hat Python" by Justin Seitz.
This Python script is a Netcat-like tool that enables users to execute commands, upload files, and establish a command shell on a remote server through a socket connection. The script uses the argparse module to handle command-line arguments and threading to manage multiple client connections.

# Requirements
This script requires Python 3 to run. There are no additional requirements or dependencies.

# Usage
The script can be run using the following command:
```
python netcat.py [options]
```
The available options are as follows:
```
-h, --help            show this help message and exit
-c, --command         command shell mode
-e EXECUTE, --execute EXECUTE
                      execute specified command
-l, --listen          listen mode
-p PORT, --port PORT  specified port (default 5555)
-t TARGET, --target TARGET
                      specified IP (default 192.168.1.12)
-u UPLOAD, --upload UPLOAD
                      upload file
```

# Examples
Here are some example commands that demonstrate the functionality of the script:
```
# Start a command shell on a remote server
python netcat.py -t 192.168.1.12 -p 5555 -l -c

# Upload a file to a remote server
python netcat.py -t 192.168.1.12 -p 5555 -u=myfile.txt

# Execute a command on a remote server
python netcat.py -t 192.168.1.12 -p 5555 -e="ls -la"

# Connect to a remote server
python netcat.py -t 192.168.1.12 -p 5555

# Echo text to a remote server port
echo 'ABC' | python netcat.py -t 192.168.1.12 -p 135
```

# Disclaimer
This tool is intended for educational and testing purposes only. Please use responsibly and with the explicit permission of the remote server owner.
