# GLPI_POC_Plugins_Shell

Description
Summary

It is possible, with the 'shell commands' plugin, to execute code on the server, thereby allowing remote command execution (RCE)

Details

There are several things to consider, as it is possible, in the 'Path', to specify the command we want to execute. Moreover, in the [NAME] section for the computer's name, we can put whatever we want, be it a link or a command.

PoC

In the 'Path' section, we add the wget command

<img width="1106" alt="318229839-971a2c5a-c18a-4c94-bae7-c94711aa5687" src="https://github.com/V3locidad/GLPI_POC_Plugins_Shell/assets/109574266/a23b9017-f900-480f-8695-efb4c46d8bf4">


In the TAG, we put [NAME]

<img width="1258" alt="318229886-b45b8759-4732-439a-badf-844747520b55" src="https://github.com/V3locidad/GLPI_POC_Plugins_Shell/assets/109574266/b486a3f2-9671-4b0f-af68-d90d32fc06f3">


In 'Associated Item', we add 'computer'

<img width="1256" alt="318229930-59b3e30d-f22c-4534-9aa8-aadd29a0dfd8" src="https://github.com/V3locidad/GLPI_POC_Plugins_Shell/assets/109574266/f9f0906b-2f46-48b4-9e83-faca4374edde">


Now, let's put a shell.php file on our computer and set up a web server

<img width="776" alt="318229970-014727d1-5655-4ae9-b206-7a377b452b4c" src="https://github.com/V3locidad/GLPI_POC_Plugins_Shell/assets/109574266/6b2777d2-b7f1-46dc-8ce4-25b557a78551">


We create a new computer with our web server in the NAME section

<img width="1234" alt="318230011-35ed15f0-d32a-4f16-8bfb-35b25ba4100b" src="https://github.com/V3locidad/GLPI_POC_Plugins_Shell/assets/109574266/9fe2ee55-658a-46cb-aacb-d55ebbdc3032">

In the 'Shell Commands' tab on the computer, we can launch our command

<img width="1035" alt="318230089-60ea78fa-a66d-4dbe-b1df-3dcd9c84e27a" src="https://github.com/V3locidad/GLPI_POC_Plugins_Shell/assets/109574266/a500d32b-7df1-4c17-bb2b-6797bdeaa00d">

We can see that the command has been successfully executed

<img width="1022" alt="318230186-47177555-4af3-4434-a68a-9acb102fb896" src="https://github.com/V3locidad/GLPI_POC_Plugins_Shell/assets/109574266/b4ed73aa-c5c8-412e-ba11-ec9140e4913c">

We start listening on our computer.

<img width="412" alt="318230226-3bca4a1e-1269-4fce-945d-2b01705d9f69" src="https://github.com/V3locidad/GLPI_POC_Plugins_Shell/assets/109574266/4e9a878f-14b0-434c-9b91-1b03f072e8b3">

We go to the link where our shell.php file is located (it is accessible without authentication)

<img width="411" alt="318230251-ea8768af-16cd-4d44-957b-c467d90f5ba6" src="https://github.com/V3locidad/GLPI_POC_Plugins_Shell/assets/109574266/96a8c40b-c188-4fe7-8a03-27be595b7f06">

We have obtained a shell on the server

<img width="983" alt="318230299-3224033b-1a4e-4bca-b3de-c4214e1bcb68" src="https://github.com/V3locidad/GLPI_POC_Plugins_Shell/assets/109574266/e82497ff-6cf4-4482-8620-8aa089741b0e">
