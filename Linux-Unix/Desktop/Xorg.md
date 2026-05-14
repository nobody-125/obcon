## libinput & libusb
libinput is a library to handle input devices in [Wayland](http://wayland.freedesktop.org) compositors and to provide a generic [X.Org](http://x.org) input driver. It provides device detection, device handling, input device event processing and abstraction so minimize the amount of custom input code compositors need to provide the common set of functionality that users expect.
##### Touchpad Config
Located at ``/etc/X11/xorg.conf.d/30-touchpad.conf:``
![[Pasted image 20251026122901.png]]
Possible configurations within this configuration include:
* ``Option "NaturalScrolling" "bool"``
* ``Option "HorizontalScrolling" "bool"
* ``Option "Tapping" "bool"
More configurations are available at ``man libinput.4``

##### Soarer's Converter
Configuration details so I can remember how to set up devices in the future. 
- As of this guide, the version required is Soarer_Converter_1.10.zip on [GH](https://geekhack.org/index.php?topic=17458.0).
- You will need ``lib32-libusb`` and ``lib32-libusb-compat`` (the latter is an AUR package, that still exists as of 2026)
- Within the **docs** folder, scan codes can be identified. Documentation on how to write a ``config.sc`` file can be found online, but is also available in the docs provided by Soarer in the file.
- Once you are satisfied with the configuration file, enter the directory with the linux tools (must be unzipped first), and then run ``./scas config.sc compiled_config_name.scb``.
- Write the changes using ``./scwr compiled_config_name.scb``. Hot-plugging the device post-write may be required for the changes to get the keyboard unstuck.
## xinitrc
Located in the home directory (``~/.xinitrc``). The sample configuration is located in ``/etc/X11/xinit/xinitrc``.
