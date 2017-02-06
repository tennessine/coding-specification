#数字化研发部GIS开发编程规范
GIS for R&D Department —— ecidi
##阅读对象
>本文主要针对数字化研发部研发过程中需遵循的一般规范和原则，阅读对象主要是编程人员。
##基本术语
>__地理数据 geographic data__ 直接或间接关联着相对于地球的某个地点的数据；

>__地理信息 geographic information__ 关于那些直接或者间接涉及相对于地球的某个地点的现象的信息；

>__地理信息服务 geographic information service__ 为用户转换、管理或提供地理信息的服务；

>__本体 population__ 被分析的事物；

>__编码 encoding__  数据转变为系列代码；

>__标识符 identitifer__ 用来唯一识别一个项或者一组项的标记；

>__插值法 interpolation method__ 在离散数据的基础上补插出连续函数值，利用这种方法可通过函数在有限个点处的取值状况，估算该函数在其他点处的值；

>__串 string__ 给定数据类型的元素的一种有序排列；

>__坐标系 coordinate system__ 以位置参考框架为基础，对于单个点的位置以及立体空间、平面或线中的各点几个关系的数学描述；

>__大地参照系 geodetic reference system__ 以规定了原点位置和坐标轴方向的大地基准为基础的坐标系；

>__大地基准 geodetic datum__ 大地坐标系的基本参照依据，包括参考椭球参数和定位参数及大地坐标的起算数据；

>__大地坐标 geodetic coordinate__ 大地测量中以参考椭球面为基准面的坐标，通常以大地经度L、大地维度B和大地高H表示；

>__要素 feature__ 真实世界现象的抽象；

>__节点 node__ 零维拓扑元素；

>__面 face__ 二维拓扑元素；

>__矢量地图 vector map__ 数据基于图论数据模型的地图；

>__矢量数据 vector data__ 由几何元素所表示的数据；

>__属性 attribute domain__ 一个属性能接受的元数据元素值的有效值范围或集合；

>__数据集 dataset__ 可标识的数据集合；

>__数据结构 data structure__ 为存储、访问、传送和获得数据所使用的计算机可读的格式；

>__数据类型 data type__ 可以赋给数据元的值的种类，例如：整型、试型、文本型、日期型等；

>__数据元 data element__ 在确定的范围内被认为不可再细分的数据单位；

>__拓扑 topology__ 对相连或相邻的点、线、面之间的关系的科学阐述，特指那种在连续映射变换下保持不变的对象性质；

>__拓扑关系 topology relationship__ 描述两个要素之间边界拓扑和点集拓扑的要素关系；

##GIS国家标准
>开发过程中涉及GIS标准问题，可参照标准链接，该标准并未更新，开发时需以国家出台最新标准为主要依据；

###地理信息基础概念相关标准
>[地理信息技术基本术语](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9C%B0%E7%90%86%E4%BF%A1%E6%81%AF%E6%8A%80%E6%9C%AF%E5%9F%BA%E6%9C%AC%E6%9C%AF%E8%AF%AD.pdf "地理信息技术基本术语")

>[地理信息一致性与测试](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9C%B0%E7%90%86%E4%BF%A1%E6%81%AF%E4%B8%80%E8%87%B4%E6%80%A7%E4%B8%8E%E6%B5%8B%E8%AF%95.pdf "地理信息一致性与测试")

>[地理信息元数据](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9C%B0%E7%90%86%E4%BF%A1%E6%81%AF%E5%85%83%E6%95%B0%E6%8D%AE.pdf "地理信息元数据")

###地图数据相关标准
>[地图符号库建立的基本规定](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9C%B0%E5%9B%BE%E7%AC%A6%E5%8F%B7%E5%BA%93%E5%BB%BA%E7%AB%8B%E7%9A%84%E5%9F%BA%E6%9C%AC%E8%A7%84%E5%AE%9A.pdf "地图符号库建立的基本规定")

>[地形图数字化规范](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9C%B0%E5%BD%A2%E5%9B%BE%E6%95%B0%E5%AD%97%E5%8C%96%E8%A7%84%E8%8C%83.pdf "地形图数字化规范")

>[地形图要素分类与代码](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9C%B0%E5%BD%A2%E5%9B%BE%E8%A6%81%E7%B4%A0%E5%88%86%E7%B1%BB%E4%B8%8E%E4%BB%A3%E7%A0%81.pdf "地形图要素分类与代码")

>[地理网格](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9C%B0%E7%90%86%E7%BD%91%E6%A0%BC.pdf "地理网格")

>[地理点位置的纬度、经度和高程的标准表示法](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9C%B0%E7%90%86%E7%82%B9%E4%BD%8D%E7%BD%AE%E7%9A%84%E7%BA%AC%E5%BA%A6%E3%80%81%E7%BB%8F%E5%BA%A6%E5%92%8C%E9%AB%98%E7%A8%8B%E7%9A%84%E6%A0%87%E5%87%86%E8%A1%A8%E7%A4%BA%E6%B3%95.pdf "地理点位置的纬度、经度和高程的标准表示法")

>[国家基本比例尺地形图分幅和编号](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9B%BD%E5%AE%B6%E5%9F%BA%E6%9C%AC%E6%AF%94%E4%BE%8B%E5%B0%BA%E5%9C%B0%E5%BD%A2%E5%9B%BE%E5%88%86%E5%B9%85%E5%92%8C%E7%BC%96%E5%8F%B7.pdf "国家基本比例尺地形图分幅和编号")

>[遥感影响平面图制作规范](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E9%81%A5%E6%84%9F%E5%BD%B1%E5%93%8D%E5%B9%B3%E9%9D%A2%E5%9B%BE%E5%88%B6%E4%BD%9C%E8%A7%84%E8%8C%83.pdf "遥感影响平面图制作规范")

>[专题地图信息分类与代码](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E4%B8%93%E9%A2%98%E5%9C%B0%E5%9B%BE%E4%BF%A1%E6%81%AF%E5%88%86%E7%B1%BB%E4%B8%8E%E4%BB%A3%E7%A0%81.pdf "专题地图信息分类与代码")

>[中华人民共和国行政区划代码](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E4%B8%AD%E5%8D%8E%E4%BA%BA%E6%B0%91%E5%85%B1%E5%92%8C%E5%9B%BD%E8%A1%8C%E6%94%BF%E5%8C%BA%E5%88%92%E4%BB%A3%E7%A0%81.pdf "中华人民共和国行政区划代码")

###基础地理信息数字产品标准
>[基础地理信息数字产品 元数据](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9F%BA%E7%A1%80%E5%9C%B0%E7%90%86%E4%BF%A1%E6%81%AF%E6%95%B0%E5%AD%97%E4%BA%A7%E5%93%81%20%E5%85%83%E6%95%B0%E6%8D%AE.pdf "基础地理信息数字产品 元数据")

>[基础地理信息数字产品 数据文件命名规则](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9F%BA%E7%A1%80%E5%9C%B0%E7%90%86%E4%BF%A1%E6%81%AF%E6%95%B0%E5%AD%97%E4%BA%A7%E5%93%81%20%E6%95%B0%E6%8D%AE%E6%96%87%E4%BB%B6%E5%91%BD%E5%90%8D%E8%A7%84%E5%88%99.pdf "基础地理信息数字产品 数据文件命名规则")

>[基础地理信息数字产品 数字高程模型](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9F%BA%E7%A1%80%E5%9C%B0%E7%90%86%E4%BF%A1%E6%81%AF%E6%95%B0%E5%AD%97%E4%BA%A7%E5%93%81%20%E6%95%B0%E5%AD%97%E9%AB%98%E7%A8%8B%E6%A8%A1%E5%9E%8B.pdf "基础地理信息数字产品 数字高程模型")

>[基础地理信息数字产品 数字栅格地图](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9F%BA%E7%A1%80%E5%9C%B0%E7%90%86%E4%BF%A1%E6%81%AF%E6%95%B0%E5%AD%97%E4%BA%A7%E5%93%81%20%E6%95%B0%E5%AD%97%E6%A0%85%E6%A0%BC%E5%9C%B0%E5%9B%BE.pdf "基础地理信息数字产品 数字栅格地图")

>[基础地理信息数字产品 数字正射影像图](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%9F%BA%E7%A1%80%E5%9C%B0%E7%90%86%E4%BF%A1%E6%81%AF%E6%95%B0%E5%AD%97%E4%BA%A7%E5%93%81%20%E6%95%B0%E5%AD%97%E6%AD%A3%E5%B0%84%E5%BD%B1%E5%83%8F%E5%9B%BE.pdf "基础地理信息数字产品 数字正射影像图")

###地理信息其他相关标准
>[世界各国和地区名称代码](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E4%B8%96%E7%95%8C%E5%90%84%E5%9B%BD%E5%92%8C%E5%9C%B0%E5%8C%BA%E5%90%8D%E7%A7%B0%E4%BB%A3%E7%A0%81.pdf "世界各国和地区名称代码")

>[县级以下行政区划代码编制规则](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%8E%BF%E7%BA%A7%E4%BB%A5%E4%B8%8B%E8%A1%8C%E6%94%BF%E5%8C%BA%E5%88%92%E4%BB%A3%E7%A0%81%E7%BC%96%E5%88%B6%E8%A7%84%E5%88%99.pdf "县级以下行政区划代码编制规则")

>[公路信息分类与代码](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%85%AC%E8%B7%AF%E4%BF%A1%E6%81%AF%E5%88%86%E7%B1%BB%E4%B8%8E%E4%BB%A3%E7%A0%81.pdf "公路信息分类与代码")

>[公路等级代码](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%85%AC%E8%B7%AF%E7%AD%89%E7%BA%A7%E4%BB%A3%E7%A0%81.pdf "公路等级代码")

>[公路路线标识规则](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%85%AC%E8%B7%AF%E8%B7%AF%E7%BA%BF%E6%A0%87%E8%AF%86%E8%A7%84%E5%88%99.pdf "公路路线标识规则")

>[公路桥梁命名编号和编码规则](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E5%85%AC%E8%B7%AF%E6%A1%A5%E6%A2%81%E5%91%BD%E5%90%8D%E7%BC%96%E5%8F%B7%E5%92%8C%E7%BC%96%E7%A0%81%E8%A7%84%E5%88%99.pdf "公路桥梁命名编号和编码规则")

>[水路信息分类与代码](https://github.com/ecidi/coding-specification/blob/master/GIS%20Standard/%E6%B0%B4%E8%B7%AF%E4%BF%A1%E6%81%AF%E5%88%86%E7%B1%BB%E4%B8%8E%E4%BB%A3%E7%A0%81.pdf "水路信息分类与代码")

##GIS开发规范
>目前，研发部主要基于M/S和B/S的架构进行项目实施，外围部分主要是移动端和前端的部分，故涉及的开发规范区别对待；
###数据来源
>公司主要以三维建筑及实体建模为主，故针对三维部分的数据来源由本公司负责提供、部署和维护；
###前端开发规范
>前端开发主要采用ecidi的前端框架[winterfall](https://github.com/ecidi/winterfall "winterfall")，本框架基于React、Router、Redux、Saga等技术路线实现，外围GIS项目开发团队使用该技术进行开发；
###移动端开发规范（Android）
>目前移动端开发主要基于Android平台，开发规范可查看该[链接](https://github.com/ecidi/coding-specification/blob/master/%E6%95%B0%E5%AD%97%E5%8C%96%E7%A0%94%E5%8F%91%E9%83%A8%E7%A7%BB%E5%8A%A8%E7%AB%AF%E5%BC%80%E5%8F%91%E7%BC%96%E7%A8%8B%E8%A7%84%E8%8C%83.md "移动端Android开发规范")；移动端借助[ArcGIS](http://www.esrichina.com.cn/2015/0108/2848.html 'ArcGIS for Android')、[CityMaker](http://www.citymakeronline.com/downloads.htm 'CityMaker')等SDK进行二次开发；



