EXECUTABLE = gl_final 
LIBS = -lGL -lGLEW `pkg-config --libs glfw3` -lassimp 
CFLAGS = `pkg-config --cflags glfw3` -ggdb3 -Wall
###############################################################################
CC = g++
SRCS := $(wildcard *.cpp)
###############################################################################
all:	$(EXECUTABLE)

$(EXECUTABLE): $(SRCS)
					$(CC) $(CFLAGS) -o $(EXECUTABLE) $(SRCS) $(LIBS)

clean:
					-rm $(EXECUTABLE)

explain:
					@echo "---------Some Info---------"
					@echo "Executable name: $(EXECUTABLE)"
					@echo "Source files: $(SRCS)"
					@echo "Object files: $(OBJS)"

run:			all
					./$(EXECUTABLE)

debug: 		all
					gdb $(EXECUTABLE)
