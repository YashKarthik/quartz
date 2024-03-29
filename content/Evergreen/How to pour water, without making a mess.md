---
publish: true
---

## The phenomenon:
- While pouring, sometimes the liquid being poured out doesn't _fall_ out of the container.
- Instead it dribbles over the lip, clinging to the sides.
## Why:
When a liquid is being poured out of the container an adhesive force is formed between the liquid and the container. Adhesion is the net result of Van der Waals force, Coulombic forces, Hydrogen bonding and Capillary forces. Gravity has to fight against this adhesion to make the liquid _fall_ out of the container.

For an optimal pouring action, we need to minimize the adhesion between the liquid and the container, and maximize the force of gravity on the water.

Since the adhesion depends on the surface properties of the container (roughness, wetting props etc), we can choose a less adhesive container (I think steel over ceramic mugs). Looking closer at adhesion, in general the adhesion between two surfaces rises as the the time of contact between them increases. So pouring the liquid faster would reduce its adhesion to the container, reducing dribbling down the sides. Pouring faster would also allow us to take advantage of the momentum mustered.

Another route could be maximizing the force of gravity on the dribbling water, till the force of gravity is larger than the adhesive force. This is pretty intuitive to us humans, but the math behind it is pretty interesting too:

![[Attachments/pouring.png]]

Since gravity has act to against the adhesive force, we split force of gravity into two mutually perpendicular _components_ using trigonometry. This helps us visualize (and calculate) how much of gravity is acting against the adhesion. When the tilt angle is small, the angle (θ) between the force of gravity and the container's surface is small. So the force acting against the adhesion F•sinθ is relatively small. Tilting increases that angle θ, hence increasing F•sinθ (the component of gravity acting against adhesion). After a certain point, the pull against the adhesion is too much and water flows.

---
**Metadata**
- People::
- Related::
- References:: [Physics Stackexchang](https://physics.stackexchange.com/questions/28982/why-does-water-pouring-from-a-glass-sometimes-travel-down-the-side-of-the-glass)
- Status:: #understood 
- Created:: 10th Jan 2023
- Updated:: `$=dv.el('t', dv.current().file.mday)`