# 20190109

## caffe功能调试

- 参考教程
~~~shell
//https://blog.csdn.net/kongxx/article/details/79019624

//安装依赖包
sudo yum install protobuf-devel leveldb-devel snappy-devel opencv-devel boost-devel hdf5-devel
sudo yum install gflags-devel glog-devel lmdb-devel
sudo yum install openblas-devel


//安装caffe

wget -c https://github.com/BVLC/caffe/archive/1.0.tar.gz
tar zxvf 1.0.tar.gz
cd caffe-1.0
cp Makefile.config.example Makefile.config


//由于我只是测试一下，机器没有GPU，所以需要使用CPU_ONLY模式，编辑Makefile.config，打开下面行

CPU_ONLY := 1

//然后，编译安装

make all
make test
make runtest

~~~
- 安装位置
~~~shell
/home/sxy/personal/project/test/caffe
~~~

