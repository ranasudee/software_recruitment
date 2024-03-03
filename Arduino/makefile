build: builddir lib build/fakeArduino.cpp build/MotorArduino.h build/fakeArduino.hpp build/MotorArduino.cpp
	
	@g++ -Wall -g -lpthread -o motorMain ./build/MotorArduino.cpp ./build/fakeArduino.cpp

builddir: 
	@mkdir -p build

build/fakeArduino.cpp: lib/fakeArduino.cpp
build/MotorArduino.h: lib/MotorArduino.h
build/fakeArduino.hpp: lib/fakeArduino.hpp
build/MotorArduino_tmp.cpp: MotorArduino/MotorArduino.ino

build/MotorArduino.cpp: build/MotorArduino_tmp.cpp
	@cp -f build/MotorArduino_tmp.cpp build/MotorArduino.cpp
	@sed -i '1 i\#include "fakeArduino.hpp"' ./build/MotorArduino.cpp

build/%:
	@cp -f $< $@

clean:
	@rm -rf build
	@rm -f motorMain