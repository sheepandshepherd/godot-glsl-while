glsl-while
==========

This adds the `while` loop to Godot Engine's simplified GLSL.

Notes
=====

- It's not a module; these files **replace** Godot's shader compiler and parser.
- The shader editor recompiles GLSL shaders in real time, so typing an infinite loop, even temporarily as you write, would instantly freeze Godot. To prevent this, I added a few lines to the compiler that limit each `while` loop to 100 iterations. (You probably shouldn't loop that many times in a shader anyway, for performance reasons.)
- There are no `break` or `continue` statements. Use `if` statements and variables instead if you need to stop the loop.

