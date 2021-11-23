CXX = g++
CFLAGS = -Wall
LDFLAGS = 

target = _main
srcs_cpp = $(wildcard ./*.cpp) 
srcs_c   = $(wildcard ./*.c) 
objs = $(srcs_cpp:.cpp=_cpp.o) $(srcs_c:.c=_c.o)

INCLUDES = -I../../include
LIB_PATH = -L../../external


.PHONY: all
all: $(target)

$(target): $(objs)
	$(CXX) -o _main $^ $(LIB_PATH) -lglfw3 -lGL -lm -ldl -lXinerama -lXrandr -lXi -lXcursor -lX11 -lXxf86vm -lpthread

$(srcs_cpp:.cpp=_cpp.o):%_cpp.o:%.cpp
	$(CXX) -c $(INCLUDES) -o $@ $<

$(srcs_c:.c=_c.o):%_c.o:%.c
	$(CXX) -c $(INCLUDES) -o $@ $<

.PHONY: FORCE
FORCE: 

clean:
	rm -f _main *.o

