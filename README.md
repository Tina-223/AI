# AI
**✔ 언어**: python\
**✔ 사용한 라이브러리**
1. NumPy: NumPy란 행렬이나 대규모 다차원 배열을 쉽게 처리할 수 있도록 지원하는 파이썬의 라이브러리입니다. 저희 프로젝트의 경우, 핵심단어 추출 기능을 구현하기 위해, 단어와 단어 사이 코사인 유사도를 비교하여 문맥상 가장 중요한 핵심 단어를 판단하는데 쓰입니다.
2. PyTorch: Python을 위한 오픈소스 머신 러닝 라이브러리로, Torch 기반이며 자연어 처리와 같은 애플리케이션을 위해 사용됩니다. 저희 프로젝트에서는 핵심 문장 추출에서 사용하는 라이브러리입니다.
3. KoNLPy: 한글 자연어 처리를 쉽고 간결하게 처리할 수 있도록 만들어진 오픈소스 라이브러리입니다. 사용자가 입력한 일기 내용을 모델이 이해할 수 있는 숫자로 바꾸는 과정에서 토크나이즈가 필수적이며, 이를 위해 okt와 komoran과 같은 토크나이즈를 사용합니다.
4. Googletrans: Google Translate API 사용을 용이하게 해주는 오픈소스 라이브러리입니다. 추출한 핵심 단어를 영어로 번역하여, 이를 pixray API에 전달하는 과정에서 사용됩니다.

**✔ 인공지능 모델**
1. transformers: 트랜스포머란 기계 번역과 같은 sequence to sequence 과제를 수행하기 위한 모델으로, 저희 프로젝트에서는 감정 분석과 감상평 출력을 하는데 사용되는 모델입니다.
  * zero-shot-classification: 특히, 감정 분석 시 zero-shot-classification 기능을 사용하여 별도의 트레이닝 없이 감정 분석을 시도했습니다. 감정을 love, joy, surprise, anger, sadness, fear, neutral, tired 이렇게 8가지의 감정만을 분석하도록 적용했습니다.
  2. KoGPT2: GPT-2 모델은 파인튜닝하여 만든 한국어 언어 모델이며, 머신러닝 알고리즘을 활용하여 입력된 샘플 텍스트를 구문론적, 문법적, 정보 등의 일관성을 갖춘 텍스트로 생성하는 자연어 처리 모델입니다. 사용자의 일기 내용에 대해 AI가 감상평을 출력하는 기능을 수행하도록 KoGPT2를 사용하였습니다.

* 다음 그림은 저희가 기획한 의도에 맞는 감상평을 출력하기 위해 수정한 샘플 텍스트입니다. 샘플 텍스트를 바탕으로 파인튜닝하여, 저희 다이어리만의 모델을 만들었습니다.
![image](https://user-images.githubusercontent.com/52921222/182778762-5db48521-3470-42fe-9cc5-97692cec8062.png)
3. sentence transformer: 자연어 처리 딥러닝 모델인 BERT를 기반으로, 문장 처리를 위해 세분화한 SBERT의 문장, 글, 이미지 임베딩을 위한 파이썬 프레임워크입니다. 
