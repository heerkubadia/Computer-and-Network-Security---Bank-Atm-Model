# Makefile for ATM and Bank

# Compiler
CXX = g++

# Compiler flags
CXXFLAGS = -Wall -Wextra -std=c++11

# Source files
ATM_SRC = atm.cpp
BANK_SRC = bank.cpp

# Executables
ATM = atm
BANK = bank

# Library path
LIB_PATH = /opt/homebrew/lib

# Default target
all: $(ATM) $(BANK)

# Build ATM
$(ATM): $(ATM_SRC)
	$(CXX) $(CXXFLAGS) -o $(ATM) $(ATM_SRC) -L$(LIB_PATH) -ljsoncpp

# Build Bank
$(BANK): $(BANK_SRC)
	$(CXX) $(CXXFLAGS) -o $(BANK) $(BANK_SRC) -L$(LIB_PATH) -ljsoncpp

# Clean build artifacts
clean:
	rm -f $(ATM) $(BANK)
