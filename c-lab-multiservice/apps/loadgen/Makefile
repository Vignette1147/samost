CC ?= cc
CFLAGS ?= -O2 -Wall -Wextra -std=gnu11

INCLUDE_DIR = ../../include
LIB_DIR = ../../build/lib
LIB = $(LIB_DIR)/libcommon.a
OBJECTS = main.o stats.o
TARGET = loadgen

.PHONY: all clean

all: $(TARGET)

$(TARGET): $(OBJECTS) $(LIB)
	$(CC) $(CFLAGS) -o $(TARGET) $(OBJECTS) $(LIB)

main.o: main.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c main.c -o main.o

stats.o: stats.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c stats.c -o stats.o

clean:
	rm -f $(OBJECTS) $(TARGET)
