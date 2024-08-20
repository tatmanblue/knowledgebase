# quick notes  
for a clean install on win 11)  
1) stop all all containers and delete, on last one server will disappear.  
2) delete server directory   
3) reboot (i dont care its not linux its windows reboot) 3.5)install win server binary  
4) these steps mydu-announcements   
5) then this mydu-server-questions  

## Step 4  
1 - Open a command prompt 
2 - Navigate to your server install directory   
3 - Run: docker pull novaquark/dual-server-fastinstall:latest  
4 - Run: docker run --rm -v "%CD%":/output/ --entrypoint cp novaquark/dual-server-fastinstall:latest -r /server/scripts /output  


Backoffice - https://localhost:12000/Backoffice

Item Hierarchy > GameplayObject > Character > defaultWallet  
