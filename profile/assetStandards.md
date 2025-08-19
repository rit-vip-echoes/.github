# **Aesthetics Standards**

# Index 
[AI Usage](#ai-usage)  

[Naming Conventions](#naming-conventions)  

[Art Pipeline](#art-pipeline)  

[File Information](#file-information)

[Aesthetics: Art & Asset Softwares](https://docs.google.com/document/d/1MNavkpXOygKtGuOJaoWBSeViJ15xxJjtohfYlFMrH8o/edit#heading=h.uqleju9r1i7q)

[Aesthetics: Music Software and Composition Guide](https://docs.google.com/document/d/19HEvmC8DD8yydG_SIaQAae3PHa3fOF3AO5Jn6QQ-52I/edit#heading=h.pdw337xzz9y)

[Branding Guidlines](https://docs.google.com/document/d/12TpMxFRPnAxTtqIhqanuayRmCgFmaLlivKxt0iqhiMU/edit?tab=t.kow94o1vljt7)

# AI Usage

AI may be used to generate keywords and ideas for assets. But for legal and ethical purposes, **DO NOT USE AI TO GENERATE FINAL ASSETS OF ANY KIND**.

# Naming Conventions 

Naming conventions are very important as they help keep large-scale projects organized. This means that all teams across the project should use these conventions when naming their assets.

Consult with your team on naming conventions. A standard naming convention is to use camel case ex. `HereIsAName`. Furthermore, the type of asset could be denoted as a prefix for ease of engine use such as `Tex_Name` for a texture. In the end, it's up to the teams to determine the standard naming conventions they will use. 

# Art Pipeline 

An art pipeline is a series of steps that designers and developers use to create assets for video games. An established pipeline helps make sure that the project is organized and communication between artists and the developers. 

## 1. **Asset Request**

Teams will use the project’s project board to keep track of needed assets (See [Task Managment](https://github.com/rit-vip-echoes/.github/blob/main/profile/taskMgmt.md) ).  
		
They will create a new issue on the project board with the relevant information for the asset. (type, description etc.). 

## 2. **Create Asset**

Team members will work to either create or find a relevant asset. If the asset is found, ensure it has the proper license to be used. 

## 4. **Communicate with team(s)**

Maintain consistent communication and show work often. This will make sure everyone is happy with the asset's direction and it aligns with what was expected. 

## 5. **Upload to Drive**

Once the asset is complete, export the asset to the correct  `raw` file format and the needed game file format (See [File Information](#file-information)) and make sure that naming conventions are followed (See [Naming Conventions](#naming-conventions)). 

Put the asset in the ***echoes*** **Drive \> Projects \> Game Name \> Asset Folder** or ***echoes*** **Drive \> Web \> RIT Official VIP Website Content \> Asset Folder**. 
Create new folders when needed for useful organization.
	

## 5. **Add to Unity** 
1. Create a new [Branch](https://github.com/rit-vip-echoes/.github/blob/main/profile/branches.md) for the asset.
2. Import the assets into that branch within Unity. 
	 -  Import settings can be changed in Unity to reduce file size/modify the asset, which can fix common issues. 
3. Optionally implement the asset where it is needed. 
5. Make a [Pull Request](https://github.com/rit-vip-echoes/.github/blob/main/profile/pullRequests.md) for the asset.
      This will allow team members to view and approve it. Be sure to link to the drive files as well. 

# File Information 

It is important to upload the raw files into the drive so that other members are able to download and work on them.

 Raw files should be accessible to all team members so that they can open the files in different software. Save raw files into the drive upon asset completion.
| Type of Asset | Raw File Extension | Exported File Extension |
| :---- | :---- | :---- |
| 2D Raster Image | .psd | .png |
| 2D Vector Image | .svg | .png and/or .svg |
| 2D Pixel Art | .ase | .png |
| 3D Model | .mb or .blend | .fbx |
| Audio | Zipped up project file | .wav |
