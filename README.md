i3status-keyboard-leds
======================

A python wrapper for i3status adding current status of keyboard leds (Caps lock, Num lock, etc...)

This wrapper is the result of [this thread](https://faq.i3wm.org/question/1258/i3bari3status-is-it-possible-to-have-caps-lock-and-num-lock-indicator/).
Special thanks to the persons who have participated to this thread.

The script contains an experimental support for the Scroll Lock key for Microsoft Natural keyboard 4000. 

The resulting bar should look like this (green arrow):
![i3bar](https://raw.github.com/syl20bnr/i3status-keyboard-leds/master/i3bar.png)

Install
---------

In a terminal:

    git clone http://github.com/syl20bnr/i3status-keyboard-leds
    cd i3status-keyboard-leds
    sudo ln -s /home/foo/bar/i3status-keyboard-leds/i3status+.py /usr/local/bin/i3status+

In your ~/.i3/config replace the call to i3status by i3status+

    # Start i3bar to display a workspace bar (plus the system information i3status
    # finds out, if available)
    bar {
        status_command    i3status+
        position          bottom
        mode              dock
        workspace_buttons yes
        tray_output       primary
        colors {
            background #000000
            statusline #999999
            focused_workspace  #ffffff #285577
            active_workspace   #ffffff #333333
            inactive_workspace #888888 #222222
            urgent_workspace   #ffffff #900000
        }
    }

