CC = gcc
CFLAGS = -Wall -Iinclude

BIN_DIR = ../bin
SRC_DIR = ../src
INC_DIR = ../include
LIB_DIR = ../lib

SRC_FILES = $(SRC_DIR)/main.c $(SRC_DIR)/primes.c
OBJ_FILES = $(SRC_DIR)/main.o $(LIB_DIR)/primes.o

TARGET = $(BIN_DIR)/program

all: $(TARGET)

$(TARGET): $(OBJ_FILES)
	$(CC) -o $@ $^

$(LIB_DIR)/primes.o: $(SRC_DIR)/primes.c $(INC_DIR)/primes.h
	$(CC) $(CFLAGS) -c $< -o $@

$(SRC_DIR)/main.o: $(SRC_DIR)/main.c $(INC_DIR)/primes.h
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(OBJ_FILES) $(TARGET)

.PHONY: all clean