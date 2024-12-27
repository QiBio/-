# 服务器用户手册
## 服务器规模

### 存储空间
### 计算资源数
## 使用指南
### 登录到命令行界面
### 传递数据
### 配置分析环境
1. 将miniconda3安装到[**工作目录**](#注意事项)。注意，miniconda3的默认安装位置为**主目录**而非**工作目录**，请在安装过程中进行手动修改。点击[此处](https://blog.csdn.net/suiyueruge1314/article/details/126705416)查看本步骤的一个参考流程。
```
bash /database/public/software/Miniconda3-latest-Linux-x86_64.sh #若想下载最新版本请访问https://docs.anaconda.com/miniconda/
```
2. 运行下述代码 在conda配置miniconda的国内镜像源。
```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pro/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/bioconda/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/qiime2
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/biobakery
conda config --set show_channel_urls yes
```
3. （可选）创建生信分析环境并安装相应分析软件。点击此处查看本步骤参考教程。
```
conda create --name fastp #创建一个名为fastp的分析环境
conda activate fastp # 进入名为fastp的分析环境
conda install fastp # 安装名为fastp的分析软件
```
4. 调用自建或[公共]分析环境(#分析环境)。注意，请在调用公共分析环境时使用绝对路径。
```
conda activate fastp #调用自建分析环境
conda activate /database/public/software/miniconda3/envs/fastp #调用公共分析环境
```

## 注意事项
- 正确区分**工作目录**与**主目录**。**工作目录**是服务器管理员分配给每位用户的用户专属目录，用户可点击此处查看；**主目录**是用于存储用户配置文件的目录，可使用命令`echo $HOME`查看。受限于服务器的存储空间分配，用户仅能在**工作目录**下进行包括**配置分析环境**在内的所有生物信息分析工作，仅能在**主目录**下进行用户配置文件的修改。
## 公共资源
### 分析环境
### 数据库
