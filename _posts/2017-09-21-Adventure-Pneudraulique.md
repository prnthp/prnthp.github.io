---
title: "Sensuator&copy; - Thailand"
---
Instead of having a proper vacation in Thailand, I decided to dabble into silicone molding, casting and soft robotics in general. I ordered some silicone rubber and some tubing, and here's what I found out while trying to make a Sensuator&copy;.

### The Mold ###
I started off with drawing the end result first: the black parts are conductive rubber and the translucent parts are normal Shore 20 A silicone rubber. The plan was to experiment with changes in conductivity during bending or deformation.
![Sensuator](/images/sensuator1.PNG)*The Sensuator&copy; CAD*

The actual 3d printed mold was made using boolean body operations. There are some ribbed features on the bottom of the mold to serve as registration features.
![Sensuator Mold](/images/sensuator_mold.PNG)*The mold*



### Lost-Wax Silicone Casting ###
If you're aware of lost-wax casting (the metal casting technique) then lost-wax silicone casting is a simplified version of that. As mentioned [here](//groups.csail.mit.edu/drl/wiki/images/2/27/Homberg_et_al._-_2015_-_Haptic_Identification_of_Objects_using_a_Modular_Soft_Robotic_Gripper.pdf), lost-wax silicone casting is useful for creating hollow features without having to join two separate silicone castings. The most useful benefit is the strength due to the absence of a seam: delamination occurs at the seams when parts are made from two pieces and joined later.

![Wax Cores](/images/waxcores.jpg)*The silicone wax core mold, and the wax cores themselves.*

In theory, it seems straight-forward: make a mold that can hold the wax in place and pour in silicone around it. Then remove the wax by melting it out. In practice, however, as someone who has had wax melted on stuff before might say, wax a bitch to clean. This becomes a nuisance when your wax is enclosed in silicone with only small holes to evacuate. I tried blasting hot water through the casting and massaging the wax out, but could only get about 90% out. It was even worse when I first tried with only one opening. If your goal is to have a cavity with a waxy interior then lost-wax casting is great.

![Sensuator V1](/images/sensuatorv1.jpg)*The milky white wax has covered the whole casting inside and out - it's virtually impossible to totally remove*

With a thin layer of wax covering the entire interior (and exterior) surface of the Sensuator&copy;, conductivity was completely gone between the inner fluid and the conductive rubber, rendering the casting into just a another soft robotics expanding bladder.

There are, however, [soluble waxes](//www.freemanwax.com/soluble-waxes.html) that are used to make hollow carbon fiber parts. This *might* make it easier to flush the wax out.

### Conductive Silicone ###
Conductive silicone is actually readily available, but it's absurdly [expensive](//siliconesolutions.com/ss-24.html). Luckily there's a guy who spent 2 years doing extensive trial-and-error to make [conductive sex toys](//www.comingle.io/). He has a detailed [instructable](//www.instructables.com/id/Silc-Circuits-High-Performance-Conductive-Silicone/) explaining the process to make conductive silicone rubber.

![Carbon fiber](/images/carbonfiber.jpg)*A piece of carbon fiber cloth*

The only ingredient for conductive silicone other than the silicone itself is carbon fiber. So I acquired some old carbon fiber cloth and cut it up into short 3-6 mm strands. **Wear a respirator while doing this, the strands are extremely light and easily become airborne.** Following the guide, I stirred in the strands into recently poured silicone rubber until the multimeter read less than 1kOhm. And it works! However the rubber becomes a lot tougher, probably close to Shore 60 A, and the mixture is a lot harder to pour/inject.

![Conductive Silicone](/images/conductivething.jpg)*Conductive Silicone!*

### Sensuator 0.1 ###
![Sensuator](/images/sensuatorv3.jpg)*Non-working prototype sensuator*

I never got a Sensuator to work properly, although I do have a solid plan to get one to Sensuate&trade;. For the pictured prototype, instead of lost-wax casting, I opted for a simpler lamination procedure with a multi-step cast: cast an open cavity, remove the wax core and flip the casting to seal the top (bottom) in the mold. Unfortunately, the conductive silicone still does not make electrical contact with the inner fluid. The conductive silicone itself has a resistance of about 150-300 Ohms, depending on your tongue angle. The plan for the next cast is to place a conductive wire that connects the inner fluid to the conductive silicone. I already tested this by sticking a wire right through the conductive silicone into the cavity from the outside. That way, I measured a meaningful resistance of the fluid but it leaks.

### Useful Notes ###
1. Food grade silicone takes about 4 hours to cure, but can be demolded after the first 40 minutes or so. (Depending on heat and ambient moisture)
1. To get enclosed parts or multiple materials, add more silicone after the demold time, the silicone can hold its shape.
1. Carbon fiber strands are extremely lightweight and can be breathed in quite easily.
1. The carbon fiber strands act as a matrix to strengthen or toughen the silicone rubber, increasing the hardness significantly. This technique of using fibers in
