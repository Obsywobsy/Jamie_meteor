# Fixed timing offsets suggested bugfix
A recent bugfix corrected the output display of fixed timing offsets to match the inputted values.
This did not fully correct the underlying problem, where inputted values were being added more than once in the execution of the Trajectory.py solving routines.
A fix is proposed to zero the fixed timing offset arrays at an earlier point in the program, preventing them from being added multiple times. In order to preserve the offset values for use in the output display, the various arrays and dictionaries containing them are copied before they are zeroed.
