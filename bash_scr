#!/bin/bash
exec > my_image.png
echo "P3 250 250 255"
for ((y=0; y<250; y++)) {
  for ((x=0; x<250; x++)) {
    echo "$((x^y)) $((x^y)) $((x|y))"
  }
}
DIR=$(stat -c '%x' $1 | cut -f 1 -d ' ')
mkdir -p $DIR
mv $1 $DIR/
