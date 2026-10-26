CC ?= cc
CFLAGS ?= -O2 -Wall -Wextra -std=gnu11

INCLUDE_DIR = ../../include
LIB_DIR = ../../build/lib
LIB = $(LIB_DIR)/libcommon.a
OBJECTS = main.o router.o
TARGET = balancer

.PHONY: all clean

all: $(TARGET)

$(TARGET): $(OBJECTS) $(LIB)
	$(CC) $(CFLAGS) -o $(TARGET) $(OBJECTS) $(LIB)

main.o: main.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c main.c -o main.o

router.o: router.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c router.c -o router.o

clean:
	rm -f $(OBJECTS) $(TARGET)
