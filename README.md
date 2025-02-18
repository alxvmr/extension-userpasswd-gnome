# gnome-shell-extension-userpasswd
An extension for GNOME that adds a button to the quick settings menu to run [userpasswd](https://github.com/alxvmr/userpasswd-gnome)

<p align="center">
    <img src="https://psv4.userapi.com/s/v1/d/5RyGCQdjUPb9QaJt0KR8Mug7ymx8OmFjOjGsg7CqfF6d3YPROkOQPxpsrdnmUAeRJNjdR_Uu6zTi6IxGp1v1wzuH6hg7NN-AoEZAXRyZZ2uZjjK5pvmMDQ/IMG_5026.png">
</p>

# Dependencies
```bash
cmake
gcc-c++
gnome-shell >= 47
userpasswd-gnome
```
> [!NOTE]
> userpasswd-gnome is a package that contains userpasswd, which runs when you click on the button (found [there](https://github.com/alxvmr/userpasswd-gnome))

# Build and install
## Local build
Run in the root directory of the project 
```bash
mkdir build
cd build
cmake ..
make
make install
```

## RPM package
The `.spec` file for the project is in the repository:
```bash
.gear/gnome-shell-extension-userpasswd.spec
```

# Start of work
After installing the extension, you need to restart `gnome-shell`:
1. Open the command execution window (`ALT + F2`)
2. Type the command: `restart`

The extension will then appear in the extension manager