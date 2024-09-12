本仓库是南京师范大学心理学院胡传鹏教授在2024年秋季学期中《高级心理统计》中的课件及相关内容.

本仓库内容由胡传鹏、潘晚坷、朱珊珊三人共同完成，基于本课程[2023年学期课件](./Archive/2023/README.md)。

我们鼓励重复使用本仓库中的内容，但需遵守本仓库的版本协议。使用前请联系胡传鹏教授，邮箱：hcp4715@hotmail.com

This is a repo for teaching Bayesian analysis.

Author: Prof. Dr. HU Chuan-Peng; PAN, Wanke; Zhu Shanshan.

Affiliation: School of Psychology, Nanjing Normal University, Nanjing, China

Please contact Prof. Hu before re-using materials in this repo.

Email: hcp4715@hotmail.com

## Outlines

| 序号 |                    课程内容                    |
| :--: | :--------------------------------------------: |
|  1  |                    课程介绍                    |
|  2  |                  Bayes' Rule                  |
|  3  |        The Beta-Binomial Bayesian Model        |
|  4  | Balance and Sequentiality in Bayesian Analyses |
|  5  |               Conjugate Families               |
|  6  |          Approximating the Posterior          |
|  7  |              MCMC under the Hood              |
|  8  |        Posterior Inference & Prediction        |
|  9  |           A Simple Normal Regression           |
|  10  |         Evaluating Regression Models 1         |
|  11  |         Evaluating Regression Models 2         |
|  12  |               GLM: Bayes factors               |
|  13  |            GLM: Logistic Regression            |
|  14  |             Hierarchical Models 1             |
|  15  |             Hierarchical Models 2             |
|  16  |                  特邀专家报告                  |

## 文件夹结构

```bash
PyBayesian/
├── .github/                     # 存放GitHub相关配置，如workflows（用于自动化任务）  
│
├── Archive/                     # 归档文件  
│   ├── 2022/                    # 2022年课件及相关数据  
│   └── 2023/                    # 2023年课件及相关数据  
│
├── data/                        # 数据文件  
│   ├── flanker_1.csv            # Flanker任务数据  
│   └── SMS_Well_being.csv       # SMS心理幸福感数据  
│
├── figs/                        # 存在使用的图片
├── .gitignore                   # Git忽略文件  
├── dockerfile                   # Docker配置文件  
├── Lecture{id}.ipynb            # 2024年第{id}讲课件  
├── LICENSE                      # 许可证文件   
├── README.md                    # 本仓库说明文件  
└── Syllabus_CN.md               # 课程大纲 (中文)
```

# 环境配置和使用

本项目有三种环境使用方式：
- 和鲸云服务器平台，专门为选课同学使用，无需额外配置环境
- dockerhub 镜像，所有用户可拉取镜像使用，见 [dockerhub镜像使用](#dockerhub镜像使用)
- 自行本地环境配置，见 [本地环境配置](#本地环境配置)


## dockerhub镜像使用

我们已经将 docker 镜像上传至 [dockerhub](https://hub.docker.com/repository/docker/wanke/nnub/)，你可以使用以下命令进行使用。

如果你已经安装了 docker desktop 或 docker engine，你可以使用以下命令拉取镜：
```bash
docker pull wanke/nnub
```

并进行运行：

```bash
docker run -it --rm -p 8888:8888 wanke/nnub
```


## 本地环境配置

有两种环境配置方式，即Docker配置和本地 python 配置。

### 本地 docoker 部署配置

首先确保你已经安装了 docker。

请克隆我们的仓库或者下载 dockerfile。

之后执行以下部署命令：
```bash
docker build -t {username}/{imagename}:2024
```
请将 `{username}` 和 `{imagename}` 替换为你自己的用户名和任意镜像名称。

之后运行：
```bash
docker run -it --rm -p 8888:8888 wanke/nnub
```

### 本地 python 配置

如果你已经安装了 python 3.10-3.11，你可以使用以下命令安装依赖：
```bash
pip install -r requirements.txt
```

