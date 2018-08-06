# OpenFaceCpp
C++ implementation for [OpenFace](https://github.com/cmusatyalab/openface) library by CMU.  

Although there are many depedencies, the repo tries to minimize manual setup steps by using hunter packaging. Currently the only package that needs to be manually setup is torch.

# Install
This is a standard cmake project. Create a build directory from root, then `cmake ..`, followed by `cmake --build .` should do the trick. 

OpenFaceCpp currently takes an an input an xml config file. A sample is in `src/OpenFaceConfig.xml`. You will see a couple models are needed, they can be found in the [original repo](https://github.com/cmusatyalab/openface/blob/master/models/get-models.sh). 

E.g. OpenFaceConfig.xml expects:
- shape_predictor_68_face_landmarks.dat: it's possible to download it by running in PS: 
`wget http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2 -O dlib/shape_predictor_68_face_landmarks.dat.bz2`
- nn4.small2.v1: get it (and other models) from [here](http://cmusatyalab.github.io/openface/models-and-accuracies/)

# What's next? 
I am currently working on figuring out a way to do without the lua stuff. That would be sweet. 
