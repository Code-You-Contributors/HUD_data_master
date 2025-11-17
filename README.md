# HUD_data

## Purpose
This repository provides **data and visualizations** to support various **nonprofits in our community** that serve individuals and families with housing needs.  

By bringing together key metrics and trends, we aim to highlight the **critical role these organizations play** in ensuring housing stability and community well-being.

## What We’ll Explore
We’ll work with datasets such as (placeholder for now till we get projects picked):
- **Meals served** – indicators of outreach and support services  
- **Rent assistance expenditures** – tracking financial support over time  
- **Individuals and families served** – measuring impact and reach  
- **Trends and patterns** – identifying needs and resource gaps  

## How the Data Will Be Used
The insights and visual materials created from this project can be used for:
- Social media campaigns 
- Community and stakeholder presentations  
- Fundraising and grant proposals  
- Strategic planning and resource allocation

## Project Goals
- Collect and organize relevant data from partner nonprofits  
- Build clear, easy-to-understand data visualizations  
- Create shareable reports and presentation-ready materials  
- Support nonprofits in **communicating their impact** and **securing funding**


### Reference repo for advanced topics

https://github.com/dmorton714/CY_post_grad_data


## Always Utilize a Virtual Environment


### Virtual Environment Commands
| Command | Linux/Mac | GitBash |
| ------- | --------- | ------- |
| Create | `python3 -m venv venv` | `python -m venv venv` |
| Activate | `source venv/bin/activate` | `source venv/Scripts/activate` |
| Install | `pip install -r requirements.txt` | `pip install -r requirements.txt` |
| Deactivate | `deactivate` | `deactivate` |


# Follow this to the best of our ability. 
We might not have some of the parts like models etc. 

```bash
data-project/
├── README.md                  # Project overview, instructions, documentation
├── requirements.txt           # Python dependencies (or environment.yml for Conda)
├── .gitignore                 # Files and folders to ignore in Git
│
├── data/
│   ├── raw/                   # Original, immutable datasets
│   ├── interim/               # Intermediate data (cleaned or partially processed)
│   └── processed/             # Final datasets ready for analysis or modeling
│
├── notebooks/
│   ├── name.ipynb   # Exploratory data analysis
│
├── src/
│   ├── __init__.py
│   ├── data/
│   │   └── load_data.py       # Data loading functions
│   ├── features/
│   │   └── build_features.py  # Feature engineering scripts
│   ├── models/
│   │   ├── train_model.py     # Training scripts
│   │   └── predict_model.py   # Inference scripts
│   └── visualization/
│       └── visualize.py       # Visualization utilities
│
├── models/
│   ├── trained_model.pkl      # Saved ML models
│   └── model_metrics.json     # Model performance tracking
│
├── reports/
│   ├── figures/               # Generated plots and images
│   └── final_report.md        # Project summary or results
│
├── tests/
│   └── test_load_data.py      # Unit tests for functions
│
└── scripts/
    ├── run_pipeline.py        # CLI or orchestration script
    └── preprocess_data.py
```