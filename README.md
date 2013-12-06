overFS - Overlapping File System
===

##Why overFS ?
Testing some ideas that are floating in my head for a while now.
I also think is an awesome opportunity to get more into kernel devel.

##So what is overFS ?
Note that this is what I would like it to be,
not what it currently is.

My goal is to have a sort of hybrid file system without having to deal
with special drive configuration nor have partitions with different 
file systems to get certain performance benefits over some kind of files.

Truth be told that nowadays anyone from average to advanced user handles
quite a lot of types of files of all sizes. Sometimes these users know
their priorities and want to selectively target certain performance 
optimizations to happen on few specific files rather the whole file system.

##LICENSE
For now assume GPLv2 however may still change.
Don't worry, it will be free software for sure. If you want
to use this source code, please contact me so we can arrange
an appropriate license for you.

##Lets Play imagine for a little!

__*HQ Videos/Video Editing:*__

Bigger blocks/inodes make more sense here, and such files should really
be packed.

__*What about altering the video file ?*__

Why not apply your working parts as copy-on-write ? That way you can use
your video editor right on top of your original file, and each time you change
a chunck, you do it copy-on-write style, 
once you save the project back to HQ big chops style.

__*Configuration files:*__

Awesome, small very important files. Sounds like copy-on-write
style file system applies better for this scenario, preferably with btrfs style
30 seconds rollback ?


##Why 'overlapping' for name ?

__*Short Answer:*__

Short name, sounds nice and still shows the main concept, doesn't appear taken.

__*Kind of Long Answer:*__

I am pretty sure I will end up reiventing the wheel at some point, specifically
when trying to get some concepts from other file systems into this hybrid version.

##Supported Kernels ?!?
__Linux kernel as first class citizen.__

_Hurd(Translators probably make this not useful) maybe_

_FreeBSD doubt (on my own) but who knows_

###Note for haters (kind of AFQ) :)

__You can get same functionality by doing X,Z,Y things on F file system.__

I don't want to thinker around existing FS's to get optimization to a single file
or folder.

__You can use partitions with different FS's settings.__

Sure then do it, Can I try hybrid approach now ?

__Project X that is just like this, why don't you go help there instead ?__

If you know of a project like these, feel free to point me to it. I certainly
will love to learn from such project. However please do not 
come with single purpose of getting me to stop the project. This project
purpose is not solely to get something new, but also give me the
opportunity to learn on the way.


