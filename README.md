# 🌦️ WeatherWise Template

This repository is a starter kit for building a Weather Advisor app that:

fetches multi-day forecasts from wttr.in (no API key),
answers simple natural-language weather questions, and
visualises temperature, rainfall, and wind with matplotlib
It also scaffolds how to document AI collaboration (conversation logs, before/after examples, reflection) so you can meet the assignment’s Intentional Promptingj requirements.

![Build With AI](https://img.shields.io/badge/Built_with-AI-blueviolet?logo=openai)
![Python](https://img.shields.io/badge/Made_with-Python-3776AB?logo=python)
![Visualisation](https://img.shields.io/badge/Includes-Visualisations-orange?logo=plotly)

---

## 🚀 How to Use This Template

1. Create Your Own Repository

Click the “Use this template” button on GitHub.

Create your own repository (name it something like weatherwise-project).

Clone it locally or open it directly in Google Colab or Jupyter Notebook.

2. Open the Main Notebook

Locate the file named starter_notebook.ipynb.

This notebook contains all the core Python functions and visualisations for the project.

3. Install Required Dependencies

Before running any code, install the required Python libraries:

pip install pyinputplus matplotlib requests


These libraries support:

requests → Fetching weather data from the wttr.in API

matplotlib → Creating temperature and precipitation visualisations

pyinputplus → Validating user inputs for menu selections

4. Run and Test Core Functions

Use the provided functions to fetch and visualise weather data:

data = get_weather_data("Perth", days=3)
create_temperature_visualisation(data)
create_precipitation_visulisation(data)
create_windspeed_visulisation(data)
parse_weather_question("What is the temperature in Perth tomorrow?")


These commands will:

Retrieve weather data for a selected city

Generate temperature and precipitation graphs

Parse a natural language weather question

5. Activate the Interactive Menu (Optional)

If you want to use the command-line menu (weather_app_menu()), add the following function aliases above the menu code block:

fetch_weather = get_weather_data
interpret_question = parse_weather_question
build_response = generate_weather_response
visualize_temperature = create_temperature_visualisation
visualize_rainfall = create_precipitation_visulisation
visualize_wind = create_windspeed_visulisation


Then run:

weather_app_menu()


This enables a simple console-based interface where users can:

View weather forecasts

Ask questions in plain English

Display different types of visualisations

6. Record Your AI Conversations

Document your collaboration with AI tools (e.g., ChatGPT, Copilot) and save each conversation as text files in the ai-conversations/ folder.
Name them sequentially (e.g., Conversation-1.txt, Conversation-2.txt, etc.).

 At least five major AI conversations are required for submission.

7. Commit and Push Regularly

Maintain good version control practices:

Make frequent, meaningful commits showing progress.

Aim for at least 15 commits that capture different stages (setup, implementation, debugging, final testing).

Example commit messages:

git add .
git commit -m "Added get_weather_data function with error handling"
git push origin main

8. Prepare for Submission

Before submitting:

Ensure all required files are included (README.md, reflection.md, AI conversations, and the notebook).

Download a ZIP file of your repository.

Submit it through your LMS according to the assignment instructions.
---

## 📁 Folder Structure
| **Folder / File**                        | **Description / Purpose**                                                   |
| ---------------------------------------- | --------------------------------------------------------------------------- |
| **ai-conversations/**                    | Stores all AI conversation logs demonstrating intentional prompting.        |
| ├── `conversation-1` to `Conversation-5` | Sequential text files containing major AI-assisted development discussions. |
| ├── `how-to-log-ai-conversations.txt`    | Instructions on how to correctly record and format AI conversations.        |
| **resources/**                           | Collection of guides, learning materials, and prompting resources.          |
| ├── `ai-tips-tricks.md`                  | General tips and techniques for working effectively with AI tools.          |
| ├── `assignment-summary.md`              | Overview and objectives of the WeatherWise assignment.                      |
| ├── `before-after-example.md`            | Demonstrates before/after improvements using intentional prompting.         |
| ├── `fetch-my-weather-llm-guide.md`      | Step-by-step guide for using the wttr.in weather API.                       |
| ├── `hands-on-ai-llm-guide.md`           | Practical reference for AI-assisted coding workflows.                       |
| ├── `prompt-by-method-step.md`           | List of structured prompting methods for different use cases.               |
| ├── `python-intentional-prompting.md`    | Python-specific guidance for structured prompting and debugging.            |
| ├── `sample-prompting-journey.md`        | Example illustrating a complete AI-driven project development journey.      |
| ├── `template-repository-beginners.md`   | Reference guide for setting up and using the starter template.              |
| **submission/**                          | Contains final deliverables and documents for submission.                   |
| ├── `checklist.md`                       | Pre-submission checklist to verify all requirements are met.                |
| ├── `reflection.md`                      | 300–500 word reflection on AI collaboration and development experience.     |
| **Root Directory**                       | —                                                                           |
| `.gitignore`                             | Lists files and folders to exclude fro                                      |


---

📄 **Quick Overview:**  Core functions

get_weather_data(city, days=3)
Calls https://wttr.in/{city}?format=j1, trims data['weather'] to days, returns dict; prints a helpful message and returns None on failure.

Visualisations (matplotlib)

create_temperature_visualisation(data)
Bars (max °C) + dotted line (min °C) per day; grid, labels, legend.

create_precipitation_visulisation(data)
Horizontal bars of total daily precipMM; opacity scales with rain intensity.

create_windspeed_visulisation(data)
Line of daily peak wind (km/h) + noon wind scatter.

Natural-language

parse_weather_question(user_q)
Extracts attribute ∈ {temperature, rain/precipitation, humidity, wind}, time_period ∈ {today, tomorrow, day after tomorrow}, and location (simple “in CITY” pattern; defaults to “Sydney”).

generate_weather_response(parsed_q, weather)
Builds readable answers for attribute & day (min/max temp; total rainfall; first-hour humidity; first-hour wind).

Menu

weather_app_menu()
Compact CLI using pyinputplus; options for report, Q&A, and each chart.
🔧 Uses legacy names; add the alias snippet (above) or rename the calls.

Testing stubs

test_get_weather_data_success() / test_get_weather_data_network_error()
Use responses + re to mock HTTP; currently point to fetch_weather (alias to get_weather_data to run).

Data shape used

data['weather'][i]['date']

['maxtempC'], ['mintempC']

['hourly'][…]['precipMM' | 'humidity' | 'windspeedKmph']

---

## 📓 Submission Checklist

Before submitting your WeatherWise project, review the following checklist to ensure that all components are complete and meet the assignment requirements.

-> Code and Functionality

    Implemented all required core functions:

    get_weather_data(location, forecast_days)

    parse_weather_question(question)

    generate_weather_response(parsed_question, weather_data)

    Created at least two working visualisations using matplotlib:

   Temperature trend chart

   Precipitation or windspeed chart

   Implemented a menu system or clear function calls for user interaction

   Included error handling for invalid inputs or missing data

  All notebook cells execute successfully without runtime errors

🧠 AI Conversation Documentation

   At least 5 AI conversation logs saved in ai-conversations/ folder

   Each file follows a clear format (e.g., Conversation-1.txt, Conversation-2.txt, etc.)

   Conversations demonstrate intentional prompting (problem-solving, debugging, and iteration)

   Includes before/after examples showing how AI input improved your code

   Shows at least one example of handling incorrect AI output

📄 Documentation

   README.md file includes:

   Project description and overview

   How to use the template

   Folder structure

   Quick start instructions

   Submission checklist

   ASSIGNMENT.md file present (original instructions and marking guide)

   Reflection document (submission/reflection.md) written (300–500 words)

   All Markdown files (.md) use consistent formatting and headings

🧪 Testing

   Test cases written for get_weather_data() (mocked API)

   Verified code behavior for both success and error conditions

   Visualisations tested with sample data to confirm output

   All outputs render correctly in the notebook

🔁 Version Control

   Repository created from the provided template

   Instructor/invigilator invited to view the repository

   Minimum of 15 meaningful commits showing iterative development

   Clear and descriptive commit messages (e.g., “Added temperature visualisation function”)

📦 Final Submission

   All required files and folders included:

   starter_notebook.ipynb
 
   README.md

   ASSIGNMENT.md

   ai-conversations/

   submission/reflection.md

   Repository zipped for LMS submission

   ZIP file tested for extraction and accessibility
  
   Notebook runs from top to bottom without errors

🌟 Optional (for Bonus Marks)
  
   Implemented third visualisation (windspeed, humidity, etc.)

   Used advanced error handling or caching techniques

   Enhanced the NLP question parsing with more robust logic

   Included additional AI analysis or reflection on project development

✅ Final Check:
  Ensure your repository is well-organised, clearly documented, and demonstrates your understanding of both coding and AI-assisted development.


--
## 🧠 Need Help with AI Prompts?

Check out:
Check out:
- `resources/ai-tips-tricks.md` — Prompting tips and pitfalls
- `resources/sample-prompting-journey.md` — Full example of AI-enhanced development
- `resources/prompts-by-method-step.md` — Prompts aligned with the 6-step dev process
- `resources/before-after-example.md` — Required: Show how your prompting improved AI-generated code


Good luck and have fun! 💡🌤️
