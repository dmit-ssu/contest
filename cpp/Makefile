SOURCES := $(wildcard *.cpp)
EXECUTABLES := $(patsubst %.cpp,%,$(SOURCES))
CXX := g++ -Wall -Wvla -g -std=c++11

all: $(EXECUTABLES)

$@: $<
	${CXX} -c $< -o $@
