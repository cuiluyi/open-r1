## QWEN-GRPO

```
conda activate openr1
cd open-r1
export CUDA_VISIBLE_DEVICES="0"   # specify the single GPU ID
MODEL=/data/cuiluyi/open-r1/data/Qwen2.5-1.5B-Open-R1-GRPO
MODEL_ARGS="pretrained=$MODEL,dtype=bfloat16,max_model_length=32768,gpu_memory_utilisation=0.8"
OUTPUT_DIR=data/evals/$(basename $MODEL)

TASK=aime24
lighteval vllm $MODEL_ARGS "custom|$TASK|0|0" \
    --custom-tasks src/open_r1/evaluate.py \
    --use-chat-template \
    --output-dir $OUTPUT_DIR
```

```
conda activate openr1
cd open-r1
export CUDA_VISIBLE_DEVICES="1"   # specify the single GPU ID
MODEL=/data/cuiluyi/open-r1/data/Qwen2.5-1.5B-Open-R1-GRPO
MODEL_ARGS="pretrained=$MODEL,dtype=bfloat16,max_model_length=32768,gpu_memory_utilisation=0.8"
OUTPUT_DIR=data/evals/$(basename $MODEL)

TASK=math_500
lighteval vllm $MODEL_ARGS "custom|$TASK|0|0" \
    --custom-tasks src/open_r1/evaluate.py \
    --use-chat-template \
    --output-dir $OUTPUT_DIR
```

```
conda activate openr1
cd open-r1
export CUDA_VISIBLE_DEVICES="2"   # specify the single GPU ID
MODEL=/data/cuiluyi/open-r1/data/Qwen2.5-1.5B-Open-R1-GRPO
MODEL_ARGS="pretrained=$MODEL,dtype=bfloat16,max_model_length=32768,gpu_memory_utilisation=0.8"
OUTPUT_DIR=data/evals/$(basename $MODEL)

TASK=gpqa:diamond
lighteval vllm $MODEL_ARGS "custom|$TASK|0|0" \
    --custom-tasks src/open_r1/evaluate.py \
    --use-chat-template \
    --output-dir $OUTPUT_DIR 
```



## QWEN

```
conda activate openr1
cd open-r1
export CUDA_VISIBLE_DEVICES="3"   # specify the single GPU ID
MODEL=/data/cuiluyi/resources/models/Qwen/Qwen2.5-1.5B-Instruct
MODEL_ARGS="pretrained=$MODEL,dtype=bfloat16,max_model_length=32768,gpu_memory_utilisation=0.8"
OUTPUT_DIR=data/evals/$(basename $MODEL)

TASK=aime24
lighteval vllm $MODEL_ARGS "custom|$TASK|0|0" \
    --custom-tasks src/open_r1/evaluate.py \
    --use-chat-template \
    --output-dir $OUTPUT_DIR
```

```
conda activate openr1
cd open-r1
export CUDA_VISIBLE_DEVICES="4"   # specify the single GPU ID
MODEL=/data/cuiluyi/resources/models/Qwen/Qwen2.5-1.5B-Instruct
MODEL_ARGS="pretrained=$MODEL,dtype=bfloat16,max_model_length=32768,gpu_memory_utilisation=0.8"
OUTPUT_DIR=data/evals/$(basename $MODEL)

TASK=math_500
lighteval vllm $MODEL_ARGS "custom|$TASK|0|0" \
    --custom-tasks src/open_r1/evaluate.py \
    --use-chat-template \
    --output-dir $OUTPUT_DIR
```

```
conda activate openr1
cd open-r1
export CUDA_VISIBLE_DEVICES="5"   # specify the single GPU ID
MODEL=/data/cuiluyi/resources/models/Qwen/Qwen2.5-1.5B-Instruct
MODEL_ARGS="pretrained=$MODEL,dtype=bfloat16,max_model_length=32768,gpu_memory_utilisation=0.8"
OUTPUT_DIR=data/evals/$(basename $MODEL)

TASK=gpqa:diamond
lighteval vllm $MODEL_ARGS "custom|$TASK|0|0" \
    --custom-tasks src/open_r1/evaluate.py \
    --use-chat-template \
    --output-dir $OUTPUT_DIR 
```

