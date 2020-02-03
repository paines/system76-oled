# system76-oled

This is a fork of system76-oled to work for Dell XPS 15 7590

Make sure that you have eDP-1 in xrandr for output.
THis should work under Ubuntu, and others if you choose on-demand via nvidia-settings or intel only.
When using nvida, the xrandr output chnages to eDP-1-1. 

For DEBIAN ONLY:
This was tested under Debian Testing (bullseye) with Intel as Primary graphics Card and nVidia as ondemand via  offloading
This can be achieved via and nvidia-drivers (440.xx) pulled from experimental 

Add:
 /usr/share/X11/xorg.conf.d/11-nvidia-offload.conf
 Section "ServerLayout"
    Identifier "layout"
    Option "AllowNVIDIAGPUScreens"
EndSection

