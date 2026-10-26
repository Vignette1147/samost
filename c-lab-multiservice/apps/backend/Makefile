CC ?= cc
CFLAGS ?= -O2 -Wall -Wextra -std=gnu11

INCLUDE_DIR = ../../include
LIB_DIR = ../../build/lib
LIB = $(LIB_DIR)/libcommon.a
OBJECTS = main.o handler.o
TARGET = backend

.PHONY: all clean

all: $(TARGET)

$(TARGET): $(OBJECTS) $(LIB)
	$(CC) $(CFLAGS) -o $(TARGET) $(OBJECTS) $(LIB)

main.o: main.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c main.c -o main.o

handler.o: handler.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c handler.c -o handler.o

clean:
	rm -f $(OBJECTS) $(TARGET)
