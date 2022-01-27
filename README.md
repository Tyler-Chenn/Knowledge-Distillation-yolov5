# Knowledge-Distillation-yolov5
## 1、知识在yolov5原始项目中修改了train.py中的损失调用，参数定义，训练方法定义，教师模型定义。
## 2、在原yolov5的loss.py文件中定义了蒸馏损失计算方法。

## 3、用MSELoss()计算中间特征矩阵的方法让教师模型监督约束学生模型应该是不行的，原因可能是大量无用的grid_cell让有价值的grid_cell淹没在了茫茫数据之中。因此应该挑选出有价值的数据点后在使用。
