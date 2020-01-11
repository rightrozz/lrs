# lrs
Python source code for generating manchester encoded binary files. Use with LRS pagers, GNU Radio and HackRF.

Please watch the following YouTube video for more information.

https://www.youtube.com/watch?v=ycLLb4eVZpI

The pager1.bin file steps through all possible restaurant id's with the pager id number set to 0.

Because setting the pager id in python to 0 will ring all pagers, transmitting this file with the provided
grc file will essentially bruteforce and make all pagers flash for 30 seconds, regardless of restaurant id.

Use the grc file to create an output file (which is named current, and stored in the /tmp/ directory), then
pass the output file to csdr to create a raw file (should be around 850mb large).  This file can then be transmitted
through hackrf_transfer as described in the video.
