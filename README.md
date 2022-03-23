# TriExporter

This is a fork of the [TriExporter](https://triexporter.codeplex.com/) project that adds support for the new shared resource cache.  
This fork will not be maintained.

## Changes

* Updated project files to VS2019
* Updated FBX SDK to 2020.2
* Fixed Exporting Meshes
    * As far as I can tell, exporting of gr2 meshes was broken due to a typo in the SharedCache.cpp
	* TriExporter was failing to display and export meshes because the path to the file was malformed.
* Removed Texture Limitation
    * The number of textures you could export with a mesh was limited (incorrectly) by the number of 'surfaces' the mesh had defined.
    * This isn't valid as 'surfaces' basically correlate with different UV sets or material IDs. Presumably this would correlate to how many different shaders or materials were applied to the mesh, not how many textures were used.

### Obtaining granny2

Looking around online, Metin2 appears to have the most recent (as of 3-2-2022) copy of granny2 bundled with it (2.12) which you can download via Steam.

However, using an older version of the dll has also worked for me (ie 2.8 from Anno 1404)

### Compiling

You will need the following:

* **FBX 2020.2 SDK** - https://www.autodesk.com/developer-network/platform-technologies/fbx-sdk-2020-2-1
* **DirectX SDK** - https://www.microsoft.com/en-us/download/details.aspx?id=6812
