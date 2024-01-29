---
description: >-
  The Valve Integrated Development Environment (commonly referred to by its
  acronym VIDE) is a third party freeware software distribution used by Source
  developers.
---

# VIDE

The **Valve Integrated Development Environment** (commonly referred to by its acronym **VIDE**) is a third party freeware software distribution used by Source developers. It is commonly used by mapmakers to pack custom content ([textures](../../../../../documentation/textures/), [models](https://developer.valvesoftware.com/wiki/Models), [soundscapes](https://developer.valvesoftware.com/wiki/Soundscapes)) into their levels.

Any and all custom content must be packed into the level with VIDE; otherwise, external users of your map will see [missing content](../../../../../documentation/textures/missing-content.md) textures in place of the custom textures only you see on your end.

## Features

* Hammer Splitter Editor
* Package Viewer (equivalent to [GCFScape](https://developer.valvesoftware.com/wiki/GCFScape))
* Particle Editor
* VBSP Editor
* VMT Editor
* Mass VMT Editor
* VTF Editor (equivalent to [VTFEdit](../vtf-and-vmt/vtfedit.md))
* Mass VTF Editor
* BSP Info
* Entity Lump Editor (equivalent to [Entspy](entspy.md))
* Pakfile Lump Editor (equivalent to [Pakrat](https://developer.valvesoftware.com/wiki/Pakrat))

## &#x20;Change Log

| <p><br><strong>Version 0.45b -- February 27, 2013</strong></p><ul><li><p><strong>Pakfile Lump Editor</strong></p><ul><li>Fixed: Incorrect gib model paths</li><li>Fixed: Certain version 21 BSPs saved with an incorrect version identifier</li><li>Fixed: Incomplete scan of pre-packed content</li><li>Changed: Scanning of packed materials is now enabled by default<br></li></ul></li><li><p><strong>Package Viewer</strong></p><ul><li>Added: Basic VPK version 2 support</li></ul></li></ul> |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| <p><br><strong>Version 0.45a -- December 25, 2012</strong></p><ul><li><p><strong>VIDE</strong></p><ul><li>Added: VTF Editor</li><li>Added: Mass VTF Editor</li><li>Fixed: File dialogs now remember last directory</li><li>Added: Single instance limitation</li><li>Added: Open file by argument<br></li></ul></li><li><p><strong>VBSP Editor</strong></p><ul><li>Fixed: Infinite loop when setting texture dimension</li><li>Fixed: Texture dimension default read from invalid prop on load</li><li>Fixed: Incorrect renaming of all tree items</li><li>Fixed: Swaped items are now saved in the correct order</li></ul><p></p></li><li><p><strong>Package Viewer</strong></p><ul><li>Fixed: Error when reading data from single digit VPK archive segments</li></ul></li></ul> |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| <p><br><strong>Version 0.38a -- January 9, 2012</strong></p><ul><li><p><strong>VIDE</strong></p><ul><li>Added: Package Viewer<br></li></ul></li><li><p><strong>Entity Lump Editor</strong></p><ul><li>Fixed: Lump written to Output window instead of BSP or LMP</li><li>Fixed: Crashing when importing VMF with entity connections</li><li>Fixed: Similarily named keyvalues overwriting each other</li><li>Removed: Brush entities loaded/saved from/to VMF</li><li>Added: Search option to invert results</li><li>Added: Option to ignore importing of hidden VMF entities<br></li></ul></li><li><p><strong>Hammer Splitter Editor</strong></p><ul><li>Fixed: Distance fields now set value upon losing focus</li><li>Fixed: Disabled editing of unreadable registry entries<br></li></ul></li><li><p><strong>Mass VMT Editor</strong></p><ul><li>Fixed: VTF material initialization using wrong path<br></li></ul></li><li><p><strong>Pakfile Lump Editor</strong></p><ul><li>Fixed: Rewrote nearly all GUI logic<br></li></ul></li><li><p><strong>Particle Editor</strong></p><ul><li>Fixed: Crash when context menu requested in blank space<br></li></ul></li><li><p><strong>VBSP Editor</strong></p><ul><li>Fixed: Various value fields setting the wrong value</li><li>Added: Texture dimension default read from first prop on load<br></li></ul></li><li><p><strong>[BSP Tools]</strong></p><ul><li>Fixed: General inconsistancy and unreliability; rewrote BSP delegate class<br></li></ul></li><li><p><strong>[VMF Tools]</strong></p><ul><li>Changed: Rewrote VMF class<br></li></ul></li><li><p><strong>[Utility Code]</strong></p><ul><li>Fixed: Improved accuracy and handling of plaintext keyvalues</li></ul></li></ul> |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |

| <p><br><strong>Version 0.32b -- June 23, 2010</strong></p><ul><li><p><strong>VIDE</strong></p><ul><li>Removed: Public use of external log file<br></li></ul></li><li><p><strong>Mass VMT Editor</strong></p><ul><li>Fixed: Undesirable behaviour with empty file list<br></li></ul></li><li><p><strong>Pakfile Lump Editor</strong></p><ul><li>Fixed: Model materials not being searched for</li><li>Added: Scan options dialog<br></li></ul></li><li><p><strong>Particle Editor</strong></p><ul><li>Added: System finder</li><li>Added: Map particle manifester</li></ul></li></ul> |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |

| <p><br><strong>Version 0.32a -- June 16, 2010</strong></p><ul><li><p><strong>VIDE</strong></p><ul><li>Added: Particle Editor</li><li>Added: Entity Lump Editor</li><li>Added: VBSP Editor</li><li>Added: Closure confirmation for modified windows</li><li>Removed: Ability to move toolbars</li><li>Removed: Ability to manually check for updates</li><li>Removed: External program launchers<br></li></ul></li><li><p><strong>BSP Info</strong></p><ul><li>Added: Option to save extracted lump with lump name instead of number</li><li>Added: Lump names according to BSP version<br></li></ul></li><li><p><strong>Mass VMT Editor</strong></p><ul><li>Added: Asterisk wildcard option</li><li>Added: Improved progress dialog<br></li></ul></li><li><p><strong>Pakfile Lump Editor</strong></p><ul><li>Fixed: Rare crash when finishing scan for referenced content</li><li>Fixed: Skybox and detail sprites not being searched for</li><li>Fixed: Rare infinite loop when reading binary data as text</li><li>Fixed: Editing of search path after scan</li><li>Added: Ability to search for and scan particle systems<br></li></ul></li><li><p><strong>VMT Editor</strong></p><ul><li>Fixed: New window from opening if open dialog was canceled</li><li>Added: Save shortcut "Ctrl + S"<br></li></ul></li><li><p><strong>[BSP Tools]</strong></p><ul><li>Added: Hard-coded lump names</li></ul></li></ul> |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| <p><br><strong>Version 0.16b -- February 26, 2010</strong></p><ul><li><p><strong>VIDE</strong></p><ul><li>Added: Ability to check for updates</li><li>Added: About information<br></li></ul></li><li><p><strong>BSP Info</strong></p><ul><li>Fixed: Window opening when the file open dialog was canceled</li><li>Fixed: Crash when closing a window after opening a BSP more than once</li><li>Fixed: Bug preventing a BSP from being read</li><li>Added: Context menu to copy lump offset and length values from the table</li><li>Added: Lump manipulation: Append, Extract, Prepend, and Replace<br></li></ul></li><li><p><strong>Mass VMT Editor</strong></p><ul><li>Added: VMT and VTF only file type selections</li><li>Added: Progress dialog for lengthy operations<br></li></ul></li><li><p><strong>Pakfile Lump Editor</strong></p><ul><li>Fixed: Crash when adding files with a CRC of 9F6FB22E</li><li>Removed: Unnecessary status entries</li><li>Added: Scan option<br></li></ul></li><li><p><strong>[VMT Tools]</strong></p><ul><li>Fixed: Formal syntax requirement</li></ul></li></ul> |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| <p><br><strong>Version 0.1a -- December 25, 2009</strong></p><ul><li>Initial release.</li></ul> |
| ----------------------------------------------------------------------------------------------- |

{% hint style="info" %}
Reference:

* [http://www.riintouge.com/VIDE/](http://www.riintouge.com/VIDE/)
* [https://developer.valvesoftware.com/wiki/VIDE](https://developer.valvesoftware.com/wiki/VIDE)
* [http://www.tophattwaffle.com/downloads/vide/](http://www.tophattwaffle.com/downloads/vide/)
{% endhint %}