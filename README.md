# yolo-coser-recognition
基于YOLO的Coser检测模型.  
当前最新版本: 20250210, 数据集大小: 701 imgs.  
欢迎发Issue/Email进行讨论(电邮请见我的GitHub Profile).  
**注意: 可能出现匪夷所思的检测结果, 若遇到此种情况, 请哈哈大笑, 谢谢!**

## 基本信息
Epoch = 300, Batch = 48.  
数据集为包含701张各种Coser照片(可能有少量重复)的, 自行标注(使用labelme)的数据集.  
数据集中所有图片均被用于训练.  
当前最新版本的模型的训练是在一台运行Arch Linux的Dell Vostro 3400笔记本电脑上使用Intel Core i5-1135G7 CPU耗时24小时左右完成的. 全程没有使用GPU(你猜为啥不用).

## 使用
1. 安装Python 3 (最新版本即可).
2. 创建并激活venv (可选, 但强烈推荐)
3. pip install ultralytics (若您是中国大陆用户, pip install ultralytics -i https://pypi.tuna.tsinghua.edu.cn/simple 也许会更快)
4. yolo predict task=detect model=runs/detect/train17/weights/best.onnx imgsz=640 source='图像/视频/含有待检测材料的文件夹路径' conf=您希望置信度大于的值

## 数据集内容
包括以下共37个角色(按归属分类, 括号内是对应标签)的Coser照片(含Kigurumi, 但较少; 目前暂时不含Furry), 基本可保证每个角色至少5张对应照片.

### VOCALOID
初音未来(coser-hatsune_miku), 洛天依(coser-luo_tianyi).

### 某科学的超电磁炮
御坂美琴(coser-misaka_mikoto), 白井黑子(coser-shirai_kuroko).

### 魔法禁书目录
茵蒂克丝(coser-index).

### 情色漫画老师
和泉纱雾(coser-izumi_sagiri).

### 哔哩哔哩
22(coser-22), 33(coser-33).

### 原神
荧(coser-lumine), 派蒙(coser-paimon), 琴(coser-jean_gunnhildr), 安柏(coser-amber), 芭芭拉(barbara_gunnhildr), 温迪(coser-barbatos), 可莉(coser-klee), 菲谢尔(coser-fischl), 砂糖(coser-sucrose), 优菈(coser-eula_lawrence), 香菱(coser-xiangling), 刻晴(coser-keqing), 七七(coser-qiqi), 胡桃(coser-hu_tao), 神里绫华(coser-kamisato_ayaka), 纳西妲(coser-nahida), 芙宁娜(coser-furina), 夏洛蒂(coser-charlotte).

### 明日方舟
W(coser-w), 杜林(coser-durin).

### 崩坏: 星穹铁道
流萤(coser-firefly).

### 孤独摇滚
后藤独(coser-gotoh_hitori), 伊地知虹夏(coser-ijichi_nijika), 山田凉(coser-yamada_ryo), 喜多郁代(coser-kita_ikuyo).

### 蔚蓝档案
白洲梓(coser-shirasu_azusa), 砂狼白子(coser-sunaokami_shiroko).

### 我的妹妹哪有这么可爱
高坂桐乃(coser-kousaka_kirino), 五更琉璃(coser-gokou_ruri).

## 为什么可能没有您喜欢的角色
由于此类数据集恐怕缺少, 故数据集乃是我自行收集图片并进行标注, 最后转换而成. 然而, 一个人, 纵使穷尽几乎所有空闲, 依然难以浩如烟海的二次元世界. 若您可以帮助, 那简直是太感谢了. 您可以发电邮来提供"收录建议", 也可以询问如何进行标注从而帮助进行标注工作. 但无论您是否想要帮助我, 都感谢您看到了这个项目.

## 关于许可证的问题
显而易见的, 我不是一位法律专业人士, 故选择了与YOLOv11相同的AGPL-3.0许可证. 若您有相关的建议, 欢迎发Issue来讨论.

## 关于获取数据集的问题
我很乐意于分享我的标注成果, 然而, 鉴于使用到的图片是从互联网上下载下来的, 作者众多, 许可证繁杂, 故自觉直接放出来不妥. 若您想要, 可以发邮件给我, 我视情况给您. 也欢迎大家提出相关的建议. 毕竟我并非法律专业人士.

## 下一步进展
当前数据集大小: 801 imgs (771已标注, 30未标注).  
新角色加入: 初春饰利, 佐天泪子, 艾丽妮, 珐露珊, 林尼特, 希格雯.

## 部分dataset.yaml的内容
``` yaml
names:
    0: coser-izumi_sagiri
    1: coser-luo_tianyi
    2: coser-eula_lawrence
    3: coser-jean_gunnhildr
    4: coser-paimon
    5: coser-firefly
    6: coser-shirasu_azusa
    7: coser-barbara_gunnhildr
    8: coser-hatsune_miku
    9: coser-w
    10: coser-xiangling
    11: coser-sucrose
    12: coser-kousaka_kirino
    13: coser-kamisato_ayaka
    14: coser-misaka_mikoto
    15: coser-ijichi_nijika
    16: coser-kita_ikuyo
    17: coser-yamada_ryo
    18: coser-gotoh_hitori
    19: coser-index
    20: coser-klee
    21: coser-22
    22: coser-lumine
    23: coser-durin
    24: coser-shirai_kuroko
    25: coser-charlotte
    26: coser-sunaokami_shiroko
    27: coser-amber
    28: coser-nahida
    29: coser-furina
    30: coser-barbatos
    31: coser-gokou_ruri
    32: coser-fischl
    33: coser-keqing
    34: coser-hu_tao
    35: coser-33
    36: coser-qiqi
```