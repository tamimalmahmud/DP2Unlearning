**Installation**

$ conda create --name torch-env pytorch torchvision pytorch-cuda=12.1 -c pytorch -c nvidia


*Also Install the following libraries*

1. datasets
2. accelerate
3. evaluate
4. matplotlib
5. hydra-core
6. omegaconf
7. peft
8. rouge_score
9. tqdm
10. einops
11. packaging
12. bitsandbytes
13. scipy
14. ninja
etc. 

**Traditional Retraining from Scrach (Benchmark retain model)**

python finetune.py --config-path /home/user_name/project_name/config --config-name finetune.yaml


**Unlearning Ready Training (Disclosure protected base model)**

python Train_dp_MLM.py --config-path /home/user_name/project_name/config --config-name Train_dp_MLM.yaml
or
python Train_dp_SGD.py --config-path /home/user_name/project_name/config --config-name Train_dp_SGD.yaml


**DP2Unlearning fine-tuning**

python FT_BaseModel.py --config-path /home/user_name/project_name/config --config-name FT_BaseModel.yaml


**Approximate Unlearning fine-tuning**

python forget.py --config-path /home/user_name/project_name/config --config-name forget.yaml


**Evaluation**

python evaluate_util.py --config-path /home/user_name/project_name/config --config-name eval_everything.yaml


**Aggregation**

python aggregate_eval_stat.py --config-path /home/user_name/project_name/config --config-name aggregate_eval_stat.yaml

retain_result=${path_to_traditional_retraining_from_scratch}
ckpt_result=${path_to_your_unlearned_method}

**Beyong KS Test**

python Beyond_KS_test.py --config-path /home/user_name/project_name/config --config-name aggregate_eval_stat.yaml





