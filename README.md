# localLLM
이 프로젝트는 [privateGPT](https://github.com/imartinez/privateGPT)기반해서 수정된 [localGPT](https://github.com/PromtEngineer/localGPT)의 코드를 이용해 작성되었습니다.

### 💡 프로젝트 내용
- langchain을 통해 원하는 문서(pdf,csv,dox 등)에 기반하여 응답할 수 있는 LLM(Large Language Model)
- local에서 LLM을 사용함으로써, 데이터 유출없이 사용하는 것이 가능해짐
- 모델은 Vicuna-7B를 사용하였고, InstructorEmbeddings을 사용하였음
- 그 외, 프로젝트 내에서 LangChain, GPT4All, LlamaCpp, Chroma, SentenceTransformers가 사용되었음
![image](https://github.com/pphhyy0620/localLLM/assets/122515100/3d0a2e87-6977-4ec2-9b26-153197aa3c9c)



# Environment Setup
가상환경 생성

 ```
 conda create -n localllm python==3.10
```

가상환경 활성화
 ```
conda activate localllm
 ```
git clone 
 ```
git clone https://github.com/pphhyy0620/localLLM.git
 ``` 
path 지정
 ``` 
cd localLLM
```
필요 라이브러리 설치
```
pip install -r requirements.txt
```
문서 로드 및 분할 (GPU, CPU 환경에 맞게 사용하시면 될 것 같습니다.)
```
# GPU
python ingest.py
# CPU
python ingest.py --device_type cpu
```
문서 기반 QA 실행
```
# GPU
python local_LLM.py
# CPU
python local_LLM.py --device_type cpu
```
- 실행결과 아래와 같이 나오고, 관련 질문을 하시면 문서에 기반하여 답변하게 됩니다.
![image](https://github.com/pphhyy0620/localLLM/assets/122515100/9f85e359-ccbc-49b0-b2ac-b7cb32c3d09b)

- 종료하고 싶다면 `exit`를 query에 적으시면 종료됩니다.


