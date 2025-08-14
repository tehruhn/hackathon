<div align="center">
    <h1>
        The Re-Align Hackathon
    </h1>
    <h4>
        <a href="#-challenge-overview">Challenge Overview</a>
        •
        <a href="#-getting-started">Getting Started</a>
        •
        <a href="#-submission-process">Submission Process</a>
    </h4>
    <h3>
        <a href="https://representational-alignment.github.io/hackathon">
            <img src="https://img.shields.io/website?url=https%3A%2F%2Frepresentational-alignment.github.io%2Fhackathon">
        </a>
        <a href="https://github.com/orgs/representational-alignment/teams/hackathon">
            <img src="https://img.shields.io/badge/maintainers-ReAlign%20hackathon%20team-yellow">
        </a>
        <a href="https://representational-alignment.github.io/hackathon">
            <img src="https://img.shields.io/badge/launched-August%202025-teal">
        </a>
        <a href="https://github.com/representational-alignment/hackathon/commits/main">
            <img src="https://img.shields.io/github/last-commit/representational-alignment/hackathon?color=blue&label=updated">
        </a>
        <a href="https://github.com/representational-alignment/hackathon/releases/latest">
            <img src="https://img.shields.io/github/v/release/representational-alignment/hackathon?color=blueviolet&label=version">
        </a>
        <a href="/LICENSE">
            <img src="https://img.shields.io/badge/licence-%C2%A9-crimson">
        </a>
    </h3>
</div>

---

Welcome to the Re-Align Workshop Hackathon! This challenge focuses on understanding and comparing representational alignment across a wide variety of vision models. Join either the 🟦 Blue Team or 🟥 Red Team and compete to discover whether representations are **universal** or **idiosyncratic**.

<table>
<tr>
<td>

## 📚 Research Context

Representational alignment has emerged as both an implicit and explicit goal in many machine learning subfields, including knowledge distillation ([Hinton et al., 2015]()), disentanglement ([Montero et al., 2022]()), and concept-based models ([Koh et al., 2020]()).
The concept has been explored under various terms including latent space alignment, conceptual alignment, and representational similarity analysis ([Kriegeskorte et al., 2008](); [Peterson et al., 2018](); [Roads & Love, 2020](); [Muttenthaler et al., 2023]()).

Recent work has leveraged human perceptual judgments to enrich representations within vision models ([Sundaram et al., 2024]()), while other research explores using brain signals to fine-tune semantic representations in language models. However, there remains little consensus on which metrics best identify similarity between systems ([Harvey et al., 2024](); [Schaeffer et al., 2024]()).

Representational alignment can help machines learn useful representations from humans with less supervision ([Fel et al., 2022](); [Muttenthaler et al., 2023](); [Sucholutsky & Griffiths, 2023]()), while also uncovering opportunities for humans to leverage domain-specific representations from machines when designing hybrid systems ([Steyvers et al., 2022](); [Shin et al., 2023](); [Schut et al., 2023]()).

</td>
</tr>
</table>

## 🏁 Quickstart

1. **Choose your team**: [🟦 Blue (universality)](#-blue-team) or [🟥 Red (idiosyncracy)](#-red-team).
2. **Fork and/or the repository** following our [setup instructions](#-getting-started).
3. **Explore the example notebooks** in our [starter code section](#-getting-started).
4. **Submit your findings** using our [submission process](#-submission-process).

Good luck! 🍀

## 🎯 Challenge Overview

We have **over 1000 vision models** available to adjudicate  This hackathon seeks to answer fundamental questions that have driven recent research in representational alignment ([Sucholutsky et al., 2023](); [Muttenthaler et al., 2024]()). Participants will join either a 🟦 Blue Team or a 🟥 Red Team, and provide JSON submissions that demonstrate the largest uniform set of models (🟦) or greatest differentiation among those models (🟥).

### 🟦 Blue Team

_"Find similarities."_
Building on work showing that different networks can learn similar representations at scale, Blue Teams search for cases where this convergence occurs.

- **🎯 Objective**: Submit a collection of models demonstrating representational and/or functional equivalence.
- **💡 Challenge**: Discover similarities among different architectures.
- **🏅 Victory condition**: Largest uniform set of representationally and/or functionally identical models.

### 🟥 Red Team

_"Drive distinctions."_
Following approaches that examine models presumed to be aligned to uncover representational differences, Red Teams develop stimuli that drive misalignment in model representations.

- **🎯 Objective**: Curate stimuli that reveal representational and/or functional differences.
- **💡 Challenge**: Identify the most informative test cases highlighting variation.
- **🏅 Victory condition**: Greatest differentiation among model representations and/or behaviors.

## 🚀 Getting Started

### 1️⃣ Fork and/or Clone Repository

*Optional*: Do you want to make a submission? Then **fork this repository**:

Click the **Fork** button near the top of the page to fork your own copy of `representational-alignment/hackathon`. You must be logged into GitHub.

⚠️ **Important**: Uncheck "Copy the main branch only" to include all branches, including branches used for submission!

**Clone and setup**:
```bash
git clone [YOUR_FORK_URL]
cd hackathon/
git checkout main
git checkout -b <team_color>_team_submissions  # blue or red
```

### 2️⃣ Environment Setup

Install [`uv`](https://astral.sh/) and dependencies:

```bash
# Install uv if you haven't already.
# On macOS and Linux:
curl -LsSf https://astral.sh/uv/install.sh | sh

# On Windows:
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

# Setup environment
uv sync

# Activate environment for Python commands
source .venv/bin/activate
```

### 3️⃣ Example Notebooks

We've provided starter notebooks to help you get started with the hackathon. These can be found in [`examples/`](examples/).

Use this command to launch them!

```bash
# Example: Launch Jupyter Lab
uv run --with jupyter jupyter lab
```

| Notebook                       | Purpose                      | Teams     |
| ------------------------------ | ---------------------------- | --------- |
| 📊 `extract_activations.ipynb` | Extract model activations    | 🟦🟥 Both |
| 🟦 `blue_team_starter.ipynb`   | Identify model similarities  | 🟦 Blue   |
| 🟥 `red_team_starter.ipynb`    | Find differentiating stimuli | 🟥 Red    |

### 4️⃣ Submission

See below!

## 📤 Submission Process

### 📋 Submission Requirements

Your final submission must be in **JSON format** and submitted as a pull request (PR), and should include a brief textual explanation of your findings.
See examples of a [Blue Team](https://github.com/representational-alignment/hackathon/pull/2) and a [Red Team](https://github.com/representational-alignment/hackathon/pull/1) submission.

#### 🟦 Blue Team JSON Format

```json
{
    "models": [
        {
            "model_name": "model1_name",
            "source": "where the model is from",
            "model_parameters": {
                "param1": "value1",
                "param2": "value2"
            }
        },
        {
            "model_name": "model2_name",
            "source": "where the model is from",
            "model_parameters": null
        }
    ]
}
```

#### 🟥 Red Team JSON Format

```json
{
    "differentiating_images": [
        {
            "dataset_name": "cifar100",
            "image_identifier": "test/girl/image_987.png"
        },
        {
            "dataset_name": "cifar100",
            "image_identifier": "test/orange/image_19.png"
        },
        {
            "dataset_name": "cifar100",
            "image_identifier": "test/bottle/image_2428.png"
        }
    ]
}
```

##### 📝 Field Descriptions

| Key                | Purpose                                  | Example                     |
| ------------------ | ---------------------------------------- | --------------------------- |
| `dataset_name`     | Name of the public dataset               | `"cifar100"`                |
| `image_identifier` | Path/ID within your `stimuli/` directory | `"test/girl/image_987.png"` |

> **⚠️ Important**: Include exactly these two keys for every stimulus. Ensure every `(dataset_name, image_identifier)` pair is unique.

### 📁 File Organization

| Team        | Directory                | Filename         | Commit Title                        |
| ----------- | ------------------------ | ---------------- | ----------------------------------- |
| 🟦 **Blue** | `blue_team_submissions/` | `team_name.json` | `Blue Team Submission: [team_name]` |
| 🟥 **Red**  | `red_team_submissions/`  | `team_name.json` | `Red Team Submission: [team_name]`  |

### 🔄 Submit Your Work

```bash
# Add your files
git add [your_files]

# Commit with proper message
git commit -m "<Blue or Red> Team Submission: [team_name]"

# Push to your fork
git push --set-upstream origin <team_color>_team_submissions
```

### 🎯 Create Pull Request

1. Go to your fork on GitHub
2. Click **"Compare & pull request"**
3. Set base branch: `<team_color>_team_submissions`
4. Title: `Blue Team: [team_name]` or `Red Team: [team_name]`
5. Submit! 🎉
