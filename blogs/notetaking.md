---
layout: page
permalink: /blogs/notetaking/index.html
title: Note Taking
---

# How I take my Notes

Notes are extensive to one's existense, if not you, it is for me. I like to keep things organized, I feel discomfortable for not taking my notes seriously which then doesn't get me to actually study when it is time. So here is my organized guide to my organized note taking.

<center>
<img src="https://media.makeameme.org/created/so-youre-telling-201b171ea0.jpg">
</center>

## I kinda like obsidian

I used OneNote for a long not to be dishonest ,but I like the obsidian note taking project, has everything that is needed. However there is less to customize when need to change things to my comfort, so I decide to keep it casual with obsidian. I use obsidian but not everytime. I use obsidian as my personal note taking diary but only when needed not everyday. I like how we can use the graph view. Obsidian is the 2nd Brain if so to speak.


<center>
<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*l6PxMm2lbqgtRkfMdWsyNA.jpeg">
</center>
<br>
What is it actually then?

## It's Vim duh!

Yes, I use neovim with custom configuration to take my serious notes, like everything I need. I write notes in LateX and Markdown. You can find a detailed setup instructions below.

## How to setup?

- Install vim/neovim (ofcourse)
- I use the VimTex plugin (My Plugin manager is VimPlug)
```init.vim
Plug 'lervag/vimtex'
let g:tex_flavor='latex'
let g:vimtex_view_method='zathura'
let g:vimtex_quickfix_mode=0
set conceallevel=1
let g:tex_conceal='abdmg'
```
- I also use UtilSnips for basic managenment
```
Plug 'sirver/ultisnips'
let g:UltiSnipsExpandTrigger = '<tab>'
let g:UltiSnipsJumpForwardTrigger = '<tab>'
let g:UltiSnipsJumpBackwardTrigger = '<s-tab>'

```
- I am bad at typing, so let's use basic spell check as:
```
setlocal spell
set spelllang=nl,en_gb
inoremap <C-l> <c-g>u<Esc>[s1z=`]a<c-g>u
```
- I also use autosave buffer as:
```
autocmd BufNewFile,BufRead *.tex :autocmd TextChanged,TextChangedI <buffer> silent write
```
What is basically does is, saves the buffer everytime I change something in my file ( Only works with .tex file ).

- Install zathura pdf viewer.

- You also need to install ```sudo apt-get install texstudio```


## How to use this setup?

Make a .tex file wherever you like, then make the basic structure ready and then press ```\ll``` while in **normal mode** for neovim. This will start the render for Vimtex and open the zathura rendered pdf version. Take a look at my setup below:
<br>
<center>
<img src="https://raw.githubusercontent.com/noorchauhan/noorchauhan.github.io/main/blogs/notetaking-assets/setup.png">
<sup><sub>Clean Clean Clean</sub></sup>
</center>

## Reach me out

Any questions can always be directed to email: _**numerchauhan[at]gmail[dot]com**_. 
