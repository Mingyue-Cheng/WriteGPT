[**中文**](./README.md) | [**English**](./README_EN.md)

<p align="center" width="100%">
<a href="" target="_blank"><img src="https://github.com/user-attachments/assets/9d0d8b09-32f3-41a3-a9e7-8ad2cb7e1721" alt="WriteGPT" style="width: 60%; min-width: 300px; display: block; margin: auto;"></a>
</p>



# 科言智能 (WriteGPT): 首个基于华为昇腾的科技文献智能助写大模型

### WriteGPT: A large language model for Chinese-English bilingual intelligent writing assistance

[![Code License](https://img.shields.io/badge/Code%20License-Apache_2.0-green.svg)](https://github.com/SCIR-HI/Huatuo-Llama-Med-Chinese/blob/main/LICENSE) [![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/release/python-390/)

在这个项目中，我们团队训练了一个名为WriteGPT (科言) 的语言大模型。首先，我们的大模型在LLaMA基础上适配了中文语义能力。同时，我们使用大量中英文学术论文数据进行微调，以提升其在科研领域专有知识理解能力。特别地，我们围绕三个写作常用场景：智能润色、批阅纠错和语言翻译进行了针对性的微调训练。

目前文修大模型已经集成了一个在线平台[访问链接：科言智能助写平台](https://writelearn.bdaa.pro/)，上线了智能润色、批阅纠错和语言翻译三个功能。未来，我们还计划上线论文问答、用户写作能力诊断、以及用户写作能力追踪功能，帮助用户在写作方面获得能力提升以及提升科研效率。

##智能润色
由于写作训练的不足，同学们可能会在写作过程中使用“咱们”，“什么的”类似口语化表达，不符合论文规范表达。通过智能算法，文修可以在保持原意的基础上，提供多种表达方式，帮助学生改进语言表达，拓展写作思路。同时，为了更好地结合毕设用语需求，研发团队在自研文修大模型中注入了大量的毕设场景语料，让润色结果更加符合毕设规范。

##批阅纠错
提供中英双语的语法纠错，帮助学生检查并纠正语法和用词错误，确保论文的准确性和流畅性。文修平台为了更好的解决文字校对的问题，准备了大量的语法纠正语料，让模型可以对修改的错误根据领域知识做出解释，不再单纯的依靠语法规则完成错误修改。

##语言翻译
针对专业术语提供准确的翻译，特别是在高科技和专业科研领域，确保翻译的专业性和规范性。特别在天文学、量子力学、医学等专业词汇丰富的领域中，传统的翻译软件往往无法准确地将这些术语翻译成符合科研规范的表述。为了更有效地服务于广大科研工作者，文修平台在自主研发的文化大模型中，融入了丰富的科研词汇翻译语料，旨在确保翻译结果能够精准地符合科研领域的规范要求。

## 欢迎大家使用我们精心打造的[文修智能写作助写平台](https://writelearn.bdaa.pro/)进行写作效率与技能提升。

## 更新日志
[2023/05/31] 文案修缮数据进行指令微调的模型WriteGPT发布。
[2024/12/20] 文修改名为科言。


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

 
