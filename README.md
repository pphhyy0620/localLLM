# localLLM
이 프로젝트는 [privateGPT](https://github.com/imartinez/privateGPT)와 [localGPT](https://github.com/PromtEngineer/localGPT)의 코드를 이용해 작성되었습니다.

### 💡 프로젝트 내용
- langchain을 통해 원하는 문서(pdf,csv,dox 등)에 기반하여 응답할 수 있는 LLM(Large Language Model)
- local에서 LLM을 사용함으로써, 데이터 유출없이 사용하는 것이 가능해짐
- 모델의 경우에는 Vicuna-7B를 사용하였고, InstructorEmbeddings을 사용하였음
- 프로젝트 내에서 LangChain, GPT4All, LlamaCpp, Chroma, SentenceTransformers가 사용되었음
