CXX = g++
CFLAGS = -Wall
LDFLAGS = 

target = _main
srcs = case1.cpp glad.c
objs = case1.o glad.o stb.o

INCLUDES = -I../../include
LIB_PATH = -L../../external


.PHONY: all
all: $(target)

$(target): $(objs)
	$(CXX) -o _main $^ $(LIB_PATH) -lglfw3 -lGL -lm -ldl -lXinerama -lXrandr -lXi -lXcursor -lX11 -lXxf86vm -lpthread

# $(objs):$(srcs)
# 	$(CXX) -c $(INCLUDES) $(srcs) -o $(objs)
case1.o:case1.cpp
	$(CXX) -c $(INCLUDES) case1.cpp -o case1.o
glad.o:glad.c
	$(CXX) -c $(INCLUDES) glad.c -o glad.o
stb.o:stb.cpp
	$(CXX) -c $(INCLUDES) stb.cpp -o stb.o


.PHONY: FORCE
FORCE: 

clean:
	rm -f _main *.o

