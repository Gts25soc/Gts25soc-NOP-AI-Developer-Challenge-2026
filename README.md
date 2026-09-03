# NOP AI Developer Challenge 2026

Public starter repository for the TSCI / GTS25 NOP Vision Intelligence engineering selection challenge.

## Goal

Build a useful, working video-intelligence capability on top of the supplied starter baseline. The challenge is intentionally platform-neutral: candidates may develop on Linux, Windows, macOS, CPU-only systems, GPUs, or other reasonable hardware.

AI-assisted development is allowed. You may use coding assistants, pretrained models, open-source libraries, public datasets, documentation, and your own engineering judgement. You are evaluated on what you build, how well it works, how well you validate it, and whether you understand and can modify your own implementation.

## What you receive

This repository provides:

- a cross-platform Python/OpenCV baseline that reads video;
- a simple moving-object detector and centroid tracker;
- configurable zones and A-to-B/B-to-A event logic;
- a NOP-style structured evidence writer;
- JSONL/CSV/snapshot outputs;
- a clear integration contract you can preserve even if you replace the baseline completely.

The baseline is deliberately simple. It is not the target solution.

## Your task

Improve or replace the baseline and build the strongest useful VMS / video-intelligence capability you can within the challenge time.

At minimum your solution must:

1. process a prerecorded video;
2. detect at least one useful object category or target;
3. maintain object identity/tracks across frames;
4. use at least two zones or a meaningful event geometry;
5. generate an event based on tracked movement/behaviour rather than counting frames;
6. avoid obvious duplicate counting;
7. produce visual output;
8. produce structured JSON evidence;
9. produce a CSV summary;
10. save evidence snapshots for generated events;
11. document setup, execution, model/runtime choices, limitations and licenses.

After meeting the base requirements, you are encouraged to add a capability that demonstrates your engineering judgement: goods flow, people counting, vehicle flow, queue/occupancy, dwell, safety events, reverse-image search, semantic retrieval, anomaly detection, or another useful VMS feature.

Read [CHALLENGE.md](CHALLENGE.md), [RULES.md](RULES.md), [SUBMISSION.md](SUBMISSION.md), and [SCORING.md](SCORING.md) before starting.

## Quick start

```bash
git clone https://github.com/Gts25soc/Gts25soc-NOP-AI-Developer-Challenge-2026.git
cd Gts25soc-NOP-AI-Developer-Challenge-2026
python -m venv .venv
```

Activate the virtual environment for your operating system, then:

```bash
pip install -r requirements.txt
python starter/main.py --input path/to/video.mp4 --output-dir output
```

Use `--display` if you want a live preview window.

## Repository layout

```text
.
├── CHALLENGE.md
├── RULES.md
├── SCORING.md
├── SUBMISSION.md
├── requirements.txt
├── config/
│   └── example_config.json
├── nop_reference/
│   ├── evidence_contract.json
│   └── event_types.md
├── starter/
│   ├── main.py
│   ├── detector.py
│   ├── tracker.py
│   ├── zones.py
│   └── evidence.py
└── tests/
    └── test_evidence_contract.py
```

## Important

Do not submit candidate solutions directly to this public repository. Develop in your own private repository or another private submission workspace and share it only with the TSCI interview team.

Do not include credentials, private datasets, customer footage, secrets, API keys or proprietary third-party material in your submission.

© 2026 Techno Support Core Innovations Pvt. Ltd. Challenge starter code is provided under the terms in `LICENSE.md`.