#CELEB-BOT 5000

Overview

This project implements a chatbot that provides personalized fitness recommendations, including workout plans, meal plans, and insights based on user preferences. It integrates Google Gemini for generating text recommendations, OpenAI DALL-E for creating visual representations, and machine learning (Random Forest) for additional predictions based on fitness data.

Features
	1.	Personalized Fitness Recommendations:
	•	Workout plans tailored to user fitness goals.
	•	Meal plans optimized for fitness objectives.
	•	Celebrity-inspired workout routines (optional).
	2.	Visual Representations:
	•	Images of workout routines and meal plans generated by DALL-E.
	3.	Predictive Insights:
	•	ML-based prediction of resting BPM based on age and fitness data.
	4.	Interactive User Input:
	•	Collect user preferences directly through input prompts.
	5.	Environment Configuration:
	•	Seamless integration with .env files to manage API keys and configurations securely.

Prerequisites
	1.	API Keys:
	•	Google Gemini API key.
	•	OpenAI API key.
	2.	Libraries:
Install required libraries using:

pip install langchain-google-genai openai python-dotenv pandas scikit-learn


	3.	Environment:
	•	Python 3.7 or later.
	•	Jupyter Notebook (or Google Colab for hosted environments).
	4.	Data:
	•	A CSV file containing fitness data with Age, Gender, and Resting_BPM columns.

How to Use
	1.	Clone the Repository:

git clone <repository_url>
cd <repository_directory>


	2.	Setup Environment Variables:
Create a .env file with the following:

GEMINI_API_KEY=<your_google_gemini_api_key>
OPENAI_API_KEY=<your_openai_api_key>


	3.	Run the Script:
Execute the code in a Jupyter Notebook or Google Colab:
	•	Provide your fitness goal and optional celebrity inspiration.
	•	View the generated workout plan, meal plan, and recommendations.
	4.	Train the Machine Learning Model:
	•	Ensure fitness_data.csv is available in the correct path.
	•	Modify train_test_split parameters or add your dataset as needed.
	5.	Generate Visual Representations:
	•	Workout and meal plans will be accompanied by AI-generated images.

Key Functions

1. User Input
	•	get_user_preferences(): Collects fitness goals and celebrity preferences.

2. Google Gemini Integration
	•	fetch_workout_data(): Generates workout plans.
	•	fetch_meal_plan(): Generates meal plans.

3. OpenAI DALL-E Integration
	•	generate_image(): Creates visuals for workout and meal plans.

4. ML Model Integration
	•	Trains a Random Forest Classifier to predict resting BPM.

5. Display Results
	•	Combines textual recommendations and AI-generated visuals for a complete user experience.

Example Workflow
	1.	Input:
	•	User enters:
	•	Fitness goal: “Build muscle.”
	•	Celebrity: “Chris Hemsworth.”
	2.	Output:
	•	Workout Plan: Weightlifting routine with a focus on hypertrophy.
	•	Meal Plan: High-protein meals with lean meats and vegetables.
	•	Visuals: AI-generated images of exercises and meals.
	•	Insight: Based on resting BPM prediction, personalized advice on recovery.

File Structure

.
├── fitness_chatbot.ipynb   # Main script
├── fitness_data.csv        # Dataset for ML model
├── .env                    # API keys
└── README.md               # Documentation

Future Enhancements
	•	Extend the ML model to include additional features like BMI and activity level.
	•	Support for more advanced queries and multilingual capabilities.
	•	Integration with fitness tracking devices.

Credits
	•	Google Gemini: For generating textual recommendations.
	•	OpenAI DALL-E: For creating workout and meal visuals.
	•	Scikit-learn: For machine learning predictions.
 	•	fitness_data.csv - Kaggle by Nadeem Majeed - Fitness Tracker Dataset
Insights into Exercise Habit, Health Metric, and Fitness Level Across Individual