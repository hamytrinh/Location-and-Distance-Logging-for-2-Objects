# Location-and-Distance-Logging-for-2-Objects
The goal is to be able to log the locations and distance between a person and a NAO robot. The origin of the coordinates system is the camera.

Information:
- Camera: Logitech C920
- Software: Ubuntu 14.04
- Programming language: C++

Instructions:
    1. Download the AprilTags C++ Library modified by MIT and originally developed by Elwin Olson from University of Michigan
    2. Go to apriltags/example/ and replace the code in apriltags_demo.cpp file with my modified version (it's important that you keep the name of the file). In this version, I added the code to calculate 3D and 2D distance between 2 tags, and log the 2D distance information to a csv file.
    3. Open terminal and compile the new code
cd apriltags
make
    4. Run the code
./build/bin/apriltags_demo
    5. The csv file, containing distance information, is inside apriltags/build/bin and called rawData.csv. You can either view it as a text file or table format using excel

    NOTES:
- The tag size in the code is 0.073m, which is the tag I'm using. You can change this information if you use another tag size to get the correct distance
- The camera id is 1 because I am using an external webcam. If you want to use a built-in webcam, the id should be 0
- I used the default tag library 36h11, tag id 0 and 1, which you can print out using the given link to test the code.

Limitations:
    1. Marker (tags) are still needed to detect Nico and the human.
    2. The view of the camera is still limited, about 60 x 72 inches on the floor.
    3. Lighting is an important factor when the person starts to move around. Sometimes the camera cannot detect the tag because of reflections.
