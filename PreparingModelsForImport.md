# Preparing Models For Import
[Home](README.md) <br>
Hello welcome to the guide for preparing a model for importing into the Rosemary Village primarily focused on the wardrobe system but can be used for anything.

## Review
Before doing the next step make sure your model is game ready as outlined [here](README.md). To review your model should have all normals outward facing, textures should be 512x512 per meter, and tri density should be to a minimum.
## Joining and Naming Parts
Now that your model will render right and be preformant we need to take some steps to make the model easier to work with in Studio. The first step of this is to join/merge your different meshes in blender this can be done with ctrl+j. When deciding what to join think about what parts use the same material, how it is supposed to move, and for wardrobe items the items type docs of which can be found [here](PreparingModelsForImport.md).<br>

---
Now lets look at a pratical example. Lets say I have full set I want to prepare to import. The set is a "static" part replacer meaning we don't intend for it to be part of the layered clothing system. First we want to name all the body parts to match the [R15 body parts](https://create.roblox.com/docs/reference/engine/enums/BodyPartR15). Don't worry if you are missing some parts we can add invisble place holders in studio.<br>

Now we think about how this model will be split into different [wardrobe items](). Now we join all meshes that belong to a single item. If the item is multi colored keep the colors seperate and name it in a way that cleary marks they are related. After your mesh is joined into the minimum possible parts make sure to check the origins if they are wonkey right clicking and doing set origin->Origin to Geometry will work for are usecase. This will ensure that if we need to move the parts in studio it will move how we expect. Finally make sure to name all your parts this will make the final steps way easier.<br>

Now that your model is ready for import see [Wardrobe Item Types]() for how to implement your items in game.
