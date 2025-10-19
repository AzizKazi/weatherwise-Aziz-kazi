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

Create your copy
On GitHub: Use this template → create your repo.
Clone locally or open in Colab.
Open the notebook
Work in starter_notebook.ipynb.
Install dependencies (first notebook cell)
pip install pyinputplus matplotlib requests


Run core functions (quick sanity check)
data = get_weather_data("Perth", days=3)
create_temperature_visualisation(data)
create_precipitation_visulisation(data)
create_windspeed_visulisation(data)
parse_weather_question("What is the temperature in Perth tomorrow?")


(Optional) Enable the compact menu
The menu cell references older helper names. Add these aliases above weather_app_menu():
fetch_weather = get_weather_data
interpret_question = parse_weather_question
build_response = generate_weather_response
visualize_temperature = create_temperature_visualisation
visualize_rainfall = create_precipitation_visulisation
visualize_wind = create_windspeed_visulisation


Then run:
weather_app_menu()
Log your AI conversations
Save each as text in ai-conversations/ (Conversation-1, Conversation-2, …).

Commit often

Aim for ≥ 15 meaningful commits showing your development journey.
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

Code & Features
 get_weather_data, parse_weather_question, generate_weather_response implemented and working.
 At least 2 visualisations working (temperature, precipitation, wind optional third).
 Menu runs or functions callable directly in notebook.
 Tests runnable (mocked) or clearly documented with expected results.

Documentation
 README.md updated (description, how to run, structure, checklist).
 AI conversations saved as text in ai-conversations/ (≥ 5 significant).
 Before/after examples included (at least 3).
 Reflection (300–500 words) completed in submission/reflection.md.

Version Control
 GitHub repo invited instructor.
 ≥ 15 meaningful commits showing progression.

Packaging & LMS
 Repo is tidy; unnecessary artifacts removed.
 Downloaded ZIP of entire repo for LMS submission.
 Notebook executes top-to-bottom without errors (or clearly marks optional cells).
 Nice-to-have (bonus credibility)
 Brief note on limitations (e.g., simple city parsing; noon wind heuristic).
 Clear error messages when data missing or network fails.

---

🧠 AI Conversations  
AI interactions in the `ai-conversations/` folder.  
See `ai-conversations/how-to-log-ai-conversations.md` for details.


--
## 🧠 Need Help with AI Prompts?

Check out:
Check out:
- `resources/ai-tips-tricks.md` — Prompting tips and pitfalls
- `resources/sample-prompting-journey.md` — Full example of AI-enhanced development
- `resources/prompts-by-method-step.md` — Prompts aligned with the 6-step dev process
- `resources/before-after-example.md` — Required: Show how your prompting improved AI-generated code


Good luck and have fun! 💡🌤️
