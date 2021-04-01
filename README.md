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

 License
---------
License for the original [DiVOC Artwork](https://di.c3voc.de/hiddenservice:artwork):
```
alles cool, aber steck dir keine Bohnen in die Ohren
```

License for the animation, assets etc.

[MIT License](LICENCE)
```
Copyright (c) 2021 L3D <l3d@c3woc.de>
```
