#Slide 1
NULL

没内容
#Slide 2
Throughout 1960's and 1970's, most human interaction with computers was done
through what are called terminals. A terminal device is a piece of hardware
that combines the keyboard with some kind of character display, which in early
days in the 1960's was some kind of printer that print out characters line by
line. Or later in 1970's, it was usually a video console, but video console
was not capable of displaying arbitrary graphics, it can only display text
characters, and these text characters could only be displayed in a fixed grid.
They wouldn't have arbitrarily positioned characters anywhere on the screen,
and also the devices only have one display font and one display color. 

在上个世纪六七十年代的时候，人机交互的主要手段是通过一种叫做“终端”的东西。终端是硬件，一般指的是一个键盘加上某种字符显示设备，最早在六十年代的时候都是打印机，一行一行的把字符打印出来。后来到了七十年代，演进成了“视频工作台“。但那时的”视频工作台”只能显示字符，不能像现在这样显示任意的图形。这些字符显示在固定的格子里，所以大小也是固定的，不像今天这样可以显示在任意的位置。那个时候一般就是：一种字体，一个颜色。

So the idea of terminal is that when they are hooked up to computer, the
computer then can send text characters and sequences to the terminal which get
displayed character by character on the screen and when the user sitting at
the keyboard types anything, a character sent from the terminal to the
computer, so does not need symmetry there. A strict sequence of characters
flows from computer to the terminal and vice versa. AS you can probably guess,
the text going in both directions was almost ASCII text.

所以终端总体上就是这么个东西，你把它连到计算机上，计算机就可以把文本（就是一个一个的字符）和序列（例如转意序列）送到终端，然后一个字符一个字符的显示出来；同样，当用户敲字的时候，这些字就从终端传给了计算机。这里也不需要对称同步，就是一串字符从计算机传到终端，或者反过来从终端传到计算机。可能大家能猜到，这些传来传去的数据基本都是ASCII字符。
#SLIDE 3

In Unix systems, a process may communicate with a terminal through a file
representing that terminal, a terminal character device file. When a process
writes to a terminal character device file, that is putting in data in the
output buffer of the device file which then going to to get sent out by the
operating system to the terminal device associated with that character device
file. Conversely, when the user at the keyboard types something, that data
get sent from the terminal to the computer and the operating system will take
that data and put it in the input buffer of the associated character device
file and then process then may read form the character device file to get that
data. So again, be cleat the terminal is a totally dumb device. When you see
text displayed on the terminal that is something that coming from processes
running on the attached computer. The only exception to this is that with the
terminal character device file we can turn on a mode called echoing. When the
terminal character device operates in the echoing mode, then any input
received from the terminal was immediately echo back out to the terminal so
that is can be displayed on the screen. In practice what this means when
echoing is non and the user types on the keyboard, then whatever key they
type, they will immediately see it appear on their screen. Just be clear that
the terminal doesn't have echoing mode, it is the terminal character device
file has echoing mode, so the data actually be sent from the terminal and
immediately back to the terminal.