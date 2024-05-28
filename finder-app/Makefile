# assignments/assignment2/Makefile

# Compiler and flags
CC := gcc
CFLAGS := -Wall -Werror -g

# Source and target
SRC := writer.c
TARGET := writer

# Output file
OUTPUT_DIR := ../assignments/assignment2
FILE_RESULT := $(OUTPUT_DIR)/fileresult.txt

# Cross-compilation support
ifdef CROSS_COMPILE
	CC := $(CROSS_COMPILE)gcc
endif

# Default target
all: $(TARGET) $(FILE_RESULT)

# Build target
$(TARGET): $(SRC)
	$(CC) $(CFLAGS) -o $@ $^

# Generate fileresult.txt
$(FILE_RESULT): $(TARGET)
	file $(TARGET) > $(FILE_RESULT)

# Clean target
clean:
	rm -f $(TARGET) $(OBJS)

.PHONY: all clean
