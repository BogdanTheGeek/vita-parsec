UNAME = $(shell uname -s)


### LINUX ###
ifeq ($(UNAME), Linux)

PLATFORM = linux

SHARED_LIBS = \
	-lm \
	-ldl \
	-lGL \
	-lpthread
endif


### COMMON ###
BIN_NAME = client
OBJS = main.o
STATIC_LIBS = lib/$(PLATFORM)/libSDL2.a

CFLAGS = \
	-Wall \
	-Wextra \
	-Wno-unused-value \
	-Wno-missing-field-initializers \
	-O3 \
	-I../../sdk \
	-Iinclude

all: clean clear $(OBJS)
	$(CC) -o $(BIN_NAME) $(OBJS) $(STATIC_LIBS) $(SHARED_LIBS)

clean:
	-@rm -rf $(OBJS)
	-@rm -rf $(BIN_NAME)

clear:
	clear
