# AyeBIOS
#### Localized source code of an open source BIOS (as per the license) derived from [SeaBIOS](https://github.com/qemu/seabios)
#### The localized source code has been created using [Hindawi Programming System](https://hindawiai.github.io)


### NOTICE
All copyrights and notices in the original source code are available under the "upstream" branch.

The Hindawi ported versions are binary deliverables delivered along with sources under the "upstream" branch.
Under jurisdictions where the translator has copyright over original translation, the Hindawi ported version
must include the additional copyright notices even if not explicitly mentioned in the original or derivative
source code files.

Copyright (C) 2021 Abhishek Choudhary

The license terms for all derivatives shall be under AyeAI Singularity Public License latest version, unless
impunged by any of the terms of the original license. These artifacts, text, source code or other deliverables
are provided AS IS, with NO WARRANTY and NO LIABILITY. These artifacts, text or source code MUST NOT BE USED
for any business critical or safety critical systems.

In case any of the terms of this license stands defective, it shall have no implication on the licensing terms
and conditions of the original source code from which these have been derived.

AyeAI, AyeAM, Hindawi Programming System, AyeBIOS are trademarks or registered trademarks of Abhishek Choudhary. 
All other trademarks are acknowledged as belonging to their respective owners.

All disputes are subject to courts in Hyderabad, Telangana, India only.

#### /NOTICE

#### From the original README
Welcome to the SeaBIOS project!  This project implements an X86 legacy
bios that is built with standard GNU tools.

Please see build and developer information at:

  http://seabios.org/Developer_Documentation

For the impatient, SeaBIOS is built for QEMU and tested on QEMU with:

  make
  qemu -bios out/bios.bin

SeaBIOS can be configured with kconfig.  To change the default
configuration one can run "make menuconfig" prior to running "make".

For other types of builds, and for more detailed developer
documentation, please see the online documentation listed above.
