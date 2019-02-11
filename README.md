# Photogrammetry-with-Agisoft

The coming project aims at finding the optimal 3D scanning method for human faces. 

Photogrammetry is selected and the software "Agisoft" is being used in this post and hence would be the primary focus of the coming discussion.

Laptop: MSI
   CPU: i7-7700HQ
   GPU: GTX 1060
   RAM: 16 GB DDR4 - 2400 MHz 

The 1st attempt contains 44 images of my friend.
    
    All image have been successfully aligned. 
            Processing time:approx. 30 mins.

    
    Mesh geometry has been populated and export into Rhino. (".obj")
        Processing time: 10 mins.
    
    Rhino read the file. Results shown at "Render" display mode.
        The texture image is good enough to reveal my friend as a 3D model.
        But, the geometry itself is really bad and it can hardly be recognized.
             Command "MeshToNumb" was used to improve the geometry.
             Result: no difference in "Render" display
                     But the 3D object model was worse, which it looks like a eroded sculpture.
                     
 The 2nd attempt contains 189 images of my friend.
    
    Not all image have been successfully aligned.
        Precision: high
            Result: 77/189
        Precision: medium (chosen)
            Result: 122/189
    
    Optimized image location:
        Result: misaligment occured.
                Tie Points: 15,170 pts.
                Dense Cloud: 9,984,322 pts. (high quality)
                    Processign time: 3 hours. 
        Mesh geometry has been populated and export to Rhino. (".obj")
            Processing time: 2 hours
