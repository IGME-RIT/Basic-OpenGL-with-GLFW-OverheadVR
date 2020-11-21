Documentation Author: Niko Procopi 2020

This tutorial was designed for Visual Studio 2019
If the solution does not compile, retarget the solution
to a different version of the Windows SDK. If you do not
have any version of the Windows SDK, it can be installed
from the Visual Studio Installer Tool

CPU Overhead VR
Prerequisites
	All other VR tutorials
	
As an attempt to reduce CPU overhead in the first render pass,
I changed the Mesh.cpp file to store all objects into one vertex
buffer and one index buffer. That way, C++ and OpenGL dont
need to constantly swap which buffers are active or inactive.

Unfortunately, this saves 0.01 ms on average, not what I had 
hoped, but the difference would probably be more noticable
which a much larger demo with hundreds of objects. Feel free
to try this optimization on larger projects