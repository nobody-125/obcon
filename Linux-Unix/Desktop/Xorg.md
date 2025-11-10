## libinput
libinput is a library to handle input devices in [Wayland](http://wayland.freedesktop.org) compositors and to provide a generic [X.Org](http://x.org) input driver. It provides device detection, device handling, input device event processing and abstraction so minimize the amount of custom input code compositors need to provide the common set of functionality that users expect.
##### Touchpad Config
Located at ``/etc/X11/xorg.conf.d/30-touchpad.conf:``
![[Pasted image 20251026122901.png]]
Possible configurations within this configuration include:
* ``Option "NaturalScrolling" "bool"``
* ``Option "HorizontalScrolling" "bool"
* ``Option "Tapping" "bool"
More configurations are available at ``man libinput.4``
## xinitrc
Located in the home directory (``~/.xinitrc``). The sample configuration is located in ``/etc/X11/xinit/xinitrc``.