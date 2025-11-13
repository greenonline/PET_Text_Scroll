# PET_Text_Scroll
Text scrolling using method from 8-Bit Show And Tell

---



## Video

 - [C64 to PET Cross-Development: Smooth Scrolling Wedding Banner](https://www.youtube.com/watch?v=6o9Hi_WrfIA&list=PLvW2ZMbxgP9wZeCcb2wSLLSHjymZcTyU-&index=3)


## Software

 - [Turbo Macro Pro rev v1.2](https://turbo.style64.org/)
 - [Crowther 3 in 1](https://csdb.dk/release/?id=38285)

## Article

From [Your Commodore Apr 1990](
https://archive.org/details/YourCommodore80Jun91/YourCommodore/YourCommodore67-Apr90/page/n63/mode/2up)

3 in 1

The vast majority of computer programmers probably have a diverse range of graphic aids. These may include screen editors, character editors or sprite editors. The only problem is that none of them can carry out all the functions that the programmer requires, Obviously the only way around this is to use a number of programs to produce one finished product.

For example, if you were writing a game you would use a character editor to produce user defined characters. You would then use these to produce the actual background for the game. A sprite editor would be used to produce the sprites. Wouldn't it be easier if it could be done with one program which encompassed all the functions you will ever need? Hence the birth of the 3 IN 1 EDITOR.

3 IN 1 consists of a sprite editor that has provision for multicolour and hi-res sprites. Sprites con be animated, copied or positioned on top of each other etc. Within the program there is also a combined character and background editor. What makes this part of the program so special is that you are not limited to designing just single screens but it is possible to define screens that take up to 32K of the computer's memory.

The editing screens act as a small window that can be moved over a much larger area. Until now most scrolling screens were designed as individual pictures and 'stuck' one next to the other at a later date.

The 3 IN 1 EDITOR has already aroused much interest in programming circles and many programmers are using it to help them design games. The complete editor program is on the tape so that it is available to anyone who is interested in graphics.

Using the Program

Once you have loaded the program and started it running, (with SYS 51500) you will be presented with the editor's main menu which offers the following options:

1) 5PRITE EDITOR
2) CHAR/SCREEN EDITOR
3) DISK COMMANDS
4) DIR
5) DISK REPORT
6) SAVE EDITOR
7) LOAD

Pressing the corresponding key will call up the specified function. Options 1 and 2 call up the sprite editor and the character/background editor respectively. These will be explained in their own sections later on.

Option 3 allows you to send the standard disk instructions to a disk drive. If you are unsure of what the commands are, the main ones are listed in Figure 1.

The DIR function will display a directory listing from any disk in the drive.

However, 3 IN 1 only uses program files (i.e. PRG), so only this type of file is listed to the screen. Also the size of the file is not given as it is not really that important.

Just in cose you ever have any disk errors, I hove included Option 5 which will read rhe error channel of the disk drive and report any errors. 

Option 6 is extremely important. This function allows you to moke more copies of the progam. If you use ihis function then you will be prompted for the filename that you wish to call the program by. The default output device when you load this program is disk. If you are using tape then you will need to change the output device. This is done by pressing F1. You will be able to tell which is currently being used for output as both this optfon and Option 7 will hove either a '1' or an '8' after them. A '1' specifies an output device of 1, i.e. cassette while an '8' means device 8 which is disk.

The final command available from the main menu is LOAD. This will LOAD the specified file into the same area of memory that it was saved from. This means that you can load any of the files created with the editor programs from the main menu.


Using the editors

Before I take a close look at the individual editor programsit is worth pointing out a few convention.
  Firstly all numerical inputs and outputs are in HEX. This is become most programmers work in hexadecimal since it is alot easier when writing machine code than using decimal. Since this program was designed as a programmers tool it is obvfous that it should use HEX. All inputs must be made up to two or four figits e.g. '00' or '0003'.

Many of the functions can be confrolled by either the cursor keys or a joystick in port two. Since the joystick only has one fire button and it may need to either erase or set points, the 'F1' key is used to select its operation. Doth editors indicate whether the joystick is in DRAW mode or erase (DEL) mode. Take a look at the labelled pictures of both editors to see where the flags are.
 As with the main menu the device for output can be either an 8 or 1. This can be changed from the pull down menu (F7).
 Again look at the pictures in order to see where the flags can be found.

The sprite editor

The sprite editor allows you to edit sprites in either multi-colour or hi-res mode. Sprites $A0 to $FF can be edited with the editor. If you are unsure about the sprite number then I suggest that you read the section on sprites in the C64 manual. If you take a look at the picture you will see that quite a lot of information on the screen.

Firstly we have the actual sprite editing screen, This displays a blown up version of the sprite being edited. If you choose multicolour then the horizontal resolution will halve, exactly the same as with multicolour sprites. Unlike most sprite editors you actually design the sprite using the colour for each dot. This means that you don't have to think which combination of dots produce which colour. Simply press one to three to select the editing colour and, hey presto!, draw dots with it.

Colour changing is also extremely easy. Press shift one to five and the corresponding colour will go through all 16 possibilities. Changing colour mode is also extremely easy, choose the option required from the menu (F7). If you want to reverse the sprite simply press CONTROL AND R. Easy isn't it?

It's not really worth mentioning all of the available commands since they are all listed in Figure 2. However, a few functions do need further explanation,

At the bottom right hand corner of the screen there are four sprites referred to as sprites zero to three. Note these are NOT the same as sprite numbers but are just used as reference numbers for the four at the bottom of screen. Usually these four positions hold the same sprites as that which is being edited. It is possible to expand these sprites using the pull down menu. To alter the way that the sprite looks simply select the desired option from the menu followed by the corresponding sprite position number (00-03).

Choosing POSITION from the menu followed by a number allows you to move that numbered sprite around the bottom of the screen. This means that you can position the four sprites next to each other or even overlap them. This may not seem all that useful at first but it is possible to make each of these four sprites different. This means that you could define a large character of up to four sprites joining the sprites together at the bottom of the screen so that you can see what they look like. It is even possible to animate this section of the screen with the number option and the Q and W keys. Choosing NUMBER followed by 00 will cause each of the four sprites at the bottom of the screen to become the same as the one being edited. If on the other hand after you enter a number greater than 00 you can set up animations.

Animation is quire difficult to explain and is best figured out with practice, However I will do my best to explain how to set up and use this special animation function.

When you enter a number greater than 00 for the number of animations after choosing NUMBER the sprites at the bottom of the screen will change. If, for example, we have enterd 01 and the current sprite was $A0, sprite 0 would be the same as the actual sprite $AO. Sprite 01 will will be the same as $A1, Sprite 02 will be the same as $A2 etc. If we now press the keys W and Q we can increment and decrement the sprite numbers at the bottom of the screen giving the appearance of animation. If we press 'W', Sprite 00 will become actual sprite $A1, Sprite 01 will become actual sprite $A2 etc. If we had entered 04 after a CONTROL N instruction then the sprites would be incremented by four every time you pressed the 'W' key, i.e., sprite 00 would become $A4, Sprite 01 would become $A5 etc.

I did say that this form of animation was complicated but if you try it then I'm sure that it will fall into place.

Just in case you have problems with this type of animation there is a simpler form. This is the ANIMATE instruction. This instruction will change all the sprites on the screen, including the large editing screen, in increments of one for a preset length. When you choose ANIMATE you will be prompted at the top of the screen for the first sprite in the sequence and the last, then the sprites will be displayed in order. Pressing 'F' and 'S' will speed up and slow down the speed of this animation.

The sprite that is in the editing window can be moved within the editing grid with the keys specified elsewhere in this article.

If WRAP-ON is set what disappears off of one edge of the editing grid will appear at the opposite edge. If WRAP-ON is set then anything moved off the grid is lost.

Characters and Sprites

The option that may seem a little strange is the ability to turn characters into sprites. The pull down menu option CHAR-BANK is used to specify which character bank you want to look at. Should you want the normal Commodore characters then enter D000 at the prompt.

COPY CHARS is used to position the desired characters in the sprite grid. When this option is selected a large square will appear in the sprite editing grid. This can be moved within the grid using the cursor keys, Once you have the block where you want your character to appear press RETURN. You will then be prompted for the character that you want to appear in the sprite. Try this using the character set at D000 and you'll soon see what this option does. Use RUN/ STOP to exit the COPY CHARS option.


All Change

It is possible to change one multi colour to another with the SWAP COLOUR option on the pull down menu, When selected this option presents you with the three multicolours at the top of the screen. Move the arrow to the colour you want to swap and press return (use cursor left/right to move arrow). Now select the second colour in the some way. When RETURN is pressed the two colours on the screen will swap over. DO NOT use this option when dealing with hi-res, use the reverse option (CTRL R) instead.


Character Screen Editor

Both of these editors are present on the same screen. The top half is the character editor while the bottom is used as a small window over a larger screen.

Quite a lot of information is present this screen and it is worth studying the commented picture in order to find where everything is.

Again it is worth looking at some of the available commands in more detail, a summary of them all can be found in Figure 3.

As with the sprite editor, characters can be edited in either multi-colour or hi-res mode, colours being chosen and changed as in the sprite editor.

Once you have entered a character you can place it anywhere within a defined background in the background editor. The 'J' key is used to move control between either the character editor or the background editor. You can see which mode you are in by seeing which cursor is flashing.

The background size is defined with the WINDOW SIZE option and the window con be anything from two by two character upwards, the maximum in either direction being $FFFF. Obviously your screen size is limited by the amount of memory available. If there is not enough room for your window then you will have to enter new values. I have made up to 32K of memory available for the window though I'm sure that you will find that you very rarely use this much. The two numbers in the middle of the screen, after the word DATA, show you where your window starts ond finishes in memory.

One very important consideration for games programmers is where they are actually going to put their screen. The BASE ADDRESS option will prompt you for the base address of the background so that you can move it where you want. Do make sure that you don't overwrite any other programs in memory, such as the editor.

You may think that it is a little limiting to just see a small section of your total graphics screen ot one time. 1 have therefore included the 'W' command which will switch to a fuli screen display in which you can move around the background, movement being controlled by the cursor keys only.

It is possible to set up o border character which is displayed around the smaller editing window. I usually leave this blank though you may try different effects by putting fancy borders around the screen. This does not apply to full screen mode.


Pointing a large area

When producing backgrounds if is quite usual for large areas of the background to be repeated elsewhere in the backdrop. A GRAB option is available that will allow you to grab a rectangular area of the backdrop and copy it to another position of the screen.

To use this mode you should be in rhe background editing section of the character editor. Move the cursor to where the top left of the block to be copied is and press the left arrow key (top right of the keyboard). Use the cursor keys to move the bottom right of the area to be copied, and the rectangular area marked will be highlighted. Once the highlight covers the total area that you want to copy press the RETURN key. Now when you move around the background you will drag with you a copy of the block marked. You can place this anywhere on the backdrop by pressing '*'. RUN/STOP is used to exit this mode.


Saving and Loading

As I said earlier, it is possible to load any type of file into memory from the main menu. It is also possible to laod any type of file from within any of the other editors as well. However the I/O device is separate in each editor so you must change it in each section of the program. 

Even though you can LOAD in any type of data from within any section of the program, you can only save each type of data from the correct editor. You must therefore be in the character editor in order to SAVE your user defined graphics. You must be in the background editor in order to save backgrounds.


Note 

When you design a background, make sure that you keep a note of the screen size that is defined, since a screen that is supposed to be 20 characters wide will look rather silly if the screen is set to 21 characters.
   That just about sums it up for the sprite editor. I'm sure that you will find it very easy to use with a little practice and that you will find most of the instructions that you are every likely to need.





Disk Commands

```none
IO                         Initiate disk
VO                         Validate disk
NO name id                 Format disk
RO new name o old name     Rename file
SO name                    Scratch file

CHARACTER/SCREEN EDITOR

Cursor/Jaystick            Move cursor
*/Fire (draw)              Draw point
Space/Fire (del)           Delete point
F1                         Joystick fire function
+                          Next character
-                          Previous character
C                          Copy character
G                          Go to character
1-3                        Select current colour
Shift 1-3                  Change colours
CLR                        Clear character
L                          Scroll character left
R                          Scroll character right
U                          Scroll character up
D                          Scroll character down
Y                          Flip on Y axis
X                          Flip on X axis
CTRL R                     Reverse character
J                          Jump to background window

Background Mode

Left Arrow                 Set top left of block
Cursors                    Move size of block
Return                     Set block
G                          Get character under cursor
*                          Place selected character
F7                         Bring up menu
SWAP COLOUR                Swap mufti colours over
BASE ADDRESS               Set start of background
FETCH CHARACTERS           Set where characters are in memory. D00D 
                           is normal set.
COPY SPRITE                Cursors to move block. 
                           RETURN to select 
                           RUN/STOP to exit

SPRITE EDITOR

Most functions as for Character/Background Editor

F7                         Bring up menu
CHAR-DANK                  Where characters are stored
                           (used by COPY-CHAR) 
COPY-CHAR                  Copy characters into sprite.
                           Use cursors to move, RETURN 
                           to place and RUN/STOP to exit. 
WRAP-SET                   LRUD wtap around ON/OFF
ANIMATE                    Use F to speed up, S to slow down
```


## BASIC code


C64

```none
5 s=1024:rem s=32768 for pet
10 dim t%(255)
20 t%(32) = 32:t%(96)=103:t%(97)=117
30 t%(101)=224:t%(103)=106:t%(106)=118
40 t%(116)=101:t%(117)=116:t%(118)=225
50 t%(160)=160:t%(224)=231:t%(225)=245
60 t%(229)=96:t%(231)=234:t%(234)=246
70 t%(244)=229:t%(245)=244:t%(246)=97
80 r$=chr$(18):m$=chr$(146)
85 print chr$(147)+chr$(5);
90 print"  "+r$+" "+m$+"  "+r$+"  "+m$+"   "+r$+"   ";
95 printm$+"  "+r$+" "+m$+"  "+r$+"  "+m$+"   "+r$+"   "+m$
100 for x=stos+39 
110 if peek(x)<>peek(x+1)then poke x,peek(x)+64
120 next
130 end

200 for x=stos+39 
210 poke x,t%(peek(x))
220 next
230 end
300 for x=5 to s+39
310 printpeek(x);:next
320 end

400 l=s+1:v=96:x=v
410 print chr$(147);
420 gosub 500
430 l=l+40:print:v=224:x=v
440 gosub 500
490 end
500 poke l,x:printchr$(29)chr$(29)x
510 x=t%(x):l=l+40
520 if x<>v goto 500
530 return
600 for x=55296to55296+39step2
610 poke x,1:pokex+1,3
620 next
630 end
```

PET

```none
5 S=32768
10 DIM T%(255)
20 T%(32) = 32:T%(96)=103:T%(97)=117
30 T%(101)=224:T%(103)=106:T%(106)=118
40 T%(116)=101:T%(117)=116:T%(118)=225
50 T%(160)=160:T%(224)=231:T%(225)=245
60 T%(229)=96:T%(231)=234:T%(234)=246
70 T%(244)=229:T%(245)=244:T%(246)=97


80 R$=CHR$(18):M$=CHR$(146)
85 PRINT CHR$(147)+CHR$(5);
90 PRINT"  "+R$+" "+M$+"  "+R$+"  "+M$+"   "+R$+"   ";
95 PRINTM$+"  "+R$+" "+M$+"  "+R$+"  "+M$+"   "+R$+"   "+M$
100 FOR X=STOS+39 
110 IF PEEK(X)<>PEEK(X+1)THEN POKE X,PEEK(X)+64
120 NEXT
130 END


200 FOR X=STOS+39 
210 POKE X,T%(PEEK(X))
220 NEXT
230 END
300 FOR X=5 TO S+39
310 PRINTPEEK(X);:NEXT
320 END


400 L=S+1:V=96:X=V
410 PRINT CHR$(147);
420 GOSUB 500
430 L=L+40:PRINT:V=224:X=V
440 GOSUB 500
490 END
500 POKE L,X:PRINTCHR$(29)CHR$(29)X
510 X=T%(X):L=L+40
520 IF X<>V GOTO 500
530 RETURN
600 FOR X=55296TO55296+39STEP2
610 POKE X,1:POKEX+1,3
620 NEXT
630 END
```

## Assembler

Note that there are two sets of `ahead1` and `ahead2`, which is odd and confusing. However, it doesn't *seem* to affect the code.

```none
;defines
pet         = 0
basicstub   = 0

mapwidth    = $fe

scrollcount = $fb
mapx        = $fc
zp1         = $fd;$fe

            .ifeq pet
            *= $0801
screen      = $0400
map         = $0a00
            .endif

            .if pet
            *= $0401
screen      = $8000
map         = $0600
            .endif

line0       = map
line1       = map+(mapwidth*1)
line2       = map+(mapwidth*2)
line3       = map+(mapwidth*3)
line4       = map+(mapwidth*4)
line5       = map+(mapwidth*5)
line6       = map+(mapwidth*6)


            ;BASIC stub
            .if basicstub
            .word basicend
            .word 2020 ;BASIC line #
            .byte $9e  ;SYS token
            .if pet
            .byte $31,$30,$33,$37 ;1037
            .endif
            .ifeq pet
            .byte $32,$30,$36,$31 ;2061
            .endif
basicend    .byte 0,0,0
            .endif

init 
            lda #147
            jsr $ffd2
            sei

            .ifeq pet
            lda#<320
            sta $0318
            lda#>320
            sta $0319
            .endif

            lda #0
            sta mapx

            lda #8
            sta scrollcount

            jsr convertmap

bigloop
            lda scrollcount
            cmp #8
            bne smoothscroll

            ;plot whole screen
            lda mapx
            clc
            adc #39
            tax
            ldy #39
loop2       lda line0,x
            sta screen+240,y
            lda line1,x
            sta screen+280,y
            lda line2,x
            sta screen+320,y
            lda line3,x
            sta screen+360,y
            lda line4,x
            sta screen+400,y
            lda line5,x
            sta screen+440,y
            lda line6,x
            sta screen+480,y
            dex
            dey
            bpl loop2
            bmi ahead1 ;bra

smoothscroll
            ldy #119
loop1
            ldx screen+240,y
            lda convert,x
            sta screen+240,y

            ldx screen+360,y
            lda convert,x
            sta screen+360,y

            ldx screen+480,y
            lda convert,x
            sta screen+480,y

            dey
            bpl loop1
 

ahead1
            dec scrollcount
            bne ahead2
            lda #8
            sta scrollcount

            inc mapx
            lda mapx
            cmp #(mapwidth-64)
            bcc ahead2
            lda #0
            sta mapx
ahead2
            jsr vblank
            jmp bigloop
vblank
            .if pet
vloop       lda $e840
            and #%00100000
            bne vloop
            .endif

            .ifeq pet
vloop       lda $d012
            cmp #$ff
            bne vloop
            .endif

            rts

convertmap
            .block
            lda #<map
            sta zp1
            lda #>map
            sta zp1+1
            ldx #7
            ldy #0

loop
            lda (zp1),y
iny
cmp (zp1),y
beq ahead1
clc
adc #64
dey
sta (zp1),y
iny
ahead1
            cpy #mapwidth
bne loop

ldy #0
clc
lda zp1
adc #mapwidth
sta zp1
bcc ahead2
inc zp1+1
ahead2
            dex
            bne loop
            rts

            .bend

convert     ;transform table

            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 32,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 103,117,0,0,0,224,0,106
            .byte 0,0,118,0,0,0,0,0
            .byte 0,0,0,0,101,116,225,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 160,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 0,0,0,0,0,0,0,0
            .byte 231,245,0,0,0,96,0,234
            .byte 0,0,246,0,0,0,0,0
            .byte 0,0,0,0,229,244,97,0
            .byte 0,0,0,0,0,0,0,0
```

Note: If there are too many spaces, too much indentation, then the `.byte` lines get corrupted by spilling over on to the next line.

```none
convert  ;transform table

         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 32,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 103,117,0,0,0,224,0,106
         .byte 0,0,118,0,0,0,0,0
         .byte 0,0,0,0,101,116,225,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 160,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 0,0,0,0,0,0,0,0
         .byte 231,245,0,0,0,96,0,234
         .byte 0,0,246,0,0,0,0,0
         .byte 0,0,0,0,229,244,97,0
         .byte 0,0,0,0,0,0,0,0
```

However, instead of fiddling around adding and removing spaces, just remove all indents and the TMP will auto indent for you.

```none
convert  ;transform table

.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 32,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 103,117,0,0,0,224,0,106
.byte 0,0,118,0,0,0,0,0
.byte 0,0,0,0,101,116,225,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 160,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 231,245,0,0,0,96,0,234
.byte 0,0,246,0,0,0,0,0
.byte 0,0,0,0,229,244,97,0
.byte 0,0,0,0,0,0,0,0
```

Complete pastable source, with excess (problematic for TMP) spaces removed:

```none
;defines
pet         = 0
basicstub   = 0

mapwidth    = $fe

scrollcount = $fb
mapx        = $fc
zp1         = $fd;$fe

            .ifeq pet
            *= $0801
screen      = $0400
map         = $0a00
            .endif

            .if pet
            *= $0401
screen      = $8000
map         = $0600
            .endif

line0       = map
line1       = map+(mapwidth*1)
line2       = map+(mapwidth*2)
line3       = map+(mapwidth*3)
line4       = map+(mapwidth*4)
line5       = map+(mapwidth*5)
line6       = map+(mapwidth*6)


            ;BASIC stub
            .if basicstub
            .word basicend
         .word 2020 ;BASICline#
         .byte $9e  ;SYS token
            .if pet
         .byte $31,$30,$33,$37 ;1037
            .endif
            .ifeq pet
         .byte $32,$30,$36,$31 ;2061
            .endif
basicend    .byte 0,0,0
            .endif

init 
            lda #147
            jsr $ffd2
            sei

            .ifeq pet
            lda#<320
            sta $0318
            lda#>320
            sta $0319
            .endif

            lda #0
            sta mapx

            lda #8
            sta scrollcount

            jsr convertmap

bigloop
            lda scrollcount
            cmp #8
            bne smoothscroll

            ;plot whole screen
            lda mapx
            clc
            adc #39
            tax
            ldy #39
loop2       lda line0,x
            sta screen+240,y
            lda line1,x
            sta screen+280,y
            lda line2,x
            sta screen+320,y
            lda line3,x
            sta screen+360,y
            lda line4,x
            sta screen+400,y
            lda line5,x
            sta screen+440,y
            lda line6,x
            sta screen+480,y
            dex
            dey
            bpl loop2
            bmi ahead1 ;bra

smoothscroll
            ldy #119
loop1
            ldx screen+240,y
            lda convert,x
            sta screen+240,y

            ldx screen+360,y
            lda convert,x
            sta screen+360,y

            ldx screen+480,y
            lda convert,x
            sta screen+480,y

            dey
            bpl loop1
 

ahead1
            dec scrollcount
            bne ahead2
            lda #8
            sta scrollcount

            inc mapx
            lda mapx
            cmp #(mapwidth-64)
            bcc ahead2
            lda #0
            sta mapx
ahead2
            jsr vblank
            jmp bigloop
vblank
            .if pet
vloop       lda $e840
            and #%00100000
            bne vloop
            .endif

            .ifeq pet
vloop       lda $d012
            cmp #$ff
            bne vloop
            .endif

            rts

convertmap
            .block
            lda #<map
            sta zp1
            lda #>map
            sta zp1+1
            ldx #7
            ldy #0

loop
            lda (zp1),y
iny
cmp (zp1),y
beq ahead1
clc
adc #64
dey
sta (zp1),y
iny
ahead1
            cpy #mapwidth
bne loop

ldy #0
clc
lda zp1
adc #mapwidth
sta zp1
bcc ahead2
inc zp1+1
ahead2
            dex
            bne loop
            rts

            .bend

convert  ;transform table

.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 32,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 103,117,0,0,0,224,0,106
.byte 0,0,118,0,0,0,0,0
.byte 0,0,0,0,101,116,225,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 160,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 231,245,0,0,0,96,0,234
.byte 0,0,246,0,0,0,0,0
.byte 0,0,0,0,229,244,97,0
.byte 0,0,0,0,0,0,0,0
```

### Use this!!!

Tided pastable source, w/ some shortened labels, with excess (problematic for TMP) spaces removed:

```none
;defines
pet      = 1
basicstb = 1

mapwidth = $fe

scrllcnt = $fb
mapx     = $fc
zp1      = $fd;$fe

         .ifeq pet
         *= $0801
screen   = $0400
map      = $0a00
         .endif

         .if pet
         *= $0401
screen   = $8000
map      = $0600
         .endif

line0    = map
line1    = map+(mapwidth*1)
line2    = map+(mapwidth*2)
line3    = map+(mapwidth*3)
line4    = map+(mapwidth*4)
line5    = map+(mapwidth*5)
line6    = map+(mapwidth*6)


         ;BASIC stub
         .if basicstb
         .word basicend
         .word 2020 ;BASICline#
         .byte $9e  ;SYS token
         .if pet
         .byte $31,$30,$33,$37 ;1037
         .endif
         .ifeq pet
         .byte $32,$30,$36,$31 ;2061
         .endif
basicend .byte 0,0,0
         .endif

init 
         lda #147
         jsr $ffd2
         sei

         .ifeq pet
         lda#<320
         sta $0318
         lda#>320
         sta $0319
         .endif

         lda #0
         sta mapx

         lda #8
         sta scrllcnt

         jsr convertmap

bigloop
         lda scrllcnt
         cmp #8
         bne smoothscroll

         ;plot whole screen
         lda mapx
         clc
         adc #39
         tax
         ldy #39
loop2    lda line0,x
         sta screen+240,y
         lda line1,x
         sta screen+280,y
         lda line2,x
         sta screen+320,y
         lda line3,x
         sta screen+360,y
         lda line4,x
         sta screen+400,y
         lda line5,x
         sta screen+440,y
         lda line6,x
         sta screen+480,y
         dex
         dey
         bpl loop2
         bmi ahead1 ;bra

smoothscroll
         ldy #119
loop1
         ldx screen+240,y
         lda convert,x
         sta screen+240,y

         ldx screen+360,y
         lda convert,x
         sta screen+360,y

         ldx screen+480,y
         lda convert,x
         sta screen+480,y

         dey
         bpl loop1
 

ahead1
         dec scrllcnt
         bne ahead2
         lda #8
         sta scrllcnt

         inc mapx
         lda mapx
         cmp #(mapwidth-64)
         bcc ahead2
         lda #0
         sta mapx
ahead2
         jsr vblank
         jmp bigloop
vblank
         .if pet
vloop    lda $e840
         and #%00100000
         bne vloop
         .endif

         .ifeq pet
vloop    lda $d012
         cmp #$ff
         bne vloop
         .endif

         rts

convertmap
         .block
         lda #<map
         sta zp1
         lda #>map
         sta zp1+1
         ldx #7
         ldy #0

loop
         lda (zp1),y
         iny
         cmp (zp1),y
         beq ahead1
         clc
         adc #64
         dey
         sta (zp1),y
         iny
ahead1
         cpy #mapwidth
         bne loop

         ldy #0
         clc
         lda zp1
         adc #mapwidth
         sta zp1
         bcc ahead2
         inc zp1+1
ahead2
         dex
         bne loop
         rts

         .bend

convert  ;transform table

.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 32,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 103,117,0,0,0,224,0,106
.byte 0,0,118,0,0,0,0,0
.byte 0,0,0,0,101,116,225,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 160,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 0,0,0,0,0,0,0,0
.byte 231,245,0,0,0,96,0,234
.byte 0,0,246,0,0,0,0,0
.byte 0,0,0,0,229,244,97,0
.byte 0,0,0,0,0,0,0,0
```


## Notes

Using VICE emulator.

### Trying to use 3-in-1

Using `crowther_-_edit23.d64`.

Contrary to what the magazine article, and the comment on the linked page, says, this does not work:

```none
LOAD"*",8,1
SYS51500
```

Use instead

```none
LOAD"CR*",8
RUN
```

Press option 2, for the editor.

Hit F7 for the menu, press enter on Window Size and X = 00FE and Y = 0007 (16 bit numbers are required)

F7 -> Set Hi Res

F7 -> Fetch: D000
F7 -> Fill Window: 20 (i.e. space)
F7 -> Border character: FF

Then <kbd>J<kbd> for jump to the map and <kbd>+<kbd> to scroll until `#A0` (i.e. reverse space)

Use the left cursor key to get to the left hand "edge" of the map - it can take a while, and it looks as is you aren't moving, but you are.

Use cursor key right to scroll 40 characters right, to leave a 40 character blank to the left of the scrolling message.

Then press `*` (of all the most awkward key presses) to draw a "pixel" using the selected character (`#A0`). `G` selects the character under the cursor, which is easier than having to scroll to A0 again.

If you having killed yourself, after having had to paint out the message using the most tedious controls ever conceived...
 
Then F7 -> Save Window, call it map2

Note: If you mess up, or make any changes, you can ***not*** overwrite the existing map. You *must* call it by a different name. I lost a large map doing exactly that.

### Trying to use TMP

TMP is unbelievably difficult to `LOAD` – a PhD. is required. You end up having to extact TMP from the original disk and make your own disk, just for simplicity's sake.

A very noisy catalog listing is produced by `LOAD"$",8` and `LIST`, full of confusing (and needless) comments. Note to developers: Trying to cram information into *every* available bit of space just leads to a very "noisy" UI/UX.

Also, on the C64, what the hell happened to `DLOAD` that was present on the PET, but seemingly dropped on the C64. How sad is that? Commodore don't like to make things easy, do they? Swine! Oh yeah, as the C64 is a home machine, Commodore made home users use awful commands, as they weren't good enough to use the "business" commands of the PET – great design decisions all round. Even `DIRECTORY` and `CATALOG` are missing – you have to use the positively prehistoric `LOAD "$",8` and then `LIST`.

Watch [Turbo Macro Pro v1.2 - Getting up and running with an easy to use and powerful C64 assembler.](https://www.youtube.com/watch?v=f231UKDhKxo) to figure out how to load TMP. Side note to developers: : If you need an instructional video to show you how to load something, then it clearly is badly designed. What is wrong with having just one or two files on a disk and allowing the user to use `LOAD"*",8`?

The two disk images:

   - `Turbo_Macro_Pro_Sep06-128_IDE64.d64` only has four files
   - `Turbo_Macro_Pro_Sep06-128_IDE64.d64` has many files (and crappy comments) and is the disk to use (apparently). You want `TMP v1.2/S.` and `TMPPREFS v1.2/S.` (what is with these unweldy filenames? )

Using `LOAD "$",8` and then `LIST` results in a listing:

```none
...
73   "TMP      V1.2/S." PRG
...
28   "TMPPREFS V1.2/S." PRG
```

To load `TMPPREFS`, use the up arrow key and change to 

```none
73   "TMP      V1.2/S." PRG
LOAD "TMPPREFS V1.2/S.",8
```
and hit enter. Then enter `RUN`.

This is the most soul destroying application to use, ever. "Back arrow plus 'L'" to load, this is very confusing to the non-native C64 user!!! The cursor just moves around. From Reddit, [weird question but....](https://www.reddit.com/r/c64/comments/qe3uvk/weird_question_but/): "Back arrow" is actually a character – Use Shift and the key to the left of the "1" key (§/±) on the Mac. Load "tmp *", will load the TMP. Enter "y" (Yes), to "overwrite prefs from loaded? (y/n)"


 - Back arrow + C - change colour, enter "0" for border, then ctrl-5 for purple (who TF invented these keystrokes?).
 - Insert/Create new blank disk (Top tip: Use a copy of the Crowther v2.3 disk)
 - Back arrow + * for disk listing
 - Back arrow + s and save the new TMP as "tmp"

When I first tried it, I didn't detach the disk, and loading tmp (`LOAD"TMP",8`) and calling `SYS 32768` didn't work, it did nothing. Let's try again...

To delete a file, see [Deleting and overwriting files on disk...howto? ](https://www.lemon64.com/forum/viewtopic.php?t=8505), there is obviously no scratch command, so

> *Delete a file:
> 
> OPEN1,8,15,"S:FILENAME":CLOSE1
> 
> Note: Since the "S" command is bugged as well, you may want to initialise the drive beforehand to avoid possible problems, using:
> 
> OPEN1,8,15,"I":CLOSE1

Apparently, every disk command is buggy, even `@`, so it is easier to just make a new disk. Soul destroying.

After creating a new disk, re-saving "tmp", and detaching the disk, the same thing happened. So soul destroying.

Note: Do ***not*** try to overwrite using @, from within TMP, as you will end up with a file named `@TMP` that is impossible to delete.

Turns out you have to use the `,1` suffix, to load the machine code into the correct location, as in

```none
LOAD"TMP",8,1
```

Then `SYS 32768` to run it.

Now, if you are using an emulator, you can just paste in the assembly code, which is also soul destroying. Actually things start of get (slightly) better from hereonin. Still soul destroying, just less so.

(command)+shift R - for extra RAM (REU), that the VICE emulator does not have turned on, by default. 

Trying to add it with F10 > Machine settings > Memory Expansion Hack settings > Memory Expansion Hack Device > C64 256k. However, it doesn't *seem* to work. Do you need to specify a RAMdisk filename? Just make up a name. But it still didn't work. I gave up (again!).

Trying F10 > Machine settings > Cartridge > RAM Expansion Module > Enable (and save image, specify `remdisk`. I found that (command)+shift R still doesn't work.

It turns out that on the original TMP disk there is a `TMP+REU` program. Load `TMP+REU *` in to `TMPPREFS` and save that as `TMP`. Now use that.

Now, just do, in VICE, F10 > Machine settings > Cartridge > RAM Expansion Module > Enable. There is no need for the memory hack, under Machine Settings, and there is no need to specify a file name for the RAM Expansion Module cartridge setting.

Note: To make your life easier, create a disk, with the Crowther editor, TMP+REU (saved as just "TMP", as the REU is essential for the TMP to load the map) and the `map2` file on it.

Continuing on, with the TMP+ERU version, and having pasted in the assembly source...

(command)+shift R, then <kbd>L</kbd> and "map", at `0A00`. 

Then (command) 3 to assemble. And, finally, <kbd>S</kbd> to run.

It works! (or hopefully it does).

RESTORE key to return to TMP (where is the RESTORE key on the emulator?). I got stuck again, at this point.

Then for the PET, reload the map to 0600, change the two defined PET flags to one (`pet` and `basicstub`, rebuild (command) + 3, 

Now, exit to the monitor (F7 > Monitor > Start Monitor). However, this is the "wrong" monitor, it isn't the "Super snapshot monitor". The "Super snapshot monitor" cartridge is available, but how do you start it? The same issue is described here, [Super Snapshot or alternatives?](https://www.reddit.com/r/Commodore/comments/jq4tsf/super_snapshot_or_alternatives/). 

From [Super snapshot 5](https://www.lemon64.com/forum/viewtopic.php?t=82255)

> You can download a Zip file on that [Wiki page](https://rr.pokefinder.org/wiki/Super_Snapshot). In that zip file is, among many others, a file called "Super_Snapshot_v5.22_v1_1990_PAL.crt". This can be used by 'The C64'. Depending on the firmware version you can use the on/off button from 'The C64' as a virtual "freeze button" from the cartridge to enter the Super Snapshot menu. Works like a charm, you just have to puzzle a little. On your Windows computer extensions probably aren't shown so Windows associates .BIN files w/ a DVD.

Use F7 > Cartridge > Attach CRT, select `Super_Snapshot_v5.22_v1_1990_PAL.crt`

So we now have two cartridges attached: The Super Snapshot and the ERU.

When (if?) you finally get Super Snapshot working, and having just loaded the map at 0600  and reassembled the PET version....

F7 > Cartridge > Cartridge freeze

Examine the bytes

```none
*R0
M 0401
D 040D
M 0600
```

Save it with

```none
SS "SCROLLTEXT",8,0401,10F8
```

Then on the PET, `DLOAD"SCROLLTEXT"` and `RUN`

Finished!!

#### Commands

Note: (command) => <kbd>±</kbd> on the Mac

See [List of commands](https://slark.me/c64-downloads/turbo-macro-pro-editor-commands.pdf)

 - (command) + c - cold start (clear memory)
            



## Conclusion

Soul.Destroying.

I stand by my statement that I made in the [README](https://github.com/greenonline/Perl-BASIC-Tool-Kit/blob/main/README.md) for my Perl BASIC Toolkit – using emulators to develop on is painful, slow, and boring. It is much faster to develop on a modern host and then just paste that over to the emulator.

However, TMP is a useful tool, although it *does* have a steep learning curve, and it is ridiculously fiddly to get started with (just to get the program to run).

3-in-1 is also a great tool, but with extruciatingly painful keypresses. Which is made worse by the, seemingly, rather unresponsive <kbd>*</kbd> key _ multiple hard long presses are required.

C64 BASIC is just dire, especially the (non-existant) disk handling tools.

Hopefully, I shall never have to use any of the three ever again! Seriously.
