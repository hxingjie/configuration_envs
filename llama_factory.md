
```bash
git clone https://github.com/hiyouga/LLaMA-Factory.git
conda create -n llama_factory_gpu python=3.10
conda activate llama_factory_gpu

conda install pytorch==2.2.0 pytorch-cuda=12.1 -c pytorch -c nvidia
pip install transformers==4.39.3
pip install datasets==2.18.0
pip install accelerate==0.28.0
pip install peft==0.10.0
pip install trl==0.8.1
pip install gradio==4.21.0
pip install scipy einops sentencepiece protobuf uvicorn pydantic fastapi sse-starlette matplotlib fire

nvidia-smi
conda install -c nvidia cuda-nvcc=12.1
pip install deepspeed==0.14.0

pip install bitsandbytes==0.38.1
```
