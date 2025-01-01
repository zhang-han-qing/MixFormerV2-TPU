# 说明
本项目用于导出 [MixFomrerV2](https://github.com/MCG-NJU/MixFormerV2) 的 ONNX 模型。模型导出后可通过 [TPUMLIR](https://tpumlir.org/) 将模型部署到SOPHGO BM168x系列的产品上。 

本项目对MixFormerV2的代码进行了剪枝优化，减少了推理过程中一部分冗余的计算。然而，需要注意的是，本项目提供的代码仅对backbone为vit的MixFormerV2模型（mixformer2_vit_online, 224_depth4_mlp1_score）验证过有效。如您正在适配其他配置下的MixFormerV2模型，可参考本项目自行修改源码。


# 使用方法 
参照[MixFomrerV2](https://github.com/MCG-NJU/MixFormerV2)项目配置环境、准备数据集和模型检查点（如`mixformerv2_small.pth.tar`）， 运行 `tracking/test.py`即可 