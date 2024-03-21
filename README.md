# &#x2B22; Hex-Zero &#x2B22; 

At its core, HX0 is a re-design of the [Tri-Zero](https://github.com/zruncho3d/tri-zero) Z motion, with a revised [Pandora Gantry](https://github.com/MasturMynd/Pandora). Without the aforementioned, none of this project would've been possible, so a great amount of thanks is due to [zruncho3d](https://github.com/zruncho3d) and [MasturMynd](https://github.com/MasturMynd) whom indirectly sent me down this rabbit hole!

![Hex-Zero_Render](/Images/Renders/Hex-Zero_Cover_Render.png)

[BOM And Sourcing Guide](https://docs.google.com/spreadsheets/d/1F7fQtRNNPEZ1YoKCzFcIuKrkByZ1SoN8qf_lLwIh3ww/edit?usp=sharing)

[Very Early Release Manual](https://docs.google.com/presentation/d/1XJv6mhR6lkI2eAlZ3oS6MfDWln81kRRjcN10jNzyiEM/edit?usp=sharing)

Common Questions And Answers


## What Differentiates Hex-Zero From Tri-Zero + Pandora Gantry?

When I started working on Hex-Zero, I wanted to address my main concern with Tri-Zero, which was the robustness of the flying bed. I also liked the more honeycomb look of the V0.2 skirts and wanted to incorporate that style into the Hex-Zero skirts. I also noticed some other compatibility issues with how I intended to build things so would need to address them. Below is a summary of some of the major tweaks and changes you'll notice when comparing Hex-Zero to Tri-Zero + Pandora Gantry.

1. Option to either **use bolts** on all bearing stacks **or pins** on all bearing stacks
2. Use **KGLM-03** spherical bearings in the flying bed Z joints (_improve rigidity_)
3. **Reduced Z height of the Z motor mounts** and skirts (_part of the aesthetic changes_)
4. **New front Z tensioners/idlers** to allow clearance with MiniSB (*with additional travel of pandora style gantry*)
5. Optimize printed parts to be **easier to print**
6. **More best-agon hexagons!**

Documentation is another frequently overlooked aspect of projects like these (and by far the most time-consuming thing to complete). When I first started this journey (_before even designing anything_), I had many questions about hardware compatibility, such as "If I do thing A, can I also do thing B", "To do thing C, what do I need for thing D" and "Will doing thing E even work!" To make this project as accessible as possible, I intend to develop documentation and resources that address as many common questions as possible!


## Community Beta Testing Builds

I want to extend a massive thanks to everyone who took a leap of faith in building and testing this project in its early stages, below is a collage of some HX0s built during the beta testing of this project :)

![Beta Testing Collage](/Images/Beta_Testing_Collage.jpg)

Credits in order of images left to right: Rahim Damji (*HX0.2*),  Hud (*HX0.1*), Siboor (*HX0.3*), Albino Deer (*HX0.4*)



## Credits

- **[Zruncho3D](https://github.com/zruncho3d)**: Creator of Tri-Zero
- **[MasturMynd](https://github.com/MasturMynd)**: Designer of Pandora's gantry
- **[Nemgrea](https://github.com/nemgrea)**: Producer of Voron 0!

## Common Questions

### Can I serial a HX0 as a V0?
**Yes**. HX0's can be serialised as a V0 _(assuming you are not converting an existing serialised V0_) and also get a HX0 serial to display on the printer!

### How Much Does It Cost To Convert My V0 To A HX0
Around **£100/$125/€115** to **£150/$190/€175**. Now you might be thinking why such a range? Well, the cost is entirely dependent on what you already have and how Gucci you want to be when buying parts, but you can convert a V0 to a HX0 somewhere in this region (_conservative estimate_) if not lower!

### Do I Need To Buy Extra Extrusion?
Technically no, but I dislike wording things like that so let me explain. 

If you have V0 with an extrusion bed, then you can build the flying bed with the stock V0 bed extrusions, and use a printed placeholder at the rear of the printer. However, LDO has started shipping kits with a kirigami and no bed extrusions, this means you will need to source at least 1x 100mm and 1x 200mm (or just 3x 100mm) extrusions for the flying bed in this case and either source an additional 200mm extrusion for the rear of the printer or use the printed place holder.

All this said it should be noted that the stock V0 extrusion bed consists of 3x 100mm extrusions and ideally you want to use a single 200mm instead of 2x 100mm on the front of the flying bed, so you still might want to source 200mm extrusions for the flying bed and the rear of the printer. I should also make clear that the additional rear extrusion isn't structural and is purely to make mounting skirts easier at the rear of the printer!

Fortunately, these additional extrusions are in lengths that can normally be found pre-cut and tapped

### Do I Need To Drill Holes In The Existing V0 Extrusions
If you want to mount the rear extrusion, then you need to drill 2 holes to accommodate this. With the printed placeholder though you can get away with not drilling holes, but I highly recommend you drill the needed holes.

There is an included jig to drill the holes making it rather easy, and as these holes are just to be able to get an Allen key through to tighten a blind joint bolt, they don't need to be accurate so there is no stress to get sub-mm or anything silly precision with them!

 
## Support

With all things, nothing is truly perfect, so if you come across any issues, no matter how small, or find something you think can be improved, please don't hesitate to reach out with suggestions/feedback on discord in the [development thread](https://discord.com/channels/825469421346226226/1095450118553084085) for this project!
