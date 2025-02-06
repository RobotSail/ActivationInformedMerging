# ActivationInformedMerging
<img width="100%" alt="Screenshot 2025-02-04 at 9 56 19 AM" src="https://github.com/user-attachments/assets/5b328cf0-797d-4aa4-9a98-1224cc4a971a" />

Model merging, a method that combines the parameters and embeddings of multiple fine-tuned large language models (LLMs), offers a promising approach to enhance model performance across various tasks while maintaining computational efficiency. 
This paper introduces Activation-Informed Merging (AIM), a technique that integrates the information from the activation space of LLMs into the merging process to improve performance and robustness. 
AIM is designed as a flexible, complementary solution that is applicable to any existing merging method.
It aims to preserve critical weights from the base model, drawing on principles from continual learning~(CL) and model compression.
Utilizing a task-agnostic calibration set, AIM selectively prioritizes essential weights during merging. We empirically demonstrate that AIM significantly enhances the performance of merged models across multiple benchmarks. Our findings suggest that considering the activation-space information can provide substantial advancements in the model merging strategies for LLMs with up to 40\% increase in benchmark performance.

# Checkpoints Used In Experiments
All checkpoints (merged with and without AIM) that were used for experiments in the paper are provided on huggingface. Below are the links to the aforementioned models:

## Models with AIM ([Collection 🤗](https://huggingface.co/collections/ahn1376/aim-merged-checkpoints-with-aim-67a226c77c915124f4bab456))

| Method | Code-Math | Code-Instruction | Math-Instruction | Code-Math-Instruction |
|--------|-----------|------------------|------------------|---------------------|
| DARE Linear | [Link 🤗](https://huggingface.co/ahn1376/DARETaskArithmetic___Code-Math___AIM) | [Link 🤗](https://huggingface.co/ahn1376/DARETaskArithmetic___Code-Instruction_Tuned___AIM) | [Link 🤗](https://huggingface.co/ahn1376/DARETaskArithmetic___Math-Instruction_Tuned___AIM) | [Link 🤗](https://huggingface.co/ahn1376/DARETaskArithmetic___Code-Math-Instruction_Tuned___AIM) |
| DARE Ties | [Link 🤗](https://huggingface.co/ahn1376/DARETies___Code-Math___AIM) | [Link 🤗](https://huggingface.co/ahn1376/DARETies___Code-Instruction_Tuned___AIM) | [Link 🤗](https://huggingface.co/ahn1376/DARETies___Math-Instruction_Tuned___AIM) | [Link 🤗](https://huggingface.co/ahn1376/DARETies___Code-Math-Instruction_Tuned___AIM) |
| Ties | [Link 🤗](https://huggingface.co/ahn1376/Ties___Code-Math___AIM) | [Link 🤗](https://huggingface.co/ahn1376/Ties___Code-Instruction_Tuned___AIM) | [Link 🤗](https://huggingface.co/ahn1376/Ties___Math-Instruction_Tuned___AIM) | [Link 🤗](https://huggingface.co/ahn1376/Ties___Code-Math-Instruction_Tuned___AIM) |
| Task Arithmetic | [Link 🤗](https://huggingface.co/ahn1376/TaskArithmetic___Code-Math___AIM) | [Link 🤗](https://huggingface.co/ahn1376/TaskArithmetic___Code-Instruction_Tuned___AIM) | [Link 🤗](https://huggingface.co/ahn1376/TaskArithmetic___Math-Instruction_Tuned___AIM) | [Link 🤗](https://huggingface.co/ahn1376/TaskArithmetic___Code-Math-Instruction_Tuned___AIM) |
| WIDEN | [Link 🤗](https://huggingface.co/ahn1376/WIDEN___Code-Math___AIM) | [Link 🤗](https://huggingface.co/ahn1376/WIDEN___Code-Instruction_Tuned___AIM) | [Link 🤗](https://huggingface.co/ahn1376/WIDEN___Math-Instruction_Tuned___AIM) | [Link 🤗](https://huggingface.co/ahn1376/WIDEN___Code-Math-Instruction_Tuned___AIM) |

## Models without AIM ([Collection 🤗](https://huggingface.co/collections/ahn1376/aim-merged-checkpoints-baseline-w-o-aim-67a15f05fa1066b3f642f2c6))

| Method | Code-Math | Code-Instruction | Math-Instruction | Code-Math-Instruction |
|--------|-----------|------------------|------------------|---------------------|
| DARE Linear | [Link 🤗](https://huggingface.co/ahn1376/DARETaskArithmetic___Code-Math) | [Link 🤗](https://huggingface.co/ahn1376/DARETaskArithmetic___Code-Instruction_Tuned) | [Link 🤗](https://huggingface.co/ahn1376/DARETaskArithmetic___Math-Instruction_Tuned) | [Link 🤗](https://huggingface.co/ahn1376/DARETaskArithmetic___Code-Math-Instruction_Tuned) |
| DARE Ties | [Link 🤗](https://huggingface.co/ahn1376/DARETies___Code-Math) | [Link 🤗](https://huggingface.co/ahn1376/DARETies___Code-Instruction_Tuned) | [Link 🤗](https://huggingface.co/ahn1376/DARETies___Math-Instruction_Tuned) | [Link 🤗](https://huggingface.co/ahn1376/DARETies___Code-Math-Instruction_Tuned) |
| Ties | [Link 🤗](https://huggingface.co/ahn1376/Ties___Code-Math) | [Link 🤗](https://huggingface.co/ahn1376/Ties___Code-Instruction_Tuned) | [Link 🤗](https://huggingface.co/ahn1376/Ties___Math-Instruction_Tuned) | [Link 🤗](https://huggingface.co/ahn1376/Ties___Code-Math-Instruction_Tuned) |
| Task Arithmetic | [Link 🤗](https://huggingface.co/ahn1376/TaskArithmetic___Code-Math) | [Link 🤗](https://huggingface.co/ahn1376/TaskArithmetic___Code-Instruction_Tuned) | [Link 🤗](https://huggingface.co/ahn1376/TaskArithmetic___Math-Instruction_Tuned) | [Link 🤗](https://huggingface.co/ahn1376/TaskArithmetic___Code-Math-Instruction_Tuned) |
| WIDEN | [Link 🤗](https://huggingface.co/ahn1376/WIDEN___Code-Math) | [Link 🤗](https://huggingface.co/ahn1376/WIDEN___Code-Instruction_Tuned) | [Link 🤗](https://huggingface.co/ahn1376/WIDEN___Math-Instruction_Tuned) | [Link 🤗](https://huggingface.co/ahn1376/WIDEN___Code-Math-Instruction_Tuned) |

# Usage
You can re-deo the experiments we have here using the provided code. Below we detail how to replicate the experiments.

## Merging Models
If you wish to merge the models yourself instead of using the provided checkpoints you can do so with the `merge.py` script provided. For example to perform DARE Ties merging on the Code, Math and Instruction Tuned models you can run:

```bash
python merge.py --method dare_ties --base_model unsloth/llama-2-13b --models_to_merge WizardLMTeam/WizardLM-13B-V1.2,vanillaOVO/WizardMath-13B-V1.0,layoric/llama-2-13b-code-alpaca --save_path ./DARE_TIES_InstructMathCode
```

## Evaluating Models on Benchmarks
Once you have the checkpoints you want to test you can run the `evaluate_model.py` script to run the benchamrks on the model. For example to run the benchmarks on the model merged above you can run:


```bash
python evaluate_model.py --model ./DARE_TIES_InstructMathCode
```

or if you wanted to use the provided checkpoints:

```bash
python evaluate_model.py --model ahn1376/DARETies___Code-Math-Instruction_Tuned
```

## Applying AIM to A Merged Model
If you want to apply AIM to any merged model you will need to provide the merged checkpoint as well as the base model checkpoint. The only hyper-parameter in AIM is $\omega$, which we recommend to be set between $0.2-0.6$ we set this to $0.4$ for the experiments in our paper, but in some cases lower values (more relaxation) will yeild better results. Below is how you can apply AIM to the checkpoint the code above makes:

```bash
python performAIM.py --merged_model ./DARE_TIES_InstructMathCode --pretrained_model_name unsloth/llama-2-13b --omega 0.4 --save_path ./DARE_TIES_AIM_InstructMathCode
```


# Summary of Findings
We find that in basically all merging methods we tested applying AIM improves performance and pushed the pareto front of the resulting model population and achieves the highest scrores in benchmarks. The figure below shows how with decreasing $\omega$ (more AIM relaxation) leads to further improvements in some models (HV gain is the hypervolume gained by adding the model to the population models used for merging (more is better)):

<img width="600px" alt="Screenshot 2025-02-04 at 10 15 38 AM" src="https://github.com/user-attachments/assets/5cd5119e-a292-45d4-972f-b2dd6febf6f8" />

We can observe this better by visualizing some of the pareto fronts for different model populations:

<img width="100%" alt="Screenshot 2025-02-04 at 10 22 25 AM" src="https://github.com/user-attachments/assets/5d88a71e-16ca-4f71-84f7-6e8de96ea69a" />

Overall the results of our experiments are as follows for the different tests:

## Base Models

| Method | Model(s) | AIM | HumanEval | MBPP | MMLU | MATH | GSM8K | IFEval | HV Gain |
|--------|----------|-----|-----------|------|------|------|-------|---------|----------|
| - | Base | - | 17.07 | 27.80 | 52.18 | 0.70 | 4.20 | 25.10 | - |
| - | Code | - | 17.07 | 31.60 | 52.91 | 6.00 | 24.10 | 26.25 | - |
| - | Instruction Tuned | - | **26.83** | **34.80** | **53.41** | 7.50 | 43.40 | **35.67** | - |
| - | Math | - | 15.24 | 27.60 | 51.89 | **13.10** | **59.10** | 21.58 | - |

## Merged Models

### DARE Task Arithmetic

| Model(s) | AIM | HumanEval | MBPP | MMLU | MATH | GSM8K | IFEval | HV Gain |
|----------|-----|-----------|------|------|------|-------|---------|----------|
| Code + Instruction Tuned | No | 26.83 | 34.40 | 53.53 | 8.40 | 45.80 | 33.42 | 0.27 |
| | Yes | 29.27 (+9.09%) | 36.00 (+4.65%) | 54.18 (+1.21%) | 8.30 (-1.19%) | 46.20 (+0.87%) | 32.00 (-4.25%) | 0.28 (+2.49%) |
| Code + Math | No | 16.46 | 28.60 | 51.96 | 15.10 | 64.70 | 22.02 | 0.23 |
| | Yes | 15.85 (-3.71%) | 29.60 (+3.50%) | 52.50 (+1.04%) | 14.80 (-1.99%) | 64.10 (-0.93%) | 21.91 (-0.50%) | 0.23 (-1.65%) |
| Instruction Tuned + Math | No | 5.49 | 19.00 | 51.08 | 9.80 | 54.30 | 32.35 | 0.18 |
| | Yes | 12.20 (+122.22%) | 28.20 (+48.42%) | 52.72 (+3.21%) | 12.90 (+31.63%) | 62.20 (+14.55%) | 31.96 (-1.21%) | 0.26 (+40.71%) |
| Code + Instruction Tuned + Math | No | 11.59 | 19.60 | 50.89 | 9.10 | 49.70 | 33.20 | 0.16 |
| | Yes | 15.85 (+36.76%) | 27.00 (+37.76%) | 52.59 (+3.34%) | 12.20 (+34.07%) | 60.70 (+22.13%) | 33.59 (+1.17%) | 0.23 (+40.59%) |

### DARE Ties

| Model(s) | AIM | HumanEval | MBPP | MMLU | MATH | GSM8K | IFEval | HV Gain |
|----------|-----|-----------|------|------|------|-------|---------|----------|
| Code + Instruction Tuned | No | 30.49 | 35.20 | 53.40 | 8.60 | 46.20 | 33.28 | 0.28 |
| | Yes | **30.49** | **36.80** (+4.55%) | 54.02 (+1.16%) | 8.60 | 47.20 (+2.16%) | 33.16 (-0.36%) | 0.29 (+1.63%) |
| Code + Math | No | 17.07 | 27.40 | 51.92 | 14.90 | 63.60 | 22.53 | 0.23 |
| | Yes | 17.68 (+3.57%) | 29.00 (+5.84%) | 52.61 (+1.33%) | 15.20 (+2.01%) | 63.90 (+0.47%) | 21.10 (-6.35%) | 0.24 (+4.00%) |
| Instruction Tuned + Math | No | 8.54 | 23.80 | 51.39 | 9.20 | 54.10 | 33.89 | 0.20 |
| | Yes | 15.85 (+85.60%) | 30.20 (+26.89%) | 52.89 (+2.92%) | 11.60 (+26.09%) | 57.80 (+6.84%) | 35.63 (+5.13%) | 0.26 (+31.22%) |
| Code + Instruction Tuned + Math | No | 13.41 | 21.20 | 51.15 | 8.70 | 51.50 | 35.75 | 0.17 |
| | Yes | 19.51 (+45.49%) | 28.60 (+34.91%) | 52.63 (+2.89%) | 11.60 (+33.33%) | 57.00 (+10.68%) | **36.20** (+1.26%) | 0.24 (+41.28%) |

### Task Arithmetic

| Model(s) | AIM | HumanEval | MBPP | MMLU | MATH | GSM8K | IFEval | HV Gain |
|----------|-----|-----------|------|------|------|-------|---------|----------|
| Code + Instruction Tuned | No | 29.27 | 33.80 | 53.44 | 8.60 | 47.10 | 31.60 | 0.28 |
| | Yes | 29.88 (+2.08%) | 35.80 (+5.92%) | 54.12 (+1.27%) | 7.80 (-9.30%) | 46.60 (-1.06%) | 32.01 (+1.30%) | 0.28 (+0.61%) |
| Code + Math | No | 18.29 | 28.60 | 52.10 | 15.00 | 64.70 | 21.92 | 0.24 |
| | Yes | 17.68 (-3.34%) | 29.20 (+2.10%) | 52.52 (+0.81%) | 14.60 (-2.67%) | 64.50 (-0.31%) | 21.54 (-1.73%) | 0.24 (-2.65%) |
| Instruction Tuned + Math | No | 4.27 | 20.20 | 51.50 | 10.00 | 54.20 | 31.31 | 0.18 |
| | Yes | 8.54 (+100.00%) | 26.40 (+30.69%) | 52.83 (+2.58%) | 12.80 (+28.00%) | 61.30 (+13.10%) | 32.62 (+4.18%) | 0.24 (+34.52%) |
| Code + Instruction Tuned + Math | No | 11.59 | 19.60 | 51.20 | 9.00 | 52.70 | 32.87 | 0.16 |
| | Yes | 15.24 (+31.49%) | 27.40 (+39.80%) | 52.63 (+2.79%) | 12.00 (+33.33%) | 58.10 (+10.25%) | 33.91 (+3.16%) | 0.22 (+31.97%) |

### Ties Merging

| Model(s) | AIM | HumanEval | MBPP | MMLU | MATH | GSM8K | IFEval | HV Gain |
|----------|-----|-----------|------|------|------|-------|---------|----------|
| Code + Instruction Tuned | No | 16.46 | 23.60 | 52.70 | 2.70 | 5.40 | 24.48 | 0.00 |
| | Yes | 15.24 (-7.41%) | 24.20 (+2.54%) | 53.15 (+0.85%) | 2.60 (-3.70%) | 5.20 (-3.70%) | 22.87 (-6.58%) | 0.05 (+inf%) |
| Code + Math | No | 15.85 | 26.80 | 51.86 | 14.30 | 62.60 | 21.63 | 0.20 |
| | Yes | 15.85 | 28.60 (+6.72%) | 52.29 (+0.83%) | **15.30** (+6.99%) | 63.80 (+1.92%) | 22.64 (+4.67%) | 0.23 (+13.55%) |
| Instruction Tuned + Math | No | 28.05 | 34.60 | 54.45 | 8.70 | 44.70 | 34.04 | 0.23 |
| | Yes | 27.44 (-2.17%) | 35.00 (+1.16%) | 54.74 (+0.53%) | 9.30 (+6.90%) | 46.10 (+3.13%) | 34.51 (+1.38%) | 0.25 (+6.38%) |
| Code + Instruction Tuned + Math | No | 21.34 | 29.20 | 53.97 | 6.30 | 29.20 | 26.95 | 0.11 |
| | Yes | 20.73 (-2.86%) | 29.20 | 54.46 (+0.91%) | 5.70 (-9.52%) | 23.70 (-18.84%) | 25.98 (-3.60%) | 0.11 (+4.33%) |

### WIDEN

| Model(s) | AIM | HumanEval | MBPP | MMLU | MATH | GSM8K | IFEval | HV Gain |
|----------|-----|-----------|------|------|------|-------|---------|----------|
| Code + Instruction Tuned | No | 26.22 | 35.60 | 54.90 | 8.30 | 45.00 | 30.42 | 0.27 |
| | Yes | 25.61 (-2.33%) | 34.60 (-2.81%) | 54.97 (+0.13%) | 8.20 (-1.20%) | 44.10 (-2.00%) | 31.60 (+3.88%) | 0.26 (-0.93%) |
| Code + Math | No | 17.07 | 29.40 | 53.35 | 14.20 | 64.40 | 24.02 | 0.24 |
| | Yes | 17.07 | 29.60 (+0.68%) | 53.36 (+0.02%) | 14.30 (+0.70%) | 62.20 (-3.42%) | 23.95 (-0.29%) | 0.24 (-1.22%) |
| Instruction Tuned + Math | No | 24.39 | 30.40 | 54.20 | 14.60 | 66.00 | 30.82 | 0.30 |
| | Yes | 23.78 (-2.50%) | 32.00 (+5.26%) | 54.69 (+0.90%) | 15.10 (+3.42%) | **68.20** (+3.33%) | 31.23 (+1.33%) | **0.31** (+2.54%) |
| Code + Instruction Tuned + Math | No | 25.00 | 33.20 | 54.58 | 13.50 | 64.20 | 31.44 | 0.29 |
| | Yes | 26.83 (+7.32%) | 32.80 (-1.20%) | **54.98** (+0.73%) | 14.40 (+6.67%) | 64.00 (-0.31%) | 32.82 (+4.39%) | 0.30 (+4.70%) |

# Citation
```bib
@misc{nobari2025activationinformedmerginglargelanguage,
      title={Activation-Informed Merging of Large Language Models}, 
      author={Amin Heyrani Nobari and Kaveh Alimohammadi and Ali ArjomandBigdeli and Akash Srivastava and Faez Ahmed and Navid Azizan},
      year={2025},
      eprint={2502.02421},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2502.02421}, 
}
```
