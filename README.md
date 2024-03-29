# img2video

## Description

This script can be used to create a video slideshow from multiple images.

## Example

The video below was created using the following command:

```console
$ img2video -o example.mp4 -r 640x480 -e random photos/*.jpg
```

All photos (c) 2023 by Harald Lapp, all rights reserved!

[Example Video -- all photos (c) by Harald Lapp](https://github.com/aurora/img2video/assets/304837/e6e4034c-af0f-48fa-a87d-b6d66fe1b154)

## Quick install

```bash
sudo wget -O /usr/local/bin/img2video https://raw.githubusercontent.com/aurora/img2video/master/img2video
sudo chmod a+x /usr/local/bin/img2video
```

## Requirements

* imagemagick *convert*
* ffmpeg

## Usage

```console
$ img2video -o <out-file>.mp4 [arguments] [--] <path-1> [<path-2> ...]
```

### Arguments

    -o, --output        Name of output file. Required parameter.
    -r, --resolution    Output resolution.
                        Defaults to: 1920x1080.
    -d, --duration      Duration to display the image between the transition.
                        Defaults to: 5.
    -t, --transition    Time of the transition between two images.
                        Defaults to: 3.
    -e, --effect        Transition effect to use. Can be specified multiple times.
                        Defaults to: fade.
    -h, --help          Display this usage information.
        --version       Show version and exit.

### Possible effects

This script uses *xfade* for transition of images.

* random

The effect *random* is a pseudo-effect that selects a random xfade filter effect and ensures that an effect is not repeated directly. The following is a list of currently available xfade transition effects:

* circleclose
* circlecrop
* circleopen
* diagbl
* diagbr
* diagtl
* diagtr
* dissolve
* distance
* fade
* fadeblack
* fadegrays
* fadewhite
* hblur
* hlslice
* horzclose
* horzopen
* hrslice
* pixelize
* radial
* rectcrop
* slidedown
* slideleft
* slideright
* slideup
* smoothdown
* smoothleft
* smoothright
* smoothup
* squeezeh
* squeezev
* vdslice
* vertclose
* vertopen
* vuslice
* wipebl
* wipebr
* wipedown
* wipeleft
* wiperight
* wipetl
* wipetr
* wipeup
* zoomin

## Disclaimer

Use with caution. This software may contain serious bugs. I can not be made responsible for
any damage the software may cause to your system or files.

## [License](LICENSE)

img2video

Copyright (C) 2024-present by Harald Lapp <harald@octris.org>

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see <http://www.gnu.org/licenses/>.
