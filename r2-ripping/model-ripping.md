---
description: How To Rip Game Models With Textures into blender
---

# Exporting Models

## Required Software

* Blender
  * Blender Source Tool - For importing models into blender
  * S/G Shader - For linking textures
* Legion - RPAK ripping tool
* Crowbar - Source Engine model tool
* Titanfall VPK Tool - Titanfall VPK tool

{% hint style="info" %}
Check down bellow for the tools page where all the link are provided
{% endhint %}

{% content-ref url="../intro/duction/tools/" %}
[tools](../intro/duction/tools/)
{% endcontent-ref %}

## Getting The Models

First, we need to actually obtain the models. You can do this by extracting this VPK file you can learn how to extract VPKs

{% content-ref url="../intro/duction/vpk-packpack.md" %}
[vpk-packpack.md](../intro/duction/vpk-packpack.md)
{% endcontent-ref %}

For the most part, models can be found in the common vpk. But you will find other models in the other vpk from Titanfall 2.

```
"Titanfall2\vpk\englishclient_mp_common.bsp.pak000_dir.vpk"
```

Next, you need to find the model you want. In this guide, as an example, the CAR SMG will be chosen. Which is located here

```
ExtractedVPK\models\weapons\car101
```

However, we can't just straight import this into blender, we will need to decompile the model using crowbar. So first, extract crowbar using your archive software of choice, and load up `crowbar.exe`

![Copy these settings here, with the filepath to your model and click decompile](<../.gitbook/assets/crowbar settings.PNG>)

Once you've decompiled the model into the folder of your choice, we need to open up blender and install blender source tools.

![Go into your preferences panel](<../.gitbook/assets/Desktop 2020.08.10 - 14.13.29.22\_1.gif>)

![Click the install button on top of the blender preferences window](../.gitbook/assets/install.png)

![Locate your add-on and install it as shown.](<../.gitbook/assets/Adding the Addon.gif>)

## Importing The Models

Next, we need to import the models using blender source tools. This can easily be done by clicking on `File > import`, and importing the `.qc` file as shown

![](<../.gitbook/assets/Importing The Model.gif>)

After the model is imported, if you zoom out it should look like this

![](<../.gitbook/assets/CARSMG import without delete.PNG>)

As you can see, it has addons equipped, such as the proscreen. We can delete this as shown below

![](<../.gitbook/assets/Deleting The Proscreen.gif>)

## Texturing The Model

Finally, we can begin to texture our model, this is perhaps the most tedious step, so buckle up

![We can begin to import the nodetree which helps with texturing the model](<../.gitbook/assets/Appending the nodes.gif>)

![Change your workspace from layout, to shading.](<../.gitbook/assets/Shading Workspace.PNG>)

![Press File / Append](<../.gitbook/assets/APPEND ME.PNG>)

![Select your SG\_Shader blend file](<../.gitbook/assets/sg shader.PNG>)

![Select The Nodetree folder, and then the S/G shader](../.gitbook/assets/nodetree.PNG)

![Delete / Import the nodes as shown](<../.gitbook/assets/Removing adding nodes.gif>)

![Set your legion settings to these here](<../.gitbook/assets/Legion Settings.PNG>)

![Copy paste the texture name and paste it into the legion extractor search bar.](<../.gitbook/assets/copy paste.gif>)

![The textures are located within the "exported\_files/materials" path for legion.](<../.gitbook/assets/car smg.PNG>)

Now, we need to link up the textures to the blender node, however. we need to figure out which texture is which type. I've created a handy little image to help you identify them

![](../.gitbook/assets/Texture-linking.png)

Link them up using the visual guide above

![](<../.gitbook/assets/adding the nodes.gif>)

## Congrats!

Once its all textured up, your model should look like this, congrats!

![](../.gitbook/assets/spijny-car.gif)
