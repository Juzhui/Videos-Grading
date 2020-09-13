# Videos-Grading

使用时，选择两个相反的话题（一个好一个坏）

分别放入1,2中

使用时，将文字材料放入 raw 中，将list放入根目录

分好词的情况下直接放入wordcut

使用顺序为 word_vector svm_ann weight_cal network

1.分词：先运行word_vector，将两个话题都分好词，分词的txt会生成到wordcut文件夹中
2.训练：将1,2的wordcut中各选取2500*3个文件放入对比的wordcut中，从刚才的位置继续运行对比文件夹中的word_vector，生成wordvec模型（3个文件）

             将好的话题的wordcut文件选1000*3个复制到0_for_bad,同理1000*3个到1_for_good，运行svm_ann，生成两个模型（2个文件）
3.使用模型，将对比文件夹中的模型复制到1,2中，继续运行weight_cal 和network得到两个csv文件结果和一个图片结果	

注意修改network中list的名称(5000_Danmei_Deal.xlsx)
