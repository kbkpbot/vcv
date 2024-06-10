
LIB = libopencv_wrapper.a
TARGETS = aruco.o asyncarray.o calib3d.o core.o dnn.o features2d.o highgui.o imgcodecs.o imgproc.o objdetect.o photo.o svd.o version.o video.o videoio.o

all: $(LIB)

%.o: %.cpp
	g++ -I /usr/local/include/opencv4 -c $<

libopencv_wrapper.a: $(TARGETS)
	ar -rc libopencv_wrapper.a $(TARGETS)
	rm $(TARGETS)
	
clean:
	rm -f *.o *.a