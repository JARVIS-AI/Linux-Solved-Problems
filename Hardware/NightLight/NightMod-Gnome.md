# Night Light Mod (Night Mod) in Gnome

As maybe some of you know after installing OS (Mine is Arch) and get gnome on your laptop there is feature named night light in gnoem and make your laptop screen warmer to help your eyes.
But after some days or some work in your OS the night light (Night Mod) doesn't work any more.

In this article I want to show you some solutions.

## What is this feature ?

This option is in Gnome Settings -> Devices -> Display -> Night Light

## Some Info

This feature work with the package named Color Management. This mechanism identified your screen and do night mod - cold color - warm color - white color - negative - and so on.
There is command in Linux OS :

```sh
$ colormgr --help
```
<style>
  .img img {
    width: auto;
    position: relative;
    -webkit-filter: drop-shadow(5px 5px 5px #222);
    filter: drop-shadow(5px 5px 5px #222);
}

..img:before,
.img:after {
    z-index: -1;
    position: absolute;
    content: "";
    bottom: 25px;
    left: 10px;
    width: 50%;
    top: 80%;
    max-width: 300px;
    background: #777;
    -webkit-box-shadow: 0 35px 20px #777;
    -moz-box-shadow: 0 35px 20px #777;
    box-shadow: 0 35px 20px #777;
    -webkit-transform: rotate(-8deg);
    -moz-transform: rotate(-8deg);
    -o-transform: rotate(-8deg);
    -ms-transform: rotate(-8deg);
    transform: rotate(-8deg);
}

.img:after {
    -webkit-transform: rotate(8deg);
    -moz-transform: rotate(8deg);
    -o-transform: rotate(8deg);
    -ms-transform: rotate(8deg);
    transform: rotate(8deg);
    right: 10px;
    left: auto;
}
</style>

<div class="img" style="align:center;">
  	<img src="img/1.png">
</div>

