# XTRACT

## 构建方法

1. 使用HCP的DWI数据，包含1021名被试；
2. 在MNI152空间手动定义了42条纤维束的seed/target/waypoint/exclusion/stop masks（位于白质内）；
3. 将MNI152空间的masks转换到每个被试的个体空间；
4. 使用概率纤维束追踪方法（FSL的bedpostx和probtrackx2）获得每条纤维束的空间分布图（每个体素的值表示有多少比例的streamline穿过该体素）；
5. 将个体空间的每条纤维束转换到MNI152空间，二值化后（阈值为0.5%）再平均，得到每条纤维束的被试分布图（每个体素的值表示有多少比例被试的纤维束包含该体素）；
6. 根据最大概率的原则得到最终的纤维束模板（hard segmentation）。

## 下载地址

* <https://github.com/SPMIC-UoN/XTRACT_atlases>
* 在FSL（6.0.2以后）中自带该分区模板。

## 其他

* 除了HCP被试的版本，还包含UK Biobank的版本（被试量1000）。
* 除了阈值为0.5%的版本，还包含0.1%的版本。
* 除了人脑的白质纤维束，还包含猴脑的版本。
* 除了模板，FSL中还包含了XTRACT的工具包，可以使用相同的方法在新的数据中重建纤维束。
* 提供了每条纤维束在灰白质边界的结束位置的皮层文件（Connectivity blueprints），即每条纤维束从哪里进入皮层灰质 。

## 参考

* Warrington, S., Bryant, K. L., Khrapitchev, A. A., Sallet, J., Charquero-Ballester, M., Douaud, G., Jbabdi, S., Mars, R. B., & Sotiropoulos, S. N. (2020). XTRACT - Standardised protocols for automated tractography in the human and macaque brain. *NeuroImage*, 217, 116923. https://doi.org/10.1016/j.neuroimage.2020.116923
