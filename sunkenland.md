# Sunkenland

Steam Page: [Link](https://store.steampowered.com/app/2080690/Sunkenland/)  

Game saves, on windows, are located at `C:\Users\{userid}\AppData\LocalLow\Vector3 Studio\Sunkenland\worlds`  

All game data is in one plain text file, json formatted file called: `World.json'  

This source [Link](https://thenerdstash.com/sunkenland-all-item-ids-and-how-to-modify-save/) list ids and items.  But their ids do not 
seem to match what we found listed here.  Looking at reddit, looks like item ids have changed.  


## item information gathered  

Version: 0.2.0  
  
| Name | Id | Max |  
| ---- | ---- | ---- |  
| Advanced Parts  | 6103 |   5 |  
| Arrow           | 6257 |   ? |  
| Ballistic Fiber | 6102 |   ? |  
| Battery         | 7012 |   ? |  
| Can Food        | 3009 |  50 |  
| Chemical Substa | 6152 |   ? |  
| Cloth           | 6001 |  20 |  
| Coal            | 6202 |   ? |  
| Copper Ingot    | 10006 | 50 |  
| Copper Ore      | 6062 |  10 |  
| Components      | 6055 |  10 |  
| Crude Grenade   | 6501 |   5 |  
| Duct Tape       | 6003 |  20 |  
| Electronics     | 6060 |  10 | 
| Flare           | 7010 |   ? |  
| Gasoline        | 6201 |  20 |  
| Glass           | 6056 |   ? |  
| Gun Part        | 6101 |   5 |  
| Iron Ingot      | 10003 | 50 |  
| Iron Ore        | 6061 |  10 |  
| Leather         | 6006 |  20 |  
| Marlin Fish Skin | 6057 | 10 |  
| Pistol Ammo     | 6254 |   ? |  
| Potatoe         | 2012 |   ? |  
| Rope            | 10001 | 30 |  
| Rubber          | 6058 |  10 |  
| Scrap           | 6004 |  20 |  
| Shark Fin       | 6059 |  10 |  
| Smokeless Pwdr  | 10004 |  ? |  
| Strawberry Seed | 6705 |   ? |  
| Sulfur          | 6151 |   ? |  
| Wood            | 6200 |  50 |  


# Research level

To change your Research level without needing resources, look for:  

```
	"ResearchLevel" : {
		"__type" : "int",
		"value" : 3
	},
```

Change `value`.  Max value is 4.  