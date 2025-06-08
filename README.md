Aircraft & Airline Chatbot
Welcome to the Aircraft & Airline Chatbot, an interactive web app built with Streamlit that lets users ask questions about European airlines, aircraft models, and live flight information.

Overview
This chatbot helps users:

Get detailed information about specific aircraft models (like Airbus A320, Boeing 737, etc.).

Learn about airlines operating in Europe, including their fleet.

Compare two aircraft models based on specifications.

Access live flight status for sample flights.

Retrieve general airline info from Wikipedia with summaries and links.

The chatbot interface features an aviation-themed design with smooth gradients, styled chat bubbles, and emoji-enhanced headers.

Features
1. Aircraft Model Information
Users can type the name of an aircraft model.

The bot returns detailed specs including:

Airlines operating the model

Number of engines

Passenger capacity

Range

Wingspan, length, height

Maximum take-off weight

2. Airline Information and Fleet
Users can ask about an airline.

The bot provides:

A Wikipedia summary about the airline.

A list of aircraft models in that airline’s fleet.

A link to the full Wikipedia page.

3. Aircraft Model Comparison
Users can input queries like:

vbnet
Copy
Edit
Compare A320 and B737
The bot compares key specs side-by-side:

Passenger capacity

Range

Wingspan, length, height

Max take-off weight

4. Live Flight Information (Static Example)
Users can request live flight data.

The bot provides static example flight details (e.g., flight number, departure/arrival airports, scheduled times, status).

Technologies Used
Streamlit: For the interactive web interface and real-time chat experience.

Pandas: To load and manage the European airlines fleet dataset.

Wikipedia API (via wikipedia Python package): To fetch airline summaries.

Difflib: For fuzzy string matching to handle user typos and approximate queries.

Python Regex: To parse comparison queries.

Custom CSS: For a clean, aviation-themed UI with styled chat bubbles and input boxes.

Dataset
The chatbot uses a CSV file european_airlines_fleet_correct.csv which contains:

Aircraft models and their specs

Airlines and their fleet information

The dataset is cleaned and processed for matching user queries.

How to Run Locally
Clone the repository:

bash
Copy
Edit
git clone https://github.com/yourusername/aircraft-airline-chatbot.git
cd aircraft-airline-chatbot
Install dependencies:

bash
Copy
Edit
pip install streamlit pandas wikipedia
Run the app:

bash
Copy
Edit
streamlit run app.py
Open the provided local URL in your browser to chat with the bot.

Usage Examples
Ask about an aircraft model:

vbnet
Copy
Edit
Tell me about the Airbus A320
Ask about an airline:

perl
Copy
Edit
What can you tell me about Lufthansa?
Get the fleet of an airline:

sql
Copy
Edit
Show me the fleet of Ryanair
Compare two aircraft:

vbnet
Copy
Edit
Compare Boeing 737 and Airbus A320
Get live flight info:

lua
Copy
Edit
Show live flight status
Code Structure Overview
load_data(): Loads and cleans the dataset.

identify_query_type(): Determines if user input is about an aircraft model or airline.

format_model_info(): Formats aircraft model specs for display.

format_airline_fleet(): Lists aircraft models for an airline.

fetch_wikipedia_summary(): Retrieves Wikipedia summaries for airlines.

format_airline_info(): Combines airline info and Wikipedia summary.

compare_aircraft_models(): Compares two aircraft on key specifications.

parse_compare_query(): Parses "compare" queries from user input.

fetch_live_flight_info(): Returns static example flight data.

Streamlit UI setup: Custom styling, input handling, and rendering chat history.

Contribution
Feel free to fork, suggest features, or report bugs!

License
This project is licensed under the MIT License.

Made with ✈️ by Fabian Anrei Ruse 
