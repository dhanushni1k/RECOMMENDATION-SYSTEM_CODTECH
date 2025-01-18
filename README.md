# RECOMMENDATION-SYSTEM_CODTECH
**COMPANY** : COSTECH IT SOLUTIONS
**NAME** : DHANUSHNI.N
**INTERN ID** : CT08FCX
**DOMAIN** : MACHINE LEARNING
**BATCH DURATION** :DECEMBER 20th ,2024 TO JANUARY 20th,2025
**MENTOR NAME** : NEELA SANTHOSH KUMAR

Recommendation System using Collaborative Filtering and Matrix Factorization
Overview
This project demonstrates the implementation of a recommendation system using collaborative filtering and matrix factorization techniques, specifically Singular Value Decomposition (SVD). The system is designed to predict user preferences and suggest personalized recommendations based on their past behavior. It leverages the MovieLens dataset, which consists of user-item interactions with ratings, to build a recommendation model. The model is evaluated using Root Mean Squared Error (RMSE) as a performance metric, and top-N recommendations are generated for users.

Technologies Used
Python: The primary programming language used for data processing and model implementation.
Pandas: For data manipulation and analysis.
Surprise: A Python library for building and analyzing recommender systems. It supports various collaborative filtering algorithms, including SVD.
Matplotlib: For plotting and visualizing evaluation metrics.
Scikit-learn: For splitting data into training and test sets.
Project Structure
bash
Copy
Edit
recommendation_system/
│
├── recommendation_system.ipynb    # Jupyter notebook containing the full implementation
├── README.md                     # Project description and usage instructions
├── requirements.txt              # Python dependencies
└── data/                         # Folder containing the dataset (optional if hosted externally)
Dataset
This recommendation system is built using the MovieLens dataset, which consists of user ratings for different movies. The dataset can be downloaded from the MovieLens website, and we use the u.data file which contains the user-item rating data.

The dataset consists of the following columns:

user_id: The ID of the user who gave the rating.
item_id: The ID of the item (movie) being rated.
rating: The rating given by the user (on a scale from 1 to 5).
timestamp: The timestamp when the rating was given.
Steps in the Project
1. Data Loading and Preprocessing
The dataset is loaded into a Pandas DataFrame, which is then converted into a format compatible with the Surprise library. The dataset is cleaned, and irrelevant columns are dropped to focus on the user-item interactions.

2. Model Building (Collaborative Filtering with SVD)
We implement collaborative filtering using Singular Value Decomposition (SVD), which is a matrix factorization technique. SVD factorizes the user-item interaction matrix into three smaller matrices and approximates missing ratings based on these factors. This helps in predicting user preferences for items they have not interacted with.

3. Model Evaluation
The performance of the recommendation model is evaluated using Root Mean Squared Error (RMSE). RMSE measures the difference between the predicted ratings and the actual ratings in the test set. A lower RMSE indicates a better model.

4. Generating Recommendations
Top-N recommendations are generated for each user based on their predicted ratings for items they have not yet rated. The recommendations are sorted in descending order of predicted ratings, and the top items are returned.

5. Visualization
The model's performance is visualized using a simple plot to showcase the RMSE values, providing insights into how well the recommendation system is performing.

Running the Project
Prerequisites
To run this project, you will need to have the following Python libraries installed:

pandas
numpy
scikit-surprise
matplotlib
You can install them using the following command:

bash
Copy
Edit
pip install -r requirements.txt
Running the Notebook
Clone or download the repository to your local machine.
Navigate to the project directory.
Open the recommendation_system.ipynb Jupyter notebook.
Execute the cells step-by-step to see how the model is built, trained, and evaluated.
Conclusion
This project demonstrates how to build a basic recommendation system using collaborative filtering with matrix factorization techniques like SVD. The system provides personalized recommendations based on historical user-item interactions. The model is evaluated using RMSE and offers valuable insights into how well the system is predicting user preferences.

For further improvements, other techniques such as KNN-based collaborative filtering, SVD++, or Deep Learning models could be explored. Additionally, other evaluation metrics like Precision, Recall, and F1-score could be used for a more comprehensive analysis.
