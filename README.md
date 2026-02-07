# until-then-ao3

### WARNING: I am NOT an HTML and CSS programmer. If you are, in fact, an HTML and CSS programmer, and you think this code sucks, then please let me know.

# Documentation and How to Use

### I'll add better documentation and instructions later, but the examples in `examples.html` should help. Again, I am not an HTML and CSS programmer.

You can use Visual Studio Code. Create a new folder, download `styles.css` and create an `.html` file. Once your code is done, you can open the HTML file in one of two ways:
- In the terminal, navigate to your folder directory. Input `start <name_of_your_file>.html`.
- Press the "Go Live" button in the bottom right toolbar to start the server.
The file will open in a browser tab.

Unfortunately, it doesn't seem that this workskin can be put inline into AO3 works given the pretty annoying HTML auto-formatter that adds `p` tags around every. single. line. Even when there's already a `div` tag. Ugh. As a workaround, you can take screenshots of the website.

## Images and Icons

To add an image, you need to add a link to the image in the `src` attribute.

When linking an image from your device, use the file path (ex. D:\Memes\Until Then\absolute_cinema_justin.png).

If you do not want to have to download images, then you can use the URL of the image file.

When linking an image from Dropbox, there will be a `dl=0` attribute at the end of the URL. Replace this with `raw=1` to be able to display the image correctly in your HTML.

A list of images are stored on [my personal Dropbox](https://www.dropbox.com/scl/fo/2xl12jnfpf0z4r105xk67/ANzVHiW1s-zn5V5z79v1sxc?rlkey=int317qqnsetfq7v77takcvtb&st=e9w35bll&dl=0). This is probably not a good idea for many different reasons, but it works... for now.

## Fonts

You can apply any font downloaded onto your device to your chats. In `styles.css` under `.phone` `font-family`, add the name of your desired font to the list. Fonts are prioritized left-to-right, and if a certain font is not available on your device, the next font will be used instead, and so forth. If your font name contains a space, you will need to add double quotes ("") around the font name.

The font used in Until Then's actual chats is **PT Sans**. You can download it [here](https://fonts.google.com/specimen/PT+Sans).

# Extras

Certain VS Code extensions can make the code editing process easier:
- **HTML View** by NS Tech Bytes provides a live preview of your file inside of VS Code.
- **HTML CSS Support** by ecmel provides Intellisense for HTML.
