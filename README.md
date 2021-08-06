# mobilenet_on_yolov4
add depthwise convolutional layer in the tag of darknet_yolo_v4_pre

# modify Makefile in 146 to 149
++ OBJ= depthwise_convolutional_layer.o
ifeq ($(GPU), 1) 
LDFLAGS+= -lstdc++ 
++ OBJ+=depthwise_convolutional_kernels.o 
endif
