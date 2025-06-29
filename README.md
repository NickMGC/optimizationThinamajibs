# Optimization Thinamajibs
stuff i use for optimizing my projects

## Funkin' packer

[Funkin Packer](https://neeeoo.github.io/funkin-packer/) is based on [Free texture packer](https://github.com/odrick/free-tex-packer) with Sparrow support. 
To optimize a spritesheet you need to click on 'Repack / Split sheet', choose a texture (.png) and the data file (.xml).

You can combine multiple spritesheets into one for sprite batching by importing another spritesheet.

### When exporting a sprite, make sure you have these settings:

* Remove file ext: ON
* Prepend folder name: ON
* Sprite Padding: 2
* Border Padding: 2
* Width & Height: 8000
* Allow rotation: ON
* Allow trim: ON
* Detect identical: ON
* Sort Exported Rows: ON
* Trim mode: trim


## oxipng

[oxipng](https://github.com/oxipng/oxipng) is a multithreaded lossless PNG/APNG compression optimizer. It can be used via a command-line interface or as a library in other Rust programs.


## Rotato

[Rotato](https://tools.rotato.app/compress) is a online lossless FFmpeg powered video optimizer, it reduces its file size without affecting video data.


## OptiVorbis
[OptiVorbis](https://optivorbis.github.io/OptiVorbis/) is a library and application for lossless, format-preserving, two-pass optimization and repair of Vorbis data, reducing its size without altering any audio information.


## Sprite Batching

Sprite batching is used to optimize draw quad calls.
Sprite batching is handled automatically in Haxeflixel, In order for sprites to become batched they need to have the same properties.

### Required conditions for a sprite to be batched:

* They must share the same spritesheet.
* They must be color-tinted in the same way (sprite.color, sprite.colorTransform...), or not be color-tinted.
* They must have the same/no blend mode.
* They must have the same/no antialiasing.
* They must have the same/no shader.

## `For loop` unrolling

If a `for loop` is unwrapped there won't be any allocation meaning that it would function the same as if you were to write it manually.
There's a section in the [Haxe](https://haxe.org/manual/cr-loop-unrolling.html) manual where you can read about it.
