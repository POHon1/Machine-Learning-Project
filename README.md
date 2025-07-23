<img src="https://github.com/user-attachments/assets/7142b6be-0439-43e4-af79-a2c7e10d37e3" width="800">

# Personal Machine Learning Projects 
**Personal portofolio repository to showcase ML projects for learning prupose.**

Code + Demo via Google Colab or Huggingface Spaces Gradio:

### Table of Contents
- [Computer-Vision-Projects](#Computer-Vision-Projects)
  - Fine-Grained Bird Classification (nabird dataset)
  - Cat and Dog Breed Detection (oxford dataset)
  - Vehicle Detection traffic (UA-DETARC dataset)
  - Indonesian coin currency counter (manual dataset collection)
  - Pokemon tcg Indonesia card counter (manual dataset collection)
- [Natural-Language-Processing-Projects](#Natural-Language-Processing-Projects)
  - Twitter text binary classification (Sentiment140Twitter dataset)
  - Llama2 short story generator Qlora ()
  - NER for Machine Learning research papers ()
  - RAG Enhanced Analysis: The Intelligent Woman’s Guide to Socialism and Capitalism ()
- [Data-science-Projects](#Data-science-Projects)
  - South Jakarta House Price Prediction (kaggle)
  - Titanic Survivor Prediction (Huggingface)
  - Customer Churn Prediction (Huggingface)

---

### Computer-Vision-Projects

Many Computer Vision projects today rely on deep learning models like CNNs or Vision Transformers. the main task is for classifying, detecting, or segmenting images.

**The key in Computer Vision isn't the model architecture anymore, i mean it still matter for example cnn based is more computational cost friendly than vision based model and vision based is stronger than cnn generaly. But the main key is data quality and how well you annotate and choose the right preprocessing method. (My opinion)**
<br/>

| Link Google Colab | Description |
| --- | --- |
| [Fine-Grained Bird Classification.](https://colab.research.google.com/drive/1nohNrI2fwLHmmRl5nGYHCdJvMZ-CoRwS?usp=sharing) | <img src="https://github.com/user-attachments/assets/3f6dc16f-c47f-4048-8eae-b92f581f7b38" width="200"><br/>This code uses the ViT-B/16 pretrained model and the NABirds dataset to predict bird species based on image, this model is trained to classify 555 different bird species.<br/><br/>Huggingface Spaces Demo link: [Demo Link.](https://huggingface.co/spaces/antokun/Fine-grained-bird-classification)<br/>Huggingface dataset repository: "antokun/nabirds"<br/><br/>**Note**: If the Hugging Face Spaces demo has not been accessed for a while, it may take some time to restart. Please be patient while the space initializes. The loading time depends on the system's cold start process. If that happens, the system's cold start may take approximately 2–5 minutes. |
| [Cat and Dog Breed Detection.](https://colab.research.google.com/drive/13-6FsqF6r8H3xPRw_g4kz8CcBdm79uwF?usp=sharing) | <img src="https://github.com/user-attachments/assets/c17d627a-8189-4d52-937c-b4b2c9613743" width="200"><br/>This code uses the YOLOv8 model and the Oxford-IIIT Pet Dataset With Annotations to detect cat and dog breeds from images. The model is trained to classify various cat and dog breeds. Video demo is inside colab code.<br/><br/>Hugging Face Spaces Demo link (image) : [Demo Link.](https://huggingface.co/spaces/antokun/Cat_and_dog_breed_real_time_detection).<br/>Hugging Face dataset repository: "antokun/The-Oxford-IIIT-Pet-Dataset-With-Annotations"<br/><br/>Note: If the Hugging Face Spaces demo has not been accessed for a while, it may take some time to restart. Please be patient while the space initializes. The loading time depends on the system's cold start process, which may take approximately 2–5 minutes.<br/><br/> *My analysis suggests that this project is somewhat underperforming because the dataset falls into the fine-grained classification category, where YOLO is not particularly well-suited. Although YOLO excels at detecting multiple objects within a single image, it is less effective for fine-grained classification tasks.<br/> For single object image classification, combining it with standard classifier such as a CNN or a ViT-based model would likely perform better. For multi object detection, achieving fine-grained classification with YOLO would require extensive fine-tuning by combining it with different backbone such as other CNN's based model or vision transformer or ect.* |
| [Vehicle Detection Traffic.](https://colab.research.google.com/drive/1vubxWBLfswlOh2mUZQVF8qWxDUKTivMM?usp=sharing) | <img src="https://github.com/user-attachments/assets/166de3f3-324b-400c-92c9-27d3ecd3aae8" width="200"><br/>This code uses the YOLOv8 model and the UA-DETRAC dataset with annotations to detect and classify vehicles from images. The model is trained to recognize various vehicle types such as buses, trucks, taxis, sedans, and more.<br/><br/>Huggingface Spaces Demo link: [Demo Link.](https://huggingface.co/spaces/antokun/Vehicle-Detection-Traffic)<br/>Huggingface dataset repository: "antokun/UA-DETARC"<br/><br/>**Note**: If the Hugging Face Spaces demo has not been accessed for a while, it may take some time to restart. Please be patient while the space initializes. The loading time depends on the system's cold start process. If that happens, the system's cold start may take approximately 2–5 minutes.<br/><br/> *This code performs well for detecting vehicles on the road. However, as with other YOLO models, the use of bounding boxes here is limited in crowded road scenarios where numerous dense vehicles lead to overlapping objects and occlusions. To improve detection coverage in such crowded populated scenes, consider using techniques such as multi-scale feature extraction or multiply detection head and model ect.* |
| [Indonesian coin currency counter.](https://colab.research.google.com/drive/1H6eE5aLaP9yO6qRUiLNl7LGgRZdoMkVT?usp=sharing) | <img src="https://github.com/user-attachments/assets/74c69cac-f6c7-42d5-baeb-7aab3b8a2dba" width="200"><br/> This application uses a YOLOv8 model fine‑tuned on the Indonesian coin currency dataset (custom self made annotation) to detect and classify Indonesian coins in images. The model recognizes five classes: **tail**, **100**, **200**, **500**, and **1000** rupiah coins.<br/><br/> Hugging Face Spaces Demo link: [Demo Link](https://huggingface.co/spaces/antokun/indonesian-coin-currency-counter)<br/> Hugging Face dataset repository: antokun/indonesian-coin-currency<br/><br/> **Note**: If the Hugging Face Spaces demo hasn’t been accessed for a while, it may take a few minutes to restart due to the system’s cold start. Please be patient while it initializes (approximately 2–5 minutes). My analysis suggests that for the most accurate results, images should be captured with minimal shadows and reflections to reduce noise in coin detection and classification.<br/><br/> *The background must be kept simple such as blank background or something that not to distracting, then proper lighting but not too flashy and not under shadow, beacuse the dataset used to train this model currently lacks of different environment such as backbround and many variation, also coin can reflect light. But the methodology implemented in this pipeline is still solid and effective for Indonesian coin counting.<br/> Future improvements should focus on expanding the dataset to include a wide range of backgrounds, lighting conditions, and coin orientations, which will enhancing accuracy and robustness under various scenarios.* |
| Pokemon tcg Indonesia card counter. | <img src="https://github.com/user-attachments/assets/e58838f4-9ec9-45ea-9ccd-ed934e37c646" width="200"><br/>This code uses the YOLOv8 nano segmentation model and Pokemon TCG Indonesia card list dataset and also custom Annotated pokemon card to detect card based on card list dataset. The model is trained to detect Pokemon card matched in database and count em.<br/><br/>Video Demo link : [Demo Link.](https://youtube.com/shorts/naVWhgJD4Rg?feature=share).<br/><br/>*this video is not representing deployed model, optimal environment is using card launcer that automate card counting with phone to detect and count cards. the problem is this project not suitable for deployment because cant run intensive live detection with smartphone, the main problem is this project still using eazyocr that based on high cost of inference. the target for this project is to run smoothly on phone without external compuation such as server with gpu. so in order to do that, replacing eazyocr with custom lightweight ocr spesific for pokemon card is the solution for this project. meanwhile yolo is ready to deployed to segment the location of the card.* |

---

### Natural-Language-Processing-Projects 

Many NLP projects nowadays focus on Decoder based transformer or can be called Large Language Models (LLM) (the rest nlp's method is for niche only like research or smth). Mainly it's focuses around answering questions or summarizing documents ect. The goal is to adapt pretrained model for spesific use cases because it's useless to do training from scratch because lack of efficiency. 

**The key in NLP is not just the model or infra, but how you prepare your dataset like garbage in garbage out. (My opinion)**
<br/>


| Link Google Colab | Description |
| --- | --- |
| [Twitter text binary classification.](https://colab.research.google.com/drive/1G01C4kehXI7Ntc0rCzhRKOFfhR6efq6-?usp=sharing) | <img src="https://github.com/user-attachments/assets/338e83b6-3095-4bf8-a1ac-ae7dcf7fb4f0" width="200"><br/>This project uses an LSTM model with the Sentiment140 dataset and GloVe 6B.50d word embeddings. This code also functions as a text tweet comment sentiment classifier demo which classify text to postive or negative.<br/><br/>The main problem for this project is dataset, because it's only provide binary classification meanwhile the datataset contain data that neither positive or negative or can say that have ambiguity label between those binary classes<br/><br/>Huggingface dataset repository: "adilbekovich/Sentiment140Twitter"<br/>Huggingface Word embeddings = "antokun/glove.6B.50d" |
| [Llama2 short story generator Qlora.](https://colab.research.google.com/drive/1pLP3ik4kikO0pMZc-74ESp16q64mnRtO?usp=sharing) | <img src="https://github.com/user-attachments/assets/bb77936c-f16c-487a-9dfa-c81014db077f" width="200"><br/> done Prefix Tuning, Typical & Contrastive Sampling. |
| [NER for Machine Learning research papers.](https://colab.research.google.com/drive/1cjRSzFBv9WnA6Zdl6IdriENaZcqtK6MX?usp=sharing) | <img src="https://github.com/user-attachments/assets/db55d206-c58f-4754-a14b-ba5fcbd4ae2d" width="200"><br/> done also. |
| [RAG Enhanced Analysis: The Intelligent Woman’s Guide to Socialism and Capitalism.](https://colab.research.google.com/drive/1g3YfCsHqTlkX38X6rhbk6o3EX_BresTd?usp=sharing) | <img src="https://github.com/user-attachments/assets/1b06254b-3ce1-4321-acfb-061f06431c45" width="200"><br/> not yet done also, Adaptive Chunking, Source‑Attribution Tokens, Chain‑of‑Thought, Contrastive Search, Faithfulness & Hallucination Metrics, Interactive Dialog & Memory, Front‑end dengan Source Highlighting, Reranking, Hybrid Retriever. |

---


### Data-science-Projects

Many Data science projects revolve around solving real-world problems using Data analysis using Machine learning. Whether predicting customer churn, detecting fraud, estimating house prices, or classifying medical conditions, the goal remains the same: turning raw data into actionable insights using ML algorithm. Commonly used techniques in these projects is XGBoost. 

**The key in Data Science is having the right data and the right approach—XGBoost takes care of the rest. (My opinion)**
<br/>

| Link Google Colab | Description |
| --- | --- |
| [South Jakarta House Price Prediction.](https://colab.research.google.com/drive/1kgMPJXeiVIimy52GG5UGLAlzAMy33KCQ?usp=sharing) | <img src="https://github.com/user-attachments/assets/303a8ad0-0f2a-47f0-84fe-eb89e8e946bf" width="200"><br/>This code also functions as a calculator to estimate house prices in South Jakarta.<br/><br/>Huggingface dataset repository: "antokun/Tabular-Dataset",  Filename = "HARGA RUMAH JAKSEL.xlsx" |
| [Titanic Survivor Prediction.](https://colab.research.google.com/drive/1g3YfCsHqTlkX38X6rhbk6o3EX_BresTd?usp=sharing) | <img src="https://github.com/user-attachments/assets/f008f40a-7fa0-4418-aa18-c655a60b58c0" width="200"><br/>This code also functions as a calculator to estimate the likelihood of a person's survival in the Titanic disaster based on several factors.<br/><br/>Huggingface dataset repository: "phihung/titanic" |
| [Customer Churn Prediction.](https://colab.research.google.com/drive/15rRXVAaS6g_913y8vdWJqj13b5q2ieRq?usp=sharing) | <img src="https://github.com/user-attachments/assets/50a80742-a299-4b7b-9f74-d4892b94719c" width="200"><br/>This code is designed to predict customer churn, helping businesses identify customers who are likely to stop using a service.<br/><br/>Huggingface dataset repository: "d0r1h/customer_churn" |


note: some of these pic isn't mine, i took it on google images :D
