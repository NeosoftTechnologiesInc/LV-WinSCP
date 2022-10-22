# LV-WinSCP

This project is a LabVIEW wrapper on top of the WinSCP .NET API.

The source code is written in LabVIEW  2015 32-bit and exposes a DQMH API and a low-level API.

## Description
This LabVIEW toolkit relies on a WinSCP.exe (v5.21 32-bit) and its related .NET API.
*These two components are embedded next to the source code and do not need to be installed separately.*

It mainly allows sending files to a distant target or getting files from it.

It also exposes methods to list files into directories and to execute **non-blocking** commands on the distant target.

At this moment, the toolkit only allows connecting distant targets through SCP.
Also, all actions are synchronous and will only return when done.

## Installation
The project is autonomous and the source can be pulled and used as is.

To implement new features in the DQMH module, DQMH 6.1 must be installed on the development PC.

The wrapper can also be installed thanks to a VIP package available on VIPM (see [https:// VIPM.io](https:// VIPM.io)). It will create a LabVIEW palette under Neosoft Technologies subsection. From there, the DQMH and low-level APIs will be available.

## Usage
This LabVIEW toolkit can be used to :

* Transfer files between a PC and a distant target
* Execute commands on a target exposing a SSH Shell.

## Support
Tell people where they can go to for help. It can be any combination of an issue tracker, a chat room, an email address, etc.

## Roadmap
Next steps :

1. Implement asynchronous transfers

2. Support FTP

3. Support SFTP

4. Support Amazon S3

## Contributing
Any contribution is welcomed as long as these rules are respected :

1. Any new 'action' on files or distant target must be accessible from the Session class and from a DQMH request.
2. If a DQMH event is added, the tester must be updated to reflect how the addition should be used.
3. All new DQMH events must be a broadcast or a Round trip (unless the time to perform the action is very well know, deterministic and below the module timeout ; in this case a 'Request and Reply' event might be accepted)
4. Ensure that DQMH best practices are respected : https://wiki.dqmh.org/dqmh/documentation/dqmh_best_practices
5. Documentation of VIs must be correctly filled and explain the purpose of each VIs created.

## Authors and acknowledgment
### Contributors 

* Cyril Gambini - Neosoft Technologies - https://www.buymeacoffee.com/cyrilg
* Brice Freund - Neosoft Technologies

### Open source projects

* WinSCP .NET API : https://winscp.net/eng/docs/library
* DQMH - https://dqmh.org

## License
This project is built under BSD-3 license.

Copyright (c) 2022, Neosoft Technologies 
All rights reserved. 

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met: 

 * Redistributions of source code must retain the above copyright notice, 
   this list of conditions and the following disclaimer. 
 * Redistributions in binary form must reproduce the above copyright 
   notice, this list of conditions and the following disclaimer in the 
   documentation and/or other materials provided with the distribution. 
 * Neither the name of Neosoft Technologies nor the names of its 
   contributors may be used to endorse or promote products derived from 
   this software without specific prior written permission. 

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF 
SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE. 

## Project status
This project is mainly maintained by Neosoft Technologies (www.neosoft.ca) and is used in several commercial projects. Any help ugrading and maintaining this library is welcomed !
