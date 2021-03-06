---
title: Releasing a Mod
layout: default
root: ../../
---

## Introduction

In this chapter we will find out how to publish a mod so that other users can use it.

* License Choices
* Packaging
* Uploading
* Forum Topic

### Before you release your mod, there are some things to think about:

* Is there another mod that does the same thing? If so, how does yours differ or improve on it?
* Is your mod useful?

## License Choices

You need to specify a license for your mod.
**Public domain is not a valid licence**, as the definition varies in different countries.

First thing you need to note is that your code and your art need different things from
the license they use. Creative Commons licenses shouldn't be used with source code,
but rather with artistic works such as images, text and meshes.

You are allowed any license, however mods which disallow derivatives are banned from the forum.
(Other developers must be able to take your mod, modify it, and release it again.)

### LGPL and CC-BY-SA

This is a common license combination in the Minetest community, as it is what
Minetest and minetest_game use.
You license your code under LGPL 2.1 and your art under CC-BY-SA.

* Anyone can modify, redistribute and sell modified or unmodified versions.
* If someone modifies your mod, they must give their version the same license.
* Your copyright notice must be kept.

Add this copyright notice to your README.txt, or as a new file called LICENSE.txt

    License for Code
    ----------------

    Copyright (C) 2010-2013 Your Name <emailaddress>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU Lesser General Public License as published by
    the Free Software Foundation; either version 2.1 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU Lesser General Public License for more details.

    You should have received a copy of the GNU Lesser General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

    License for Textures, Models and Sounds
    ---------------------------------------

    CC-BY-SA 3.0 UNPORTED. Created by Your Name

### WTFPL or CC0

These licenses allows anyone to do what they want with your mod.
Modify, redistribute, sell, leave out attribution.
They can be used for both code and art.

## Packaging

There are some files that we recommend you include in your mod
when you release it.

### README.txt

You should provide a readme file. This should state:

* What the mod does.
* What the license is.
* Current version of mod.
* How to install the mod.
* What dependencies there are / what the user needs to install.
* Where to report problems/bugs or get help.

See appendix for an example and a generator

### description.txt

Write a sentence or two explaining what your mod does.
Be concise without being too vague. This is displayed in the mod store.

For example:

    GOOD: Adds soups, cakes, bakes and juices. The food mod which supports the most ingredients.
    BAD:  The food mod for Minetest.

### screenshot.png

Screenshots should be 3:2 (3 pixels of width for every 2 pixels of height)
and a [minimum size of 300 x 200px](https://github.com/minetest/minetest/issues/2874).
This is displayed in the mod store.



Uploading
---------

In order for a potential user to download your mod, you need to upload it to somewhere
which is publicly accessible.\\
I will outline several methods you can use, but really you should use the one that works
best for you, as long as it mets these requirements:\\
(and any other requirements which may be added by forum moderators)

* **Stable**      - the hosting website should not just shutdown randomly.
* **Direct link** - you should be able to click a link on the forum and download the file,
                   without having to view another page.
* **Virus Free**  - pretty obvious.

### Github, or another VCS

It is recommended that you use a Version Control System for the following reasons:

* Allows other developers to submit changes (easily).
* Allows the code to be previewed before downloading.
* Allows users to submit bug reports.

However, such systems may be hard to understand when you first start out.

The majority of Minetest developers use GitHub as a website to host their code,
however that doesn't matter that much.

* [Using Git](http://git-scm.com/book/en/v1/Getting-Started) - Basic concepts. Using the command line.
* [GitHub for Windows](https://help.github.com/articles/getting-started-with-github-for-windows/) - Use a graphical interface on Windows to upload your code.

### Forum Attachments

You could use forum attachments instead.
This is done when creating a mod's topic - covered below.

First, you need to zip the files into a single file. This varies from operating system to operating system.

On Windows, go to the mod's folder. Select all the files. Right click, Send To > Compressed (zipped) folder.
Rename the resulting zip file to the name of your modfolder.

On the create a topic page, see below, go to the "Upload Attachment" tab at the bottom.
Click browse and select the zipped file. I suggest that you enter the version of your mod in the comment field.

<figure>
    <img src="{{ page.root }}/static/releasing_attachments.png" alt="Upload Attachment">
    <figcaption>
        Upload Attachment tab.
    </figcaption>
</figure>

## Forum Topic

You can now create a forum topic. You should create it in
the ["WIP Mods"](https://forum.minetest.net/viewforum.php?f=9) (Work In Progress)
forum.\\
When you consider your mod no longer a work in progress, you can
[request that it be moved](https://forum.minetest.net/viewtopic.php?f=11&t=10418)
to "Mod Releases."

### Content

The requirements of a forum topic are mostly the same as what is recommended for a README.txt

* What the mod does.
* What the license is.
* Current version of mod.
* How to install the mod.
* What dependencies there are.
* Where to report problems/bugs or get help.
* Link to download, or an attachment.

You should also include screenshots of your mod in action, if relevant.

Here is an example. The Minetest forum uses bbcode for formating.


    Adds magic, rainbows and other special things.

    See download attached.

    [b]Version:[/b] 1.1
    [b]License:[/b] LGPL 2.1 or later

    Dependencies: default mod (found in minetest_game)

    Report bugs or request help on the forum topic.

    [h]Installation[/h]

    Unzip the archive, rename the folder to to modfoldername and
    place it in minetest/mods/minetest/

    (  GNU/Linux: If you use a system-wide installation place
        it in ~/.minetest/mods/minetest/.  )

    (  If you only want this to be used in a single world, place
        the folder in worldmods/ in your worlddirectory.  )

    For further information or help see:
    [url]http://wiki.minetest.com/wiki/Installing_Mods[/url]

If you modify the above example for your mod topic, remember to
change "modfldername" to the name of the folder your mod should be
in.

### Title

Subject of topic must be in one of these formats:

* [Mod] Mod Title [modname]
* [Mod] Mod Title [version number] [modname]
* eg: [Mod] More Blox [0.1] [moreblox]

### Profit

<figure>
    <img src="{{ page.root }}/static/releasing_profit.png" alt="Profit">
    <figcaption style="display:none;">
        Profit
    </figcaption>
</figure>

## Appendix: Readme and Forum Generator

<noscript>
    <p>Javascript is required for this section!</p>
</noscript>

Title: <input id="t_title" value="My Super Special Mod"><br />
Modname: <input id="t_name" value="mysuperspecial"><br />
Description: <input id="t_desc" value="Adds magic, rainbows and other special things."><br />
Version: <input id="t_version" value="1.1"><br />
License: <input id="t_license" value="LGPL 2.1 or later"><br />
Dependencies: <input id="t_dep" value="default mod (found in minetest_game)"><br />
Download: <input id="t_download" value="http://example.com/download.zip"><br />
Additional:<br />
<textarea id="t_add">Report bugs or request help on the forum topic.</textarea><br />

<pre><code id="readme">My Super Special Mod
====================

Adds magic, rainbows and other special things.

Version: 1.1
License: LGPL 2.1 or later
Dependencies: default mod (found in minetest_game)

Report bugs or request help on the forum topic.

Installation
------------

Unzip the archive, rename the folder to mysuperspecial and
place it in minetest/mods/

(  GNU/Linux: If you use a system-wide installation place
    it in ~/.minetest/mods/.  )

(  If you only want this to be used in a single world, place
    the folder in worldmods/ in your worlddirectory.  )

For further information or help see:
http://wiki.minetest.com/wiki/Installing_Mods</code></pre>

<pre><code id="forum">Adds magic, rainbows and other special things.

[b]Version:[/b] 1.1
[b]License:[/b] LGPL 2.1 or later
[b]Dependencies:[/b] default mod (found in minetest_game)
[b]Download:[/b] http://example.com/download.zip

Report bugs or request help on the forum topic.

[h]Installation[/h]

Unzip the archive, rename the folder to mysuperspecial and
place it in minetest/mods/

(  GNU/Linux: If you use a system-wide installation place
    it in ~/.minetest/mods/.  )

(  If you only want this to be used in a single world, place
    the folder in worldmods/ in your worlddirectory.  )

For further information or help see:
http://wiki.minetest.com/wiki/Installing_Mods</code></pre>

<script src="http://blog.rubenwardy.com/static/jquery.min.js"></script>
<script>function regen() {
    var title = $("#t_title").val();
    var name = $("#t_name").val();
    var desc = $("#t_desc").val();
    var version = $("#t_version").val();
    var license = $("#t_license").val();
    var dep = $("#t_dep").val();
    var add = $("#t_add").val();

    var download = $("#t_download").val();

    {
        var res = ((title.length > 0) ? title : name) + "\n";
        var header_count = res.length - 1;
        for (var i = 0; i < header_count; i++) {
            res += "=";
        }
        res += "\n\n";

        res += desc + "\n\n";

        if (version != "") {
            res += "Version: " + version + "\n";
        }

        res += "License: " + license + "\n";
        res += "Dependencies: " + dep + "\n\n";

        if (add != "") {
            res += add + "\n\n";
        }

        res += "Installation\n------------\n\nUnzip the archive, rename the folder to ";
        res += name + " and\nplace it in minetest/mods/\n\n";

        res += "(  GNU/Linux: If you use a system-wide installation place\n" +
            "\tit in ~/.minetest/mods/.  )\n\n" +
            "(  If you only want this to be used in a single world, place\n" +
            "\tthe folder in worldmods/ in your worlddirectory.  )\n\n" +
            "For further information or help see:\n" +
            "http://wiki.minetest.com/wiki/Installing_Mods\n";

        $("#readme").text(res);
    }

    {
        var res = desc + "\n\n";

        if (version != "") {
            res += "[b]Version:[/b] " + version + "\n";
        }

        res += "[b]License:[/b] " + license + "\n";
        res += "[b]Dependencies:[/b] " + dep + "\n";

        res += "[b]Download:[/b] " + download + "\n\n";

        if (add != "") {
            res += add + "\n\n";
        }

        res += "[h]Installation[/h]\n\nUnzip the archive, rename the folder to ";
        res += name + " and\nplace it in minetest/mods/\n\n";

        res += "(  GNU/Linux: If you use a system-wide installation place\n" +
            "\tit in ~/.minetest/mods/.  )\n\n" +
            "(  If you only want this to be used in a single world, place\n" +
            "\tthe folder in worldmods/ in your worlddirectory.  )\n\n" +
            "For further information or help see:\n" +
            "http://wiki.minetest.com/wiki/Installing_Mods\n";

        $("#forum").text(res);
    }
}

$(function() {
    jQuery('input').on('input propertychange paste', regen);
    jQuery('textarea').on('input propertychange paste', regen);
});
</script>
