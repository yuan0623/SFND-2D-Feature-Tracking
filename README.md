# SFND 2D Feature Tracking

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./2D_feature_tracking`.

## Rubric Points

### Data Buffer
- MP.1 Data Buffer Optimization: 

  check `MidTermProject_Camera_Student.cpp` line 66-68.
### Keypoints
- MP.2 Keypoint Detection:
  check `MidTermProject_Camera_Student.cpp` line 83-110, `matching2D.hpp` and `matching2D_Student.cpp`
- MP.3 Keypoint Removal:
  check `MidTermProject_Camera_Student.cpp` line 119-134,
### Descriptors
- MP.4 Keypoint Descriptors:
  All the required descriptors are inplemented, check `matching2D_Student.cpp` line 72-100.
- MP.5 Descriptor Matching:
  FLANN matching and k-nearest neighbor selection are implemented, check `matching2D_Student.cpp` line 19-31, line 39-55, respectively.
- MP.6 Descriptor Distance Ratio:
  Descriptor Distance Ratio is implemented, check `matching2D_Student.cpp` line 44-51.
### Performance
- MP.7 Performance Evaluation 1

  - SHITOMASI: 125 118 123 120 120 113 114 123 111 112
  - HARRIS: 50 54 53 55 56 58 57 61 59 57 
  - FAST: 149 152 150 155 149 149 156 150 138 143 
  - BRISK: 264 282 282 277 297 279 289 272 266 254 
  - ORB: 92 102 106 113 109 125 130 129 127 128 
  - AKAZE: 166 157 161 155 163 164 173 175 177 179
  - SIFT: 138 132 124 137 134 140 137 148 159 137
- MP.8 Performance Evaluation 2

  - Detector: SHITOMASI, Descriptor: BRISK
  
    95 88 80 90 82 79 85 86 82 
    
  - Detector: SHITOMASI, Descriptor: BRISK
    
    115 111 104 101 102 102 100 109 100 

  - Detector: SHITOMASI, Descriptor: ORB
    
    104 103 100 102 103 98 98 102 97 
  - Detector: SHITOMASI, Descriptor: FREAK
      
    90 88 87 89 83 78 81 86 84 
  - Detector: SHITOMASI, Descriptor: AKAZE
        
    code cannot run, this combination does not work
  - Detector: SHITOMASI, Descriptor: SIFT
        
    code cannot run, this combination does not work
    
  - Detector: HARRIS, Descriptor: BRISK
            
    43 39 45 44 37 41 44 52 48 
  - Detector: HARRIS, Descriptor: BRIEF
                
    48 49 47 51 53 49 52 56 55 
  - Detector: HARRIS, Descriptor: ORB
                
    46 44 48 51 48 50 50 58 54
  - Detector: HARRIS, Descriptor: FREAK
                    
    43 45 44 40 42 47 43 48 51 
  - Detector: HARRIS, Descriptor: AKAZE
                      
    code cannot run, this combination does not work
  - Detector: HARRIS, Descriptor: SIFT
                        
    code cannot run, this combination does not work
  - Detector: FAST, Descriptor: BRISK
  
    97 104 101 98 85 107 107 100 100 
  - Detector: FAST, Descriptor: BRIEF
  
    119 130 118 126 108 123 131 125 119 
  - Detector: FAST, Descriptor: ORB
  
    122 122 115 129 107 120 126 122 118
  - Detector: FAST, Descriptor: FREAK
  
    97 98 94 99 88 99 104 99 103 
  - Detector: FAST, Descriptor: FREAK
  
    97 98 94 99 88 99 104 99 103 
  - Detector: FAST, Descriptor: AKAZE
                      
    code cannot run, this combination does not work
  - Detector: FAST, Descriptor: SIFT
                        
    code cannot run, this combination does not work
  - Detector: BRISK, Descriptor: BRISK
    
    171 176 157 176 174 188 173 171 184 
  - Detector: BRISK, Descriptor: BRIEF
      
    178 205 185 179 183 195 207 189 183 
  - Detector: BRISK, Descriptor: ORB
        
    160 171 157 170 154 180 171 175 172 
  - Detector: BRISK, Descriptor: FREAK
          
    160 178 156 173 160 183 169 179 168 
  - Detector: BRISK, Descriptor: AKAZE
                        
    code cannot run, this combination does not work
  - Detector: BRISK, Descriptor: SIFT
                          
    code cannot run, this combination does not work
  - Detector: ORB, Descriptor: BRISK
    
    73 74 79 85 79 92 90 88 91 
  - Detector: ORB, Descriptor: BRIEF
    
    49 43 45 59 53 78 68 84 66 
  - Detector: ORB, Descriptor: ORB
      
    65 69 71 85 91 101 95 93 91 
  - Detector: ORB, Descriptor: FREAK
    
    42 36 45 47 44 51 52 49 55 
  - Detector: AKAZE, Descriptor: BRISK
    
    137 125 129 129 131 132 142 146 144 
  - Detector: AKAZE, Descriptor: BRIEF
  
    141 134 131 130 134 146 150 148 152
    
  - Detector: AKAZE, Descriptor: ORB
    
    130 129 128 115 132 132 137 137 146
  - Detector: AKAZE, Descriptor: FREAK
  
    126 128 128 121 123 132 145 148 137 
    
  - Detector: AKAZE, Descriptor: AKAZE
    
    138 138 133 127 129 146 147 151 150 
  - Detector: AKAZE, Descriptor: SIFT
      
    code cannot run, this combination does not work
  - Detector: SIFT, Descriptor: BRISK
    
    64 66 62 66 59 64 64 67 80 
  - Detector: SIFT, Descriptor: BRIEF
      
    86 78 76 85 69 74 76 70 88 
  - Detector: SIFT, Descriptor: ORB
  
    code cannot run, this combination does not work
  - Detector: SIFT, Descriptor: FREAK
  
    64 72 65 66 63 58 64 65 79 
  - Detector: SIFT, Descriptor: AKAZE
    
    code cannot run, this combination does not work
  - Detector: SIFT, Descriptor: SIFT
- MP.9 Performance Evaluation 3
  - The spreadsheet can be found [here](https://docs.google.com/spreadsheets/d/1uxNoxjb7APyzbs_wWEZHTDqBL1qvrkhQDfxyXEYi0ek/edit?usp=sharing)