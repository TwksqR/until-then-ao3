# until-then-ao3

### WARNING: I am NOT an HTML and CSS programmer. If you are, in fact, an HTML and CSS programmer, and you think this code sucks, then please let me know.

# Documentation and How to Use

You can use Visual Studio Code and install the extension "HTML CSS Support". In your current folder, download `styles.css` and add your code in an `.html` file. Once done, press the "Go Live" button in the bottom right to start the server. A tab will open in your browser.

Unfortunately, it doesn't seem that this workskin can be put inline into AO3 works given the pretty annoying HTML auto-formatter that adds `p` tags around every. single. line. Even when there's already a `div` tag. Ugh. As a workaround, you can take screenshots of the website.

As images cannot be embedded into the stylesheet, they must be sourced from an external storage site. See `images.txt` for a sample list of images that you can use.

### I'll add better documentation and instructions later, but the examples in `examples.html` should help. Again, I am not an HTML and CSS programmer.

# Images and Icons

A list of images are stored on [my personal Dropbox](https://www.dropbox.com/scl/fo/2xl12jnfpf0z4r105xk67/ANzVHiW1s-zn5V5z79v1sxc?rlkey=int317qqnsetfq7v77takcvtb&st=e9w35bll&dl=0). This is probably not a good idea for many different reasons, but it works... for now.

When using an image from Dropbox, there will be a `dl=0` tag at the end of the URL. Replace this with `raw=1` to be able to display the image correctly in your HTML.

# Fonts

You can apply any font downloaded onto your device to your chats. In `styles.css` under `.phone` `font-family`, add the name of your desired font to the list. Fonts are prioritized left-to-right, and if a certain font is not available on your device, the next font will be used instead, and so forth. If your font name contains a space, you will need to add double quotes ("") around the font name.

The font used in Until Then's actual chats is **PT Sans**. You can download it [here](https://fonts.google.com/specimen/PT+Sans).
