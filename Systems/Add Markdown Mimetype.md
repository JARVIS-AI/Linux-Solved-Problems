# Add MD mime-type to set of mimes and give it a icon

If your OS dont have any mime type for markdown files (.markdown and .md) do the following :

## Let us start

At first prepare some icon for this kind of files
Second :

```sh
$ ls /usr/share/icons/PACKAGENAMEICONS
```

and put the icon in there.

#### Table for add mime type to file in OS

|                   Path                   |             Usage              |
| :--------------------------------------: | :----------------------------: |
|        `~/.config/mimeapps.list`         |         user overrides         |
|         `/etc/xdg/mimeapps.list`         |     system-wide overrides      |
| `~/.local/share/applications/mimeapps.list` |  (deprecated) user overrides   |
| `/usr/local/share/applications/mimeapps.list` </br> `/usr/share/applications/mimeapps.list` | distribution-provided defaults |



These are location of mimelist that you must add this :

**`text/markdown`** to the file.



After you login or reboot.

You will see your markdown documents in your prepared icon for it.

But One note : The name of that icon must be **text-x-markdown.svg**.



## Thanks

Thank you again for follow one of our other solving tut.
If our solving is useful for you come and give me a star, its like a cup of coffee. :)
Thanks.
