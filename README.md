# TGL-Cplusplus-Object-Library

TGL (Tiny Generic Library) is a C++ object library, mainly focused on Win32 (therefore not so high performance) video game programming.

There's the base TGL, which handles:
	-(tgl Errors.h) errors that take place in the TGL objects
	-(tgl Functions.h) general functions, not bound to any object
	-(tgl Operators.h) operator overloads for the TGL objects
	-(tgl String Functions.h) a remake of the C string functions
	-(tgl String Operators.h) operator overloads for TGL string objects
	-(tgl.h)
		-TGL class declarations
		-variables used by TGL
		-variables that memorize the addresses of every TGL object and whether their destructors were called
		-TGL function declarations
		-TGL operator declarations
		-the includes to the other TGL files
	-(tglAngler.h) calculating trigonometric values on one's own circle conventions (where a circle can be split in any number of degrees, up to 2^32-1 degrees)
	-(tglAudio.h) playing raw audio, with the use of Win32
	-(tglButton.h) simplifying the process of creating, deleting, customizing buttons for the interface
	-(tglDisplay.h) using Win32 to display raw bitmaps on windows
	-(tglInterface.h) simplifying the process of creating layers of interface (each object can have multiple buttons, as well as addresses to other interface objects, perfect for previous/next page)
	-(tglNumber.h) computing big numbers (and I mean REALLY big numbers. Numbers that can easily reach 4 billion digits, and theoretically up to 2^64, or more, digits; it may not be a necessity, but it's just an experiment that I wanted to add)
	-(tglString.h) C strings, very much like the std::string object; the methods and member variables are nearly identical in nature
	-(tglTextIO.h) text output on windows contained within tglWindow objects (with customizable character images)
	-(tglTexture.h) raw bitmap image loading, as well as allocating and modifying pixels in memory. This object's purpose is not only simplicity for image drawing, but also providing an easy way to draw multiple image layers, to prepare them for display
	-(tglVector.h) mathematics/physics/video games vectors, which have x, y, z, w values, perfect for position, speed, acceleration, jerk, and jounce, all available in up to 4 dimensions
	-(tglWindow.h) creating windows with ease, by using Win32 functions and variables
 
Then there's the RC (Ray Casting) extension, for Ray Casting in video games, which handles:
	-(tglRC Functions.h) general RC functions, not bound to any object
	-(tglRC.h)
		-RC class declarations
		-variables used by RC
		-variables that memorize the addresses of every RC object and whether their destructors were called
		-RC function declarations
		-RC operator declarations
		-the includes to the other RC files
	-(tglRCCamera.h) camera positioning, rotation, as well as rendering whatever's in its sight. A camera can be a player, a portal, a normal camera, etc. (meaning the object gives liberty to the programmer)
	-(tglRCWall.h) the lines present in the 2D terrain, which represent walls (at the moment, vertical straight walls)

Including tgl.h will automatically include the other TGL files, as long as they're in the same folder.
Including tglRC.h will automatically include the other RC files, as long as they're in the same folder. tgl.h must be included first.
