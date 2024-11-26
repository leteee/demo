# cmake-demo

## 环境准备
```shell
sudo apt-get update && sudo apt install g++ -y
```

## build
- 方法一
```shell
rm build -rf && mkdir build && g++ -o build/main main.cpp hello/hello.cpp world/world.cpp -I ./world
```
- 方法二
```shell
rm build -rf && mkdir build && cd build
g++ -c ../main.cpp -I ../world
g++ -c ../hello/hello.cpp
g++ -c ../world/world.cpp
g++ -o main main.o hello.o world.o
cd ..
```

## run
```shell
./build/main
```