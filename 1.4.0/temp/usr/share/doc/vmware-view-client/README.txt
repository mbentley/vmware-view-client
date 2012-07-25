VMware View Client 1.4.0
Build 639205, 2012-03-01

VMware is a registered trademark or trademark (the "Marks") of VMware, Inc.
in the United States and/or other jurisdictions and is not licensed to you
under the terms of the LGPL version 2.1. If you distribute VMware View Open
Client unmodified in either binary or source form or the accompanying
documentation unmodified, you may not remove, change, alter or otherwise
modify the Marks in any manner. If you make minor modifications to VMware
View Open Client or the accompanying documentation, you may, but are not
required to, continue to distribute the unaltered Marks with your binary or
source distributions. If you make major functional changes to VMware View
Open Client or the accompanying documentation, you may not distribute the
Marks with your binary or source distribution and you must remove all
references to the Marks contained in your distribution. All other use or
distribution of the Marks requires the prior written consent of VMware.
All other marks and names mentioned herein may be trademarks of their
respective companies.

Copyright (C) 1998-2012 VMware, Inc. All rights reserved. VMware
software products are protected by one or more U.S. Patent Numbers
6,075,938, 6,397,242, 6,496,847, 6,704,925, 6,711,672, 6,725,289,
6,735,601, 6,785,886, 6,789,156, 6,795,966, 6,880,022, 6,944,699,
6,961,806, 6,961,941, 7,069,413, 7,082,598, 7,089,377, 7,111,086,
7,111,145, 7,117,481, 7,149,843, 7,155,558, 7,222,221, 7,260,815,
7,260,820, 7,269,683, 7,275,136, 7,277,998, 7,277,999, 7,278,030,
7,281,102, 7,290,253, 7,343,599, 7,356,679, 7,409,487, 7,412,492,
7,412,702, 7,424,710, 7,428,636, 7,433,951, 7,434,002, 7,447,854,
7,475,002, 7,478,173, 7,478,180, 7,478,218, 7,478,388, 7,484,208,
7,487,313, 7,487,314, 7,490,216, 7,500,048, 7,506,122, 7,516,453,
7,529,897, 7,555,747, 7,577,722, 7,581,064, 7,590,982, 7,594,111,
7,596,594, 7,603,704, 7,606,868, 7,620,766, 7,620,955, 7,624,240,
7,636,831, 7,657,659, 7,657,937, 7,665,088, 7,680,919, 7,693,996,
7,694,101; patents pending.


WELCOME
-------

Welcome to the release of VMware View Client 1.4.0.

For VMware View partners, official builds of VMware View Client are
available through VMware Partner Engineering. If you don't feel
you can use an official build, perhaps because you are targeting a
processor architecture other than x86 or have functional requirements
that don't fit with our official build, we hope that the open source
release will help you produce a custom client. Whether you are using
an official build, a client derived from the View Open Client sources,
or a client written from scratch, contact Partner Engineering to
certify your product as View compatible.

VMware View Client is optimized for thin client devices: the
installed disk footprint is less than two megabytes, it has minimal
RAM requirements, and it has only a few library dependencies.

For more details on the features and capabilities of this client, please
refer to the end user documentation and the administrator's guide, both
of which are available in the installation package.

For system requirements, compilation, installation, and configuration
instructions, known and resolved issues, and troubleshooting tips,
please consult the wiki at the Google Code site for the open-source
project:

http://code.google.com/p/vmware-view-open-client/w/list


CONTACT
-------

Contact information is available at the Google Code site for the
open-source project:

http://code.google.com/p/vmware-view-open-client/


SUPPORT
-------

At the time of this release, official builds of VMware View Client for
Linux are only available through certified partners. Support is
available through them. A list of certified partners can be found on
vmware.com.

Official builds have the text, "VMware View," while versions based on 
the source release have the text, "VMware View Open Client."

Informal support for the source distribution may be found at:

http://code.google.com/p/vmware-view-open-client/


OPEN SOURCE
-----------

VMware View Client includes software which may be covered
under one or more open source agreements. For more information please
see the open_source_licenses.txt file located in the doc directory.

KNOWN ISSUES IN THIS RELEASE
----------------------------

*) When configuring for client-side caching you need to include spaces 
before and after the '=' symbol. For example:
   pcoip.image_cache_size_mb = 50

*) When configuring for FIPS, you need to include spaces before and after
the '=' symbol. For example:
   pcoip.enable_fips_mode = 1

*) When using the --kioskLogin option and if the pre-login message is enabled,
the user will have to acknowledge the message before he can access the desktop.
To avoid having the user do this, disable pre-login messages.

*) When using the --kioskLogin option if the user were to log off or disconnect
from the desktop session, the client will return to the desktop selector screen.
To avoid that, use the --once option to exit the client. Use an external script
file to relaunch the View client.

*) When using the --once option in kiosk mode (--kioskLogin), the client will
not exit if the login failed.

*) The client will automatically connect to a desktop if the -n command line
option is used together with the following config file options:
   view.autoConnectBroker = "TRUE"
   view.autoConnectDesktop = "FALSE"
   
*) Audio out on the Pandaboard does not work when using the RDP protocol. This is
a known issue with Ubuntu: https://wiki.ubuntu.com/ARM/MaverickReleaseNotes



