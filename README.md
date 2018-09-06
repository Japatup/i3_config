## my modest i3 and i3 blocks configuration files

#### btw, how to add icons in your i3blocks.conf file ?
Quite easy actually, but I wasted some time to find it, so here is the way I chose :

1) You need to install the fonts the icons you want are in. As for me, I installed fonts-font-awesome : 
    ```bash
    aptitude install fonts-font-awesome
    ```
2) For Debian 9, which is the OS I use, Stretch repos don't have the 5.0 version of fonts-font-awesome, but only 4.7 . Not a problem, but you will have less choice for your icons. See [https://fontawesome.com/v4.7.0/icons/](https://fontawesome.com/v4.7.0/icons/) for the list.
3) Now the font is installed, you must declare i3 you want to use it. In your i3 config file (for me it is *~/.config/i3/config*), add this setting in the bar section : 
    ```bash
    bar {
    # (...)
    font pango:DejaVu Sans Mono, Awesome 8
    # (...)    
    ```
4) And here comes the nice part : inserting icons in your i3blocks.conf file, as labels for instance. To do so, you may
    - copy paste the symbol from the fontawesome web site [https://fontawesome.com/v4.7.0/icons/](https://fontawesome.com/v4.7.0/icons/)
    - or insert the icons unicodes directly in your conf file. I used vim to do that, but I think Emacs can do it as well, and maybe graphical editors too.
        - with vim then, put your cursor at the desired place for the icon
        - go into insert mode (a or i)
        - enter "ctrl+v"
        - then enter the letter "u"
        - and write the unicode of your chosen icon (four characters, as "f012" for example)
        - once done, save and quit (":wq" for newbies as me :)  )
        - your icons should be here !