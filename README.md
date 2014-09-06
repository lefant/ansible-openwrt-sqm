openwrt-sqm
===========

traffic shaping config of your openwrt based cerowrt system.

this role currently only works with cerowrt.

look at the following pages for details on configuration:
[https://www.bufferbloat.net/projects/cerowrt/wiki/Setting_up_SQM_for_CeroWrt_310]

for vanilla openwrt you may want to start looking here:
[http://wiki.openwrt.org/doc/uci/qos]

Role Variables
--------------

there is a nested dict `sqm` containing keys for `device` and
`settings.upload` and `settings.download`. find suitable values using
the link above. you *must* adjust them to your local environment for
good results.

you may want to consider `hash_behaviour=merge` in your ansible.cfg

Dependencies
------------

[lefant.openwrt-uci]

Example Playbook
----------------

[https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml]

Requirements
------------

must be kept minimal as this is supposed to run on openwrt embedded
systems. in particular we try get by with plain POSIX shell, using
neither python nor bash in any way. lua could be an option as that
seems to be the openwrt scripting language of choice.

this role will only work with the cerowrt flavour of openwrt.

License
-------

BSD

Author Information
------------------

Fabian Linzberger, [http://e.lefant.net/]



[https://www.bufferbloat.net/projects/cerowrt/wiki/Setting_up_SQM_for_CeroWrt_310]: https://www.bufferbloat.net/projects/cerowrt/wiki/Setting_up_SQM_for_CeroWrt_310
[http://wiki.openwrt.org/doc/uci/qos]: http://wiki.openwrt.org/doc/uci/qos
[https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml]: https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml
[http://wiki.openwrt.org/doc/uci/firewall]: http://wiki.openwrt.org/doc/uci/firewall
[lefant.openwrt-uci]: https://galaxy.ansible.com/list#/roles/1645
[http://e.lefant.net/]: http://e.lefant.net/
