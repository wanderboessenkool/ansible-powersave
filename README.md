laptop_powersave
================

Basic extra powersaving steps for a laptop running Fedora

This role configures powersaving for:
* Generic USB devices
* Genreic PCI devices
* Intel i915 graphic
* Intel snd_hda_intel audio
* Powertop service
* Tuned profiles

Variables
---------

The following variables can be set to influence the roles behaviour:

* ```laptop_powersave_enable_powertop``` (Default: True): Whether or not to install ```powertop``` and enable the ```powertop.service``` one-shot tuner.

* ```laptop_powersave_enable_tuned`` (Default: True): Enable or disable ```tuned.service```

* ```laptop_powersave_tuned_profile`` (Default: ```powersave```): Which ```tuned``` profile to activate.

* ```laptop_powersave_i915_tuning``` (Default: True): Enable module options for intel graphics cards.

* ```laptop_powersave_snd_hda_intel_tuning``` (Default: True): Enable module options for Intel HD Audio kernel module

* ```laptop_powersave_enable_usb_powersave``` (Default: True): Enable generic USB powersaving using ```udev``` rules.

* ```laptop_powersave_enable_pci_powersave``` (Default: True): Enable generic PCI powersaving using ```udev``` rules.

* ```laptop_powersave_usb_excludes```: Exclude certain USB devices from generic powersaving, useful for things like bluetooth adapters and network cards. The syntax is a list of dictionaries using ```vendor``` and ```product``` keys. For example:
```
laptop_powersave_usb_excludes:
  - {vendor: '0cf3', product: 'e300'}
  - {vendor: '0bda', product: '8153'}
```

Contact
-------

Please send any suggestions to <wander.boessenkool@hcs-company.com>, pull requests are also welcomed.
