CXX = g++
CFLAGS = -Wall
LDFLAGS = 

target = _main
srcs = case4.cpp glad.c
objs = case4.o glad.o stb.o

INCLUDES = -I../include
LIB_PATH = -L../external


.PHONY: all
all: $(target)

$(target): $(objs)
	$(CXX) -o _main $^ $(LIB_PATH) -lglfw3 -lGL -lm -ldl -lXinerama -lXrandr -lXi -lXcursor -lX11 -lXxf86vm -lpthread

# $(objs):$(srcs)
# 	$(CXX) -c $(INCLUDES) $(srcs) -o $(objs)
case4.o:case4.cpp
	$(CXX) -c $(INCLUDES) case4.cpp -o case4.o
glad.o:glad.c
	$(CXX) -c $(INCLUDES) glad.c -o glad.o
stb.o:stb.cpp
	$(CXX) -c $(INCLUDES) stb.cpp -o stb.o


.PHONY: FORCE
FORCE: 

clean:
	rm -f _main *.o

