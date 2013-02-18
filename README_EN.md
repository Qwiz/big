## B.I.G. (Bash Image Generator) Readme

Sorry, but my english is really bad..

### About

This script was written for creating pixelart pictures in Linux console. It converts any picture in JPEG or PNG to a bunch of escape sequences, which can be used in shell.

### How to use

This script can only resize and convert whole image or use its fragment.
You can also redirect the output of the script to a file.

##### Resizing image

To resize an image you should use `-r` flag and multiplier.
For example: Command `./big.py some_image.png -r 4` will draw an image 4 times smaller than original.
Multipliers like 0.5 haven't been tested.

##### Drawing a fragment of image (useful for spritesheets)

If you need to convert only a fragment of an image, you need to use flags `-c`, `-p` and `-s`.

 - `-c` flag to crop an image
 - `-s size` flag to choose a size of fragment
 - `-p position` flag to choose fragment of an image. Should be in 'number of sizes'

For example you need to cut a 32x32 fragment 5th from left and 7th from top edge of an image
`./big.py some_image2.png -c -p 5,7 -s 32,32`