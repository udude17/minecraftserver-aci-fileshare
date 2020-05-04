# minecraftserver-aci-fileshare
Minecraft Server Azure Container Instance with File Share

Type FORGE was chosen to have a chance at using mods on the server.

Here are some instructions to get in running in an Azure Subscription with Contributor rights:

		Step 1:  Create storage account and file shares with names noted in the template resource section
		
		Step 2:  Edit the TYPE to be either FORGE or other type
		
		Step 3:  Update the storage account name (prefix only) to match what you chose in Step 1
		
		Step 4:  Update the dnsName
		
		Step 5:  Deploy template either 
        	 	Azure Portal, create new "Template Deployment (using custom template)" 
             		Paste the raw text into the editor, save and deploy
             
NOTES:  
The main files after using the game are on the file share in the /world directory. 

Consider the /save-all commmand to flush the server to the file share before exiting the game. An ACI container stop command in the Azure Portal does generally make the minecraft server save to disk, but I would wait 1 minute regardless, just in case. 


Have fun. 

