# cameradar-Arm64-version

众所周知，Cameradar这个项目想要在本地编译是一个相对困难的事情，因为需要的libcurl版本会比较低

在此给出完整的编译方法：

> git clone https://github.com/Ullaakut/cameradar.git
> cd cameradar
> wget https://curl.se/download/curl-7.63.0.zip
> unzip curl-7.63.0.zip -d curl
> mkdir curl
> unzip curl-7.63.0.zip -d curl/
> cd curl
> cd curl-7.63.0
> configure --prefix=/root/Desktop/tools/cameradar/curl
> ./configure --prefix=/root/Desktop/tools/cameradar/curl
> make
> make install
> export PKG_CONFIG_PATH=/root/Desktop/tools/cameradar/curl/lib/pkgconfig:$PKG_CONFIG_PATH
> pkg-config --modversion libcurl
> cd ../../cmd/cameradar
> go build .

最后生成的cameradar就可以使用了
