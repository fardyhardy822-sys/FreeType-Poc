# PS4-FreeType-WebKit-Poc

CVE-2025-27363

Hello everyone! 
I hope someone can take advantage of this... please test on both PS4 and PS5. 
If you see malformed %% after running...  is a possible entry point.

TEST:  https://the-maxu.github.io/PS4-FreeType-WebKit-Poc/

REPO: https://github.com/The-Maxu/PS4-FreeType-WebKit-Poc

ORIGINAL POC: https://github.com/zhuowei/CVE-2025-27363-proof-of-concept

Affects up to FreeType 2.13.0
-PS4 12.00 appears to be using 2.9.0 (according to webkit source code released by PS)

I don't know if it will be useful or not. 
I don't know if it can be scaled.
But it has been used to infect Android and iOS devices via PDF files, resulting in RCE. 

I just want to contribute my two cents. And if it's useful, we all win.


You can see more details about the CVE at:
https://cvefeed.io/vuln/detail/CVE-2025-27363 :
An out of bounds write exists in FreeType versions 2.13.0 and below (newer versions of FreeType are not vulnerable) when attempting to parse font subglyph structures related to TrueType GX and variable font files. The vulnerable code assigns a signed short value to an unsigned long and then adds a static value causing it to wrap around and allocate too small of a heap buffer. The code then writes up to 6 signed long integers out of bounds relative to this buffer. This may result in arbitrary code execution.




Well, that's all. I just wanted to share the FreeType Out-of-Bounds Write Vulnerability CVE, since it affects PS4 systems and apparently also PS5. Perhaps someone who knows how to scale it will take advantage of it.

Regards.
