## conda command
```shell
conda info -e // 查看所有环境
conda create --prefix=C:\Application\anaconda3\envs\envs_name // 指定路径创建环境
conda remove -n envs_name --all // 删除环境
activate envs_name // 激活环境

conda list
conda install package_name
conda uninstall package_name
conda update package_name

conda install python=3.10 // 安装python
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

// 2024.1.25
conda install pytorch torchtext torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
重新安装 pytorch torchtext torchvision torchaudio
```
```python
// 验证pytorch
import torch
import torchtext

print(torch.__version__)  # 2.1.2
print(torch.version.cuda)  # 11.8
print(torch.backends.cudnn.version())  # 8700
print(torchtext.__version__)  # 0.16.2
gpu = torch.device('cuda')
x = torch.rand(5,3).to(gpu)
x: tensor([[3.3000e-01, 7.9273e-01, 4.6684e-01],
        [6.6042e-04, 9.2719e-01, 9.1276e-01],
        [5.9449e-01, 1.7616e-01, 7.3718e-01],
        [8.4496e-01, 9.6554e-01, 8.8205e-01],
        [9.8886e-01, 2.7237e-01, 8.9327e-01]], device='cuda:0')
```

## pycharm configuration
<img src=".\conda.assets\image-20230724203402801.png" alt="image-20230724203402801" style="zoom: 30%;" />

定位到conda.bat文件后才可以找到环境

## some package install
### 配置 pycocotools

pip install pycocotools

[windows下pycocotools的安装及避坑 - 飞桨AI Studio星河社区 (baidu.com)](https://aistudio.baidu.com/projectdetail/980509)

[windows下安装pycocotools - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/130697744)

### labelImg的安装和使用

envs_pytorch:  pip install labelImg

删除  hxj\.labelImgSettings.pkl

检查下载的位置:  C:\Users\hxj\AppData\Roaming\Python\Python310\Scripts\labelImg.exe

剪切到:  C:\Application\anaconda3\envs\envs_pytorch\Scripts\labelImg.exe

编辑环境变量

出现如下错误时，到canvas.py中修改

```python
 File "C:\Users\hxj\AppData\Roaming\Python\Python310\site-packages\libs\canvas.py", line 530, in paintEvent
    p.drawLine(self.prev_point.x(), 0, self.prev_point.x(), self.pixmap.height())
TypeError: arguments did not match any overloaded call:
  drawLine(self, QLineF): argument 1 has unexpected type 'float'
  drawLine(self, QLine): argument 1 has unexpected type 'float'
  drawLine(self, int, int, int, int): argument 1 has unexpected type 'float'
  drawLine(self, QPoint, QPoint): argument 1 has unexpected type 'float'
  drawLine(self, Union[QPointF, QPoint], Union[QPointF, QPoint]): argument 1 has unexpected type 'float'
```

526  p.drawRect(int(left_top.x()), int(left_top.y()), int(rect_width), int(rect_height))

530  p.drawLine(int(self.prev_point.x()), 0, int(self.prev_point.x()), int(self.pixmap.height()))

531  p.drawLine(0, int(self.prev_point.y()), int(self.pixmap.width()), int(self.prev_point.y()))

出现错误原因是3.10以上版本导致

### d2l

pip install [d2l](https://so.csdn.net/so/search?q=d2l&spm=1001.2101.3001.7020) ——> pip install [d2l](https://so.csdn.net/so/search?q=d2l&spm=1001.2101.3001.7020) pandas==1.5.3，最终解决成功install d2l ，似乎是因为pandas版本不兼容的问题

### scikit-learn

pip install scikit-learn

### vscode configuration

setting -> search "execute":

python > Terminal: Execute in File Dir

check True : 

whether to use execute in the file's directory, instead of the current open folder
