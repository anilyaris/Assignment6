# ME-C3100 Computer Graphics, Fall 2017
# Lehtinen / Kemppinen, Ollikainen, Aarnio
#
# Assignment 6: Real-Time Shading

Student name: Anıl YARIŞ
Student number: 643454
Hours spent on requirements (approx.): 3 hours
Hours spent on extra credit (approx.): 5 hours

# First, a 10-second poll about this assignment period:

Did you go to exercise sessions?
No.
Did you work on the assignment using Aalto computers, your own computers, or both?
Only on my own computer.
# Which parts of the assignment did you complete? Mark them 'done'.
# You can also mark non-completed parts as 'attempted' if you spent a fair amount of
# effort on them. If you do, explain the work you did in the problems/bugs section
# and leave your 'attempt' code in place (commented out if necessary) so we can see it.

R1       Sample diffuse texture (1p): done
R2        Sample normal texture (1p): done
R3  Blinn-Phong diffuse shading (2p): done
R4 Blinn-Phong specular shading (2p): done
R5     Normal transform insight (4p): attempted

Answers for R5:
* First question is answered in the appropriate places in the code.
* In R2, if the normals weren't transformed to camera space all vectors used in the shading process had to be transformed to world space.
* For the rest of the questions I couldn't really understand what kind of an answer is expected from us. For me things look fine, I wouldn't make a
  change to the shading. I tried to use the hint but they don't help with the questions. As the first hint suggested I checked the changes between
  the two modes when flying around the object and obviously one changes colors while the other doesn't, but it is supposed to be this way because one
  is not transformed to the camera space so the normals are unaffected whereas the other one updates the drawn normals based on the position and
  direction of camera. And for the hint about the light, the directions are transformed to camera space before being passed to the shader, but this
  is also obvious based on the convention being used. Moreover, each of these sub-questions are awarded approximately the same points as each of the
  previous requirements, which I find unfair in terms of point given per effort spent, so I'm kind of disappointed about the format of this requirement.

# Did you do any extra credit work?

I implemented moving lights. Pressing K toggles the rotation animation of the lights, pressing L resets the rotation.

Also implemented color variations. Pressing H starts/stops the movement of colored bands, pressing J resets the colors (to get back to the
unaltered view the color animation must be stopped first with H, then reset with J). The color pattern of the bands is unnecessarily complex,
I thought it would look cooler but it doesn't look any different from random colors. The calculation can be found on lines 623-626 of App.cpp,
how it affects the shader can be found on lines 66-82 of pshader.glsl.

I also tried to implement shadows but I couldn't. I roughly understood what I needed to do but couldn't figure out how I should use the given variables
in shaders. For example I couldn't figure out how to utilize the shadow sampler because the other samplers took their inputs from files whereas I needed
to provide depth information but it is calculated in the vertex shader.

# Are there any known problems/bugs remaining in your code?

Nothing that I could observe.

# Did you collaborate with anyone in the class?

No.

# Any other comments you'd like to share about the assignment or the course so far?

Again, I think R5 should have been different, either its points should have been lower or it should be a coding requirement.