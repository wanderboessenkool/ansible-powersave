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

* laptop_powersave_enable_powertop (Default: True): Whether or not to install ```powertop``` and enable the ```powertop.service``` one-shot tuner.


Contact
-------

Please send any suggestions to <wander.boessenkool@hcs-company.com>, pull requests are also welcomed.
