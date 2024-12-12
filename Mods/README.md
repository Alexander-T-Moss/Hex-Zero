# &#x2B22; Mods & Additions &#x2B22; 

![Waveshare_Banner_Image](https://github.com/Alexander-T-Moss/Hex-Zero/blob/main/Images/Renders/Hex-Zero_Render_Waveshare_Mod_Banner.png)


# List Of Mods

|              Author              |             Mod Name             |            Description           |
| -------------------------------- | -------------------------------- | -------------------------------- |
| Alexander T-Moss |  [3mm Panel Clips](/Mods/Alexander_T-Moss/3mm_Panel_Clips) | Allows the use of 3mm foam tape |
| | [Handles](/Mods/Alexander_T-Moss/Handles) | Somewhere to grab onto to lift the printer up |
| | [Full Height Panels](/Mods/Alexander_T-Moss/Full_Height_Panels) | Hard mounted top hat and info on using full height panels (BoxZero esque)|
| | [Bed Fans](/Mods/Alexander_T-Moss/Bed_Fans) | Mounts for 3010 blower fans on the underside of the bed |
| | [Hex Panels](/Mods/Alexander_T-Moss/Hex_Panels) | For if you want more bestagons in your printer |
| | [Skirt Fans](/Mods/Alexander_T-Moss/Skirt_Fans) | Mounts for a pair of 3010's on the side skirts |
| MechaXx |[Waveshare 2.8 Screen](/Mods/MechaXx/Waveshare_28_Screen) | Waveshare 2.8 screen front skirt mount |
| tiramisu |[Serial Plates](/Mods/tiramisu/Serial_Plates) | HX0 Serial Plate for 1515 extrusions |
| Hoeby |[Bottom Wago Holder](/Mods/Hoeby/Bottom-Wago-holder) | Wago Block Holder |
| | [Bottom FT EMS](/Mods/Hoeby/Bottom_FT_EMS) | Bottom FT EMS |
| | [Front belt tensioner](/Mods/Hoeby/Front_Belt_Blocks) | Different belt clamping in front tensioner |
| | [Extended MantaRay kinematic](/Mods/Hoeby/MantaRay%20mount%20with%20extend) | Prevent easelly dropping MantaRay |
| | [HX0_Anthead](/Mods/Hoeby/MantaRay%20mount%20with%20extend) | AntHead with mods specially for HX0 |

<br>
<br>
<br>


# Information For Adding A Mod
Below is a quick summary of changes required for submitting a mod to the mods folder

## Table Structure
Information for updating the table for the addition/modification of a mod
- Put the name of the mod hyperlinked to the location of the mod in the repo
- A short single-sentence description of the mod
- Your name as the author

Example table entry: `| Your Name Here |  [Mod Folder Name](Link_To_Mod_Folder) | Short Description |`

## Folder Structure
Information for updating the `Mods` folder for the addition/modification of a mod

The `Mods` folder uses a 2 layer folder structure to organize all the mods
1. `Author Folder` - Top-level folder where all of an author's mods are
2. `Mod Folder` - The folder for an individual mod, which will be found in its relevant `Author Folder`

### Example Of Mod Folder Structure

| `Mods` Folder | `Author Folder` | `Mod Folder` |
| --- | --- | --- |
| Mods | Person 1 | Mod A From Person 1 |
|  |  | Mod B From Person 1 |
|  |  | Mod C From Person 1 |
|  | *Person 2 | *Mod D From Person 2 |
|  | Person 3 | Mod E From Person 3 |
|  |  | Mod F From Person 3 |

_*Note: If someone has a single mod it still has an author folder_

## What Must A Mod Folder Need To Include
At a bare minimum, each mod folder should contain a CAD file (_ideally a .step and/or .f3d file_), STLs (_ideally oriented correctly for printing_) a **screenshot from CAD or a photo** of the mod installed and a short `README.md` providing the relevant information for the mod

Also, make sure there are no spaces in any file or folder name (_using underscores `_` or dashes `-` where required_)
