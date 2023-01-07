# Wardrobe Item System
[Home](README.md) <br>
The wardrobe item system is relatively simple. At its core is a simple structure
* Model
    * Asset
    * Item Module

The model should be placed in serverstorage->Wardrobe->*Category*. 
****
Below is a example of what the Item Module looks like and what each value does for info relating to how to set up specific items see  [Wardrobe Item Types]()
```lua
-- Grabbing required modules
local WardrobeTypes = require(game.ServerStorage.Wardrobe.WardrobeTypes)
local OutfitSlot = require(game.ReplicatedStorage.OutfitSlot)

local ItemInfo = {
    -- The name that will be displayed in the wardrobe GUI
	DisplayName = "Example Hair",
    -- The outfit slot the asset belongs to
    -- See the OutfitSlot item module in replicated storage for more info
	Slot = OutfitSlot.Hair,
    -- The id of the image that should be displayed in wardrobe UI
	ImageId = 9903596064,
    -- Wether or not the player needs to have the item in there inventory to equip it
	NeedsUnlock = true,

    -- The type of the asset
    -- This will determine how the game reads the TypeInfo
	Type = WardrobeTypes.Accessory,

    -- Info relating to the type specified above
    -- Type info examples can be found in the Wardrobe Item Types section
	TypeInfo = {
		asset = script.Parent.Accessory
	}
}
return ItemInfo
```

Next I reccomend reading preparing a model for import! Or if you already understand the naming conventions skip to wardrobe Item Types
* [Preparing Model For Import]()
* [Wardrobe Item Types]()
