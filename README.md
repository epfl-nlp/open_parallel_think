# Open Parallel Think

Parallel reasoning datasets for mathematics and code. Each ZIP contains one JSONL file whose rows group multiple trajectories for a task.

## Files

| File | Description | Size |
| --- | --- | ---: |
| `open_parallel_think_math.jsonl.zip` | Parallel mathematical reasoning trajectories | 329.71 MiB |
| `open_parallel_think_code.jsonl.zip` | Parallel code reasoning trajectories | 595.97 MiB |

## Dataset statistics

| Dataset | Rows | Total trajectories | Trajectory groups |
| --- | ---: | ---: | ---: |
| Math | 59,247 | 508,056 | 63,507 |
| Code | 40,000 | 211,529 | 35,334 |

Trajectory groups are counted by unique `guid`.

## Data structure

Each JSONL row has the following structure:

```json
{
  "guid": "string",
  "trajectories": ["string"],
  "queries": [
    {
      "answer": "string",
      "question": "string"
    }
  ],
  "task": "string",
  "statistic": {},
  "num_tokens": 0,
  "frontier_demonstration": "string",
  "source": "string"
}
```

For Math, `statistic` contains `answer_lengths`, `correct_ratio`, and
`extracted_answers`; Math rows also include `accuracy_bucket`. For Code,
`statistic` contains `answer_lengths`, `correct_ratio`, `corrects`, and `models`.

## License

The datasets are licensed under the
[Creative Commons Attribution 4.0 International License](LICENSE). Third-party
source material remains subject to any separate rights or notices that apply.

## Citation

```bibtex
@misc{open_parallel_think_math_2026,
  author    = {Chen, Zeming and Wu, Haotian and Bosselut, Antoine},
  title     = {Open Parallel Think Math},
  year      = {2026},
  publisher = {EPFL NLP Lab},
  url       = {https://github.com/epfl-nlp/open_parallel_think}
}

@misc{open_parallel_think_code_2026,
  author    = {Chen, Zeming and Wu, Haotian and Bosselut, Antoine},
  title     = {Open Parallel Think Code},
  year      = {2026},
  publisher = {EPFL NLP Lab},
  url       = {https://github.com/epfl-nlp/open_parallel_think}
}
```
