[**中文**](./README.md) | [**English**](./README_EN.md)

<p align="center" width="100%">
<a href="" target="_blank"><img src="https://github.com/user-attachments/assets/9d0d8b09-32f3-41a3-a9e7-8ad2cb7e1721" alt="WriteGPT" style="width: 60%; min-width: 300px; display: block; margin: auto;"></a>
</p>



# 文修 (WriteGPT): 首个基于昇腾的中英双语智能助写大模型

### WriteGPT: A large language model for Chinese-English bilingual intelligent writing assistance

[![Code License](https://img.shields.io/badge/Code%20License-Apache_2.0-green.svg)](https://github.com/SCIR-HI/Huatuo-Llama-Med-Chinese/blob/main/LICENSE) [![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/release/python-390/)

在这个项目中，我们训练了一个名为WriteGPT (文修) 的语言大模型。首先，我们的大模型在LLaMA基础上适配了中文语义能力。同时，我们使用大量中英文学术论文数据进行微调，以提升其在科研领域专有知识理解能力。特别地，我们围绕三个写作常用场景：文本润色、错误检测和智能翻译进行了针对性的微调训练。

目前文修大模型已经集成了一个在线平台，上线了写作润色、智能批阅和智能翻译三个功能。未来，我们还计划上线用户能力诊断、以及用户写作能力追踪功能，帮助用户在写作方面获得能力提升。

##写作润色
文本优化！只需输入您的文本并选择文本优化策略，即可轻松提升您的写作水平。我们的智能系统将为您提供优化后的内容，确保文笔清晰、连贯，并具有吸引力。不论是完善论文、提炼商业提案，还是增强创意作品，我们的文本优化功能将帮助您精准、有力地传达您的信息。立即体验语言提升的力量，让您的写作达到新的高度！

##智能批阅
依托领先的人工智能技术和大规模语料库，不断学习和优化，以提供最准确和细致的纠错服务。立即下载我们的软件，让文本纠错成为您写作之路上的不可或缺的良师益友。开启一段流畅无误的写作旅程！

##智能翻译
跨越语言的壁垒，文本翻译助您畅游世界！我们自豪地推出全新软件，专注于提供卓越的文本翻译功能，为您带来无与伦比的翻译体验。无论您是在国际商务、学习、旅行还是日常生活中需要翻译的帮助，我们的软件将成为您的得力助手。

## 欢迎大家使用我们精心打造的[文修智能写作助写平台](https://writelearn.bdaa.pro/)进行写作效率与技能提升。

## 更新日志
[2023/07/31] 文案修缮数据进行指令微调的模型WriteGPT发布。


## 模型效果测试

### 写作润色功能


| Case | 测试输入 | WriteGPT输出 |
|:------------- |:------------- |:---------------|
|Case1|该研究旨在探讨人工智能在医疗诊断中的应用。通过收集大量的医学数据和利用深度学习算法，人工智能可以帮助医生准确诊断疾病，并提供个性化的治疗方案。本研究将对人工智能的优势进行综述，并探讨其在医疗领域的潜在影响。| **本研究旨在深入探讨人工智能在医疗诊断中的应用。通过收集大量的医学数据并运用深度学习算法，人工智能能够为医生提供精确的疾病诊断，并提供个性化的治疗方案。本研究将全面回顾人工智能的优势，并深入探讨其在医疗领域的潜在影响。**|
Case2|In this research, an in-depth investigation is conducted to identify the underlying mechanisms of action of a novel antiviral drug on inhibiting the replication of the HIV virus in human cells, thus offering potential insights for future therapeutic developments.| **In this study, a comprehensive analysis is undertaken to uncover the underlying mechanisms through which a novel antiviral drug inhibits the replication of the Human Immunodeficiency Virus (HIV) in human cells. This research provides potential avenues for future therapeutic advancements.**|

### 智能批阅功能


| Case| 测试输入 | WriteGPT输出 |
|:------------- |:------------- |:---------------|
|Case3|The reserch experimens invlolved three grups of studentes, ad each group was give a diffrent task to camplete.| **{<br>"Misspellings": ["reserch", "experimens", "involved", "grups", "studentes", "give", "diffrent", "camplete"],<br>"Grammatical errors": [],<br>"the corrected sentence": "The research involved three groups of students, each given a different task to complete.",<br>}**|

### 智能翻译功能


| Case|测试输入 | WriteGPT输出 |
|:------------- |:------------- |:---------------|
|Case4|Quantum computing represents a paradigm shift in computational power, promising to revolutionize fields such as cryptography, optimization, and drug discovery. Unlike classical computers that rely on binary bits, quantum computers harness the principles of quantum mechanics, utilizing quantum bits (qubits) to perform complex calculations at an exponentially faster rate. The unique properties of qubits, such as superposition and entanglement, enable quantum computers to solve problems with astonishing efficiency. However, the development and scalability of quantum systems pose significant challenges, requiring breakthroughs in areas such as qubit stability and error correction.| **量子计算代表了计算能力的范式转变，承诺将革命化诸如密码学、优化和药物发现等领域。与经典计算机依赖于二进制位不同，量子计算利用量子力学原理，利用量子位（qubits）以指数级更快的速度执行复杂计算。量子位的独特性质，如叠加和纠缠，使量子计算机能够以惊人的效率解决问题。然而，量子系统的开发和可扩展性面临重大挑战，需要在量子位稳定性和错误纠正等领域实现突破。**|
Case5|随着科技的快速发展，人工智能已经变得越来越普遍。它在许多领域中发挥着重要的作用，如医疗诊断、自动驾驶和语音识别。然而，人工智能也引发了一些社会和道德问题，需要我们进行深入的讨论和研究。| **With the rapid development of technology, artificial intelligence has become increasingly prevalent. It plays a crucial role in many fields, such as medical diagnosis, autonomous driving, and speech recognition. However, artificial intelligence also raises some social and ethical issues that require deep discussion and research.**|

   



## 项目参与者

本项目由中国科学技术大学认知智能全国重点实验室iCanary项目组[程明月](https://github.com/Mingyue-Cheng)（项目负责人）、[杨纪千](https://github.com/yangjq713)、[张如娇](https://github.com/imsery)、[罗彧淙](https://github.com/GodFire66666)完成，指导教师为刘淇教授、陈恩红教授。


## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Mingyue-Cheng/WriteGPT&type=Date)](https://star-history.com/#Mingyue-Cheng/WriteGPT&Date)



  

## 致谢

本项目参考了以下开源项目，在此对相关项目和研究开发人员表示感谢。

  

- Facebook LLaMA: https://github.com/facebookresearch/llama
- Stanford Alpaca: https://github.com/tatsu-lab/stanford_alpaca
- alpaca-lora by @tloen: https://github.com/tloen/alpaca-lora

  

## 免责声明

本项目相关资源仅供学术研究之用，严禁用于商业用途。使用涉及第三方代码的部分时，请严格遵循相应的开源协议。模型生成的内容受模型计算、随机性和量化精度损失等因素影响，本项目无法对其准确性作出保证。本项目数据集绝大部分由模型生成，对于模型输出的任何内容，本项目不承担任何法律责任，亦不对因使用相关资源和输出结果而可能产生的任何损失承担责任。

 
