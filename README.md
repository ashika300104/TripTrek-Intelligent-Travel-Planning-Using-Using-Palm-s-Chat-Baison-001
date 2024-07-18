TITLE: TripTrek: Intelligent Travel Planning Using Using Palm’s Chat-Baison-001

TEAM: 

ASHIKA.K.R.K – 21MIS0004
NILANI.S.E     -   21MIS0017
AKSHITHAA.S – 21MIS0308

PROJECT DESCRIPTION 

TripTrek is an AI-powered travel planning platform designed to revolutionize the way people plan and organize their trips. By leveraging advanced artificial intelligence algorithms, TripTrek offers users personalized travel itineraries tailored to their preferences, interests, and budget constraints. The platform combines machine learning models with rich travel data to provide users with comprehensive recommendations for accommodations, activities, dining options, transportation, and more. With TripTrek, travelers can say goodbye to the hassle of manually researching and organizing every  aspect of their trip and instead enjoy a seamless and stress-free travel planning experience.

Scenario 1: Family Vacation Coordination
TripTrek helps families plan their vacations by taking user inputs such as destination and number of days to generate a detailed itinerary. It suggests family-friendly attractions like amusement parks, museums, and scenic spots, and provides recommendations for nearby restaurants and cafes that cater to diverse dietary needs. The output is a day-by-day itinerary that includes timings for visits to attractions, meal breaks at recommended food places, and suggested activities for relaxation and entertainment, ensuring a balanced and enjoyable trip for all family members.

Scenario 2: Business Travel Planning for Professionals
TripTrek streamlines business travel for professionals by taking user inputs like destination and number of days to create a comprehensive itinerary. It recommends key business venues such as conference centers and meeting locations, along with local attractions for downtime. Additionally, it provides suggestions for nearby restaurants and cafes suitable for business lunches and dinners. The output is a detailed day-by-day schedule that includes meeting times, locations, and meal breaks at recommended food places, helping professionals maximize their time and maintain productivity during their trip.

Scenario 3: Educational Trip for Students
TripTrek assists in planning educational trips for students by taking inputs like destination and number of days to produce a structured itinerary. It suggests educational and historical sites, museums, universities, and science centers that align with the trip's educational goals. Furthermore, it provides recommendations for student-friendly dining options, including affordable restaurants and food courts. The output is a day-by-day itinerary that includes timings for visits to educational sites, meal breaks at recommended food places, and leisure activities, ensuring a balanced and engaging trip for students.

PROJECT FLOW

Users input text into the UI of Inquisitive.
The input text is then processed and analyzed by the PALM architecture, which is integrated into the backend.
PALM autonomously generates questions based on the input text.
The generated questions are sent back to the frontend for display on the UI.
Users can view the dynamically generated questions and interact with them to gain deeper insights into the content.

To accomplish this, we have to complete all the activities listed below,

Requirements Specification
Create a requirements text file to list the required libraries
 Install the required libraries
Initializing the PALM
Generate PALM API
Initialize the pre-trained model
Interfacing with Pre-trained Model
Questions Generator

Model Deployment
Deploy the application using Streamlit

PRIOR KNOWLEDGE
You must have prior knowledge of the following topics to complete this project.

LLM & PALM: https://cloud.google.com/vertex-ai/docs/generative-ai/learn-resources
Streamlit: https://www.datacamp.com/tutorial/streamlit

PROJECT STRUCTURE

Create the Project folder which contains files as shown below:

app.py: It serves as the primary application file housing both the model and Streamlit UI code.
requirements.txt: It enumerates the libraries necessary for installation to ensure proper functioning.

Milestone 1 : Requirements specification

Specifying the required libraries in the requirements.txt file ensures seamless setup and reproducibility of the project environment, making it easier for others to replicate the development environment.

Activity 1: Create a requirements text file to list the required libraries

                          
streamlit: Streamlit is a powerful framework for building interactive web applications with Python.
google-generativeai: Python client library for accessing the GenerativeAI API, facilitating interactions with pre-trained language models like chat-baison-001 .
altair<5 :  Python library for data visualization, providing a simple and intuitive API for creating interactive visualizations, especially for datasets smaller than 5 million rows (Altair<5).


Activity 2 : Install the required libraries

              
Open the terminal.
Run the command: pip install -r requirements.txt
This command installs all the libraries listed in the requirements.txt file

Milestone 2 : Initializing the PALM
The Google API key is a secure access token provided by Google, enabling developers to authenticate and interact with various Google APIs. It acts as a form of identification, allowing users to access specific Google services and resources. This key plays a crucial role in authorizing and securing API requests, ensuring that only authorized users can access and utilize Google's services.For initializing the model we need to generate PALM API.

Activity 1: Generate PALM API

Click on the link (https://developers.generativeai.google/). 
Then click on “Get API key in Google AI Studio”. 
Click on “Get API key” from the right navigation menu.
Now click on “Create API key”. (Refer the below images)
Copy the API key.


After signing in to your account, navigate to the 'Get an API Key' option. Clicking on this option will redirect you to another webpage.

Next, click on 'Create API Key' and choose the generative language client as the project. Then, select 'Create API key in existing project'.
Copy the newly generated API key as it is required for loading the pre-trained model.


Activity 2 : Initialize the pre-trained model

Import necessary files

Streamlit, a popular Python library, is imported as st, enabling the creation of user interfaces directly within the Python script.
Importing the palm module: This line imports the palm module from the google.generativeai package.

Configuration of the PALM API with the API key and initialize translator

Configuring the API key: The configure function is used to set up or configure the Google API with an API key. The provided API key, in this case, is " AIzaSyBv_2Br0SYxHDxuC-u7FM4fKCwqXXXXXX".
The Translator class facilitates language translation capabilities within the application.

Define the model to be used

The line model_name = "models/chat-bison-001" sets the variable model_name to the string "models/chat-bison-001", which identifies a specific model provided by Google’s PaLM (Pathways Language Model) API.
This variable is used in subsequent API calls to specify which model to use for generating responses based on user prompts.

To change the background and add pictures

Milestone 3 : Interfacing with Pre-trained Model

In this milestone, we will build a prompt template to generate code based on user description and language.

Activity 1 : Questions Generator


When the button is pressed, it initializes placeholders for the itinerary and nearby food places. It then constructs a prompt incorporating the user-provided destination and number of days.
The prompt is sent to the AI model (specified by model_name) to generate the itinerary. During this process, a spinner is displayed to indicate that the system is working.
If the generation is successful, the resulting itinerary is displayed in a text area. 
If an error occurs, detailed error messages are shown, and users are prompted to check their inputs and try again. 
This approach ensures a user-friendly experience, guiding users through generating and viewing their custom travel plans.

Milestone 4 : Model Deployment

In this milestone, we are deploying the created model using streamlit. Model deployment using Streamlit involves creating a user-friendly web interface for deploying machine learning models, enabling users to interact with the model through a browser. Streamlit provides easy-to-use tools for developing and deploying data-driven applications, allowing for seamless integration of machine learning models into web-based applications.

Activity 1 : Deploy the application using Streamlit

Give the project title , Description and Describe the scenarios

The provided code introduces TripTrek, an AI-driven travel planning platform aimed at revolutionizing trip organization. It leverages advanced AI algorithms to offer personalized itineraries
Three scenarios illustrate TripTrek's capabilities: Family Vacation Coordination, Business Travel Planning for Professionals, and Educational Trips for Students, showcasing its ability to cater to diverse travel needs with tailored itineraries and recommendations.

Take user inputs

In this section of the Streamlit application, users are prompted to input their travel destination and the number of days for their trip. 
The st.text_input function is used to capture the destination as a text input from the user, allowing them to specify the location they plan to visit. 
The st.number_input function is then employed to obtain the number of days for the trip, with a minimum value of 1 day and a maximum of 30 days, allowing users to select the duration of their stay using a convenient stepper interface. 
These inputs are essential for generating a personalized travel itinerary, as they provide the necessary parameters for the AI model to tailor recommendations for activities, accommodations, dining options, and other travel-related details specific to the user's chosen destination and trip length.
Run The Web Application

Open the anaconda prompt from the start menu
Navigate to the folder where your Python script is.
Now type “streamlit run app.py” command
Navigate to the localhost where you can view your web page

Now, the application will open in the web browser.

DEMO LINK : https://youtu.be/sDVTP5vTPrY




