# &#x2B22; Questions And Answers &#x2B22;
![Hex-Zero_Banner_Image](https://github.com/Alexander-T-Moss/Hex-Zero/blob/main/Images/Renders/Hex-Zero_Render_Toolhead_Banner.png)


## How Much Does It Cost To Convert My V0 To A HX0?
Approximately **£100/$125/€115** to **£150/$190/€175**. You may be wondering why there is such a wide range. The cost is entirely dependent on what you already have and how Gucci you want to be when purchasing parts, but you can convert a V0 to a HX0 for somewhere in this range (_conservative estimate_), if not less!

## What Probe Should I Use With My HX0?
There are a few probe options to choose from, all with pros and cons and options depending on what tool head you are using but all need the same general considerations when deciding what is best for your HX0 build!

1. Where is the probe going to dock (_if applicable_)? - Ideally, the dock should put the probe out of the way of the tool head during normal printing. Thanks to the additional XY travel from the Pandora-style gantry in HX0, you get a bit more freedom in probe dock placement. I recommend using a probe mount dock that situates the probe in the rear left corner (_looking into the printer_)

2. How does the probe attach to the tool head (_if applicable_)? Will the additional parts for where the probe attaches to the tool head cause areas where parts will collide when the tool head moves? The main area to pay consideration to is the rear vertical z extrusions. You can often configure the printer in a way to avoid this area to prevent a possible collision

Below is a table detailing some probe and dock combinations and a short pro/con summary for them

| Toolhead Compatibility | Probe | Dock | Pro | Con |
| --- | --- | --- | --- | --- |
| DB & MiniSB | [Klicky]() | [Multple Options](https://github.com/jlas1/Klicky-Probe/tree/main/Printers/Voron/v0#probe-dock-mounts-1) | Well-Documented and community tested | May reduce useable print area and requires homing to front left corner |
|  | [SlideSwipe](https://github.com/chestwood96/SlideSwipe) | N/a | No issues with travel restrictions/collisions | More complex than other probes and needs additional hardware |
| DB Only | [ZeroClick](https://github.com/zruncho3d/ZeroClick?tab=readme-ov-file) | `Centre` | Nice dock position | Toolhead mount may collide with rear z verticle extrusions |

It's also worth noting that HX0 is designed and tested with DB in mind and not MiniSB, so your mileage with MiniSB may vary. Also each of the recommended probes pro/cons above assume using the DB cowl with it's respective probe mount

## Do I Need To Buy Extra Extrusion?
Technically, no, but I dislike wording things like that, so allow me to explain. 

If you have a V0 with an extrusion bed, you can build the flying bed using the stock V0 bed extrusions and a printed placeholder at the back of the printer. However, LDO has begun shipping kits with a kirigami and no bed extrusions, which means you will need to source at least one 100mm and one 200mm (or just three 100mm) extrusions for the flying bed in this case, as well as an additional 200mm extrusion for the printer's rear or use the printed place holder.

All that being said, the stock V0 extrusion bed is made up of three 100mm extrusions, and ideally, you want to use a single 200mm instead of two 100mm on the front of the flying bed, so you may still need to source 200mm extrusions for the flying bed and while you're at it, get one for the back of the printer. I should also clarify that the additional rear extrusion is not structural and is only there to make mounting skirts easier at the back of the printer!

Fortunately, these additional extrusions are in lengths that can typically be found pre-cut and tapped

## Do I Need To Drill Holes In The Existing V0 Extrusions?
If you want to mount the rear extrusion, drill two holes to accommodate it. With the printed placeholder, however, you can avoid drilling holes, but I strongly advise you to drill the necessary holes.

There is a jig included to drill the holes, making it rather simple, and because these holes are only to allow an Allen key through to tighten a blind joint bolt, they do not need to be accurate, so there is no need to go for sub-mm or anything silly precise with them!

## Can I Serial A HX0 As a V0?
**Yes**. HX0s can be serialised as a V0 (_assuming you are not converting an existing serialised V0_) while also receiving a HX0 serial to display on the printer!

# Still Got Questions?

Please feel free to reach out on the [dedicated development channel](https://discord.com/channels/825469421346226226/1220161815455989800) for this project in the doomcube discord server!
