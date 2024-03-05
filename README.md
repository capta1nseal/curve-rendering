# curve-rendering
Experiments in rendering curves

## project status
This project is currently in the planning phase.

If you came here expecting something, sorry to let you down. Don't worry though! A timeline has been created and it won't be long before there's something to get your hands on.

You should get involved if interested. see contributing.

### planned end product
The end product for this project won't be the next big piece of interactive software you'd be proud to put on your CV.

The goal is to learn, and to make something fun in the process.

With that out of the way, let's get into stuff the end product will have:
- neat, well-documented code
- a modern graphics pipeline
- clean, interactive visuals
- reference materials for anyone hoping to render curves of any type for any purpose


#### development environment
Primarily developed in visual studio code on linux. see contributing if your development platform is not linux.

Systems built upon are C++ with Vulkan with an SDL2 context.
- C++ because it is fast, modern and I (capta1nseal) am already familiar.
- SDL2 solely for vulkan context and inputs.
- Vulkan for a modern graphics pipeline and shaders (and later down the line compute shaders).
  - side note, shaders are written in GLSL then compiled to SPIRV for Vulkan.

Build using g++ and make. ```build-essential``` recommended.

Everything is currently statically linked, subject to change as the project grows.

TO DOCUMENT: GLM if it ends up being used.

Required libraries on include path:
- ```libSDL2-dev```
- ```vulkan-tools```
- ```libvulkan-dev```
- ```vulkan-validationlayers-dev```
- ```spirv-tools```

apt:
```
sudo apt install build-essential libSDL2-dev vulkan-tools libvulkan-dev vulkan-validationlayers-dev spirv-tools
```
TO DOCUMENT: installing build tools and sdl2 with dnf or pacman. Should be very easy to find online, if not already installed.
dnf:
```
sudo dnf install vulkan-tools vulkan-loader-devel mesa-vulkan-devel vulkan-validation-layers-devel
```
pacman:
```
sudo pacman -S vulkan-devel
```

Once functionality is implemented, a github actions workflow will be implemented to build and distribute the project online.

##### contributing
In case you wish to contribute, the best way to do so is to create an issue for discussion, or fork and create a pull request preferably including an email address, discord, telegram or other simple means of communication. No changes are necessary at that point, in fact communicating beforehand is preferable. Chances are, your hypothetical changes will conflict with something already being worked on. Save yourself the trouble and get in touch first :)

The aim of the project is to be as approachable as possible, but currently building on or for a platform other than linux has not been done or documented.

If you want to help expand this project's out-of-box ease-of-use to other platforms, contributions are greatly appreciated.

Document your changes as well as possible, because PRs containing anything mysterious will not be approved. Don't worry about strict standards though, just try to stick to what you observe already present elsewhere.

If you personally dislike the programming paradigms used here of appearing like object-oriented programming, yet only ever instancing most classes once: that's valid. However, in the interests of encapsulation, readability, reusability and making project structure easy on the brain, that's how things have been organised.
