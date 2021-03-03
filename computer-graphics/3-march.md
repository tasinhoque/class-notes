6 Rasterization Pipeline

Viewing frustrum

Perspective project is more common

---

[Taken from [Wikipedia](<https://en.wikipedia.org/wiki/Ray_tracing_(graphics)>)]

In 3D computer graphics, ray tracing is a rendering technique for generating an image by tracing the path of light as pixels in an image plane and simulating the effects of its encounters with virtual objects. The technique is capable of producing a high degree of visual realism, more so than typical scanline rendering methods, but at a greater computational cost. This makes ray tracing best suited for applications where taking a relatively long time to render can be tolerated, such as in still computer-generated images, and film and television visual effects (VFX), but generally more poorly suited to real-time applications such as video games, where speed is critical in rendering each frame. In recent years, however, hardware acceleration for real-time ray tracing has become standard on new commercial graphics cards, and graphics APIs have followed suit, allowing developers to add real-time ray tracing techniques to games and other real-time rendered media with a lesser, albeit still substantial hit to frame render times.

Ray tracing is capable of simulating a variety of optical effects, such as reflection and refraction, scattering, and dispersion phenomena (such as chromatic aberration). It can also be used to trace the path of sound waves in a similar fashion to light waves, making it a viable option for more immersive sound design in video games by rendering realistic reverberation and echoes. In fact, any physical wave or particle phenomenon with approximately linear motion can be simulated with these techniques.

Path tracing is a form of ray tracing that can produce soft shadows, depth of field, motion blur, caustics, ambient occlusion, and indirect lighting. Path tracing is an unbiased rendering method, but a large number of rays must be traced to obtain high quality reference images without noisy artifacts.

Hybrid ray-tracing is a combination of ray-tracing and rasterization.

---

[Takin from [Wikipedia](https://en.wikipedia.org/wiki/Rasterisation)]

Rasterisation (or rasterization) is the task of taking an image described in a vector graphics format (shapes) and converting it into a raster image (a series of pixels, dots or lines, which, when displayed together, create the image which was represented via shapes).[1][2] The rasterised image may then be displayed on a computer display, video display or printer, or stored in a bitmap file format. Rasterisation may refer to the technique of drawing 3D models, or the conversion of 2D rendering primitives such as polygons, line segments into a rasterized format.

---

Vector algebra
