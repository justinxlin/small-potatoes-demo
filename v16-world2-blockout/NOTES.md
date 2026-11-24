# v16 world2 blockout

Untested rough playable model. This file is not a design source. World2 uses its own local coordinates: origin at the chip center, +x east, +z north (the top of the layout drawing). Later worlds may stack on Y; no horizontal offset is defined here.

Saddle `y = 5 * (x²/1600 − z²/900)` spans 10 units and is not flattened. Chip thickness is 1.75. Potato body width is 1.

Footprints taken from the user plan drawing, with the stated sizes:

- gear workshop, diameter 12, center (0, 16)
- plaza 20×20, center (0, 0)
- left shop 20×8, center (−26, 0)
- right market 15×20, center (23.5, 0)
- roads are 6 wide: z = 10 and z = −8 reach across the chip, the x = 0 spine runs north–south, and z = 0 links the shop, plaza, and market

Platform tops are horizontal, set above the highest chip point under each footprint, with skirts down into the saddle. Roads ramp over 4.5 units. The potato height is that same surface plus the body radius along the normal.

Spawn is (0, −18), on the open south spine. 取景模式 can orbit, zoom, and pan. 复制镜头参数 writes camera position, lookAt, fov, zoom, up, near, far, and the potato position and quaternion. If the clipboard fails, the JSON stays in the textarea.
