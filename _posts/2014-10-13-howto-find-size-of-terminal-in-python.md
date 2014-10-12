---
layout: post
title: "HOWTO: Find size of terminal in Python"
description: ""
category: coding
tags: [python]
---
{% include JB/setup %}
This small code snippet show how to find the number of rows and columns in your Python terminal.

    import os
    rows, columns = os.popen('stty size', 'r').read().split()

This can be particularly useful when printing menus or similar in a console application. It allows you to easily print a line across the entire length of your terminal, without having to worry about overlap. Be careful though, in the above snippet, rows and columns are strings, hence in the example below, columns is converted to a integer first.

    print("-"*int(columns))
