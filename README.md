# three.confetti.explosion.js
The confetti explosion effect based on THREE.JS GPU Particle System

# Live demo:
https://mrgoonie.github.io/three.confetti.explosion.js/

![alt text](https://github.com/mrgoonie/three.confetti.explosion.js/raw/master/screenshot.png)

![alt text](https://github.com/mrgoonie/three.confetti.explosion.js/raw/master/explain.jpg)

# How to use:

Include the plugin's javascript file:
`<script type="text/javascript" src="../dist/three.confetti.explode.min.js"></script>`

Create a particle system:
```
var confetti = new ExplosionConfetti({
	rate: 1, // percent of explosion in every tick - smaller is fewer - be careful, larger than 10 may crash your browser!
	amount: 200, // max amount particle of an explosion
	radius: 800, // max radius of an explosion
	areaWidth: 500, // width of the area 
	areaHeight: 500, // height of the area 
	fallingHeight: 500, // start exploding from Y position
	fallingSpeed: 1, // max falling speed
	colors: [0xffffff, 0xff0000, 0xffff00] // random colors
});
scene.add( confetti.object );
```

Also in render function:
```
function render(){
	...
	if(confetti) confetti.update();
	...
}
```

# Remove:

`confetti.dispose();`

That's it!