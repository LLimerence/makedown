## 记录一些日常中不注意的问题
### pytohn
* model.train()  
训练过程中会在程序上方添加一句model.train( )，作用是启用 batch normalization 和 dropout 。  
如果模型中有BN层（Batch Normalization）和 Dropout ，需要在训练时添加 model.train( )。
model.eval()的作用是不启用 Batch Normalization 和 Dropout。
model.eval() 是保证 BN 层能够用全部训练数据的均值和方差，即测试过程中要保证 BN 层的均值和方差不变。对于 Dropout，model.eval( ) 是利用到了所有网络连接，即不进行随机舍弃神经元。
* os库  
  > os.path.adspath()  返回他的绝对路径
* glob库  
  > glob.glob（os.path.join(path,"*.png")） 返回path路径下面的所有png图像
