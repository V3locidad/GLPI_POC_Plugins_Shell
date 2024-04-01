# GLPI_POC_Plugins_Shell

Description
Summary

It is possible, with the 'shell commands' plugin, to execute code on the server, thereby allowing remote command execution (RCE)

Details

There are several things to consider, as it is possible, in the 'Path', to specify the command we want to execute. Moreover, in the [NAME] section for the computer's name, we can put whatever we want, be it a link or a command.

PoC

In the 'Path' section, we add the wget command



In the TAG, we put [NAME]

Capture d’écran 2024-03-30 à 22 57 09
In 'Associated Item', we add 'computer'

Capture d’écran 2024-03-30 à 22 57 36
Now, let's put a shell.php file on our computer and set up a web server

Capture d’écran 2024-03-30 à 22 59 55
We create a new computer with our web server in the NAME section

Capture d’écran 2024-03-30 à 23 00 37
In the 'Shell Commands' tab on the computer, we can launch our command

Capture d’écran 2024-03-30 à 23 01 08
We can see that the command has been successfully executed

Capture d’écran 2024-03-30 à 23 02 47
We start listening on our computer.

Capture d’écran 2024-03-30 à 23 04 19
We go to the link where our shell.php file is located (it is accessible without authentication)

Capture d’écran 2024-03-30 à 23 03 49
We have obtained a shell on the server

Capture d’écran 2024-03-30 à 23 05 05
