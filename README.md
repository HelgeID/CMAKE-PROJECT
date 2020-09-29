# CMAKE-PROJECT
# 
1. Download MinGW. Додати папку bin в %PATH%.
2. Download cmake. Додати папку bin в %PATH%.
3. Test: 
	cmake --version, gcc --version
4. Команда для генерації make.exe: 
	copy c:\MinGW\bin\mingw32-make.exe c:\MinGW\bin\make.exe

5. У папці з проектом створити файл: CMakeLists.txt та папу build, де будуть cmake-файли.
6. Команда: cd build

7. Для генерації Makefile:
	cmake .. -G "MinGW Makefiles"
8. Для створення *.exe:
	make

!!! Якщо установлена VS, то команда: cmake .. (без ключа) автоматично згенерує для студії !!!

!!! Команда cmake .   --> cmake-файли будуть знаходитись у папці з проектом !!!


Файли проекта: *.cpp --> use CPP-компілятор

Файли проекта: *.c --> use C-компілятор

####################################################
# приклад CMakeLists.txt
####################################################

cmake_minimum_required(VERSION 3.18.2)

#set project

project(MyProject)

#set standart and flags

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -g")

file(GLOB CPPS "*.cpp" CS "*.c")

add_executable(${PROJECT_NAME} ${CPPS} ${CS})

####################################################
