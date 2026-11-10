# MASTER PROMPT — Movie Popularity Prediction Using Big Data & Machine Learning

## 1. YOUR ROLE

Act as a Senior Data Scientist, Big Data Engineer, Machine Learning Engineer, Python Developer, UI/UX Designer, and Software Architect.

Your task is to plan and guide the development of a complete university Big Data project titled:

**Movie Popularity Prediction Using Big Data and Machine Learning**

You must create a professional, technically correct, well-organized, and fully implementable project that satisfies all the attached university requirements.

You must prioritize:
- Simplicity and reliability.
- Correct implementation.
- Clear project structure.
- Meaningful use of PySpark.
- Appropriate Machine Learning techniques.
- Professional and modern Dashboard design.
- Easy installation and execution.
- A complete and understandable final submission.

Do not overcomplicate the project with unnecessary technologies or advanced techniques that do not provide meaningful value.

The project should be suitable for a university team of five students.

---

## 2. PROJECT CONTEXT

### Project Name
Movie Popularity Prediction Using Big Data and Machine Learning.

### Project Scope
Movies only.

Do not expand the project to YouTube videos, social media videos, or other video categories.

### Main Objective

Develop a data-driven system that analyzes movie metadata and predicts movie popularity using Machine Learning.

The system should also provide useful analytical insights about the factors and patterns associated with movie popularity.

### Main Prediction Target

Popularity Score Prediction (Regression).

The model should receive selected movie features and predict a numerical popularity score.

### Technical Stack

Use the following technologies:

- Python.
- Jupyter Notebook.
- Apache Spark / PySpark.
- Pandas and NumPy when appropriate.
- Matplotlib / Seaborn / Plotly for visualization.
- Scikit-learn for Machine Learning.
- Streamlit for the interactive dashboard.
- Git and GitHub for project management and deployment.

Do not introduce additional frameworks unless absolutely necessary.

### Deployment Requirements

The project must support:

1. Running locally on a computer.
2. Online deployment, preferably using Streamlit Community Cloud.

Choose a deployment approach that is simple, reliable, and compatible with the selected project architecture.

---

## 3. UNIVERSITY REQUIREMENTS — STRICT COMPLIANCE

Carefully analyze the attached file named Project Requirements.docx.

Treat it as the primary authority for the project's mandatory requirements.

The project must satisfy every requirement below:

### A. Team Requirements
- Team size: 5 students.

### B. Data Collection
- Obtain a relevant movie dataset.
- Document the original dataset source.
- Explain the dataset structure and features.
- Provide proper attribution.

### C. Data Preprocessing
- Inspect the dataset.
- Identify and handle missing values.
- Remove duplicate records where appropriate.
- Handle invalid values and inconsistent data types.
- Prepare features for analysis and Machine Learning.

### D. Apache Spark / PySpark
PySpark must be used meaningfully.

Demonstrate actual Spark operations, including relevant examples of:

- DataFrame operations.
- Filtering.
- Aggregation.
- Grouping.
- Joins when appropriate.
- Spark SQL.
- Data transformation.

Do not simply import PySpark or create an unused SparkSession.

Clearly explain which operations are performed using Spark and why.

### E. Data Analysis (EDA)
Perform Exploratory Data Analysis and identify meaningful patterns.

### F. Project-Specific Analysis
Implement a suitable Machine Learning approach for movie popularity prediction.

Train and evaluate appropriate models.

### G. Interactive Dashboard
Build a functional interactive dashboard that includes:

- Project title and description.
- Meaningful KPIs.
- Relevant charts and visualizations.
- Interactive filters and selections.
- Important analytical findings.
- Machine Learning results where applicable.

### H. Final Deliverables

The final project must include:

1. Source code and Jupyter Notebooks, including one consolidated PySpark data-processing and cleaning notebook.
2. Dataset or working dataset link with attribution.
3. Working interactive dashboard.
4. Concise project report.
5. Presentation and demonstration.
6. README containing installation and execution instructions.

Do not ignore, replace, or weaken any mandatory university requirement.

---

## 4. DATASET RESEARCH AND SELECTION

Research and select the most appropriate real-world dataset for this project.

### Initial Recommended Dataset

Start by evaluating:

**The Movies Dataset — Rounak Banik**

Source:
https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset

This dataset contains metadata for approximately 45,000 movies and additional MovieLens rating data.

Potentially useful information includes:

- Movie title.
- Budget.
- Genres.
- Runtime.
- Release date.
- Original language.
- Production companies.
- Production countries.
- Revenue.
- Popularity.
- Vote average.
- Vote count.
- Ratings data.

Do not automatically assume that every column is suitable.

### Your Responsibilities

1. Verify the dataset source and its available files.
2. Identify the exact files required.
3. Inspect the available columns.
4. Determine whether the dataset contains a suitable popularity target.
5. Evaluate missing values and data quality.
6. Explain the dataset's limitations.
7. Decide whether additional datasets are necessary.

Prefer one main dataset to avoid unnecessary integration complexity.

Additional datasets should only be used when they provide a clear benefit.

### Dataset Selection Output

Provide:

- Dataset name.
- Original source and download link.
- Dataset size.
- Number of records.
- Available files.
- Relevant columns.
- Target column.
- Data quality concerns.
- Reasons for selecting it.
- Alternative dataset if the recommended one is unavailable.

Never invent dataset statistics or claim to have downloaded or inspected files without actually doing so.

---

## 5. FEATURE SELECTION AND TARGET DEFINITION

Select the most appropriate features for predicting movie popularity.

Evaluate potential features such as:

- Budget.
- Genres.
- Runtime.
- Release year.
- Release month.
- Original language.
- Production country.
- Production company.
- Other suitable movie metadata.

Identify the target column:

**Popularity**

Explain its meaning and how it is represented in the selected dataset.

### Critical Data Leakage Prevention

Define the prediction scenario clearly.

If the intended scenario is predicting popularity before a movie is released:

- Do not use revenue.
- Do not use vote count.
- Do not use vote average.
- Do not use user ratings collected after release.
- Do not use other information that would only become available after release.

These variables may be analyzed separately during EDA, but must not be used as pre-release prediction inputs.

Explain that the dataset's recorded popularity score is a snapshot or time-dependent measurement, not necessarily a fixed pre-release outcome.

If the dataset cannot support a genuine pre-release prediction target, explicitly state this limitation and propose the simplest scientifically defensible approach.

Do not promise high prediction accuracy without evidence.

Produce a final feature selection table containing:

| Feature | Data Type | Purpose | Selected? | Reason |
|---|---|---|---|---|

Keep the feature selection simple and explainable.

---

## 6. COMPLETE SYSTEM ARCHITECTURE

Design the complete system architecture.

The architecture should explain the relationship between:

1. Raw Dataset.
2. Data Ingestion.
3. PySpark Processing.
4. Data Cleaning.
5. Feature Engineering.
6. Exploratory Data Analysis.
7. Machine Learning Training.
8. Model Evaluation.
9. Model Saving.
10. Streamlit Dashboard.
11. Online Deployment.

Provide:

- A system architecture diagram using Mermaid.
- A clear explanation of each component.
- Data flow between components.
- Input and output of each stage.
- Technologies used at each stage.

Avoid unnecessary databases, APIs, microservices, or cloud infrastructure.

Use a simple architecture that can be implemented by five university students.

---

## 7. PYSPARK DATA PROCESSING PIPELINE

Design a complete and practical PySpark workflow.

Include:

### Single-Notebook Requirement — Important

Keep the complete PySpark data-processing workflow in ONE notebook:

**`notebooks/01_data_processing_and_cleaning.ipynb`**

Do not split Spark initialization, loading, inspection, data cleaning, transformation, feature engineering, Spark operations, and saving into multiple Python files or separate notebooks.

Organize this notebook into clearly titled sections and executable cells. You may define helper functions inside the same notebook when useful, but do not create separate `spark_processing.py`, `preprocessing.py`, or `feature_engineering.py` files for this workflow.

### Processing Steps

1. **Spark Initialization:** Explain installation and initialize one SparkSession.
2. **Dataset Loading:** Read the original CSV file(s) into Spark DataFrames.
3. **Data Inspection:** Use `show()`, `printSchema()`, `describe()`, and `count()`.
4. **Data Cleaning:** Handle missing values, duplicate movies, invalid budget/runtime/popularity values, and incorrect data types.
5. **Data Transformation and Feature Engineering:** Extract release year/month, process genres, convert columns, and create only useful derived features.
6. **Meaningful Spark Operations:** Demonstrate `filter()`, `select()`, `groupBy()`, `agg()`, joins where justified, and Spark SQL.
7. **Validation:** Check row counts, schemas, missing values, duplicates, and key value ranges after processing.
8. **Save Processed Data:** Save the final cleaned and transformed dataset to `data/processed/` in a suitable format such as Parquet (or CSV if justified).

### Notebook Output and Handoff

The notebook must produce one clearly defined processed dataset that becomes the input for the EDA and Machine Learning stages. Document its output path, schema, and important columns.

Use Spark for actual data processing. Do not perform all processing in Pandas and add meaningless Spark code merely to satisfy the requirement.

If the additional MovieLens ratings files are used, process them in this same notebook as a clearly separated optional analysis section. Do not include post-release ratings in a pre-release prediction model.

Keep EDA and model training in their own notebooks because they are separate project stages; the requirement to use one file applies to the complete data-processing and cleaning pipeline, not to the entire project.

---

## 8. EXPLORATORY DATA ANALYSIS (EDA)

Design a useful EDA plan that directly supports the project objective.

Include suitable analyses such as:

1. Movie popularity distribution.
2. Popularity by genre.
3. Movie releases by year.
4. Budget versus popularity.
5. Runtime versus popularity.
6. Popularity by release month.
7. Popularity by original language.
8. Correlation analysis.
9. Distribution of movie budgets.
10. Other meaningful relationships supported by the actual data.

For each analysis, specify:

- The question being investigated.
- Required columns.
- Appropriate visualization.
- Expected analytical value.
- Possible insight.

Recommend suitable visualizations:

- Bar charts.
- Line charts.
- Scatter plots.
- Histograms.
- Box plots.
- Correlation heatmaps.

Do not invent analytical findings.

Actual findings must be calculated from the dataset.

---

## 9. MACHINE LEARNING PIPELINE

Build a simple but reliable regression pipeline.

### Recommended Models

Evaluate the following models:

1. Linear Regression — baseline model.
2. Decision Tree Regressor.
3. Random Forest Regressor.

An additional Gradient Boosting model may be included only if it provides meaningful value without making implementation unnecessarily complex.

### Pipeline Steps

1. Feature selection.
2. Feature engineering.
3. Categorical encoding.
4. Numerical preprocessing.
5. Train/Test Split.
6. Model training.
7. Hyperparameter tuning if appropriate.
8. Model comparison.
9. Best model selection.
10. Model serialization.
11. Prediction testing.

### Evaluation Metrics

Use:

- MAE.
- RMSE.
- R² Score.

Explain each metric in simple language.

Produce a model comparison table.

Include:
- Model name.
- MAE.
- RMSE.
- R².
- Final selection.

Do not fabricate results.

Results must come from actual model execution.

### Model Explainability

Include a simple feature importance analysis where supported.

Explain which movie features contribute most to the model's predictions.

### Important

Choose the simplest suitable implementation.

PySpark must be used for data processing as required.

Scikit-learn may be used for model training and evaluation if it provides a simpler and more reliable implementation.

Clearly document the relationship between the Spark pipeline and the Machine Learning pipeline.

---

## 10. PROFESSIONAL STREAMLIT DASHBOARD

This is the most important presentation component of the project.

Although the overall project should remain simple, the dashboard must look highly professional.

Design it as a polished movie analytics web application rather than a basic university assignment.

### Dashboard Design Direction

Create a modern cinematic analytics interface.

Suggested visual identity:

- Dark cinematic theme.
- Deep navy / charcoal backgrounds.
- Carefully selected accent colors.
- Modern typography.
- Clean layouts.
- Consistent spacing.
- Professional cards.
- Elegant charts.
- Responsive design.
- Smooth and intuitive navigation.

Avoid:
- Default-looking Streamlit pages.
- Excessive colors.
- Cluttered layouts.
- Unnecessary animations.
- Too many charts on one page.
- Inconsistent typography.
- Decorative elements that reduce usability.

Use Plotly for interactive visualizations.

### Dashboard Structure

Create the following pages:

#### PAGE 1 — Overview

Display:
- Total Movies.
- Average Popularity.
- Highest Popularity.
- Average Budget.
- Most Common Genre.
- Movie release trends.

Include:
- Summary KPI cards.
- Popularity distribution.
- Movies by year.
- Popularity by genre.
- Short analytical insights.

#### PAGE 2 — Movie Explorer

Allow users to explore the dataset.

Include:
- Search by movie title.
- Filter by genre.
- Filter by release year.
- Filter by language.
- Filter by budget range.
- Sort by popularity.

Display relevant movie information in a clean table or card layout.

#### PAGE 3 — Popularity Prediction

Create an interactive prediction interface.

Allow users to enter the features required by the trained model.

Examples:
- Budget.
- Genre.
- Runtime.
- Release year.
- Release month.
- Language.

The prediction form must use exactly the same feature transformations and order used during model training.

After clicking the prediction button, display:

- Predicted Popularity Score.
- A clear visual representation of the predicted result.
- A brief interpretation of the result.

Do not invent an arbitrary popularity threshold or present an uncalibrated score as a guaranteed category.

#### PAGE 4 — Data Insights

Include:
- Genre analysis.
- Budget analysis.
- Release trends.
- Runtime analysis.
- Correlation analysis.
- Interactive charts.
- Key findings.

#### PAGE 5 — Model Performance

Include:
- Model comparison.
- MAE.
- RMSE.
- R².
- Actual vs Predicted visualization.
- Feature importance.
- Best model identification.

### Dashboard Engineering Requirements

- Use reusable components.
- Separate data loading from UI code.
- Cache appropriate datasets.
- Avoid retraining the model every time the dashboard opens.
- Load the saved trained model.
- Handle invalid inputs.
- Handle missing model files gracefully.
- Display clear error messages.
- Optimize loading performance.
- Ensure all filters and buttons actually work.

### Dashboard Deliverables

Provide:
1. Complete page structure.
2. UI/UX design specifications.
3. Navigation design.
4. Component descriptions.
5. Color palette and typography.
6. Chart specifications.
7. Functional implementation plan.

The dashboard must be fully connected to the actual processed data and trained model.

Do not deliver a static UI mockup as a replacement for a functional application.

---

## 11. COMPLETE PROJECT FOLDER STRUCTURE

Design a clean, professional folder structure.

Use a structure similar to:

Movie_Popularity_Prediction/
│
├── data/
│   ├── raw/                         # Original downloaded dataset
│   └── processed/                   # Output produced by the processing notebook
│
├── notebooks/
│   ├── 01_data_processing_and_cleaning.ipynb  # ALL PySpark loading, inspection, cleaning,
│   │                                           # transformation, feature engineering and saving
│   ├── 02_eda.ipynb                  # Exploratory analysis using processed data
│   └── 03_model_training.ipynb       # Model training, evaluation and model export
│
├── models/
│   └── best_model.pkl               # Saved trained model (actual filename may vary)
│
├── dashboard/
│   └── app.py                       # Streamlit dashboard; may contain the pages/components
│                                      # in one file unless splitting becomes genuinely necessary
│
├── reports/
│
├── requirements.txt
├── README.md
└── .gitignore

Explain the purpose of every folder and important file.

**Do not create a `src/` folder or separate processing modules for this project by default.**
The full PySpark data-processing and cleaning pipeline must remain in
`01_data_processing_and_cleaning.ipynb`. Keep only genuinely separate project stages
(EDA, model training, and dashboard) in their respective files.

If the project later becomes too large to maintain, you may recommend extracting reusable
functions into modules, but explain the concrete reason and ask before changing this
simple structure.

---

## 12. COMPLETE CODE IMPLEMENTATION PLAN

Prepare a practical implementation roadmap.

Use this file plan by default:

1. `notebooks/01_data_processing_and_cleaning.ipynb`
   - One complete notebook containing Spark setup, dataset loading, inspection, cleaning,
     transformations, feature engineering, required Spark operations, validation, and
     saving the processed dataset.
   - Do not split these steps across multiple `.py` files or notebooks.
2. `notebooks/02_eda.ipynb`
   - Reads the processed dataset created by notebook 01 and performs EDA.
3. `notebooks/03_model_training.ipynb`
   - Reads the processed dataset, prepares the ML pipeline, trains and evaluates models,
     and saves the selected model and evaluation results.
4. `dashboard/app.py`
   - Loads the saved processed data and trained model and provides the interactive dashboard.
5. `requirements.txt` and `README.md`
   - Dependencies and project instructions.

For each file, specify its purpose, inputs, outputs, dependencies, and execution order.

When implementation begins, provide complete runnable notebook cells in the correct order
for each notebook, and complete runnable code for each required Python file. The data
processing and cleaning code must all be delivered together as one notebook, not as
separate files.

Code must:
- Be organized.
- Include useful comments.
- Handle common errors.
- Use consistent variable names.
- Avoid duplicated logic.
- Match the selected dataset's actual columns.
- Be compatible with the chosen libraries.

Do not provide pseudocode when actual implementation is requested.

Do not use placeholder code for essential functionality.

Do not silently omit important files.

When modifying a file, provide its complete updated content rather than isolated fragments unless a small patch is explicitly requested.

---

## 13. DEPLOYMENT

Prepare two deployment methods.

### A. Local Deployment

Provide:
- Python environment setup.
- Dependency installation.
- PySpark setup.
- Dataset placement.
- Notebook execution order: `01_data_processing_and_cleaning.ipynb` → `02_eda.ipynb` → `03_model_training.ipynb`.
- Model training instructions.
- Dashboard execution command.

The final dashboard should be runnable using:

streamlit run dashboard/app.py

Adjust the command if the final folder structure requires it.

### B. Online Deployment

Prefer Streamlit Community Cloud.

Explain:
- GitHub repository preparation.
- Required files.
- Dependency management.
- Model file handling.
- Dataset handling.
- Application configuration.
- Deployment steps.
- Common deployment errors.

Do not assume that local file paths or large raw datasets will work online.

If the raw dataset is too large, prepare compact processed files and a saved model for dashboard deployment.

Do not expose API keys, passwords, or private credentials.

---

## 14. FINAL PROJECT REPORT

Create a professional report structure.

The report must cover:

1. Introduction.
2. Problem Statement.
3. Project Objectives.
4. Dataset Description.
5. Data Collection.
6. Data Preprocessing.
7. PySpark Implementation.
8. Exploratory Data Analysis.
9. Feature Engineering.
10. Machine Learning Methodology.
11. Model Evaluation.
12. Dashboard Implementation.
13. Results and Discussion.
14. Limitations.
15. Conclusion.
16. References.

Explain what evidence, charts, tables, and screenshots should be included in each section.

Keep the report concise, clear, academically appropriate, and consistent with the actual implementation.

Do not claim results that were not obtained.

---

## 15. FINAL PRESENTATION

Design a professional PowerPoint presentation for the university project.

Recommended slide structure:

1. Title Slide.
2. Project Overview.
3. Problem Statement.
4. Project Objectives.
5. System Architecture.
6. Dataset Description.
7. Data Preprocessing.
8. PySpark Implementation.
9. EDA Findings.
10. Machine Learning Approach.
11. Model Comparison.
12. Dashboard Demonstration.
13. Prediction Example.
14. Results and Limitations.
15. Conclusion.
16. Team Contributions.

Specify the content and suggested visuals for every slide.

The presentation should be visually consistent with the dashboard's cinematic design.

Avoid text-heavy slides.

---

## 16. README AND DOCUMENTATION

Prepare a professional README.md containing:

- Project description.
- Main objectives.
- Technologies used.
- Dataset source.
- Folder structure.
- Installation instructions.
- Execution instructions.
- Dashboard launch instructions.
- Deployment instructions.
- Model information.
- Limitations.
- Team members.
- References.

All instructions must match the actual implementation.

---

## 17. TEAM TASK DISTRIBUTION

Divide the project among five students.

Suggested initial responsibilities:

Member 1:
Data Collection and Dataset Research.

Member 2:
Own the single `01_data_processing_and_cleaning.ipynb` notebook, containing the entire PySpark loading, inspection, cleaning, transformation, validation, and processed-data export workflow.

Member 3:
EDA and Data Visualization.

Member 4:
Machine Learning and Model Evaluation.

Member 5:
Streamlit Dashboard and Integration.

Also explain:
- Shared responsibilities.
- Integration points.
- Required outputs from each member.
- Execution dependencies.
- Suggested work order.

Ensure that the dashboard developer receives the processed data and saved model in a consistent format.

---

## 18. TESTING AND VALIDATION

Create a testing checklist.

Verify:

### Data
- Dataset loads successfully.
- Required columns exist.
- Missing values are handled.
- Duplicate records are addressed.
- Data transformations work correctly.

### PySpark
- Spark initializes successfully.
- DataFrames are created.
- Required transformations execute.
- Processed data is saved correctly.

### Machine Learning
- Model training completes.
- Train/Test separation is correct.
- No target leakage exists.
- Metrics are calculated correctly.
- Model is saved and loaded successfully.
- Prediction inputs match training features.

### Dashboard
- Every page loads.
- Filters work.
- Search works.
- Charts display actual data.
- Prediction functionality works.
- Invalid inputs are handled.
- Model loading errors are handled.

### Deployment
- Local execution works.
- Online deployment works.
- Required dependencies are available.

Provide a final requirement compliance checklist mapping every university requirement to its implementation and corresponding deliverable.

---

## 19. PROJECT MANAGEMENT AND IMPLEMENTATION RULES

Follow these rules throughout the project:

1. Simplicity is more important than unnecessary complexity.
2. Every technology must have a clear purpose.
3. Do not add features simply to make the project look bigger.
4. Do not invent dataset columns, results, or model performance.
5. Verify dataset compatibility before writing code.
6. Keep the implementation consistent across the processing notebook, EDA notebook, ML notebook, and dashboard.
7. Keep data cleaning and feature creation centralized in `01_data_processing_and_cleaning.ipynb`; do not recreate a second, conflicting cleaning pipeline elsewhere. Any model-specific transformations must be fitted on training data and reused identically at prediction time.
8. Prevent data leakage.
9. Keep the dashboard visually sophisticated but technically lightweight.
10. Ensure all mandatory university requirements are satisfied.
11. Document limitations honestly.
12. Make every implementation step reproducible.

If a recommended approach is unnecessarily complicated, choose a simpler alternative and explain why.

If an essential technical decision is uncertain, explain the available options and recommend one rather than silently assuming.

Do not ask unnecessary questions when a reasonable technical decision can be made.

---

## 20. REQUIRED OUTPUT AND WORKFLOW

Work in the following phases.

### PHASE 1 — Complete Project Blueprint

First, analyze the attached university requirements and produce:

1. Requirement-by-requirement analysis.
2. Final project definition.
3. Dataset selection and justification.
4. Final feature selection.
5. Target definition and prediction scenario.
6. System architecture.
7. PySpark workflow.
8. EDA plan.
9. Machine Learning pipeline.
10. Dashboard structure and UI/UX specifications.
11. Project folder structure.
12. Deployment strategy.
13. Report structure.
14. Presentation structure.
15. README structure.
16. Team task distribution.
17. Testing plan.
18. Final compliance checklist.

This phase must be detailed enough to serve as the main reference document for the entire team.

### PHASE 2 — Dataset Verification

Verify the chosen dataset, its source, files, columns, size, and suitability.

Identify any required downloads and explain how to obtain them.

Do not proceed using imaginary or unverified columns.

### PHASE 3 — Step-by-Step Implementation

After the blueprint is established, implement the project in logical stages.

For each stage:

- Explain the objective.
- Identify the files involved.
- Provide complete code.
- Explain how to run it.
- Specify expected outputs.
- Provide validation steps.
- Explain how it connects to the next stage.

Do not jump ahead before essential dependencies are ready.

### PHASE 4 — Dashboard Development

Develop the complete professional Streamlit dashboard.

Prioritize visual quality, usability, functional interactions, and integration with the actual model.

### PHASE 5 — Finalization

Prepare and validate:

- Complete source code.
- Notebooks.
- Dataset references.
- Working dashboard.
- Report.
- Presentation.
- README.
- Local execution.
- Online deployment.

Perform a final compliance audit against the attached university requirements.

---

## 21. FINAL INSTRUCTIONS

Your first response must focus on PHASE 1: Complete Project Blueprint.

Do not immediately generate thousands of lines of code.

First establish a technically correct, realistic, and complete plan.

The final objective is to deliver a project that is:

- Simple enough for a five-student university team.
- Complete enough to satisfy every university requirement.
- Technically correct.
- Built around meaningful PySpark processing.
- Supported by properly evaluated Machine Learning models.
- Presented through a highly professional interactive dashboard.
- Easy to run locally and deploy online.
- Easy for every team member to understand and explain during the final presentation.

Think like a professional engineering team delivering a real, working data analytics product, while respecting the time, skill level, and scope of a university project.

**Start with the attached Project Requirements.docx and produce the complete Phase 1 Project Blueprint.**