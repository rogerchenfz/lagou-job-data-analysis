# lagou-job-data-analysis
Data acquisition(web crawler), processing, visualization and statistical inference

近年来，数据分析岗位的需求热度持续攀升。为了深入了解数据分析岗位的相关情况，本项目从拉勾网上爬取了2020年7月24日发布的数据分析岗位，通过数据处理、数据分析、可视化及统计推断，对数据分析岗位进行了一系列探究。

注：使用的package包括 pymysql, requests, re, random, time, json, pandas, numpy, matplotlib, seaborn, pyecharts, jieba, wordcloud, math, scikit-learn。其中 pyecharts 为1.8.1版本，scikit-learn 为0.22.2版本，部分参数与旧版本不一致，如果包为旧版本运行会报错。

# 目录
## 1  数据获取
### &emsp;1.1  创建lagou_job数据库
### &emsp;1.2  创建data_analysis表
### &emsp;1.3  headers设置及cookie获取
### &emsp;1.4  创建写入MySQL数据库的函数insert_mysql
### &emsp;1.5  创建爬取数据的函数get_data
### &emsp;1.6  调用函数爬取数据
### &emsp;1.7  *前期尝试

## 2  信息查询
### &emsp;&emsp;2.1  公司数量
### &emsp;2.2  城市数量
### &emsp;2.3  查找地点在厦门的数据分析岗位信息
### &emsp;2.4  查找经验要求不限或应届毕业生、学历要求为本科的数据分析岗位信息
### &emsp;2.5  查找特定公司的数据分析岗位信息
### &emsp;2.6  查找工作技能需要Python的数据分析岗位信息
### &emsp;2.7  在2.4的基础上查找周末双休的数据分析岗位信息

## 3  数据处理
### &emsp;3.1  删除重复数据
### &emsp;3.2  查看缺失数据

## 4  数据分析与可视化
### &emsp;4.1  数据分析岗地点分析
#### &emsp;&emsp;4.1.1  数据分析岗城市分布图
#### &emsp;&emsp;4.1.2  数据分析岗城市分布热力图
### &emsp;4.2  数据分析岗薪资分析
#### &emsp;&emsp;4.2.1  薪资总体分析
#### &emsp;&emsp;4.2.2  薪资与城市
#### &emsp;&emsp;4.2.3  薪资与工作经验
#### &emsp;&emsp;4.2.4  薪资与学历
#### &emsp;&emsp;4.2.5  薪资与公司融资阶段
#### &emsp;&emsp;4.2.6  薪资与公司规模
### &emsp;4.3  数据分析岗行业领域分析
### &emsp;4.4  数据分析岗工作技能分析
#### &emsp;&emsp;4.4.1  工作技能矩形树图
#### &emsp;&emsp;4.4.2  工作技能词云图
### &emsp;4.5  数据分析岗福利分析

## 5  统计推断
### &emsp;5.1  多元线性回归模型：以城市、工作经验、学历要求为自变量
#### &emsp;&emsp;5.1.1  对城市、工作经验、学历均使用标签编码
#### &emsp;&emsp;5.1.2  将城市的编码转化成独热编码
### &emsp;5.2  对数线性回归模型：对薪资取对数，以城市、工作经验、学历要求为自变量
#### &emsp;&emsp;5.2.1  对数线性回归
#### &emsp;&emsp;5.2.2  随机森林回归
### &emsp;5.3  对数线性回归模型：加入部分工作技能要求
#### &emsp;&emsp;5.3.1  对数线性回归
#### &emsp;&emsp;5.3.2  随机森林回归

## 6  参考
