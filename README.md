Root Directory
app/: Contains the main pipeline notebook for the support ticket system. ( NOT YET UPDATED! )

Final_Pipeline_Support_ticket_draft_.ipynb: The primary notebook for the support ticket pipeline, including Pinecone integration and Zapier email automation.
data/: Contains datasets used for training and testing the system.

helpdesk_customer_multi_lang_tickets.csv: Multilingual customer support tickets.
helpdesk_customer_tickets (1).csv: Customer support tickets dataset.
train-00000-of-00001-a5a7c6e4bb30b016.parquet: Training data in Parquet format.
rough/: Contains exploratory work and drafts for various components of the project.

Analysis/: Exploratory data analysis (EDA) notebooks and scripts.
Automated Response/: Drafts and experiments for automated response generation.
Integrations/: Integration scripts and experiments with third-party tools.
Issue Prevention Dashboard/: Work on dashboards for issue prevention.
Project_Submission_P2 (Automated Response)/: Submission-ready files for the automated response component.
Project_Submission_P2 (Data Analysis)/: Submission-ready files for the data analysis component.
Real Time Escalation/: Work on real-time escalation systems.
Sentiment Analysis/: Sentiment analysis experiments and notebooks.
README.md: This file, providing an overview of the project.

ticket

Features
Automated Ticket Resolution:

Retrieves similar past issues using vector embeddings and Pinecone.
Generates personalized responses using OpenAI's GPT models.
Email Integration:

Integrates with Zapier and ngrok for automated email responses.
Multilingual Support:

Handles support tickets in multiple languages.
Real-Time Escalation:

Identifies and escalates critical issues in real-time.
Sentiment Analysis:

Analyzes customer sentiment to prioritize and personalize responses.
Issue Prevention Dashboard:

Provides insights into common issues and trends to prevent future problems.
Setup Instructions
Prerequisites
Python 3.10 or later.
Required Python libraries (install via pip):
pip install pandas numpy openai pinecone-client sentence-transformers transformers ngrok zapier
API keys for:
OpenAI
Pinecone
Zapier
ngrok (if using local tunneling)
Steps to Run the Pipeline
Clone the Repository:

git clone <repository_url>
cd <repository_directory>
Set Up Environment Variables: Create a .env file in the root directory and add your API keys:

OPENAI_API_KEY=your_openai_api_key
PINECONE_API_KEY=your_pinecone_api_key
ZAPIER_API_KEY=your_zapier_api_key
NGROK_AUTH_TOKEN=your_ngrok_auth_token
Run the Pipeline: Open the Final_Pipeline_Support_ticket_api_.ipynb notebook in Jupyter or Google Colab and execute the cells.

Test the System:

Input a sample support ticket in the notebook.
Verify that the system retrieves similar issues and generates a response.
Check your email for the automated response (if Zapier integration is set up).
