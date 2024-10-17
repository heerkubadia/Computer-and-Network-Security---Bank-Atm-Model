# Makefile for ATM and Bank

# Compiler
CXX = g++

# Compiler flags
CXXFLAGS = -Wall -Wextra -std=c++11 -I/opt/homebrew/include

# Library path
LIB_PATH = /opt/homebrew/lib

# Libraries
LIBS = -ljsoncpp

# Source files
ATM_SRC = atm_locally_working_18oct.cpp
BANK_SRC = bank_locally_working_18oct.cpp

# Executables
ATM = atm
BANK = bank

# Default target
.PHONY: all clean
all: $(ATM) $(BANK)

# Build ATM
$(ATM): $(ATM_SRC)
	$(CXX) $(CXXFLAGS) -o $@ $^ -L$(LIB_PATH) $(LIBS)

# Build Bank
$(BANK): $(BANK_SRC)
	$(CXX) $(CXXFLAGS) -o $@ $^ -L$(LIB_PATH) $(LIBS)

# Clean build artifacts
clean:
	rm -f $(ATM) $(BANK)
