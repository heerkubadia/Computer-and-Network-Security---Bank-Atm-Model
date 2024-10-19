# Compiler
CXX = g++

# Compiler flags
CXXFLAGS = -Wall -Wextra -std=c++11 -I/opt/homebrew/include -I/opt/homebrew/Cellar/openssl@3/include

# Library paths
JSON_LIB_PATH = /opt/homebrew/Cellar/jsoncpp/1.9.5/lib
SSL_LIB_PATH = /opt/homebrew/Cellar/openssl@3/lib

# Libraries
LIBS = -ljsoncpp -lssl -lcrypto

# Source files
ATM_SRC = atm_locally_working_18oct.cpp
BANK_SRC = bank_final.cpp

# Executables
ATM = atm
BANK = bank

# Default target
.PHONY: all clean
all: $(ATM) $(BANK)

# Build ATM
$(ATM): $(ATM_SRC)
	@echo "Building $(ATM)..."
	$(CXX) $(CXXFLAGS) -o $@ $^ -L$(JSON_LIB_PATH) -L$(SSL_LIB_PATH) $(LIBS)
	@echo "$(ATM) built successfully."

# Build Bank
$(BANK): $(BANK_SRC)
	@echo "Building $(BANK)..."
	$(CXX) $(CXXFLAGS) -o $@ $^ -L$(JSON_LIB_PATH) -L$(SSL_LIB_PATH) $(LIBS)
	@echo "$(BANK) built successfully."

# Clean build artifacts
clean:
	@echo "Cleaning up..."
	rm -f $(ATM) $(BANK)
	@echo "Cleanup complete."

# Check library paths
check:
	@echo "Checking library paths..."
	@if [ -d "$(JSON_LIB_PATH)" ]; then echo "JSON Library Path: Exists"; else echo "JSON Library Path: Not Found"; fi
	@if [ -d "$(SSL_LIB_PATH)" ]; then echo "SSL Library Path: Exists"; else echo "SSL Library Path: Not Found"; fi
	@if [ -f "$(JSON_LIB_PATH)/libjsoncpp.dylib" ]; then echo "JSON Library: Exists"; else echo "JSON Library: Not Found"; fi
	@if [ -f "$(SSL_LIB_PATH)/libssl.dylib" ]; then echo "SSL Library: Exists"; else echo "SSL Library: Not Found"; fi
	@if [ -f "$(SSL_LIB_PATH)/libcrypto.dylib" ]; then echo "Crypto Library: Exists"; else echo "Crypto Library: Not Found"; fi
