# dai_lab   
##### dai_lab(2022.07~2025.02)에 있는 동안 프로젝트에 참여하면서 작성한 코드들
---------------------------------------------------------------------------   

Layer-wise attention code
- BERT_base
  - 실험 비교군으로 사용하는 BERT를 재구현하고 실험을 진행한 코드
  - GLUE 벤치마크로 평가를 진행했으며 데이터셋과 pre-trained 모델은 모두 huggingface hub를 통해 받아서 사용했음
- BERT_custom
  - BERT 코드에 layer-wise attention을 적용시키고 실험을 진행한 코드
  - GLUE 벤치마크로 평가를 진행했으며 데이터셋과 pre-trained 모델은 모두 huggingface hub를 통해 받아서 사용했음
- visualization
  - 실험 중에 수집한 각 계층에 적용된 attention weight을 시각화하는 코드
- result_visualization
  - 논문에 들어갈 시각 자료를 만드는 코드
   
Long context understanding code (진행 중)
- generate_dataset
  - 기존의 LongBench라는 벤치마크에 사용하기 위한 train & validation 데이터셋을 언어 모델 mistral-7B를 이용하여 생성하는 코드
  - huggingface hub에서 mistral-7B를 받아오고 long context 데이터셋인 cosmopedia를 format에 맞춰 변경하여 instruction으로 사용하여 데이터셋을 생성하도록 함
- generate_text
  - 데이터셋과 pre-trained 모델을 모두 huggingface hub에서 받아와 instruction tuning을 진행하는 코드
- eval_test
  - 학습된 모델로 생성한 결과가 downstream task에 대해 적합한 지를 구글의 gemini-api를 이용해 판단하는 코드
