# Bugs I Found

Total: 26

## [Construct 3](https://www.construct.net/)

Total: 21

- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/5545). Getting the AsJSON of a sprite with a child threw an error and could hang the preview. Fixed in r288.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/5895). A sprite's width and height drifted to values like 192.9999999999994 as its animation played. Closed as won't fix, since it comes from floating-point rounding.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/6691). Exporting with "Recompression" enabled failed outright when OptiPNG couldn't recompress the project's icon. Fixed in r333.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/6874). Dropping a zip holding a corrupt WebP into the Animations Editor crashed Construct. Fixed in r338.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/6883). Cropping the transparent edges of many animations at once ran the browser out of memory. Fixed in r339.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/6948). The "Save to local browser" option was missing from Save As in Edge and Chrome. Closed as by design, since browsers that can save local files offer that instead.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/6979). Importing one particular image into the Animations Editor failed in r337 to r339, and closing the editor afterwards crashed Construct. Fixed in r341.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/7814). A global sprite with the Pathfinding behavior stopped finding paths after a layout change. Closed as not a bug, because the example's second layout had no event sheet.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/7868). HTML exports over 500 MB couldn't update through their offline service worker. Fixed in r382.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8176). The "Recreate initial objects" action didn't bring back a destroyed global object. Closed as by design, since a global object is only created once per run.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8189). The debugger showed no name for a probability table made with Advanced Random's "Create probability table from JSON". Fixed in r404.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8213). Objects with different "Compression for export" settings could render invisible, because lossy and lossless spritesheets shared filenames. Fixed in r406.2.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8214). The "Integrated 3D Engine" example failed to preview with "Failed to load the project main script". Closed as can't reproduce, since clearing the browser cache fixed it.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8216). A project's import map went unused, so its main script failed to load. Closed as external, since browsers didn't support import maps in workers.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8218). The debugger didn't load a project's import map, so its main script failed to load. Fixed in r408.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8642). Neither "Save all animations" option in the Animations Editor did anything. Fixed in r444.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8709). Pressing delete right after selecting many animations crashed Construct. Fixed in r450.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8771). Unlocking a 9-patch from the Properties Bar left it unselectable in the Layout View. Fixed in r456.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8772). The platform information spelled "Persistent" as "Persistant". Fixed in r454.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8794). A truncated PNG was refused as an unsupported format, and dropping it on a layout made the "Rendering spritesheets" count climb forever. Closed without a fix, since checking every PNG would slow imports down.
- [GitHub issue](https://github.com/Scirra/Construct-bugs/issues/8868). The "Integrated 3D Engine" example stopped previewing in r466, failing to load its main script. Fixed in r467.

## [Linux kernel](https://www.kernel.org/)

Total: 1

- [Mailing list post](https://lore.kernel.org/netdev/Dvrf8IhF3j09acNeO4Muc57tY7i1vJz5ckdk@vineyardtechnologies.org/). An AF_UNIX `SOCK_SEQPACKET` socket's `recv()` can return 0 while a message is still queued, and the message is lost. A fix was drafted in reply but hasn't been submitted yet.

## [NVIDIA Linux driver](https://www.nvidia.com/en-us/drivers/unix/)

Total: 1

- [Forum post](https://forums.developer.nvidia.com/t/615-71-09-gldeletesemaphoresext-blocks-for-16-ms-on-every-512th-call-gl-ext-semaphore-fd/385870). Every 512th `glDeleteSemaphoresEXT` call blocks for about 16 ms while the driver frees the semaphores it queued. NVIDIA reproduced it and filed internal bug 6931032, with no fix released yet.

## [PixiJS](https://pixijs.com/)

Total: 2

- [GitHub issue](https://github.com/pixijs/pixijs/issues/12019). The WebGPU renderer hardcoded `bgra8unorm` for its canvas and pipelines, so it couldn't output HDR. Fixed in v8.20.0, which takes those formats from the view's texture.
- [GitHub issue](https://github.com/pixijs/pixijs/issues/12080). On WebGPU, the garbage collector unloaded uniform buffers that cached bind groups still used, turning the canvas black. Fixed in v8.20.0.

## [Steam](https://store.steampowered.com/)

Total: 1

- [GitHub issue](https://github.com/ValveSoftware/Proton/issues/548#issuecomment-6506183004). Steam points to a non-existent Linux build for Torchlight. Still open.
