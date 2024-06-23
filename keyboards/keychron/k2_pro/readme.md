# Keychron K2 Pro

![Keychron K2 Pro](https://github.com/Keychron/ProductImage/blob/main/K_Pro/k2_pro.jpg?raw=true)

A customizable 84 keys TKL keyboard.

* Keyboard Maintainer: [Keychron](https://github.com/keychron)
* Hardware Supported: Keychron K2 Pro
* Hardware Availability: [Keychron K2 Pro QMK/VIA Wireless Mechanical Keyboard](https://www.keychron.com/products/keychron-k2-pro-qmk-via-wireless-mechanical-keyboard)

Make example for this keyboard (after setting up your build environment):

    make keychron/k2_pro/ansi/rgb:via

Flashing example for this keyboard:

    make keychron/k2_pro/ansi/rgb:via:flash

**Reset Key**: Connect the USB cable, toggle mode switch to "Off", hold down the *Esc* key or reset button underneath space bar, then toggle then switch to "Cable".

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

# VIM Mode

> Heavily based on https://www.reddit.com/r/olkb/comments/dbdrwp/vim_binding_on_my_keyboard_using_qmk/

### The following commands works:
```
h, j, k, l 				Arrow keys
[no]h, [no]j, [no]k, [no]l,		Arrow keys [no] times

w					word forward
[no]w					[no] words forward
b					word backwards
[no]b					[no] words backwards
e					to end of word forward
[no]e					to end of [no] word forward

u					undo, cmd-z
0					go to beginning of line
$ or ^					go to end of line
G					To end of document
gg					To beginning of document
i					leave vim command mode
a					go right, then leave command mode
I					to to beginning of line, then leave command 
					mode
A					to end of line, then leave command mode

c, d and y can be used in most of these as well. So for example, you can do
c4l					Change 4 characters to the right
c12w					Change 12 words
dgg					Delete to beginning of document

dG					Delete to end of document
yG					copy text to end of document
cgg					Change to beginning of document



Change, c followed by something
-------------------------------
cl					change char to the right, removes the 
					char and leaves command mode
ch					change char to the left, removes the 
					char and leaves command mode
cw					change word, removes the word and 
					leaves command mode
cb					change word to the left, removes the 
					word and leaves command mode
c$					change to end of line
C					same as c$
c0					change to beginning of line


Some of these can have a number as well, such as
c[no]w
[no]cw
[no]cl
c[no]b


Delete, d followed by something
===============================
The following works like the 'c' equivalent but doesn't leave command mode
dl			
dh
dw
db
d$
D
d0

d[no]w
[no]dw
d[no]l
[no]cb


More delete
===========
x 					remove next char, like del
X					remove the prev char, like backspace
[no]x
[no]X

Yank, add to paste buffer. y followed by something
=================================================
yw					yanks next word
yl					yanks next char
yy					yanks the whole line

y[no]w, [no]yw				yanks [no] words
y[no]y, [no]yy				yanks [no] rows

Paste, p
========
p					Paste at current position
P					Insert new line above current and
					paste

Please note that the d and x operations does not add to the paste buffer, 
unlike normal vi.


r[x]					replace next char with [x]
v 					visual mode
o 					adds line below current, 
					leaves command mode
O 					adds line above current, 
					leaves command mode
/					cmd-f, leaves command mode
n					find next, cmd-g, 
:w					save, cmd-s
:q					quit, cmd-q

```