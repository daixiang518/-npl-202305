# npl-202305
# -npl-202305
面向藏语文本标题生成任务
<br>
1. 任务背景
文本标题生成是自然语言生成研究的一个重要方向，近年来受到学术界和工业界的广泛关注。文本标题生成旨在生成能够概括或评价文本主要内容的简短、连贯且信息丰富的标题。针对标题生成的研究有助于阅读者快速获取文本主要内容和主旨，也可以避免标题缺失或者题不对文对读者的误导。通过本共享任务，我们希望能够吸引更多研究者和开发者关注藏语文本生成研究。通过针对藏语文本标题生成研究，进一步推动藏语生成理论和实践问题的研究水平。本任务得到中国中文信息学会自然语言生成专业委员会（筹）支持，将在中国自然语言生成大会召开研讨会，并在大会上对获奖团队颁奖。
2. 任务介绍
本任务给定藏语文本作为模型输入，要求参与者设计实现藏语文本标题生成模型，使模型根据输入文本生成包含文本主要内容和主旨且自然流畅的藏语标题。
<br>
3. 数据集简介
数据为csv格式，包括标题和文本两列，中间用逗号隔开,每一行对应一个样本。示例如下：

<TABLE class=MsoTableGrid style="BORDER-TOP: medium none; BORDER-RIGHT: medium none; BORDER-COLLAPSE: collapse; BORDER-BOTTOM: medium none; BORDER-LEFT: medium none; mso-table-layout-alt: fixed; mso-border-alt: solid windowtext 1.0pt; mso-yfti-tbllook: 1184; mso-padding-alt: 0cm 5.4pt 0cm 5.4pt; mso-border-insideh: 1.0pt solid windowtext; mso-border-insidev: 1.0pt solid windowtext" cellSpacing=0 cellPadding=0 width="91%" border=1><TBODY>
<TR style="HEIGHT: 20pt; mso-yfti-irow: 0; mso-yfti-firstrow: yes">
<TD style="BORDER-TOP: windowtext 1pt solid; HEIGHT: 20pt; BORDER-RIGHT: windowtext 1pt solid; WIDTH: 5.52%; BORDER-BOTTOM: windowtext 1pt solid; PADDING-BOTTOM: 0cm; PADDING-TOP: 0cm; PADDING-LEFT: 5.4pt; BORDER-LEFT: windowtext 1pt solid; PADDING-RIGHT: 5.4pt" width="5%">
<P class=MsoNormal style="TEXT-ALIGN: center; LINE-HEIGHT: 150%; TEXT-INDENT: 24.1pt; mso-char-indent-count: 2.0" align=center><B><SPAN lang=EN-US style="FONT-SIZE: 12pt; FONT-FAMILY: KaiTi; LINE-HEIGHT: 150%; mso-bidi-font-family: KaiTi"><?xml:namespace prefix = "o" ns = "urn:schemas-microsoft-com:office:office" /><o:p>&nbsp;</o:p></SPAN></B></P></TD>
<TD style="BORDER-TOP: windowtext 1pt solid; HEIGHT: 20pt; BORDER-RIGHT: windowtext 1pt solid; WIDTH: 33.36%; BORDER-BOTTOM: windowtext 1pt solid; PADDING-BOTTOM: 0cm; PADDING-TOP: 0cm; PADDING-LEFT: 5.4pt; BORDER-LEFT: medium none; PADDING-RIGHT: 5.4pt; mso-border-left-alt: solid windowtext 1.0pt" width="33%">
<P class=MsoNormal style="TEXT-ALIGN: center; LINE-HEIGHT: 150%; TEXT-INDENT: 24.1pt; mso-char-indent-count: 2.0" align=center><B><SPAN style="FONT-SIZE: 12pt; FONT-FAMILY: KaiTi; LINE-HEIGHT: 150%; mso-bidi-font-family: KaiTi">标题<SPAN lang=EN-US><o:p></o:p></SPAN></SPAN></B></P></TD>
<TD style="BORDER-TOP: windowtext 1pt solid; HEIGHT: 20pt; BORDER-RIGHT: windowtext 1pt solid; WIDTH: 61.1%; BORDER-BOTTOM: windowtext 1pt solid; PADDING-BOTTOM: 0cm; PADDING-TOP: 0cm; PADDING-LEFT: 5.4pt; BORDER-LEFT: medium none; PADDING-RIGHT: 5.4pt; mso-border-left-alt: solid windowtext 1.0pt" width="61%">
<P class=MsoNormal style="TEXT-ALIGN: center; LINE-HEIGHT: 150%; TEXT-INDENT: 24.1pt; mso-char-indent-count: 2.0" align=center><B><SPAN style="FONT-SIZE: 12pt; FONT-FAMILY: KaiTi; LINE-HEIGHT: 150%; mso-bidi-font-family: KaiTi">文本<SPAN lang=EN-US><o:p></o:p></SPAN></SPAN></B></P></TD></TR>
<TR style="HEIGHT: 20pt; mso-yfti-irow: 1; mso-yfti-lastrow: yes">
<TD style="BORDER-TOP: medium none; HEIGHT: 20pt; BORDER-RIGHT: windowtext 1pt solid; WIDTH: 5.52%; BORDER-BOTTOM: windowtext 1pt solid; PADDING-BOTTOM: 0cm; PADDING-TOP: 0cm; PADDING-LEFT: 5.4pt; BORDER-LEFT: windowtext 1pt solid; PADDING-RIGHT: 5.4pt; mso-border-top-alt: solid windowtext 1.0pt" width="5%">
<P class=MsoNormal><SPAN style="FONT-SIZE: 12pt; FONT-FAMILY: KaiTi; mso-bidi-font-family: KaiTi">藏语<SPAN lang=EN-US><o:p></o:p></SPAN></SPAN></P></TD>
<TD style="BORDER-TOP: medium none; HEIGHT: 20pt; BORDER-RIGHT: windowtext 1pt solid; WIDTH: 33.36%; BORDER-BOTTOM: windowtext 1pt solid; PADDING-BOTTOM: 0cm; PADDING-TOP: 0cm; PADDING-LEFT: 5.4pt; BORDER-LEFT: medium none; PADDING-RIGHT: 5.4pt; mso-border-left-alt: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext 1.0pt" width="33%">
<P class=MsoNormal><SPAN lang=BO style='FONT-SIZE: 12pt; FONT-FAMILY: "Microsoft Himalaya"; mso-ansi-font-size: 10.5pt; mso-bidi-language: BO'>སློབ་འབྲིང་བོད་སྐད་ཡིག་སྦྱོང་བའི་སྤྲོ་བ་སྐྱེད་བསྲིང་བྱ་ཐབས་སྐོར་མདོ་ཙམ་གླེང་བ།<o:p></o:p></SPAN></P>
<P class=MsoNormal><SPAN lang=EN-US style='FONT-SIZE: 10pt; FONT-FAMILY: "Times New Roman",serif'><o:p>&nbsp;</o:p></SPAN></P></TD>
<TD style="BORDER-TOP: medium none; HEIGHT: 20pt; BORDER-RIGHT: windowtext 1pt solid; WIDTH: 61.1%; BORDER-BOTTOM: windowtext 1pt solid; PADDING-BOTTOM: 0cm; PADDING-TOP: 0cm; PADDING-LEFT: 5.4pt; BORDER-LEFT: medium none; PADDING-RIGHT: 5.4pt; mso-border-left-alt: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext 1.0pt" width="61%">
<P class=MsoNormal><SPAN lang=BO style='FONT-SIZE: 12pt; FONT-FAMILY: "Microsoft Himalaya"; mso-ansi-font-size: 10.5pt; mso-bidi-language: BO'>སློབ་ཁྲིད་ཡག་པོ་བྱས་ཏེ་ཤེས་ལྡན་མི་སྣ་གང་མང་ཞིག་གསོ་སྐྱོང་བྱ་རྒྱུ་ནི་དགེ་བའི་བཤེས་གཉེན་ཚོའི་འགན་འཁྲི་དོར་མེད་ཅིག་ཡིན་ལ།ལས་འགན་དེ་སྒྲུབ་པའི་བརྒྱུད་རིམ་ནང་སློབ་སྦྱོང་བྱེད་འདོད་ཀྱི་སྤྲོ་བ་སྐྱེད་བསྲིང་བྱེད་རྒྱུ་ནི་ལས་འགན་དེ་ལེགས་འགྲུབ་ཡོང་བའི་སྔོན་འགྲོའི་ཆ་རྐྱེན་ཞིག་ཀྱང་རེད།གལ་སྲིད་སྦྱངས་བྱའི་ཡོན་ཏན་ལ་སྤྲོ་བ་སྐྱེད་གྱུར་ན་རིག་ཚན་གང་ཞིག་སྦྱངས་རུང་ཚེགས་མེད་དུ་ཤེས་ཐུབ་ཅིང་དེ་ཡང་རང་ཉིད་ཀྱི་ལོ་འགའི་སློབ་ཁྲིད་ཀྱི་ཉམས་མྱོང་ལས་ཤེས་གསལ་རེད།དེང་སྐབས་སློབ་མ་ཁག་ཅིག་བོད་སྐད་ཡིག་སྦྱོང་འདོད་ཀྱི་སྤྲོ་བ་དེ་ཙམ་ཆེན་པོ་མེད་ལ་ཧུར་བརྩོན་རང་བཞིན་ཡང་ཆེན་པོ་མེད་པར་བརྟེན་སློབ་སྦྱོང་གི་སྦྱངས་འབྲས་ཀྱང་ཚད་ངེས་ཅན་ཞིག་དང་བློ་ཡིད་འཚིམ་པ་ཞིག་ཐོབ་ཀྱི་མེད།</SPAN></P></TD></TR></TBODY></TABLE>
4. 评价指标
本任务采用ROUGE-1，ROUGE-2和ROUGE-L作为评价指标衡量生成标题和标准答案之间的相似性。
<br>
5. 时间安排
	时间	说明
报名注册	5月8日	发布共享任务说明，接受参与者报名
发布训练集	5月10日	发布训练数据集
发布测试集	6月25日	发布测试数据集
提交结果	7月1日	提交测试数据集结果和技术报告
评测会议	7月23日	发布任务最终结果，并进行颁奖和研讨
<br>
6. 发起单位
发起单位：青海师范大学、中央民族大学
指导单位：中国中文信息学会自然语言生成与智能写作专业委员会（筹）
 	 	 
李琳，青海师范大学
赵小兵，中央民族大学
联系方式：meetingqhnu@sohu.com<br>
7. 反作弊声明
(1)	参与者禁止注册多账户报名，经发现将取消成绩并严肃处理。
(2)	参与者禁止在指定考核技术能力的范围外利用规则漏洞或技术漏洞等不良途径提高成绩排名，经发现将取消成绩并严肃处理。
(3)	可以接触到赛题相关数据的人员，其提交结果将不计入排行榜及评奖。<br>
  8. 交流平台
主办方建立技术讨论群（微信群），供选手讨论、沟通，主办方也将安排工作人员定期在群内答疑，且后续的相关活动信息均会在群内发布。

### Github地址：https://github.com/daixiang518/npl-202305
### 如遇数据集下载不了或者下载缓慢问题，请使用百度网盘下载：链接：https://pan.baidu.com/s/1wEtslAw2z4HDSGwkpnJQ7g  提取码：2023

