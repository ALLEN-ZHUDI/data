# 多车辆旋转目标跟踪数据集 
与现有的多目标跟踪数据集相比，本文将旋转边界框引入到数据集中，提出旋转目标跟踪基准数据集，该数据集是为带有注释的定向边界框和属性的车辆无人机场景设计的。填补了跟踪领域不存在旋转目标跟踪车辆类别的数据集的空白，视频中的车辆以不同的视角获取，经常被图像边界截断。同时，设计了OBBMOT基准，对旋转多目标跟踪的性能评价。
# 数据收集与数据集规模
将收集的无人机航拍交通道路上车辆视频和从Visdrone2019数据集中筛选出来的交通道路航拍视角的数据图片总计七个场景，经过标注处理，形成了用于旋转目标跟踪训练与测试的旋转目标跟踪数据集OBBMOT。OBBMOT数据集中超过2600帧用735辆车进行标注，总共标记了约6.7万个车辆边界框。进行了几轮交叉检查以确保高质量的注释。有关与其他基准数据集的详细比较，如表3-2所示。前六列：训练/测试数据的数量 (1k = 103) 表示包含至少一个对象、对象轨迹的数量以及唯一对象边界框的数量的图像数量。其余列：每个数据集的附加属性，即“D”：检测任务，“T”：跟踪任务，“P”：目标对象是行人，“C”：目标对象是车辆，“O”：表示旋转框标记。

![image](https://github.com/ALLEN-ZHUDI/data/assets/55532249/f896773a-999f-4b57-b408-ea3c5850b54e)

经过对比发现本文制作的数据集的帧数和目标数与主流数据集还是有差距，但是边界框的标注数量和主流数据集相当，并且实现了旋转框的标注，这是在主流数据集中所不具备的。
# 数据格式与数据集划分
数据标注的注释文件举例如下图所示。为了获得整个基准测试的有效结果，必须为每个序列创建遵循上述格式的单独 txt文件，称为“groundtruth.txt”。数据集中共划分为七个文件夹，每个文件夹对应相应的场景，其中文件夹01,02,03，04的数据来源于visdrone2019里筛选出目标对象为道路行驶车辆的数据，文件夹05,06,07的数据来源于网络收集的航拍对象为道路行驶车辆的数据。对应每个场景都有各自的groundtruth.txt，放在对应的文件夹中。

![image](https://github.com/ALLEN-ZHUDI/data/assets/55532249/4114ce9d-c0b9-4448-9516-42e557b5d1bf)


所有图像都转换为png格式，并按顺序命名为4位文件名称（例如 0001.png）。检测和注释文件是简单的逗号txt文件。每行代表一个对象实例，包含 7个值，如表3-3所示。

![image](https://github.com/ALLEN-ZHUDI/data/assets/55532249/102ab8f7-1fd3-450d-99f1-4410838aee73)


数据集的训练集和测试集的划分与详情，如表3-4所示。其中包括数据集每个文件夹里包含的帧数，图片的分辨率，跟踪的目标总数，采集数据的设备是静态的还是动态的，车辆目标的密集程度，无人机视角的高度以及天气状况等。

![image](https://github.com/ALLEN-ZHUDI/data/assets/55532249/60fc088a-981d-4450-b9f1-ebf6f32cf602)

# 数据集图示

![image](https://github.com/ALLEN-ZHUDI/data/assets/55532249/a46ec160-a5c2-4466-8139-6811e9ea87bc)

# 数据集下载
链接：https://pan.baidu.com/s/1BlvEPiusO4bULnUBjz3pwA 
提取码：g3dw
