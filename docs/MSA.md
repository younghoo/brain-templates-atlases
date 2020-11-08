# [MSA](https://github.com/yetianmed/subcortex)

## 构建方法

* 样本使用的是HCP 3T（n=1080）和7T（n=183）的静息态fMRI数据

* 计算皮下体素与皮层灰质的功能连接矩阵、皮下体素间的相似性矩阵、计算adjacency matrix/Laplacian matrix以及对应的eigenvalues/eigenvectors、第二小的eigenvalue对应的eigenvector能够解释最多的功能连接的变化，即反映功能连接梯度。
* 估计梯度变化的方向和大小、根据梯度主方向重建出梯度变化的曲线（类似于弥散成像中的纤维束追踪方法）、根据梯度的局部最大值和假设检验可以大致分割出（单侧）８个区域，称为Scale I Atlas，包括杏仁核、海马、苍白球、腹隔核、尾状核、壳核以及前后部丘脑。
* 在Scale I Atlas的8个区域中，分别重复上述过程，每个区域进一步细分，共可以划分出（单侧）16个区域，这是Scale II Atlas；重复前面的步骤（直到边界不再显著），可以得到Scale III Atlas，包含（单侧）25个区域，和Scale IV Atlas，包含（单侧）27个区域。

## 下载地址

* https://github.com/yetianmed/subcortex
* 模板提供NIFTI/CIFTI两种格式
* 模板提供MNI152 Non-linear 6th generation Asymmetric和MNI152 Non-linear 2009c Asymmetric两种模板空间
* 提供3T/7T两种模板（7T的分区多一些）
* 提供了个体化分区工具

## 参考资料

* Tian, Y., Margulies, D. S., Breakspear, M., & Zalesky, A. (2020). Topographic organization of the human subcortex unveiled with functional connectivity gradients. *Nature Neuroscience*, 23(11), 1421–1432.

