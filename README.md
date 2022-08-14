# xv6-labs-2021

## 环境搭建

### MacOS

先下载xcode命令⾏⼯具，再下载homebrew包管理⼯具。而后使⽤brew安装riscv，即

```shell
brew tap riscv/riscv
brew install riscv-tools
```

然后添加到环境变量中，找到你`riscv-gnu-toolchain`的安装位置，我的是在`/usr/local/opt/riscv-gnutoolchain/`中。因此可以修改配置文件，即

```shell
vi ~/.bashrc
```

添加安装工具链位置路径，即

```shell
PATH=$PATH:/opt/homebrew/opt/riscv-gnutoolchain/bin
```

然后使其生效，即

```shell
source ~/.bashrc
```

最后再使⽤brew安装qemu即可，参考[官网教程](https://pdos.csail.mit.edu/6.828/2021/tools.html)

```shell
brew install qemu
```

## 测试环境配置是否成功

随便找个工作目录，将项目克隆到本地

```shell
git clone git://g.csail.mit.edu/xv6-labs-2021
```

然后进入项目

```shell
cd xv6-labs-2021
```

由于每个实现都处在不同的branch分支，因此转换到第一个实验的分支`util`

```shell
git checkout util
```

通过Makefile和qemu模拟器启动xv6，参考[第一个实验](https://pdos.csail.mit.edu/6.828/2021/labs/util.html)

```shell
make qemu
```
