# **OverTheWire Bandit Writeups**
> This repository contains writeups and screenshots of the first 20 levels under the Bandit Wargame. The Bandit wargame is aimed at absolute beginners. It will teach the basics needed to be able to play other wargames.
>
The OverTheWire Bandit challenges are a series of war games that focus on teaching and improving your command-line and cybersecurity skills. The challenges are hosted on the OverTheWire website and are designed to be progressively more difficult. They are an excellent way to learn about Linux and security, making them suitable for both beginners and more experienced users. The Bandit challenges are a great way to gain hands-on experience in system administration and security, as well as improve your familiarity with Linux command-line utilities. As you progress through the levels, you'll learn about various security concepts, including file permissions, privilege escalation, basic cryptography, and more. Each level provides a unique and fun learning experience.

## Level 0
This level involves logging into the game using SSH. 

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/a5109047-e2da-43e3-9cc6-5891c274db62)

SSH, which stands for Secure Shell, is a cryptographic network protocol used for securely connecting to and managing remote servers and devices over an unsecured network. It provides a secure, encrypted method for logging into and executing commands on a remote machine, as well as for secure file transfer. SSH is widely used for various purposes, including system administration, remote access, and secure data transfer.
The host we need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. 

## Level 1
The password to this level is stored in the readme file in the home directory. 

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/7b851d33-cbdb-4a4a-bded-1d2d51e37d68)

 

## Level 2
The password to this level is stored in a file called – located in the home directory of the system. 
./ is used to specify the current directory. This ensures that the - is treated as a file in the current directory.
- is the name of the file that needs to be read

 ![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/d2a28bbf-e5ab-4501-b86e-d6f26472901f)

 

## Level 3
The password to the level is stored in a file called spaces in the filename located in the home directory. In this example, the backslashes are used to escape the spaces in the filename, allowing you to read the file without needing quotation marks.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/a9562cc3-d8ed-48ef-bae8-5c1a7cb238a5)


 

## Level 4
The password to this level is in a hidden file in the inhere directory. Hidden files in Unix-like operating systems are typically files whose filenames start with a dot (.) character. These files are hidden in the sense that they are not displayed when you use common commands to list files or directories, such as ls. They are often used to store configuration or metadata information that is not meant to be directly accessed by users.
To locate hidden files, you can use the -a (or --all) option with the ls command, which instructs ls to show hidden files in the listing.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/5ba0af96-47f9-4e90-8777-073f4175ab6e)

## Level 5
The password for the next level is stored in the only human-readable file in the inhere directory.
file: This is the file command, a Unix/Linux utility used to determine and display information about the type of a file.
./: This represents the current directory. In Unix-like systems, ./ is a shorthand notation for the current working directory. In this context, it tells the file command to look for the specified files in the current directory.
-file0*: This is a pattern used to match files in the current directory. The pattern -file0* indicates that you want to match files that start with -file0 and can have any characters after that. The asterisk * is a wildcard that matches any number of characters. So, this pattern matches filenames like -file01, -file02, and so on.
Putting it all together, the file ./-file0* command checks the file type of all files in the current directory whose names start with -file0. The file command will return information about the type of each matched file, which could be things like text, binary, image, or various other file types. This is useful when you want to quickly identify the file types in a directory, especially if you're dealing with a mix of file formats.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/f6ee1a7c-76d3-4671-84ff-a1464340b9ea)









## Level 6
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:  human-readable, 1033 bytes in size, not executable.
find: This is the find command, a versatile utility used to search for files and directories in a specified location.
-type f: This is a test condition for find that specifies you're looking for files (not directories). The -type f option filters out directories and selects only regular files.
-readable: This is another test condition for find. It filters for files that are readable by the user running the command. In other words, it looks for files that you have read permissions on.
!: The exclamation point ! is used to negate the following condition. In this case, it negates the -executable condition, which means it selects files that are not executable.
-executable: This is a test condition for find that checks whether a file is executable. By using ! before it, we're excluding files that are executable.
-size 1033c: This is a test condition for find that specifies the size of the files to search for. In this case, it's looking for files with a size of 1033 bytes. The c indicates that the size is measured in bytes.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/672fcdd2-8ba1-4e7f-b75c-0ee8ca7cdfab)

 

## Level 7 

The password for the next level is stored somewhere on the server and has all of the following properties:owned by user bandit7, owned by group bandit6, 33 bytes in size
The find command is again utilized to solve this level. 
/: This is the starting directory for the search. In this case, / represents the root directory, which means the search will begin at the root of the file system and traverse through all directories.
-type f: This is a test condition for find that specifies you're looking for files (not directories). The -type f option filters out directories and selects only regular files.
-size 33c: This is a test condition for find that specifies the size of the files to search for. In this case, it's looking for files with a size of 33 bytes. The c indicates that the size is measured in bytes.
-group bandit6: This is a test condition for find that filters files based on their group ownership. It selects files that belong to the group named "bandit6."
-user bandit7: This is another test condition for find that filters files based on their user ownership. It selects files that are owned by the user named "bandit7."

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/95c6c5ad-04bf-4ae0-a9cb-284b9c7c1cea)

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/af7ece3c-18a8-470c-9da8-d3ad2a261183)



 
 


## Level 8 
The password for the next level is stored in the file data.txt next to the word millionth.
cat data.txt: The cat command is used to concatenate and display the contents of one or more files. In this case, it is used to display the contents of a file named data.txt. data.txt is the input file for this command, and cat will display its content to the standard output (usually your terminal).
| (pipe): The pipe symbol | is used to redirect the standard output (stdout) of the command on its left to the standard input (stdin) of the command on its right. In this case, it pipes the output of cat data.txt as input to the next command, grep.
grep millionth: The grep command is used to search for patterns in text. In this command, it searches for the word "millionth" within the text received from cat data.txt. If "millionth" is found within the text, grep will display the lines containing that word.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/3baef231-67a9-4857-ab1a-a64e20d723cf)

 
## Level 9
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.
sort data.txt: The sort command is used to sort the lines in a text file. In this case, it's sorting the lines in the file data.txt. After execution, the lines in data.txt will be sorted in lexicographic (alphabetical) order.
| (pipe): The pipe symbol | is used to redirect the standard output (stdout) of the command on its left to the standard input (stdin) of the command on its right. In this case, it pipes the sorted output from sort data.txt to the next command, uniq -c.
uniq -c: The uniq command is used to filter out duplicate lines from a sorted input. The -c option is used to count the number of occurrences of each unique line. In this case, it will provide a count of how many times each line appears in the sorted data.
| (pipe): Another pipe is used to redirect the output from uniq -c to the next command, grep "1 ".
grep "1 ": The grep command is used to search for patterns in text. In this command, it searches for lines containing the pattern "1 " (a space after the number 1). This will match lines from the output of uniq -c where the count is exactly 1.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/9c5c137a-4497-4f49-9766-94f7e0dff2fe)


 

## Level 10
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.
cat data.txt: The cat command is used to concatenate and display the contents of the file named data.txt. It reads the content of the file and sends it to the standard output (usually your terminal).
| (pipe): The pipe symbol | is used to redirect the standard output (stdout) of the command on its left to the standard input (stdin) of the command on its right. In this case, it pipes the output of cat data.txt as input to the next command, strings.
strings: The strings command is used to extract human-readable text from binary files or data. It scans the input data for sequences of printable characters and displays them.
| (pipe): Another pipe is used to redirect the output from strings to the next command, grep ^=.
grep ^=: The grep command is used to search for patterns in text. In this command, it searches for lines that start with the = character.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/591754a7-3d57-4134-85e4-d194f0ee858b)


 
## Level 11
The password for the next level is stored in the file data.txt, which contains base64 encoded data.
Base64 encoding is a method of encoding binary data, such as files or non-text data, into a text-based format. It is commonly used in computing and data transmission to represent binary data as ASCII text, making it easier to store, transfer, and display data in systems that expect text.
Key features of Base64 encoding include:
•	Character Set: Base64 encoding typically uses the characters A-Z, a-z, 0-9, along with two additional characters (usually '+ and '/), which are used to represent the 64 possible values (hence "Base64").
•	Padding: Base64-encoded data may have padding characters, typically '=' at the end of the encoded data, to ensure that the length of the encoded data is a multiple of 4. This padding helps align the data for proper decoding.
•	URL-safe Base64: To accommodate URL parameters and avoid potential encoding conflicts, URL-safe Base64 replaces '+' with '-' and '/' with '_'.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/9b562209-7101-4e7c-8832-d3226a366bb5)


 
## Level 12
ROT13, which stands for "rotate by 13 places," is a simple letter substitution cipher used to obscure text by shifting the letters of the alphabet 13 positions. It's a basic and reversible form of encryption, often used for fun or as a simple way to hide text from casual readers.
To decode a message encoded with ROT13 (rotate by 13 places) in the terminal, you can use the tr command, which is a simple text manipulation tool. The ROT13 encoding is a simple letter substitution cipher that replaces a letter with the 13th letter after it in the alphabet, wrapping around if needed.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/5214ced9-70d4-471a-8740-a04d9cf902d0)

## Level 13

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed.
We start by creating a directory in which we can work under /tmp. We use the xxd -r command to reverse the operation performed by the xxd command. xxd is a utility that is typically used to create a hexadecimal dump of a binary file or to convert binary data into a hexadecimal representation.

The hint states that the file was compressed multiple times, so we use the file command at each instance in order to figure out what compression tool has been used. After finding out the compression tool we accordingly use the mv tool to add the desired extension and perform the necessary decompression. We continue this process until we finally encounter the ASCII text file that contains the password to the next level.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/a78f7f4b-51e6-4e48-acd4-ca83975ed056)
![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/0b046cc9-d9d3-4ec7-8216-7059fc904e88)
![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/bb86a3b9-1718-4bae-93c6-55b824221c0b)
![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/34b1eb28-d5ea-430d-bafa-fef882a78bbc)





 
 
 
 

## Level 14
The objective here is to obtain the password for Bandit Level 14 by utilizing an SSH private key. After logging in, you list the contents of your home directory (the ls -la command). In this directory, you find a file named sshkey.private.
The next step is to copy the sshkey.private file from the remote server (Bandit Level 13) to your local machine using scp. 

After copying the sshkey.private file, you change the permissions of the file to make it readable only by you. This is done to protect the private key from unauthorized access. The chmod command is used, 400 sets the permissions so that the file is readable by the owner and not accessible by others.

-i sshkey.private: Specifies the private key to use for authentication.
bandit14@bandit.labs.overthewire.org: The username and hostname for Level 14.
-p 2220: Specifies the port to connect to.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/af2dc692-d299-40f4-bf88-18f65efa50c2)
![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/53182f9f-9107-4069-8b4a-f4d435b2f6d4)

 
 

## Level 15
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.
The nc command, which stands for "netcat," is a versatile and powerful networking utility available on Unix-like operating systems. It can be used for various network-related tasks, such as port scanning, network debugging, transferring files, and creating network connections. nc is often referred to as the "Swiss Army knife" for networking due to its wide range of capabilities. 
So, the command nc localhost 30000 initiates a network connection to a service or application running on your local machine on port 30000. The exact behavior and purpose of this connection depend on the service or application listening on port 30000.
![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/b9af6225-abb1-4fb8-a39f-ff9e00875225)

 

## Level 16
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.
SSL (Secure Sockets Layer) encryption is a cryptographic protocol that is used to secure the communication between a client and a server over a network, typically the internet. SSL/TLS (Transport Layer Security, the successor to SSL) ensures that data transmitted between the client and server remains confidential and cannot be easily intercepted, read, or altered by malicious actors. It provides encryption, data integrity, and authentication to protect the privacy and security of information exchanged over the network.

When you run this command, OpenSSL's s_client utility initiates an SSL/TLS handshake with the server running on localhost at port 30001. It performs the following actions:

•	It starts the SSL/TLS handshake by sending a ClientHello message to the server.
•	It checks the server's SSL/TLS certificate (if available) and verifies its authenticity. If the server does not have a certificate or if it's self-signed, you might see a warning.
•	It completes the SSL/TLS handshake and establishes an encrypted connection.
•	You can then interact with the server over this encrypted connection. Any data you send or receive will be encrypted and secured.
![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/13f83603-6482-4069-91b9-1a34cafedf22)




 
Submitting the previous password gives us the next: 
![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/ca66404f-77c2-453a-b7dd-578719dbbca2)

 
## Level 17

The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t.
nmap: This is the command to invoke Nmap.
-sV: This option tells Nmap to perform service version detection. In other words, it will attempt to identify the services running on the open ports by analyzing their responses. This can help in determining which specific software or application is running on each port.
-T4: This option sets the timing template to "aggressive" (T4). It controls the speed at which Nmap performs the scan. T4 is faster than the default timing template, but it can be more aggressive and may consume more resources. This option is suitable for relatively stable and responsive networks.
-p 31000-32000: This option specifies the range of ports to scan. Nmap will scan all ports within the range of 31000 to 32000. This is useful for discovering open ports on a target system.
localhost: This is the target host you want to scan. In this case, "localhost" refers to the local machine, so Nmap will perform a scan on ports in the specified range on your own machine.

After connecting to the 31790 port with "openssl s_client -connect localhost:31790" and entering the password for bandit16 one obtains a private RSA key which can be used to ssh into the next level !

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/acf59dac-835e-4e72-a3bc-764966a156d0)
![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/82e48866-da90-4e06-826c-9c5e22eb30d5)
![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/c057c171-4251-4f20-a10e-f1c95aabe74b)




 
    

## Level 18

There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new
The command diff passwords.old passwords.new is used to compare the contents of two text files, passwords.old and passwords.new, in order to identify and display the differences between them.
diff: This is the command used to compare files in Unix-like operating systems. It can identify and display the differences between two text files.
passwords.old and passwords.new: These are the file names of the two text files you want to compare.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/04efa9b8-af05-45d8-b691-f211dddbeb27)

 

## Level 19

The password for the next level is stored in a file readme in the home directory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.
When you log in via SSH, the default shell specified in your user account's configuration is typically Bash. If someone has tampered with your .bashrc file to trigger a logout, you can try specifying a different shell when connecting using SSH. For example, you can use the sh shell:

  ![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/b5e8fc8b-8f7f-4491-ba7f-b9d6f238d554)




## Level 20

On running the ls command we see an executable binary file. We observe that when we use the binary file we are assigned the uid for bandit20 as well which means we can run commands as if we are bandit20.
The command ./bandit20-do cat /etc/bandit_pass/bandit20 is attempting to read and display the contents of the /etc/bandit_pass/bandit20 file using the cat command.

![image](https://github.com/KarsCode/OverTheWire-Bandit-Writeups/assets/117924364/fa261e3a-b1b7-4414-a827-63d4864f4ad9)


 





 




