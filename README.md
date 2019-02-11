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
            
Pros:
   1. Do not requir specific tools. Any camera can do the work.
   2. Agisoft is relatively cheap for licensing.
   3. Can be apply to a huge range of scale, from urban site model to an object.
   4. Can be export to various modeling software, such as Rhino and c4d, for further mesh clean up.

Cons:
      Agisoft:
         1. Processing time varies according to your CPU. (Can goes up to multiple hours.)
         2. Location of images may not be success fully identified.
         3. Missing an important image may require a complete redo.
         4. Resolution of the model relies on the texture image, pure mesh geometry can easily dsitorted. 
     Model with fine detials requires a sophisticate setup which drives up the cost:
         1. Perfect lighting.
         2. Multiple high resolution cameras.
         3. Locational identifying object maybe necessary.
