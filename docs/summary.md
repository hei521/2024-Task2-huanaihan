总结与反思
1>所使用的Git,Conda命令及解释
Git
  1.git clone https://github.com/hei521/2024-Task-huanaihan.git -----克隆
  2.git checkout -b dev   ----创建开发分支
  3.git add ...   -----添加到暂存区
  4.git commit -m "..."  -----提交更改
  5.git push origin main -----推送到远程仓库
Conda
  1.conda create --name test python=3.9   -----创建环境
  2.conda activate test ----激活环境
  3.pip install -r requirements.txt ----创建虚拟环境并安装仓库中的依赖
  4.python plot.py ----运行程序，生成图像
2>Anaconda环境配置的优点与缺点
  1.优点：依赖隔离---每个项目可创建独立环境，避免不同项目的 Python 或库版本冲突
          跨平台支持----支持 Windows、Linux、macOS，环境配置文件（environment.yml）可跨平台复用。
          包管理高效---通过 Conda 可一键安装复杂科学计算库（如 NumPy、SciPy），自动解决依赖关系。
          快速复现环境----通过 conda env export > environment.yml 导出配置，他人可一键复现相同环境。
   2.缺点：体积庞大---基础安装包约 3GB，包含大量预装库（如 MKL、OpenSSL），占用磁盘空间。
           网络依赖性强---国内用户需切换镜像源（如清华源），否则安装速度慢甚至失败。
           虚拟环境启动慢----相比 Python 原生 venv，Conda 环境激活时间较长（尤其是 Windows 系统）。
3>Git分支管理中的经验
   1.功能开发使用'feature-*'分支
   2.合并前先执行'git pull --rebase'
4>部署过程中遇到的问题及解决方案
   1.在应用访问拉取其他仓库时拉取错误----重新克隆引用
   2.在移动图片时对图片形式写入错误-----更改图片形式
   3.打字过快打错字----重新核对，重新输入