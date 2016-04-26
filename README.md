# API

## QuickStart


```c++
x.SetInputFormat(int width, int height, int format)
```

The following parameters are used:

| Image | OK |
| --- | --- |
| width | Width of the image |
| height | Height of the image |





```c++

#include <artemis1.h>


x = new Artemis1Detector();

x.setModel(algocian::PERSON_UPRIGHT_12)

x.setDetectionHeights(0.1,0.9); // Detect a person from 10% to 90% height of the image

x.setInputFormat(640,480,algocian::FMT_RGB24)
x.setInputFormat(640,480,algocian::FMT_YUV24)
x.setInputFormat(640,480,algocian::FMT_IPLIMAGE)




while(1) {



algocian::detections persons;

persons = x.detect(char *data);
persons = x.detect(IplImage *input_image);


if(persons.size() > 0) { 
  printf("Alert! Person Detected");
  printf("  at location %d %d", );
  
}

x.saveOutputImage("/tmp/output.jpg");

}


```


## GetDetections ##

