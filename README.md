# Volume Renderer

### Volume Rendering
Volume rendering is a technique used in computer graphics and visualization to generate a 2D or 3D image from a 3D volume dataset. The volume dataset typically represents a physical or simulated object or space, and is composed of many voxels (volumetric pixels) arranged in a regular grid.
The volume rendering process involves assigning colors and transparency values to each voxel based on its density or other physical properties, and then projecting the resulting image onto a 2D or 3D screen. This allows for the visualization of complex structures and data that would be difficult or impossible to represent with traditional surface rendering techniques.
There are several types of volume rendering techniques, including direct volume rendering, surface rendering, and hybrid rendering. Direct volume rendering is the most common, and involves rendering the entire volume directly, without any intermediate surface representation. Surface rendering involves extracting the surfaces of objects from the volume data and rendering them separately, while hybrid rendering combines both direct and surface rendering techniques.
Volume rendering is widely used in fields such as medical imaging, scientific visualization, and computer-aided design, among others, to create detailed and realistic visualizations of complex data.

### Single Pass Volume Rendering
A single pass volume renderer is a type of volume rendering technique that allows for the efficient rendering of 3D volumetric data in a single pass, without the need for multiple passes or intermediate buffers.
In a single pass volume renderer, the entire volume is processed and rendered in a single pass through the rendering pipeline, using specialized algorithms and data structures to optimize the rendering process. This contrasts with traditional multi-pass rendering techniques, which require multiple passes through the pipeline and intermediate buffers to generate a final image.
Single pass volume rendering techniques can offer significant performance benefits over traditional multi-pass rendering techniques, as they require less memory and reduce the overhead associated with intermediate buffer management. They are particularly useful for real-time applications such as interactive medical imaging or virtual reality, where fast rendering speeds and low latency are critical.
Some common single pass volume rendering techniques include ray casting, texture-based rendering, and splatting. Each of these techniques involves different algorithms and data structures to efficiently render 3D volumetric data in a single pass. 

### Ray Marching Technique
Ray marching is a technique used in computer graphics and visualization to generate images of 3D objects and environments, particularly for volume rendering. It involves tracing a ray from the viewer's eye through a 3D space, and incrementally stepping along the ray to determine the color and opacity of each point it intersects.
Unlike traditional ray tracing, which traces a ray from the eye to the light source, ray marching works by incrementally stepping along the ray from the eye to the object, using the accumulated opacity at each step to determine the final color and opacity of the object. This allows for the efficient rendering of complex 3D volumes and environments, such as clouds, smoke, and other natural phenomena.
Ray marching can be used in combination with other techniques, such as volumetric lighting and shading, to create realistic and detailed visualizations of complex 3D scenes. It is also commonly used in real-time applications such as video games and virtual reality, where fast rendering speeds and low latency are critical.
One common challenge in ray marching is the need for adaptive step sizes along the ray, particularly in regions with high variability or density. Various techniques, such as ray differential analysis and adaptive sampling, have been developed to address this challenge and improve the accuracy and efficiency of ray marching algorithms.

### Instruction to run the code. 
1. Open Project in QtCreator.
2. Run the Project.

### Intruction to load different volume
1. Place the volume file in the project folder (the one with the .pro file)
2. In the openglwidget.cpp file's initializeGL() method, in the call to loadVolume
    replace the name of the file with the parameter. In the same method replace 
    texW, texH, texD with the respective width, height and depth of the volume to load

### Note : I used Qt 5.13 in Ubuntu 18.04
