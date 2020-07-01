# CHS-DRG 野生分组器

### CHS_DRG_GROUPER
#### (China Healthcare Security Diagnosis Related Groups，CHS-DRG)
## 概述
- 一个依据 <医保办发〔2020〕29号 > 做的野生分组器<br>
（A home made DRG Grouper based on the file 2020-29）
- 发现国家公布了CHS-DRG的分组方案，较前一版增加了DRG组，<br>
从医学角度看，这版分组还是比较严谨的，就ICD的细分度和米国ICD异曲同工，<br>
将PDF转成csv过程中发现治疗方式的手术组合也制定了详细规则，如肾/胰移植和脊柱前后路手术等，<br>
总之，有了这版方案原则，基本上就可以自己构建个分组器玩玩了
- 于是准备空余时间用Python写一个，但没有实际数据验证，部分code只能先按理论来

### Notes
- 以下几个ADRG因为没有具体ICD10或9对应，不小心dropna去掉了，貌似暂时也用不上

|ADRG|Count|
|---|---|
|DD1|1|
|XJ1|1|
|TB1|1|
|BC2|1|
|ZZ1|1|
|SB1|1|
|VC1|1|
|WJ1|1|

- 整理MCC、CC的排除规则表发现原文件 **表7-18** 表是缺失的，目前原因未知
- 发现http://www.nhsa.gov.cn/robots.txt 是404，暂且就取医保局网上的ICD编码信息生成一些虚拟病案首页信息
