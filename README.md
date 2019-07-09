# OpenC64KernalCart
OpenC64KernalCart is an Open Hardware Multi-KERNAL Cartridge for the Commodore 64.
 
![Board](https://raw.githubusercontent.com/SukkoPera/OpenC64KernalCart/master/doc/render-top.png)
 
### Summary
This project is derived from an old Turbo DOS V3 cartridge with the help of Jani. It allows replacing the [KERNAL (i.e.: operating system)](https://www.c64-wiki.com/wiki/Kernal) of a Commodore C64 computer with one that is stored on an external cartridge.

OpenC64KernalCart is designed to accept a 64 KB (512 Kilobit) (E)EPROM with a 27512-style pinout. Such chips can hold up to 8 KERNAL images, which can then be selected by jumpers. This makes it very easy to switch among KERNALs at will, without the need of opening the C64 every time. The recommended part is Winbond W27C512 (or W27E512, which is widely available, cheap and electrically erasable, which avoids the need for a clunky UV-eraser. This is the only part that was thoroughly tested. Other parts, even smaller in size, will probably work, but will require an ad-hoc configuration.

The only inconvenience is that you will need to open your C64 once, in order to connect a wire to CPU pin 28 (or wherever you can find the HIRAM signal, grab a multimeter and check for continuity here and there). You will need to connect this wire to the header that is provided on the cartridge for full KERNAL replacement. Note that the cartridge will also appear to work even when this wire is not connected, but that will not allow the external KERNAL to have access to the full RAM range of the C64, which will lead to incompatibilities.

Jani has published [a nice article](http://blog.worldofjani.com/?p=3736) on how we developed this cartridge and how it works in detail, so please refer to it for further information.

### Configuration
**IMPORTANT: ALWAYS TURN YOUR C64 OFF BEFORE MOVING THE CONFIGURATION JUMPERS.**
 
When flashing the contents, make sure that every file is exactly 8192 bytes long and just concatenate them. Then use the following table to set the jumper configuration for your image of choice:

| KERNAL Image # | A13 | A14 | A15 |
|----------------|-----|-----|-----|
| 1              |  L  |  L  |  L  |
| 2              |  H  |  L  |  L  |
| 3              |  L  |  H  |  L  |
| 4              |  H  |  H  |  L  |
| 5              |  L  |  L  |  H  |
| 6              |  H  |  L  |  H  |
| 7              |  L  |  H  |  H  |
| 8              |  H  |  H  |  H  |
 
### License
The OpenC64KernalCart documentation, including the design itself, is copyright &copy; SukkoPera 2019.

OpenC64KernalCart is Open Hardware licensed under the [CERN OHL v. 1.2](http://ohwr.org/cernohl).

You may redistribute and modify this documentation under the terms of the CERN OHL v.1.2. This documentation is distributed *as is* and WITHOUT ANY EXPRESS OR IMPLIED WARRANTIES whatsoever with respect to its functionality, operability or use, including, without limitation, any implied warranties OF MERCHANTABILITY, SATISFACTORY QUALITY, FITNESS FOR A PARTICULAR PURPOSE or infringement. We expressly disclaim any liability whatsoever for any direct, indirect, consequential, incidental or special damages, including, without limitation, lost revenues, lost profits, losses resulting from business interruption or loss of data, regardless of the form of action or legal theory under which the liability may be asserted, even if advised of the possibility or likelihood of such damages.

A copy of the full license is included in file [LICENSE.pdf](LICENSE.pdf), please refer to it for applicable conditions. In order to properly deal with its terms, please see file [LICENSE_HOWTO.pdf](LICENSE_HOWTO.pdf).

The contact points for information about manufactured Products (see section 4.2) are listed in file [PRODUCT.md](PRODUCT.md).

Any modifications made by Licensees (see section 3.4.b) shall be recorded in file [CHANGES.md](CHANGES.md).

The Documentation Location of the original project is https://github.com/SukkoPera/OpenC64KernalCart/.

### Support the Project
Since the project is open you are free to get the PCBs made by your preferred manufacturer, however in case you want to support the development, you can order them from PCBWay through this link:

[![PCB from PCBWay](https://www.pcbway.com/project/img/images/frompcbway.png)](https://www.pcbway.com/project/shareproject/OpenC64KernalCart_V1.html)

You get my gratitude and cheap, professionally-made and good quality PCBs, I get some credit that will help with this and [other projects](https://www.pcbway.com/project/member/shareproject/?bmbid=41100). You won't even have to worry about the various PCB options, it's all pre-configured for you!

Also, if you still have to register to that site, [you can use this link](https://www.pcbway.com/setinvite.aspx?inviteid=41100) to get some bonus initial credit (and yield me some more).

Again, if you want to use another manufacturer, feel free to, don't feel obligated :). But then you can buy me a coffee if you want:

<a href='https://ko-fi.com/L3L0U18L' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi2.png?v=2' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>


### Get Help
If you need help or have questions, you can join [the official Telegram group](https://t.me/joinchat/HUHdWBC9J9JnYIrvTYfZmg).

### Thanks
- Jani for involving me into this project.
