[![MIT License](https://raw.githubusercontent.com/c3woc/divoc-animation/main/.github/license.svg?sanitize=true)](https://github.com/c3woc/divoc-animation/blob/main/LICENSE)

C3WOC DiVOC Animation
========================

Visit [di.c3voc.de](https://di.c3voc.de) for more information about DiVOC.


 Tipps and Tricks
------------------

### Turn SVG into PNG
```
for i in *.svg
do
    echo "Transform Image: $i"
    inkscape \
    --actions="export-filename:$i.png; export-do;"\
    --export-dpi 96 \
    --export-background white \
    $i
done
```

### Turn PNG to MP4
```
ffmpeg -framerate 24 \
  -pattern_type glob -i '*.png' \
  -c:v libx264  -preset slow \
  -crf 22 -pix_fmt yuv420p \
  result.mp4
```

### Turn PNG into webm with alpha channel
```
ffmpeg -framerate 24 \
  -pattern_type glob -i '*.png' \
  -pix_fmt yuva420p \
  result.webm
```

 License
---------
License for the original [DiVOC Artwork](https://di.c3voc.de/hiddenservice:artwork):
```
alles cool, aber steck dir keine Bohnen in die Ohren
```

License for the animation, assets etc.

[MIT License](LICENSE)
```
Copyright (c) 2021 L3D <l3d@c3woc.de>
```
