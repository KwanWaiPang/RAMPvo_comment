[comment]: <> (# RAMP-VO)

<!-- PROJECT LOGO -->

<p align="center">

  <h1 align="center"> RAMP-VO (复现及中文注释版~仅供个人学习记录用)
  </h1>

[comment]: <> (  <h2 align="center">PAPER</h2>)
  <h3 align="center">
  <a href="https://rpg.ifi.uzh.ch/docs/IROS24_Pellerito.pdf" target="_blank">Paper</a> 
  | <a href="https://github.com/uzh-rpg/rampvo" target="_blank">Original Github Page</a>
  </h3>
  <div align="center"></div>

# 配置过程记录
* 创建conda环境
~~~
<!-- rm -rf .git -->

conda env create -f environment.yml
conda activate rampvo

conda activate rampvo 
~~~
* 采用的服务器CUDA Version: 12.0；Python 3.10.15因此应该可以用下面的安装
~~~
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu124

pip install -r requirements.txt
~~~
* 但是会报错显示"The detected CUDA version (11.7) mismatches the version that was used to compile PyTorch (12.4). Please make sure to use the same CUDA versions." 应该还是cuda版本不匹配，改为下面试试（注意需要把pip install -r requirements.txt中的torch-scatter注释掉）
~~~
pip install torch==1.11.0+cu113 torchvision==0.12.0+cu113 torchaudio==0.11.0 --extra-index-url https://download.pytorch.org/whl/cu113

pip install torch-scatter==2.0.9 -f https://data.pyg.org/whl/torch-1.11.0+cu113.html
pip install -r requirements.txt
~~~

* 下载eigen
~~~
wget https://gitlab.com/libeigen/eigen/-/archive/3.4.0/eigen-3.4.0.zip
unzip eigen-3.4.0.zip -d thirdparty
~~~