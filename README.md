## Course Recommendation Engine Assignment

This repository contains a Jupyter Notebook implementing a Course Recommendation Engine using embeddings and a vector database. The solution is designed for the assignment and enables instructors to easily test and grade the work.

---

### Table of Contents
1. [Environment Setup](#environment-setup)
2. [How to Run](#how-to-run)
3. [Notebook Overview](#notebook-overview)
4. [Testing & Evaluation](#testing--evaluation)
5. [Troubleshooting](#troubleshooting)

---

## Environment Setup

1. **Clone the repository**
	 ```bash
	 git clone <repo-url>
	 cd A2_Course_Recommendation
	 ```

2. **Create and activate Python environment**
	 - The environment is auto-configured if opened in VS Code.
	 - Or manually create a virtual environment:
		 ```bash
		 python3 -m venv .venv
		 source .venv/bin/activate
		 ```

3. **Install dependencies**
	 - All required packages are listed in `requirement.txt`:
		 ```bash
		 pip install -r requirement.txt
		 ```

---

## How to Run

1. **Open `Assignment2.ipynb` in Jupyter or VS Code.**
2. **Run all cells sequentially.**
	 - The notebook is self-contained and will:
		 - Download the course dataset
		 - Compute embeddings
		 - Index courses in ChromaDB
		 - Provide a recommendation function
		 - Test with 5 sample user profiles

---

## Notebook Overview

The notebook is structured as follows:

1. **Introduction**: Brief description of the recommendation engine and assignment goals.
2. **Installation**: Instructions for installing required packages (for notebook users).
3. **Imports**: Loads all necessary libraries (`pandas`, `sentence-transformers`, `chromadb`, etc.).
4. **Dataset Loading**: Loads the course catalog from a public URL.
5. **Embeddings & Indexing**: Generates embeddings for each course and indexes them in ChromaDB for fast similarity search.
6. **Recommendation Function**: Defines a function to recommend courses based on user profile and completed courses.
7. **Evaluation**: Tests the engine with 5 sample queries, each with comments on the relevance of recommendations.

---

## Testing & Evaluation

The notebook includes 5 sample user profiles:

1. **Profile 1**: Completed 'Python Programming for Data Science', interested in data visualization.
2. **Profile 2**: Knows Azure basics, wants to manage containers and build CI/CD pipelines.
3. **Profile 3**: Background in ML fundamentals, wants to specialize in neural networks and production workflows.
4. **Profile 4**: Wants to build and deploy microservices with Kubernetes.
5. **Profile 5**: Interested in blockchain and smart contracts, no prior experience.

For each profile, the notebook:
- Runs the recommendation function
- Prints top-5 recommended courses with similarity scores
- Provides comments on the relevance of recommendations

---

## Troubleshooting

- If you encounter missing package errors, re-run:
	```bash
	pip install -r requirement.txt
	```
- Ensure the virtual environment is activated before running the notebook.
- If ChromaDB or embedding model fails, check internet connectivity and package versions.

---

## Notes for Instructor

- The notebook is fully reproducible and does not require any private data or API keys.
- All code is commented for clarity.
- Evaluation comments are provided for each test case to help with grading.

---

For any issues, please contact the student or refer to the assignment instructions.
