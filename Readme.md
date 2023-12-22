# Polygon-Operation


Polygon Operation is a project developed for the Algorithmic and Programming II class at UPC.
The objective of this program is to provide an intuitive and easy way of doing different calculus related to polygon geometry from the computer terminal. The entire of Polygon Operation is written in C++.

## Instalation <a name="introduction"></a>

Polygon Operation requires the library [pngwriter](https://github.com/pngwriter/pngwriter) to be installed. Pngwriter is a library for C++ that is used for the creation of images. It’s used here for the creation of polygons graphics.
Install the library:
```bash
git clone https://github.com/pngwriter/pngwriter.git
```
Install the cmake:
```bash
    brew install cmake
```
Install the libpng:
```bash
    brew install libpng
```
Install the freetype:
```bash
    brew install freetype
```

Compile:

```bash
cd pngwriter

cmake -DPNGwriter_USE_FREETYPE=OFF -DCMAKE_INSTALL_PREFIX=$HOME/libs .

make

make install 
```
 
All .png and .txt documents created with the operation will be stored in the code folder. Also, the .txt files loaded must be in the same folder.

Polygon’s Points are given in pairs (first x-coordinate and second y-coordinate) and are real numbers, polygon colors have to be specified in RGB code (three real numbers from 0 to 1). All polygons created are black(0, 0, 0).

All polygons created must be named with a string.

Files name’s have to be introduced in string format and with the .txt extension.

The commands that don't need answer will output "ok" if the process is done correctly.


Functions <a name="functions"></a>

polygon
``` bash
polygon p1 0 0 6 8 3 -2 
ok
``` 

Create or overwrite a polygon with the given points.

print
```bash
print p1 
0.000 0.000 6.000 8.000 3.000 -2.000
```
Print the points of the specified polygon.

vertices
```bash
vertices p1
3
```
Print the number of vertices of the specified polygon.


list
```bash
list
p1 p2 p3
```
Print the names of all polygons.

save
```bash
save s.txt p1 p2 p3
ok
```
Save polygon information to a file.

load
```bash
load s.txt
ok
```
Load polygon information from a file.

draw
```bash
draw p.png p1 p2 p3
ok
```
Create a .png image with a representation of specified polygons.

intersection
```bash
intersection p1 p2 p3
ok
intersection p1 p2
ok
```
Create a polygon from the intersection of specified polygons.

union
```bash
union p1 p2 p3
ok
union p1 p2
ok
```
Create a polygon from the convex union of specified polygons.


inside
```bash
inside p1 p2
ok
```
Check if the first polygon is inside the second.


Algorithms <a name="algorithms"></a>

The program is based on the implementation of the classes Point and ConvexPolygon. The convex hull algorithm used is Andrew's monotone chain.

Other Information <a name="other"></a>

Comments can be written with a # at the beginning of the line. All doubles are printed with a precision of 3 decimals.


This reordered version follows a more structured and organized format, making it easier to read and understand.

