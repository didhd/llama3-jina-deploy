# Amazon SageMaker Profiling - SageMaker에서 Jina 모델, Llama 모델 및 배포 및 NVIDIA Nsight Systems를 이용한 Profiling

## 개요

이 저장소에는 AWS SageMaker에서 Jina 모델, Llama 모델을 배포하고 사용하는 방법, 그리고 NVIDIA Nsight Systems를 설치하는 방법을 설명하는 Jupyter 노트북이 포함되어 있습니다. Jina Embeddings 모델을 사용하여 Retrieval-augmented generation (RAG) 애플리케이션을 만드는 위한 기본적인 사전 작업을 다룹니다. 또한 SageMaker JumpStart를 사용하여 Llama 텍스트 생성 모델을 배포하고 NVIDIA Nsight Systems를 설정하여 성능 분석을 수행하는 방법도 포함되어 있습니다.

### 이 저장소의 노트북 목록:

1. **1.meta-textgeneration-llama-3-8b_sdk.ipynb**: SageMaker Python SDK를 사용하여 SageMaker JumpStart 텍스트 생성 모델을 배포하고 엔드포인트를 호출하는 방법을 설명합니다. (SageMaker Studio에서 실행)
2. **2.jinaai-embeddings-v2-base-en_nb.ipynb**: Jina 모델을 SageMaker에 설정하고 배포하는 단계별 가이드입니다. (SageMaker Studio에서 실행)
3. **3.llama3-training-local.ipynb**: SageMaker local 모드를 사용하여 Llama 3 모델을 파인튜닝하는 방법을 설명합니다. (SageMaker Notebook Instance에서 실행)
4. **4.install-nvidia-nsight.ipynb**: Amazon Linux 2의 SageMaker 노트북 인스턴스에 NVIDIA Nsight Systems를 설치하는 방법을 제공합니다. (SageMaker Notebook Instance에서 실행)

## 사전 요구 사항

- AWS 계정이 필요합니다. 계정이 없으시면 [AWS 계정 등록](https://portal.aws.amazon.com/billing/signup)을 통해 등록할 수 있습니다.
- AWS SageMaker에 대한 기본 지식이 필요합니다.
- SageMaker Studio 환경이 설정되어 있어야 합니다. 노트북 1과 2는 SageMaker Studio의 **Data Science 3.0 이미지**와 **ml.t3.medium** 인스턴스를 사용하여 작성되었습니다.
- SageMaker Notebook Instance가 설정되어 있어야 합니다. 노트북 3과 4는 SageMaker Notebook Instance에서 실행됩니다.

## 사용 방법

### 1. meta-textgeneration-llama-3-8b_sdk.ipynb (SageMaker Studio에서 실행)

이 노트북은 SageMaker JumpStart를 사용하여 텍스트 생성 모델을 배포하고 엔드포인트를 호출하는 방법을 설명합니다.

### 2. jinaai-embeddings-v2-base-en_nb.ipynb (SageMaker Studio에서 실행)

이 노트북은 Jina Embeddings 모델을 SageMaker에 배포하고 사용하는 방법을 안내합니다.

### 3. llama3-training-local.ipynb (SageMaker Notebook Instance에서 실행)

이 노트북은 SageMaker local 모드를 사용하여 Llama 3 모델을 파인튜닝하는 방법을 설명합니다.

### 4. install-nvidia-nsight.ipynb (SageMaker Notebook Instance에서 실행)

이 노트북은 Amazon Linux 2의 SageMaker 노트북 인스턴스에 NVIDIA Nsight Systems를 설치하는 방법을 제공합니다.

## 정리

비용 발생을 방지하기 위해 배포된 엔드포인트를 정리하는 것을 잊지 마세요:

```python
predictor.delete_predictor()
```

## 라이선스

이 프로젝트는 MIT 라이선스에 따라 라이선스가 부여됩니다. 자세한 내용은 LICENSE 파일을 참조하십시오.
