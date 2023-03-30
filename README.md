# Few-Shot-Learning-for-Intrusion-Detection-in-Railway-Video-Surveillance
这是一个基于小样本学习的用于铁路入侵检测的项目，代码基于PaddlePaddle实现。  
深度学习模型在实际铁路部署中具有场景差异问题及侵限小样本问题，这两个问题导致现有传统深度学习模型在实际铁路视频监控场景中迁移困难、样本稀少等问题，因此本项目设计了一个基于MAML(Model-Agnostic Meta-Learning)算法的铁路入侵检测模型，在背景差异较大的测试场景下，仅通过少量标注数据，即可达到较高的入侵检测准确率。  
本项目代码主要包括以下文件：  
* learner.py 构建入侵检测基模型，用于入侵检测分类任务的具体实现
* meta.py 构建元模型，该元模型旨在为基模型寻找最优的初始化参数
* local_dataset_ds_msk.py 构建数据集，从数据集中按场景进行划分并抽样得到训练及测试任务
* train_msk.py 基于掩码增强的模型训练
* test.py 目标场景下的模型测试
* maml_9.pdparams 经过训练后的模型权重，可以直接用于模型测试

