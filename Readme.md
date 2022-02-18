# Information on the stl file
## MM 804 - Graphics and Animations

# Download the required packages in your local system with the given commands.

pip install -r requirements.txt

Downloaded the 3D model from https://www.thingiverse.com/thing:5167431

# Information on the stl file

Name: House_Tower_Gate.stl
Size: 50.7 MB or 50,672,934 bytes
Type: STL
Vertex Count for Original Model: 505,873
Vertex Count for Clipped Out Part of Model: 308,009
Vertex Count for Remaining Part of Model: 203,324
Vertex Count for Intersection part of the Model: 2775

## VTK version

vtk==9.1.0


## Setup on Mac and Windows

1. Install Python3 version 3.8.8

   Refer the webiste https://docs.python-guide.org/starting/install3/osx/)

2. Install the requirements package

   pip install -r requirements.txt

3. Run the Script

   python visualizer.py

## Run Through Code
``` shell
 
read_stl = vtk.vtkSTLReader()   # Here we will Read input file vtkSTLReader()
read_stl.SetFileName("House_Tower_Gate.stl")
read_stl_mapper = vtk.vtkPolyDataMapper()  # We Create PolyMapper for the stl and send to output port.

``` shell

stl_Plane = vtk.vtkPlane() # Now we create a plane with origin as center of stl data and set normal
stl_Plane.SetOrigin(stl_Center)
stl_Plane.SetNormal(1, 0, 1) 
stl_Clipper = vtk.vtkClipPolyData() # Create a clipper to clip the object/data using ClipPolyData()
stl_Clipper.SetInputConnection(stl_Normals.GetOutputPort())
```


## OutPut

### First Angle Output
![Screenshot](Result.png)

### Second Angle Output
![Screenshot](Res1.png)


### Third Angle Output
![Screenshot](Res2.png)


### Fourth Angle Output
![Screenshot](Res3.png)


