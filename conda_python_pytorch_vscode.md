conda infeo -e // 查看所有环境
conda create --prefix=C:\Application\anaconda3\envs\envs_name // 指定路径创建环境
conda remove -n envs_name --all // 删除环境
activate envs_name // 激活环境

conda intall python=3.10 // 安装python
conda install pytorch torchvision torchaudio pytorch-cuda=11.7 -c pytorch -c nvidia // 安装pytorch
conda install jupyter notebook // 安装jypyter notebook

conda config --set remote_read_timeout_secs 1000.0 // 设置安装时间上限

// 解决jupyter notebook运行错误问题
conda uninstall pyzmq
conda install pyzmq
// 解决jupyter notebook运行错误问题

// 提示缺少sqlite3所需要的dll文件
// https://www.sqlite.org/download.html 下载对应版本后放在C:\Application\anaconda3\envs\envs_name\DLLs 文件夹下

// 将环境导入jupyter notebook
conda install ipykernel 
python -m iptykernel install --user --name envs_pytorch
// 将环境导入jupyter notebook

vscode下载python、pylance扩展
激活环境
打开文件夹，新建.py，ctrl+shift+p查找python: select interpreter选择环境即可
