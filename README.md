# Medium-Unity-2022
Unity 2022.3.16f1

# Guidelines

## Asset Naming
First of all, no **spaces** on file or directory names  
  
### Folders
`PascalCase`  \
Prefer a deep folder structure over having long asset names  \
  \
Directory names should be as concise as possible, prefer one or two words  \
If a directory name is too long, it probably makes sense to split it into sub directories  \
  \
  \
Try to have only one file type per folder  \
Use `Textures/Trees`, `Models/Trees` and not `Trees/Textures`, `Trees/Models`  \
  \
That way its easy to set up root directories for the different software involved, for example,  \
Substance Painter would always be set to save to the Textures directory  \
  \
  \
If your project contains multiple environments or art sets, use the asset type for the parent directory:  \
`Trees/Jungle`, `Trees/City` not `Jungle/Trees`, `City/Trees`  \
  \
Since it makes it easier to compare similar assets from different art sets to ensure continuity across art sets  
  
#### Debug Folders
`[PascalCase]`  \
This signifies that the folder only contains assets that are not ready for production  \
For example, having an `[Assets]` and `Assets` folder  
  
### Non-Code Assets
Use `Tree_Small` not `Small_Tree`  \
While the latter sound better in English, it is much more effective  \
to group all tree objects together instead of all small objects  \
  \
  \
Use `Weapon_MiniGun` instead of `Weapon_Gun_Mini`  \
Avoid this if possible, for example,  \
`Vehicles_FighterJet` should be `Vehicles_Jet_Fighter` if you plan to have multiple types of jets  \
  \
  \
Prefer using descriptive suffixes instead of iterative:  \
`Vehicle_Truck_Damaged` not `Vehicle_Truck_01`  \
  \
If using numbers as a suffix, always use 2 digits:  \
`Tree_01`, `Tree_02`, `Tree_03`  \
And **do not** use it as a versioning system! Use `git` or something similar  
  
## Textures
File extension: `PNG`, `TIFF`, `HDR`  

#### Texture Suffixes
|Suffix|Texture|
|:--|:--|
|`_BC`|Base color|
|`_N`|Normal|
|`_M`|Metallic|
|`_S`|Smoothness|
|`_E`|Emission|
|`_AO`|Ambient Occlusion|
|`_H`|Height|
|`_D`|Displacement|
|`_Mask`|Mask|
  
#### RGB Masks
|Channel|Texture|
|:--|:--|
|R|Smoothness|
|G|Metallic|
|B|Ambient Occlusion|

##### The blue channel can vary depending on the type of material:  
- For character materials use the `B` channel for _subsurface opacity/strength_  
- For anisotropic materials use the `B` channel for the _anisotropic direction map_  

## Prefabs
Always reset transform position of the prefabs  \
(Set to `0 0 0`)  