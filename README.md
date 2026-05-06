# ProBench

ProBench collects competition problems from [Codeforces](https://codeforces.com/), [Luogu](https://www.luogu.com.cn/), and [Nowcoder](https://ac.nowcoder.com/) to evaluate models' code reasoning capabilities in competitive programming. It ensures code robustness through online code evaluation, while also providing comprehensive analysis of models' code reasoning abilities.

## Usage

**Data**. We have provided all problem descriptions in the `codeforce`, `luogu`, and `nowcoder` folders, and the statistical information for these problems is displayed in `pred/problem_list.json`. **The evaluation problem set will be continuously updated here for the 2026 version.**

**Get Responses**. First, you need to use your model to generate responses and solution code based on the provided problems. We offer code for generation using vLLM and APIs (e.g., OpenAI) in `pred/get_response.py`. If you have alternative code, you can refer to `generate_prompts` and `save_response` in `pred/utils.py` to ensure a unified output format.

**Code Evaluation**. Due to platform restrictions and double-blind review policies, we cannot publicly share the automated submission scripts at this stage. For the purpose of the review process, we have provided pre-computed evaluation logs and results in the supplementary material. The full automated evaluation pipeline will be publicly released upon de-anonymization.

## Leaderboard

| Rank | Model                          | Type   | Pass@1 |
| ---- | ------------------------------ | ------ | ------ |
| 1    | o4-mini                        | Closed | 56.55  |
| 2    | DeepSeek-R1-0528               | Open   | 49.76  |
| 3    | Gemini-2.5-flash               | Closed | 42.60  |
| 4    | Doubao-1-5-thinking-pro-250415 | Closed | 42.43  |
| 5    | DeepSeek-R1                    | Open   | 38.15  |
| 6    | Hunyuan-t1-20250521            | Closed | 35.25  |
| 7    | Claude-Sonnet-4                | Closed | 33.69  |
| 8    | QwQ-32B                        | Open   | 32.57  |
| 9    | Ernie-x1-turbo-32k             | Closed | 28.09  |
| 10   | GLM-Z1-AirX                    | Closed | 27.82  |
| 11   | QwQ-32B-Preview                | Open   | 20.93  |
| 12   | DeepSeek-V3                    | Open   | 16.38  |
| 13   | Qwen2.5-72B-Instruct           | Open   | 11.50  |
| 14   | Mistral-Large-Instruct-2411    | Open   | 10.54  |
| 15   | Qwen2.5-Coder-32B-Instruct     | Open   | 9.48   |
| 16   | Llama-3.1-70B-Instruct         | Open   | 7.99   |
| 17   | Codestral-22B-v0.1             | Open   | 5.08   |
| 18   | Skywork-o1-Open-Llama-3.1-8B   | Open   | 5.06   |
| 19   | Mixtral-8x22B-Instruct-v0.1    | Open   | 4.27   |