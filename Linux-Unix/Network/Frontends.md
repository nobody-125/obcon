### NetworkManager
NetworkManager provides two frontends, `nmtui` and `nmcli`. The text-user interface is intuitive and can be navigated with the keyboard. The command-line interface generally does not need to be used, however, it is useful in providing quick information:
* `nmcli d`: list available devices.
* `nmcli d wifi connect <ssid> password <psk>`: simple way to connect to a network
* `nmcli con delete <ssid>`: forgets a network, useful if for instance, NetworkManager complains that for whatever reason "secrets were required but not provided".
### iNet Wireless Daemon
Can be used in combination with NetworkManager. The daemon must either be enabled or started for `iwd` to work. Running `iwctl` creates a new session in the tty that allows the user to interact with `iwd`.
* The most common name for the device name (at least on laptops) is `wlan0` but it can be listed using `device list`.
* `station wlan0 get-networks`: List all networks in the area
* `station wlan0 connect 'ssid'`: Connect to the network.