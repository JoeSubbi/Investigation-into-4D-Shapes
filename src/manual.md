# User manual 

<!-- Describe how to use your software, if this makes sense for your code. Almost all projects should have at least some instructions on how to run the code. More extensive instructions can be provided here. -->

Building and running the Unity project experiment is described in `readme.md`.

Using the rotor python module in `../data/notebooks/Rotor.py`:
```py
import Rotor

rotor = Rotor.Rotor4() # create a rotor

# create the bivector component to rotate from one vector to another
a = Rotor.Vector4(1, 0, 0, 0)
b = Rotor.Vector4(0, 1, 0, 0)
bv = Rotor.Bivector4.wedge(a, b)

# specify amount to rotate by
angle = 3.14159/2

# Build rotor
rotor.bv_constructor(bv, angle)

# To rotate one rotor by another rotor (redundant in this example)
rotor * Rotor.Rotor4()

# To rotate a vector using the sandwich product
v = Rotor.Vector4(1, 0, 0, 0)
v = rotor.rotate(v)
print(v) # will produce ~ v(0,1,0,0)
```