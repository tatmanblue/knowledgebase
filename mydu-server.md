# My Du Server Setup

## Windows 
Not required but highly recommend you start with clean environment  
1. Stop all the docker containers
2. Remove all lingering containers, all images, all volumes
3. Delete the server install directory and all subdirectories
4. Reboot

Then these are the steps I gleaned from a few different sources.  
1. Down load the latest server install because it was updated today
2. Install that
3. run ipconfig to find your local ip adress
4. from the server install folder run `scripts\config-set-domain.bat config/dual.yaml http://10.0.0.106 10.0.0.106` (use your local ipaddress, not public)
5. run `scripts\maintenance-mode-off.sh`
6. stop and restart du server (use the batch files provided)
7. log into backoffice https://localhost:12000/Backoffice using admin account and password you setup during in the install (step 2)
8. create user accounts, other config. Any user accounts that will be used to play the game need to have the game role assigned.
9. run the my du client
10. once your at the server selection screen, in server url field use the ip address in steps 3 and 4, login and password from the accounts you created in the backoffice (if you don't want to use admin)

I think that was it for me. I think the real trick was steps 4,5, and correct ip address in 9
