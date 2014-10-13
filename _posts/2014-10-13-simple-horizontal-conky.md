---
layout: post
title: "Simple Horizontal Conky"
description: ""
category: themes 
tags: [conky, xfce]
---
{% include JB/setup %}

I've spent most of day dodging real work by creating and tweaking a Conkyrc.

This configuration gives a nice horizontal bar, showing;

+ CPU usage
+ CPU frequency
+ Memory usage
+ FS usage
+ CPU & HDD tempertures
+ Number of unread emails in my Gmail inbox

Here's how it looks

![Horizontal Conky showing various computer stats]({{site.url}}/assets/images/screenshots/screenshot_131014_conky.png)

Displaying the number of unread emails was achieved using a script found on the [Archwiki](https://wiki.archlinux.org/index.php/conky#Display_number_of_new_emails_.28Gmail.29)

For those interested, here's the contents of my .conkyrc

    alignment top_middle
    background transparent
    border_width 1
    cpu_avg_samples 2
    default_color 88559c 
    default_outline_color 88559c
    default_shade_color 88559c
    draw_borders no
    draw_graph_borders no
    draw_outline no
    draw_shades no
    use_xft yes
    xftfont Source Code Pro Regular:size=8
    gap_x 2 
    gap_y 2 
    minimum_size 5 5
    net_avg_samples 2
    no_buffers no
    out_to_console no
    out_to_stderr no
    extra_newline no
    own_window no
    own_window_class Conky
    own_window_type desktop
    stippled_borders 0
    update_interval 0.5
    uppercase no
    use_spacer none
    show_graph_scale no
    show_graph_range no
    double_buffer yes
    no_buffers yes
    
    TEXT
    ${voffset 3}${cpubar 6,100}${voffset -1}  @ $freq_g Ghz | $mem RAM | ${fs_used_perc /}% ROOT | ${execi 2 sensors | grep Physical | cut -c 18-24} CPU | ${execi 2 hddtemp /dev/sda | cut -c 33-37} HDD | ${execpi 60 ~/bin/gmail.py}

