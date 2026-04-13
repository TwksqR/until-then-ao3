# until-then-ao3

**DISCLAMER: I am NOT an HTML and CSS programmer. If you are, in fact, an HTML and CSS programmer, and you think this code sucks, then please let me know.**

This workskin *is* AO3 friendly! Simply copy and paste the contents of `styles.css` into an AO3 workskin and enjoy!

# Documentation and How to Use

**Again, I am not an HTML and CSS programmer. If you find my instructions below to be terrible (I don't blame you), [W3Schools](https://www.w3schools.com/html/) and [Codecademy](https://www.codecademy.com/article/visual-studio-code) are very good resources if you're new to HTML and CSS. Also, check out the examples I made in the `examples` folder using these workskins, as well as my only publish work on AO3 so far (the file contains the entire thing).**

To help with creating your cool looking things faster, you can use Visual Studio Code. When downloaded, you can also download the extensions listed in [Extras](#extras), like **Live Server** which lets you open and preview your work as an actual webpage.

## Setting up your project

To start developing, create a new folder on your computer.  Download `styles.css` from this repository and place it in the folder you just created.

Create a new `.txt` file. Name it whatever you want, but make sure to replace the `.txt` extension with `.html`. Alternatively, you can just download/copy and paste any of the `.html` files already provided in this repository. Whatever you choose to do, place it in the same folder as `styles.css`.

If you're making an `.html` file from scratch, add `<!doctype html>` to your very first line. On your second and third lines, add `<html>` and `</html>` respectively. Those things surroudned by `<` and `>` (angle brackets) are called *tags*, and they're the backbone of HTML. Content is placed and nested in between opening and closing tags to indicate hierarchy and functional purpose. Note that closing tags have an extra `/` in it, placed before the tag name. Everything in your website (or work in this case) will be inserted in between the `html` tags.

### Head

Let's add our first tag to our website, the `head` tag. Just like the `html` tag, it goes between `<` and `>`, with the closing tag having an extra `/`. In your `head` tag, add `<meta charset="UTF-8" />`. This tells your website that you're using the standard UTF-8 character encoding standard, which basically means virtually every character in virtually any language you can think of is supported on your website.

If you are opening your work as a webpage, you can optionally add a `title` tag here as well, whose contents will appear as the tab name in your browser.

### Linking the stylesheet

So the way HTML and CSS work is that while HTML tells you what is shown on your screen, CSS tells you *how* to show what is on your screen. Basically, HTML is for content, while CSS is for *★ aesthetics ★*. `.css` files detail **stylesheets**, which when linked to an `.html` file, allow the **rules** included in the stylesheet to be used in said `.html` file. In order to link a stylesheet to an `.html` file, you need to add a `link` tag to your `head`. If you placed your `.html` file and `styles.css` in the same folder, this link tag will be `<link rel="stylesheet" href="styles_ao3.css" />`. `rel` and `href` are attributes of the tag, which provide even more detail pertaining to that certain tag.

## Making your first cool thing

Now that our setup is done, let's move on to the fun part: actually writing the code that makes up your work! Below your `head` tag but inside your `html` tag, add a `body` tag. This tag is for adding pretty much everything that goes inside your website (except for footers but we won't have to worry about those).

But before we do that, I should probably tell you what HTML and CSS **classes** are. Each tag is used for a different purpose, whether it's `head` for important stuff related to your website, `body` for your website contents, `p` for indicating a paragraph, or `div` for being used for pretty much fucking everything (it's literally *the* default tag, use it however you want; I used them a lot in my examples for anything that has no other appropriate tag!). Classes, on the other hand, are used to tell different tags how to behave and look, regardless of the tag used. Classes are defined in stylesheets (`.css` files) to be used in `.html` files. To add a class attribute to a tag, add `class="<name-of-class>"` after the opening tag name (but before the `>`), replacing `name-of-class` with... y'know.

Each of the workskins that I make have different structures and class designs, but the basic gist of it is that they will each start with a base class, for example `phone-chat`, which I'll use in this documentation since it's the only workskin I've made so far. Anyway, this class will be used any time you want to make text look like it's a direct messaging app, so you can finally see your so-desperately-needed Ryan x Jessica chatfic come to life (I see you, Mossy).

In the messaging app in until then, there are three distinct parts: the header, which shows the chat name, icon, and activity status; the body, which contains all the messages sent in the chat; and the footer, which contains the textbox that you type in (you can't actually type in it, but trust me your readers will be amazed when they see what you've made). 

### Header {#header}

For the header, this is the format I've gone for:
```
<div class="chat-header">
	<img class="chat-ui-button-back hidden" src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/20/icon_back.th.png" />
	<div class="chat-header-center">
		<img class="chat-icon hidden" src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/20/louise_pfp.th.png" />
		<h4 class="chat-name">9-Pearl 1415 \m/</h4>
		<p class="chat-activity-status">active now</p>
	</div>
	<img class="chat-ui-button-info hidden" src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/20/icon_info.th.png" />
</div>
```

If you want to change the chat name, just change the text in `chat-name`. Likewise, to change the chat icon, just replace the image link in `chat-icon`. Don't worry about the `hidden` class, that's for those crazy people who disable Creator workskins on AO3; you can add it if you want, but it's not strictly necessary (the `hidden` class just hides the content of the tag when Creator workskins are disabled; images without CSS formatting will appear at their actual size, unless you hide them altogether).

For instructions on how images work with HTML (and AO3), see [Images and Icons](#images-and-icons)

### Body {#body}

Now this is the most time consuming part. Below `chat-header`, add a `chat-body` tag. If you'd like your chat to be scrollable (like in-game), add the `scrollable` class to the same tag as `chat-body` (yes, tags can have multiple classes). You'll also need to add the `fixed` class to `phone-chat` as well.

To add a simple DM message, add a `div` with class `message-body` in `chat-body`, and nested in that `div`, add a `p` (paragraph) tag. You can add whatever you want in your `p` tag, and it will be displayed as a text message. If you'd like to add more messages in the same body, just add more `p` tags in `chat-body`.

"But wait," you say, "these are just incoming messages! What if my POV character wants to send a message of their own?" Well, my friend, just change the class to `message-body-right`. That's it.

Add more tags in your `chat-body` with class `message-body` or `message-body-right`, and soon enough, you'll have a conversation on your hands!

(Excerpt taken from my own work, *Mate in 4*)
```
<div class="phone-chat">
	<div class="chat-header">
		<img class="chat-ui-button-back hidden" src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/20/icon_back.th.png" />
		<div class="chat-header-center">
			<img class="chat-icon hidden" src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/20/cathy_pfp.th.png" />
			<h4 class="chat-name">Cathy Portillo</h4>
			<p class="chat-activity-status">active now</p>
		</div>
		<img class="chat-ui-button-info hidden" src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/20/icon_info.th.png" />
	</div>
	<div class="spacer-1em"></div>
	<div class="chat-body">
		<p class="chat-action">Today 8:27 PM</p>
		<div class="message-body">
			<p>uyyyyyyy mark!</p>
			<p>guess who invited me to her chess match tomorrow :3</p>
		</div>
		<div class="message-body-right"><p>Now kiss 💋</p></div>
		<div class="message-body">
			<p>ew perv</p>
			<p>and dickhead</p>
		</div>
	</div>
</div>
```

### Footer

Not much to say here, except this just replicates the footer of the messaging app found in *Until Then*. You can add your own text in the textbox (also remove the `-empty` text in the class name, to change the color of the text), as if someone were mid-sentence when something else happens in your story.

```
<div class="chat-footer hidden">
	<div>
		<p class="chat-textbox-empty">Start typing</p>
		<img class="chat-ui-button-send hidden" src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/20/icon_send.th.png" />
	</div>
</div>
```

### Group chats

So in group chats, there's more info to identify who's sending what message. This means that the structure of the incoming messages will be a bit more complex (with a few new classes), but it's not *too* bad, I don't think?

I'm too lazy to explain it so here's an example:
(Excerpt taken and adapted from [ultradragonman's comic](https://discord.com/channels/1225579253744144515/1255281497070502050/1436581191842009151) and [theexorcist2464's Louise Axe Scepter image](https://discord.com/channels/1225579253744144515/1255281497070502050/1296780628808699937))
```
<div class="chat-body">
	<div class="texter-gc">
		<img class="texter-icon hidden" src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/20/cathy_pfp.th.png" />
		<h5 class="texter-name">Cathy</h5>
		<div class="message-body">
			<p>yooo prez welcome!!!</p>
		</div>
	</div>
	<h5 class="texter-name hide">Louise</h5>
	<div class="message-body-right">
		<p>Yes, thank you</p>
	</div>
	<div class="texter-gc">
		<img class="texter-icon hidden" src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/20/ryan_pfp.th.png" />
		<h5 class="texter-name">Ryan</h5>
		<div class="message-body">
			<p>nice to see the gang back together</p>
		</div>
	</div>
	<div class="texter-gc">
		<img class="texter-icon hidden" src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/20/angel_pfp.th.png" />
		<h5 class="texter-name">Angel</h5>
		<div class="message-body">
			<p>can i post my morning selfies</p>
		</div>
	</div>
	<div class="texter-gc">
		<img class="texter-icon hidden" src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/29/pfp_default.th.png" />
		<h5 class="texter-name">Kate</h5>
		<div class="message-body">
			<p>please don't.</p>
		</div>
	</div>
	<h5 class="texter-name hide">Louise</h5>
	<div class="message-body-right">
		<p>I'm afraid not.</p>
	</div>
</div>
```

The `h5` is not stricly necessary; this can be just a `p`, it's more just a semantic meaning thing since it's the texter's name. `h5` just means it's a sub-sub-sub-sub-header, or in other words, not *that* important.

### Images in chat

Adding images to chat messages is actually pretty simple: just add an `img` tag with the attribute `src` containg the URL to your image. GIFs work too!

```
<div class="message-body-right">
	<img src="https://squidgeimages.s3.us-west-002.backblazeb2.com/2026/03/20/jaggy_and_cathy.png" />
	<p>Oops it wasnt me!</p>
</div>
```

See [Images and Hosting](#images-and-icons) for more information.

### Extra add-ons to note

There are a few extra classes I've added to spice up the chat messages, such as
- `chat-action`: Used for timestamps or notifications of someone new joining the group.
- `chat-read-receipt`: Used for indicating when someone else has read your messages.
- `chat-icon-gc`: This doesn't exist in the original game, but you know when a group chat you're in doesn't have an actual icon, so instead they display the profile pictures of a few members? So that's what this is for. Add multiple `img` tags inside a tag with class `chat-icon-gc` for this effect.
- `chat-mention`: Used for mentions/pings.
- `chat-emoji`: On social media apps like Instagram or Discord, messages containing only emojis are enlarged.
- `spacer-1em`: Literally just a tag that serves as a spacer. Do not put anything in it, just a single ` ` (space) character (this is to combat AO3's HTML sanitizer, which removes tags with no content). Used for non-scrollable phone chats to add spacing between the header, body, and footer.
- `change-on-hover`: Used for replacing content when the user hovers over it; useful for works containing in multiple languages so the reader won't have to copy and paste each and every sentence into a translator.

## All done!

Once your code is done (make sure to save!), you can preview your creation in one of two ways:
- In your computer's terminal (for Windows, open the Start Menu and type in `cmd`), enter `cd <directory_of_folder>`. To get your folder's directory, click on the textbox at the top of File Explorer and copy the highlighted text. Enter `start <name_of_your_file>.html`.
- With **Live Server** installed the Press the "Go Live" button in the bottom right toolbar to start the server.
The file will open in new tab in your browser. If not, manually open a new tab in your browser, and type `localhost:5500` in the address bar.

Once on the server, open the html file from the list of files. Voila! Your beautiful work is now on your screen.

## Images and Icons {#images-and-icons}

To add an image, you will need to add it to an online image hoster, such as Squidge. This is what I use as it is quite easy to use, and the URLs are quite compact.

Oh, and by the way, when it comes to linking images, you will need to add a **direct** link to the image. Not to some preview on the website.

A list of useful images related to Until Then are listed in `image_sources.txt` and stored on [my personal Squidge album.](https://images.squidge.org/album/xeOla).

## Fonts

You can apply any font downloaded onto your device to the workskin. In `styles.css` under `.phone` `font-family`, add the name of your desired font(s) to the list. Fonts are prioritized left-to-right and separated by commas (`,`). If a certain font is not available on your device, the next font in the list will be used instead. If your font name contains a space, you will need to add double quotes ("") around the font name.

The font used in Until Then's actual phone screens is **PT Sans**. You can download it [here](https://fonts.google.com/specimen/PT+Sans).

# Showcase

I've uploaded [a showcase of this stylesheet in action](https://archiveofourown.org/works/80788041/chapters/212214971) on AO3 so you can see how it looks. Hopefully it looks really awesome because I spent more time working on this than I probably should have lol

# Extras {#extras}

Certain VS Code extensions can make the code editing process easier:
- **Live Server** by **Ritwick Dey** allows you to host a local server for your html file on your computer, so you can preview your work in your browser before uploading it to AO3. All saved changes you make in VS Code on your HTML and CSS files will be instantly reflected on your live preview.
- **HTML CSS Support** by **ecmel** provides Intellisense for HTML.

# Got Questions?

Hit me up on Discord (username **twksqr**)! I do have an Instagram, but that is for personal life only.
