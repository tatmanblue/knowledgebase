# Sunkenland

Steam Page: [Link](https://store.steampowered.com/app/2080690/Sunkenland/)  

## World Saves

Game saves, on windows, are located at `C:\Users\{userid}\AppData\LocalLow\Vector3 Studio\Sunkenland\worlds`  

All game data is in one plain text file, json formatted file called: `World.json'  

This source [Link](https://thenerdstash.com/sunkenland-all-item-ids-and-how-to-modify-save/) list ids and items.  But their ids do not 
seem to match what we found listed here.  Looking at reddit, looks like item ids have changed.  


## item information gathered  

Version: 0.2.0  
  
| Name | Id | Max |  
| ---- | ---- | ---- |  
| 50 cal Ammo      | 6251  |  1K |  
| Advanced Parts   | 6103  |   5 |  
| Arrow            | 6257  |  50 |  
| Ballistic Fiber  | 6102  |   ? |  
| Battery          | 7012  |   ? |  
| Black Powder     | 6252  |  50 |  
| Bush Seed        | 6701  |   ? |  
| Can Food         | 3009  |  50 |  
| Chemical Substa  | 6152  |   5 |  
| Cloth            | 6001  |  20 |  
| Coal             | 6202  |   ? |  
| Components       | 6055  |  10 |  
| Copper Ingot     | 10006 |  50 |  
| Copper Ore       | 6062  |  10 |  
| Cotton Seed      | 6703  |   ? |  
| Crude Grenade    | 6501  |   5 |  
| Duct Tape        | 6003  |  20 |  
| Electronics      | 6060  |  10 |  
| Fine Plank       | 10005 |   ? |  
| Flare            | 7010  |   ? |  
| Gasoline         | 6201  |  20 |  
| Glass            | 6056  |   ? |  
| Gun Part         | 6101  |   5 |  
| Herbal Med       | 3002  |  30 |  
| Iron Ingot       | 10003 |  50 |  
| Iron Ore         | 6061  |  10 |  
| Leather          | 6006  |  20 |  
| Lemon Seed       | 6704  |   ? |  
| Marlin Fish Skin | 6057  |  10 |  
| Military Grenade | 6502  |   ? |  
| Modern Parts     | 10012 |   ? |  
| Modern Gun Part  | 10013 |  50 |   
| Molotov Cocktail | 6503  |   5 |  
| Pistol Ammo      | 6254  | 500 |  
| Potatoe          | 2012  |   ? |  
| Rifle Ammo       | 6255  |   ? |  
| Rope             | 10001 |  30 |  
| Rubber           | 6058  |  10 |  
| Scrap            | 6004  |  20 |  
| Scrap Metal Stk  | 24039 |     |  
| Shark Fin        | 6059  |  10 |  
| Shotgun Ammo     | 6256  |   ? |  
| Skull Crusher Ax | 1108  |   ? |  
| Smokeless Pwdr   | 10004 |   ? |  
| Soda             | 3012  |   ? |  
| Steel Ingot      | 10008 |  50 |  
| Strawberry Seed  | 6705  |   ? |  
| Sulfur           | 6151  |   ? |  
| Wood             | 6200  |  50 |  


### Research level

To change your Research level without needing resources, look for:  

```
	"ResearchLevel" : {
		"__type" : "int",
		"value" : 3
	},
```

Change `value`.  Max value is 4.  

### Water distiller -- manual

Change `SeawaterAmount` (max 10) to add sea water which will get processed to `WaterAmount`.  Update `WaterAmount` for drinkable water (max 5).

```
	"WaterDistrillers" : {
		"__type" : "System.Collections.Generic.List`1[[WaterDistrillerData, Assembly-CSharp, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null]],mscorlib",
		"value" : [
		{
			"BuildingID" : -158760,
			"SeawaterAmount" : 10,
			"Fuel" : 10,
			"WaterAmount" : 5,
			"IsWorking" : false
		}
	]
	}
```
