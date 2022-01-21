---
description: Info about our customizability of skins along side the formats.
---

# Custom Skin Info & Formats

{% hint style="info" %}
These are not the only ways to customize a skin. You can innovate as always. If you feel you made a discovery feel free to share it in the Discord server!
{% endhint %}

## Using Custom Skins

### DDS Format

If you want to use DDS format skins. We recommend the frequently updated Titanfall2-SkinTool found here; [https://github.com/zxcPandora/Titanfall2-SkinTool](https://github.com/zxcPandora/Titanfall2-SkinTool).&#x20;

Simply download formatted skins. Getting custom skins below:

Backup your pc\_stream.rpak. Then follow your chosen tools instructions.&#x20;

{% content-ref url="dds-format-tools.md" %}
[dds-format-tools.md](dds-format-tools.md)
{% endcontent-ref %}

### VTF Format

If you want to use VTF format skins. There is no current tool to automate the application of VTF format skins. If you want to learn how to manually apply VTF format skins we have a guide for that! Linked below:

{% content-ref url="../vtf-format-cgs.md" %}
[vtf-format-cgs.md](../vtf-format-cgs.md)
{% endcontent-ref %}

## Info on skin formats:

## 2 kinds of skins (VTF format and DDS format)

### VTF format

VTF is the first found custom gun skin method. VTF custom skins take editing a path in a .mdl file to use the skin and script in the `client_mp_common.bsp.pak000_000.vpk` vpk or creating a vpk patch; `client_mp_common.bsp.pak000_228.vpk`.&#x20;

* Unshaded textures
* Up to 4k skins
* Animated skins (VMT options)
* Viewed from afar
* Works on low graphics
* Can use transparency

### DDS format

DDS is the 'best' custom skin method. DDS custom skins takes injecting skins into the games `pc_stream.starpak` file.&#x20;

* Properly shaded skins
* Distance based visibility; viewing from up close.&#x20;
* Community made tools
* high quantity high-quality skins
* Most commonly used

## Skin style possibilities

### Static, Single frame

Static skins are skins that don't move in any way. Compatible with VTF and DDS format. Simple and at times, most elegant. DDS formats only skin style.

### Moving texture, Single frame

Only available with VTF format. Moving skins are skins that have a code group in their `.vmt` that moves your vtf texture to your desired parameters. The code block to move your textures is below; note this goes into your models `.vmt` file:

```
"Proxies"
    {
        "TextureScroll"
        {
            "texturescrollvar" "$baseTextureTransform"
            "texturescrollrate" "-0.03"
            "texturescrollangle" "180"
        }
    }
```

Change `"texturescrollrate" "-0.03"` to change speed of movement. \
Change `"texturescrollangle" "180"` to change direction of  movement.

### Animated texture, Multiple frames

Only available with VTF format. Animated skins are skins that create a moving affect or active scene by using multiple frames. You wont need multiple vtf's as VTFEdit creates one file with every frame inside. Mind that this increases size; which can have affects in recompiling. Note you can use Add-ons on your image editors to help with making animated skins. You need this code group in your models `.vmt` to activate animation; found below.

```
"Proxies"
    {
        "AnimatedTexture"
        {
            "animatedTextureVar"	"$basetexture"
			"animatedTextureFrameNumVar"	"$frame"
			"animatedtextureFrameRate"	"2"
        }
    }
```

Change `"animatedtextureFrameRate" "2"` to change framerate in game.

## Getting Custom Skins:

be nice, and check below page link.

{% content-ref url="../getting-vtfs.md" %}
[getting-vtfs.md](../getting-vtfs.md)
{% endcontent-ref %}