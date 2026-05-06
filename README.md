# ProBench

ProBench collects competition problems from [Codeforces](https://codeforces.com/), [Luogu](https://www.luogu.com.cn/), and [Nowcoder](https://ac.nowcoder.com/) to evaluate models' code reasoning capabilities in competitive programming. It ensures code robustness through online code evaluation, while also providing comprehensive analysis of models' code reasoning abilities.

## Usage

**Data**. We have provided all problem descriptions in the `codeforce`, `luogu`, and `nowcoder` folders, and the statistical information for these problems is displayed in `pred/problem_list.json`. **The evaluation problem set will be continuously updated here for the 2026 version.**

**Get Responses**. First, you need to use your model to generate responses and solution code based on the provided problems. We offer code for generation using vLLM and APIs (e.g., OpenAI) in `pred/get_response.py`. If you have alternative code, you can refer to `generate_prompts` and `save_response` in `pred/utils.py` to ensure a unified output format.

**Code Evaluation**. Due to platform restrictions and double-blind review policies, we cannot publicly share the automated submission scripts at this stage. For the purpose of the review process, we have provided pre-computed evaluation logs and results in the supplementary material. The full automated evaluation pipeline will be publicly released upon de-anonymization.

## Leaderboard

| Rank | Model                        | Size    | Reasoning | Pass@1 |
| ---- | ---------------------------- | ------- | --------- | ------ |
| 1    | QwQ-32B-Preview              | 32B     | 1         | 20.93  |
| 2    | DeepSeek-V3                  | 37/671B | 0         | 16.38  |
| 3    | Qwen2.5-72B-Instruct         | 72B     | 0         | 11.50  |
| 4    | Mistral-Large-Instruct-2411  | 123B    | 0         | 10.54  |
| 5    | Qwen2.5-Coder-32B-Instruct   | 32B     | 0         | 9.48   |
| 6    | Llama-3.1-70B-Instruct       | 70B     | 0         | 7.99   |
| 7    | Codestral-22B-v0.1           | 22B     | 0         | 5.08   |
| 8    | Skywork-o1-Open-Llama-3.1-8B | 8B      | 1         | 5.06   |
| 9    | Mixtral-8x22B-Instruct-v0.1  | 22/176B | 0         | 4.27   |
