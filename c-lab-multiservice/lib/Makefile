CC ?= cc
CFLAGS ?= -O2 -Wall -Wextra -std=gnu11
AR ?= ar

INCLUDE_DIR = ../include
BUILD_DIR = ../build/lib
LIB = $(BUILD_DIR)/libcommon.a
OBJECTS = net.o http.o utils.o

.PHONY: all clean

all: $(LIB)

$(LIB): $(OBJECTS)
	@mkdir -p $(BUILD_DIR)
	$(AR) rcs $@ $(OBJECTS)

net.o: net.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c net.c -o net.o

http.o: http.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c http.c -o http.o

utils.o: utils.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c utils.c -o utils.o

clean:
	rm -f $(OBJECTS) $(LIB)
