# ✍️ Project Reflection

## AI Tools Used
What tools did you use (e.g., ChatGPT, Copilot)? How did they help?
-> For this project, I primarily used ChatGPT as my conversational development assistant. It played a central role throughout the coding and design process of the Weather  application. ChatGPT helped me:

Design and refine core functions such as get_weather_data, parse_weather_question, and generate_weather_response.
Improve error handling and structure a user friendly interface using pyinputplus.
Add data visualisations with matplotlib for temperature and precipitation trends.
Test and debug the application through guided examples of unit testing and mock API responses.
Prepare for deployment, including instructions for packaging with PyInstaller and writing a professional README.md.

In short, ChatGPT acted like an interactive tutor and coding partner it explained why each change was necessary, showed alternative implementations, and helped me understand the reasoning behind each design choice.


## Prompting Techniques
Which intentional prompting strategies did you apply?

I deliberately applied multiple intentional prompting strategies during my conversations to get high-quality results and deeper understanding:

Restating the problem – Before each coding request, I rephrased the task in my own words (e.g., “I want to fetch weather data for a given location and handle invalid inputs gracefully”).
Requesting pseudocode before implementation – I often asked for a step-by-step outline before requesting the full code (e.g., for parsing user questions).
Iterative refinement – After receiving an initial solution, I asked follow-up prompts to improve input validation, modularity, and error handling.
Challenging edge cases – I tested how the AI would handle invalid cities, API failures, and network issues to strengthen resilience.
Design trade-off discussions – I queried whether to use wttr.in vs OpenWeatherMap, and when to modularise or package code separately for deployment.
Code explanation requests – I frequently asked for detailed explanations of how specific lines of code worked, improving my conceptual understanding.
These prompting methods ensured that my interaction with ChatGPT was thoughtful and goal-driven rather than passive.

## What Worked Well?
Describe one thing you’re proud of.
I’m most proud of how the project evolved iteratively through collaboration with the AI.
Initially, I had a basic function that could only fetch raw weather data. Through progressive prompting, it transformed into a complete, user friendly, and modular application with data validation, clear error messages, and visual outputs.
The visualisation functions were particularly rewarding—seeing the temperature and precipitation charts come to life confirmed that the AI guidance and my applied understanding were working together effectively.

I’m also proud that I didn’t just copy suggestions; I questioned, modified, and integrated them into my own coding style, which helped me build confidence as a developer.



## What Would You Do Differently?
Describe one thing you'd change if you had more time.
If I had more time, I would focus on enhancing the natural language interface by integrating a lightweight NLP library such as spaCy or transformers to better understand varied user queries.
I’d also like to improve the modular testing framework by adding automated test cases for the user interface layer and creating mock datasets for more complex scenarios.
Additionally, exploring OpenWeatherMap as an alternative API with richer datasets would provide more flexibility and improve forecast accuracy.


## Final Thoughts
Any parting comments on your learning experience?
This project was a significant learning experience that demonstrated how AI can be a genuine partner in problem solving and software design.
I learned that effective use of AI tools isn’t about accepting every response but about collaborating intentionally, using clear prompts, and critically evaluating outcomes.
The process helped me strengthen my programming, debugging, and documentation skills while also teaching me how to communicate technical requirements precisely.

Overall, I feel more confident in applying AI-assisted workflows for real-world software projects and in understanding the importance of human oversight, critical thinking, and iterative improvement when working with generative AI tools.
