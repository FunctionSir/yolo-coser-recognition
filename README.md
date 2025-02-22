# yolo-coser-recognition
基于YOLO的Coser检测模型.  
当前最新版本: 20250212, 数据集大小: 1061 imgs.  
欢迎发Issue/Email进行讨论(电邮请见我的GitHub Profile).  
**注意: 可能出现匪夷所思的检测结果, 若遇到此种情况, 请哈哈大笑, 谢谢!**

## 基本信息
Ver 20250210: Epochs = 300, Batch = 48, 701 imgs.  
Ver 20250211: Epochs = 100, Batch = 16, 901 imgs.  
Ver 20250212: Epochs = 200, Batch = 16, 1061 imgs.  
当前数据集为包含1061张各种Coser照片(可能有少量重复)的, 自行标注(使用labelme)的数据集.  
数据集中所有图片均被用于训练.  
当前最新版本的模型使用了一块Nvidia GTX 1050Ti (4GiB GDDR显存) 进行训练.

## 使用
1. 安装Python 3 (最新版本即可).
2. 创建并激活venv (可选, 但强烈推荐)
3. pip install ultralytics (若您是中国大陆用户, pip install ultralytics -i https://pypi.tuna.tsinghua.edu.cn/simple 也许会更快)
4. pip install onnx onnxslim onnxruntime (若您是中国大陆用户, pip install onnx onnxslim onnxruntime -i https://pypi.tuna.tsinghua.edu.cn/simple 也许会更快)
5. yolo predict task=detect model='模型文件的路径, 最好使用onnx格式的, 速度更快' imgsz=640 source='图像/视频/含有待检测材料的文件夹路径' conf=您希望置信度大于的值

## 数据集内容
包括以下共68个角色(按归属分类, 括号内是对应标签)的Coser照片(含Kigurumi, 但较少; 目前暂时不含Furry), 基本可保证每个角色至少5张对应照片.

### VOCALOID
初音未来(coser-hatsune_miku), 洛天依(coser-luo_tianyi).

### 某科学的超电磁炮
御坂美琴(coser-misaka_mikoto), 白井黑子(coser-shirai_kuroko), 初春饰利(coser-uiharu_kazari), 佐天泪子(coser-saten_ruiko).

### 魔法禁书目录
茵蒂克丝(coser-index).

### 情色漫画老师
和泉纱雾(coser-izumi_sagiri).

### 哔哩哔哩
22(coser-22), 33(coser-33).

### 原神
荧(coser-lumine), 派蒙(coser-paimon), 琴(coser-jean_gunnhildr), 安柏(coser-amber), 芭芭拉(coser-barbara_gunnhildr), 温迪(coser-barbatos), 可莉(coser-klee), 菲谢尔(coser-fischl), 砂糖(coser-sucrose), 优菈(coser-eula_lawrence), 香菱(coser-xiangling), 刻晴(coser-keqing), 七七(coser-qiqi), 胡桃(coser-hu_tao), 神里绫华(coser-kamisato_ayaka), 纳西妲(coser-nahida), 芙宁娜(coser-furina), 夏洛蒂(coser-charlotte), 珐露珊(coser-faruzan), 绮良良(coser-kirara), 莱依拉(coser-layla), 琳妮特(coser-lynette), 钟离(coser-morax), 宵宫(coser-naganohara_yoimiya), 妮露(coser-nilou), 诺艾尔(coser-noelle), 珊瑚宫心海(coser-sangonomiya_kokomi), 早柚(coser-sayu), 希格雯(coser-sigewinne), 行秋(coser-xingqiu), 莫娜(coser-mona), 八重神子(coser-yae_miko), 申鹤(coser-shenhe), 烟绯(coser-yanfei), 提纳里(coser-tighnari), 柯莱(coser-collei), 云堇(coser-yun_jin), 多莉(coser-dori).

### 明日方舟
W(coser-w), 杜林(coser-durin), 艾丽妮(coser-irene).

### 崩坏: 星穹铁道
流萤(coser-firefly).

### 孤独摇滚
后藤独(coser-gotoh_hitori), 伊地知虹夏(coser-ijichi_nijika), 山田凉(coser-yamada_ryo), 喜多郁代(coser-kita_ikuyo).

### 蔚蓝档案
白洲梓(coser-shirasu_azusa), 砂狼白子(coser-sunaokami_shiroko).

### 我的妹妹哪有这么可爱
高坂桐乃(coser-kousaka_kirino), 五更琉璃(coser-gokou_ruri).

### 你的名字
宫水三叶(coser-miyamizu_mitsuha).

### 天气之子
天野阳菜(coser-hina_amano).

### 铃芽之旅
岩户铃芽(coser-iwato_suzume).

### 间谍过家家
阿尼亚(coser-anya_forger).

### 葬送的芙莉莲
芙莉莲(coser-frieren).

### 绝区零
铃(coser-belle).

### 魔法少女小圆
巴麻美(coser-tomoe_mami), 鹿目圆(coser-kaname_madoka).

## 为什么可能没有您喜欢的角色
由于此类数据集恐怕缺少, 故数据集乃是我自行收集图片并进行标注, 最后转换而成. 然而, 一个人, 纵使穷尽几乎所有空闲, 依然难以浩如烟海的二次元世界. 若您可以帮助, 那简直是太感谢了. 您可以发电邮来提供"收录建议", 也可以询问如何进行标注从而帮助进行标注工作. 但无论您是否想要帮助我, 都感谢您看到了这个项目.

## 关于许可证的问题
显而易见的, 我不是一位法律专业人士, 故选择了与YOLOv11相同的AGPL-3.0许可证. 若您有相关的建议, 欢迎发Issue来讨论.

## 关于获取数据集的问题
我很乐意于分享我的标注成果, 然而, 鉴于使用到的图片是从互联网上下载下来的, 作者众多, 许可证繁杂, 故自觉直接放出来不妥. 若您想要, 可以发邮件给我, 我视情况给您. 也欢迎大家提出相关的建议. 毕竟我并非法律专业人士.

## 当前部分dataset.yaml的内容
``` yaml
names:
    0: coser-klee
    1: coser-hatsune_miku
    2: coser-sangonomiya_kokomi
    3: coser-barbara_gunnhildr
    4: coser-kamisato_ayaka
    5: coser-nahida
    6: coser-mona
    7: coser-misaka_mikoto
    8: coser-sunaokami_shiroko
    9: coser-izumi_sagiri
    10: coser-miyamizu_mitsuha
    11: coser-furina
    12: coser-keqing
    13: coser-morax
    14: coser-charlotte
    15: coser-faruzan
    16: coser-noelle
    17: coser-kita_ikuyo
    18: coser-yamada_ryo
    19: coser-ijichi_nijika
    20: coser-gotoh_hitori
    21: coser-jean_gunnhildr
    22: coser-kousaka_kirino
    23: coser-shirai_kuroko
    24: coser-amber
    25: coser-layla
    26: coser-eula_lawrence
    27: coser-firefly
    28: coser-gokou_ruri
    29: coser-luo_tianyi
    30: coser-barbatos
    31: coser-durin
    32: coser-sigewinne
    33: coser-lynette
    34: coser-yae_miko
    35: coser-hu_tao
    36: coser-shenhe
    37: coser-lumine
    38: coser-sucrose
    39: coser-nilou
    40: coser-iwato_suzume
    41: coser-saten_ruiko
    42: coser-xiangling
    43: coser-paimon
    44: coser-yanfei
    45: coser-uiharu_kazari
    46: coser-qiqi
    47: coser-w
    48: coser-shirasu_azusa
    49: coser-tighnari
    50: coser-sayu
    51: coser-22
    52: coser-kirara
    53: coser-collei
    54: coser-naganohara_yoimiya
    55: coser-fischl
    56: coser-33
    57: coser-anya_forger
    58: coser-yun_jin
    59: coser-frieren
    60: coser-xingqiu
    61: coser-belle
    62: coser-irene
    63: coser-hina_amano
    64: coser-tomoe_mami
    65: coser-index
    66: coser-kaname_madoka
    67: coser-dori
```