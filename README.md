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