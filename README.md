# Rosemary Village Creating And ImportingAssets
Hello and welcome to a ever expanding on how to creating and importing assets into Rosemary village

## General Rules
Before we begin I want to give some general rules of creating game ready assets.
#### Keep in mind the target hardware.
When you are making anything relating to rendering you need to keep in mind that everything has to be done 60ish times a second. That only leave 16ms of time to render each frame.
Now you are probably asking well okay cool but what does that have to do with importing models? Well for Rosemary Village are target hardware varys in power greatly so every tri, texture, and light matters. Be creative in thinking of ways to optimize your assets and still get the target look.
#### Tri Density
When making meshes keep in mind the intended size of the model in the game world. And the distance the player will be viewing the model from.  It is hard to give any general reccomendations on density but general models over 10k tris start to become slow on mobile. Make sure to check wire frame and see if it looks very dense is places and see if you can reduce the tris in that area.

#### Normals
What is a normal? A normal tell the engine which way a face is pointing. The image below shows a simple plane being lit along a surface normal offset by a texture type called a normal map.
Credit for the image and more detailed info can be found at: https://learnopengl.com/Advanced-Lighting/Normal-Mapping

[![](https://learnopengl.com/img/advanced-lighting/normal_mapping_ground_normals.png)](https://learnopengl.com/img/advanced-lighting/normal_mapping_ground_normals.png)

Now how does this relate to creating game ready assets? Well when the engine lights a model a key component how how it decides to do so is the normals. For example if a normal is facing towards a light will be lighter and one facing a way will be darker.  
Now for a more pratical Example in the image below on the left you notice how the model looks inside out? This is because of a optimization called back face calling that doesnt render triangles facing away from the camera. The one one the right has all the normals facing the correct direction. To recaculate the normals in blender just go into edit mote ctrl+A to select all then shift+n to recaculate normals.  
[![](https://media.discordapp.net/attachments/1053745787391180850/1060341441064337429/BadVsGoodNormals.png)](https://media.discordapp.net/attachments/1053745787391180850/1060341441064337429/BadVsGoodNormals.png)
<br>
(Note: to get this view in blender go to the top right view mode changer and change click the downward arrow and look for backface culling if it doesn't show try a different view mode)  

#### Texures and VRAM
So textures can be both a optimization or a large performance hog depending on the bottle neck. Textures are stored in something called VRAM (Video Random Access Memory). When the VRAM is filled to much it can cause major performance drops so keeping in the mind the resolution of images/textures is important. The general Rule in game dev 512x512 per meter in third person games which is a good target.

## Importing Wardrobe Items
**NOTE: THIS SECTION IS VERY WIP AND LIKELY TO CHANGE**
