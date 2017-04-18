# WiFi Range Extender Config

Copy the `etc/config/firewall` to the same path on your Omega - replacing the original - to set up your Omega as a range extender. Run `/etc/init.d/firewall restart` for it to take effect.

tl;dr - change this bit:
```
config zone
	option name 'wan'
	option output 'ACCEPT'
	option forward 'REJECT'
	option masq '1'
	option mtu_fix '1'
	option network 'wwan'
	option input 'ACCEPT'
```

to make sure that:

```
	option output 'ACCEPT'
	option input 'ACCEPT'
	option input 'ACCEPT'
```
