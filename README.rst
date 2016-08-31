Wejive (Python Version)
======================

Reverse engineered drivers for the `We-Vibe
<http://www.we-vibe.com>`__ line of bluetooth controlled vibrators.

Description
-----------

We-Vibe is the name of both a company and the line of vibrators sold
by that company. 

Protocol
--------

Wevibe toys uses BTLE to connect to a host, with no pairing or long
term key exchange. After this, the host can send pattern selection and
intensity commands, as well as receiving back data about things like
processor temperature.
  
To control pattern selection and intensity on the device, a 8-byte
command of the following format is used:

0f XX 00 YZ 00 00 00 00

XX - Index of the pattern

Y - "Internal" motor power (4-bit)
Z - "External" motor power (4-bit)

Python Implementation
---------------------

The python implementation in the library allows access to the
aforementioned functionality. As it is using pybluez and gattlib, it
will currently only work on linux (and also requires some boost
installs. Sorry. I'm not happy about it either.).

License
-------

wejibe-py is BSD licensed.

    Copyright (c) 2016, Metafetish
    All rights reserved.
    
    Redistribution and use in source and binary forms, with or without
    modification, are permitted provided that the following conditions are met:
    
    * Redistributions of source code must retain the above copyright notice, this
      list of conditions and the following disclaimer.
    
    * Redistributions in binary form must reproduce the above copyright notice,
      this list of conditions and the following disclaimer in the documentation
      and/or other materials provided with the distribution.
    
    * Neither the name of the project nor the names of its
      contributors may be used to endorse or promote products derived from
      this software without specific prior written permission.
    
    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
    AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
    IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
    DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
    FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
    DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
    SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
    CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
    OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
    OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
