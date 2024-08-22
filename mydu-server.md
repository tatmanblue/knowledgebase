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
5. run `scripts\maintenance-mode-off.bat`  if that is missing, run `docker-compose run --entrypoint /usr/bin/curl sandbox -v -d '' http://queueing:9630/parameters/maintenance/false`
6. stop and restart du server (use the batch files provided)
7. log into backoffice https://localhost:12000/Backoffice using admin account and password you setup during in the install (step 2)
8. create user accounts, other config. Any user accounts that will be used to play the game need to have the game role assigned.
9. run the my du client
10. once your at the server selection screen, in server url field use the ip address in steps 3 and 4, login and password from the accounts you created in the backoffice (if you don't want to use admin)

I think that was it for me. I think the real trick was steps 4,5, and correct ip address in 9


## Make a Market
```
----------------------------------------------------------------

HOW TO MAKE OWN MARKET 

----------------------------------------------------------------

DO THIS ALL FROM BO  ( BACK OFFICE )

GO INTO PLAYERS ---> admin  ( or what ever your player name is ) 

Go TO INVENTORY AND ADD ITEMS =

ADD ITEM " Static Core ANY SIZE " 

ADD ITEM " MARKET POD "

ADD ITEM " MARKET UNIT M " <---- MARKET UNIT M SUPER IMPORTAND NOT THE OTHER ONCE ONLY  !!!! M !!!!!


MARKET UNIT IS THE BIG ANTENNA THINGY ( IF IT SHOWS ERROR ITEM)

MARKET POD IS THE TINY THINGY ( IF IT SHOWS ERROR ITEM)


NEXT STEP  =  GO INTO GAME  PLACE STATIC CORE " ANY SIZE "  ---->  PLACE "MARKET UNIT M " IN BUILDMODE AND PLACE FIRST " MARKET UNIT M " 



NEXT STEP  = PLACE  MARKET POD  " MARKET POD "  --> THEN LINK "MARKET POD" --->  TO  " MARKET  UNIT M "


NEXT STEP =  RELOG ( RESTART GAME OR JUST LOGOUT AND BACK INTO YOUR SERVER )



DONE    YIPPIIIII 




HOW TO  CHANGE NAME OF  YOUR OWN MARKET OR NEW ONCES WHAT HAVE BEEN PLACED

2 WAYS TO DO IT  FAST WAY OR SLOW WAY 

----------------------------------------------------------------

FAST WAY  

----------------------------------------------------------------

GO TO BO  

CLICK ON MARKETS 

SCROLL DOWN FIND YOUR NEW MAKET MOSTLY NAMED " My Market "

TAKE THE ID ( NUMBER FAR LEFT ) 

SCROLL DOWN ON THE BATCH PARAMETER UPDATE

WRITE ID INTO MARKET ID FILD

GO 2 DOWN AND WRITE NEW NAME INTO UPDATE PARAMETERS

PRESS UPDATE

RELOG GAME CLIENT  OR IF U HAVE A BIG SERVER WITH MANY PLAYER  RESTART SERVER

DONE 

HYYYYYPEEEEEEE WUPPPIIII DOOO 




----------------------------------------------------------------

SLOW WAY

----------------------------------------------------------------


FIRST  STEP  =  CMD IN SERVER FOLDER 

NEXT STEP PASTE THIS IN CMD WITH RIGHTCLICK IN WINDOW OF CMD   = 


docker-compose exec postgres psql -U postgres -d dual


NEXT STEP COPY PASTE BEHIND " dual=#  " THIS CODE  TO SEE ALL MARKETS =      


select * from market; 

NEXT STEP FIND YOUR MARKET IN THE LIST  ( SPAM SPACEBAR UNTIL BOTTUM )



NEXT STEP LOOK FOR " MY MARKET " AND  GET THE ID AND CHANGE NAME IN THE NEXT CODE PLS READ THE CODE AND INSERT YOUR ID + WANTED NAME= 


update market set name ='INSERT NEW NAME HERE' where id = 'INSERT ID HERE';

NEXT STEP  RUN THIS CODE  + YOUR ID WHAT U INSERT THERE  1 TIME TO CHECK IF THE NAME OF MARKET CHANGED =


INFO = REMOVE THE INSERTIDHERE AND ADD YOUR ID THERE FROM THE MARKET

select * from market where id = INSERTIDHERE;  

LAST STEP = 

RELOG AND JOIN INTO SERVER AGAIN AND ITS DONE  IF YOUR SERVER IS BIG WITH MANY PPL JUST DO A SERVER RESTART SO EVERYONE WILL SEE THE MARKET

----------------------------------------------------------------



```
