# &#x2B22; Hex-Zero &#x2B22; 

At its core, HX0 is a re-design of the [Tri-Zero](https://github.com/zruncho3d/tri-zero) Z motion, with a revised [Pandora Gantry](https://github.com/MasturMynd/Pandora). Without the aforementioned, none of this project would've been possible, so a great amount of thanks is due to [zruncho3d](https://github.com/zruncho3d) and [MasturMynd](https://github.com/MasturMynd) whom ultimately sent me down this rabbit hole!

When I set out on this project, I initially intended for this to be a simple mod for Tri-Zero only to be used by myself, but oh boy did it escalate quickly into becoming its own standalone project with many people (_I am endlessly grateful for_) beta testing this and helping it become it's own entity. As it stands now Hex-Zero is a platform for some future projects I have planned!

![Hex-Zero_Render](/Images/Renders/Hex-Zero_Render_Blue.png)

## What Differentiates Hex-Zero From Tri-Zero + Pandora Gantry?

When I started work on Hex-Zero I wanted to fix my main concern with Tri-Zero, the robustness of the flying bed, along with that I preferred the more honeycomb look of the V0.2 skirts, so also wanted to incorporate that style into the Hex-Zero skirts. I also noticed some other compatibility issues with how I intended to build so would need to address them. Below is a short list summarising some of the major tweaks and changes you'll see when comparing Hex-Zero to Tri-Zero + Pandora Gantry:

1. Option to either **use bolts** on all bearing stacks **or pins** on all bearing stacks
2. Use **KGLM-03** spherical bearings in the flying bed Z joints (_improve rigidity_)
3. **Reduced Z height of the Z motor mounts** and skirts (_part of the aesthetic changes_)
4. **New front Z tensioners/idlers** to allow clearance with MiniSB (*with additional travel of pandora style gantry*)
5. Optimize printed parts to be **easier to print**
6. **More best-agon hexagons!**

Another often overlooked aspect of projects like these is documentation (_and is also by far the most time-consuming part of doing this_). When I started this journey (_before even designing anything_) I had many questions about the compatibility of hardware etc.. "if I do thing A, can I also do thing B", or "to do thing C, what do I need for thing D", or "will doing thing E even work!". To make this project as accessible as possible, I hope to create documentation and resources that answer as many common questions as possible!


## So You Want To Build A Hex-Zero?

The bill of materials to convert a V0.2 to a HX0 can be found [here](https://docs.google.com/spreadsheets/d/1F7fQtRNNPEZ1YoKCzFcIuKrkByZ1SoN8qf_lLwIh3ww/edit?usp=sharing) (*make sure to read the comments for help on what you'll need*). Then with everything ordered, you can get cracking printing the [STLs](https://github.com/Alexander-T-Moss/Hex-Zero/tree/main/STLs). For now, you will need to use the CAD for a large portion of your build as a reference when building your HX0, but a complete instruction manual is being created to be released later (*Insert Soon Trademark Meme*)!



## You Read The Manual?

By far the most time-consuming part of this project is creating a build manual. So it is far from done, but the latest version of what is currently completed can be found [here](https://docs.google.com/presentation/d/1XJv6mhR6lkI2eAlZ3oS6MfDWln81kRRjcN10jNzyiEM/edit?usp=sharing). If you notice anything wrong with it, please don't hesitate to point issues out to me so I can quickly resolve them, all I ask is you bear in mind that the manual is in a very early stage and still requires a lot of work to be completed :)



## Toolheads & Probes

Any probe and tool head combination that works with Tri-Zero should work on Hex-Zero, and with the extra XY movement freedom from the Pandora-style gantry, it allows more flexibility in placing probe docks.



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
**Yes**. HX0's can be serialised as a V0 _(assuming you are not converting an existing serialised V0_) and also get an HX0 serial to display on the printer!

### How Much Does It Cost To Convert My V0 To A HX0
Around **£100/$125/€115** to **£150/$190/€175**. Now you might be thinking why such a range? Well, the cost is entirely dependent on what you already have and how Gucci you want to be when buying parts, but you can convert a V0 to a HX0 somewhere in this region (_conservative estimate_) if not lower!
 
## Support

With all things, nothing is truly perfect, so if you come across any issues, no matter how small, or find something you think can be improved, please don't hesitate to reach out with suggestions/feedback on discord in the [development thread](https://discord.com/channels/825469421346226226/1095450118553084085) for this project!
