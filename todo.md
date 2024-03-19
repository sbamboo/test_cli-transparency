- Load text into pixelMatrix of pixel where pixel has bg and fg, retrived dynamicly from text by splitting ansi sequences out and save their pos in a stack, then iterate over the chars and make a pixel() instance with char,lastBgFromStack,lastFgFromStack with a global "base-background-color" set.
The matrix should be sized of conSize using conUtils.
- With layerManager() allow mergin of layer bgcolors for same pixelpos with an opacity value blending with bellow-layer bgcolor, from bottom to top.
- Opacity is set for bg and/or fg for each pixel.
- Before printing use optimize method to remove repeated ansi-sequences.