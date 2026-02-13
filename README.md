# Keeko IME Unit Dictionary

## 一个按 城市(city) 与 县城(countyTown) 维度拆分的地名输入法词库仓库。

适用于：
- 小狼毫 / Rime
- 搜狗输入法
- 百度输入法
- QQ输入法
- 其他支持自定义词库的输入法


## 仓库结构
<pre>
├── city/                  # 城市级别地名
│   ├── shanghai.yaml         # 上海
│   ├── nanjing.yaml
│   ├── hangzhou.yaml         # 杭州 (地级市、也是省会)(该词库文件包含杭州市下辖的区、街道。不包含淳安县、建德市等词库)
│   ├── jinhua.yaml           # 金华 (地级市)(金华市词库中不包含义乌市，武义县等countyTown级别词库)
│   └── ...
│
├── countyTown/            # 县城级别地名
│   ├── zhejiang/             #浙江省
│   │   ├── ninghai.yaml           #宁海县 (该词库文件包含宁海县下辖的街道、乡镇)
│   │   ├── yiwu.yaml              #义乌市 (县级市)
│   │   └── ...
│   │
│   ├── guangxi/              #广西壮族自治区
│   │   ├── yangshuo.yaml          #阳朔县 (该词库文件包含阳朔县下辖的街道、乡镇)
│   │   ├── gongchengyaozu.yaml    #恭城瑶族自治县
│   │   └── ...
│   └── ...
└── README.md
</pre>


## 数据分类说明

1️⃣ 城市(city) 市级行政级别

包含：
直辖市
地级市
自治州
特别行政区

2️⃣ 县城(countyTown) 县级行政级别

包含：
县
县级市
自治县
旗


## 设计原则

1. city 不包含 countyTown 粒度
2. countyTown 为最小可维护单元 (不再细分)
3. 词库之间避免重复收录 (允许不同行政单位下的重名区、县，如杭州市-西湖区、南昌市-西湖区，重庆市-江北区、宁波市-江北区)
