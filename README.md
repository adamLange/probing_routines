# GCODE Probing Routines

Useful gcode routines for probing, probe calibration, machine calibration ect
and python scripts and jupyter notebooks for generation of probing gcode and
visualization of probe results are contained in this repository.

Use this software, instructions, and at your own risk.  A lot of the code in here is
messy now so be sure not to run garbage code and don't crash your machine.


## License

Copyright (c) 2020 Adam Lange

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


## Calibration

One of the most useful gcode routines in the repository is 'probe\_xy\_cal\_y\_plus.ngc'.
This program is used to calibrate the touch probe in the xy plane by probing a surface on the plus
y side.  To before starting this routine the user must jog the machine so that it is within
20mm of the surface to probe.  Run the program.  It will probe the surface then pause. During each pause
rotate the probe 90 degrees.  After the program has completed global parameters #<_probe_dx> and 
#<_probe_dy> will be defined and can be used by other probing routines.

