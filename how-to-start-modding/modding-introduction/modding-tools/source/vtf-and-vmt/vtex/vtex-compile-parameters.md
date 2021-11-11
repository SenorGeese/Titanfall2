# Vtex - Compile Parameters

[Vtex](./) can accept a list of additional compile parameters during its execution. These parameters are optional, but sometimes necessary to get a good result.

The list is written in the form of a simple text (.txt) document with the same name as the [targa (.tga)](../../../../../../documentation/file-format/truevision-graphics-adapter-tga.md) image to compile, and it should be put in the same folder as it, namely in the `SteamApps/common/gamefolder/materialsrc/` folder, where gamefolder is the game folder of the current game (`cstrike`/`dod`/`hl2`/`hl2mp`).

Example usage from one of the files for the console background:

```
nonice 1
nolod 1
nomip 1
```

## Parameters

### allmips&#xD;

Force texture to use all mipmaps (No minimum mipmap).

### alphatest\_hifreq\_threshhold&#xD;

### alphatest\_threshhold&#xD;

### alphatest&#xD;

To do: What do these do?

### alphatodistance&#xD;

Creates alpha-to-distance textures.

### anisotropic&#xD;

Force at least Anisotropic filtering on the compiled texture.

### bumpscale&#xD;

Sets texture's bumpscale value, which controls normal map intensity.

### clamps&#xD;

### clampt&#xD;

### clampu

Do not allow the texture to wrap in the S, T, or U coordinate space, respectively. This is most often used for sprites that are not tiled.

{% hint style="info" %}
&#x20;**Tip:**When a texel is requested that is outside of the texture, one of two techniques is used: **Clamping** limits the texel to the texture size, moving it to the nearest if it is more than the texture size. **Wrapping** makes the texel move back into the texture by increments (each to size of the texture). Wrapping causes a texture to be repeated; clamping causes it to be in one spot only.
{% endhint %}

### distancespread&#xD;

How much to spread alpha when creating alpha-to-distance textures.

### dudv&#xD;

Texture is a Du/Dv map.

### dxt5

&#x20;Force [DXT5](https://developer.valvesoftware.com/wiki/DirectX\_Texture\_compression\_5) compression, even if the source has no alpha channel.

### maxheight&#xD;

### maxheight\_360&#xD;

### maxwidth&#xD;

### maxwidth\_360

Sets maximum texture size for "High" (mat\_picmip 0) texture quality. Negative mat\_picmip settings will go above this limit.

### mipblend

&#x20;**To do: **Figure out how to make this work

### nocompress&#xD;

Do not use compression on this texture. Useful for textures with fine gradation (like light halos).

### nodebug&#xD;

No debug override.

### nolod&#xD;

Do not use lower resolution versions of this texture regardless of texture quality (mat\_picmip) settings. Used for non-world graphics such as HUD art.

### nomip

Do not use mipmapping for this texture. Used for materials like skyboxes and menu backgrounds.

{% hint style="warning" %}
&#x20;**Bug:** The MIPs are still generated and loaded! Use [VTFEdit](../vtfedit.md) to reduce texture footprint.
{% endhint %}

### nonice&#xD;

Do not use NICE filtering on this texture’s lower mip-levels.

### normal&#xD;

Texture is a normal map. Implies nonice, so all normals will be kept normalized during mipmap generation.

{% hint style="info" %}
&#x20;**Note:**Automatically applies when the texture name ends with `_normal`
{% endhint %}

### normalalphatodudvluminance&#xD;

Use alpha channel as luminance when converting from normal maps to Du/Dv maps

### normaltodudv

Converts the texture to a Du/Dv map.

### numchannels

How many channels to import from source file. (1 = Red only, 2 = Red and Green, 3 = RGB, 4 = RGB + Alpha) Omitted color channels are replaced with full color intensity.

### oneovermiplevelinalpha&#xD;

Alpha channel fades out as mipmaps get smaller.

### pfm&#xD;

Source texture is a portable floatmap. Used for HDR.

### pfmscale (float)&#xD;

Used to scale floatmap intensity.

### pointsample&#xD;

Do not filter this texture in-game.

### premultcolorbyoneovermiplevel&#xD;

Color channel fades out as mipmaps get smaller. Used when converting normal maps to Du/Dv maps.

### procedural&#xD;

Texture is procedural.

### reduce&#xD;

### reducex&#xD;

### reducey

Downscales on both, only X, or only Y axes, respectively. Value must be a power of two, and tells VTEX how to reduce the dimensions (2 = half size, 4 = quarter size, 8 = eighth size, etc.).

### rendertarget&#xD;

Texture is a rendertarget.

### singlecopy&#xD;

To do: What does this do??

### skybox&#xD;

Used for compiling [skyboxes](../../../../../../documentation/textures/skybox-basics/). This assures the edges match between each facet.

### spheremap\_negz&#xD;

### spheremap\_z&#xD;

### spheremap\_negy&#xD;

### spheremap\_y&#xD;

### spheremap\_negx&#xD;

### spheremap\_x&#xD;

To do: Are these functional?

### ssbump

Used for [self-shadowing bump maps](../../../../../../documentation/textures/bump-map/usdssbump.md)($ssbump).

{% hint style="info" %}
&#x20;**Note:**Automatically applies when the texture name ends with `_height-ssbump`
{% endhint %}

### startframe (integer)&#xD;

### endframe (integer)&#xD;

Used for animated textures. Textures must be named as texture000, texture001, texture002, etc. The startframe defines the beginning frame and the endframe defines the ending frame. Up to 1,000 frames are allowed.

### stripalphachannel&#xD;

Used to tell Vtex to ignore the source texture's alpha channel.

### stripcolorchannel&#xD;

Used to create a texture with no color data.

### trilinear&#xD;

Force at least Trilinear filtering on the compiled texture.

### volumetexture&#xD;

Creates a volumetric texture.

### Using .psd 'file info' parameters

Textures compiled from [.psd files](../../../../../../documentation/file-format/psd-photoshop-document.md) can have command line parameters saved into the [.psd](../../../../../../documentation/file-format/psd-photoshop-document.md) directly. To do this, use the 'File Info' menu in Photoshop and add your [Vtex ](./)commands into the "description" text field. These parameters will get evaluated by [Vtex ](./)when the [.psd file](../../../../../../documentation/file-format/psd-photoshop-document.md) is compiled.

Here's an example of usage for creating a flashlight that won't tile:

```
clamps 1;
clampt 1;
border 0;
```

{% hint style="info" %}
Source: [https://developer.valvesoftware.com/wiki/Vtex\_compile\_parameters](https://developer.valvesoftware.com/wiki/Vtex\_compile\_parameters)
{% endhint %}
