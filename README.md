##PASAH (Pennsylvania Search Area for Housing)

#Overview
PASAH is a graphical user interface (GUI) application that allows users to input city names within Pennsylvania and retrieve information about various metrics such as Walk Score, Transit Score, Bike Score, Population, Crime Index, and House Values. The data is displayed dynamically through tables and visualized using pie charts and bar charts, with additional visualization for house value trends over time.

#Features
1.	City Search: Search for cities in Pennsylvania and display detailed information such as Walk Score, Crime Index, Population, and House Values.
2.	Data Visualization: Provides dynamic pie charts comparing the selected city's population with top or bottom 5 cities and bar charts comparing city scores.
3.	House Value Trends: Visualizes house value trends over time for the selected city.
4.	Interactive GUI: Built with tkinter for a user-friendly and dynamic interface.
5.	Data Handling: Loads and processes data from CSV files for city metrics, such as Walk Score, Crime Index, and House Values.

#Requirements
•	Python 3.10.15
•	Required packages:
 - pandas
 - matplotlib
 - requests
 - beautifulsoup4
 - tkinter (built-in with Python)
 - PIL (built-in with Python)
 - webbrowser (built-in with Python)
You can install the required packages using pip:

[BASH]
pip install pandas matplotlib requests beautifulsoup4
Installation

Step 1: Install Anaconda
If you don't have Anaconda installed, download it from the official website and follow the installation instructions for your operating system.

Step 2: Create and Set Up the Environment
To create and activate the environment:

1.	Create a new environment using Python 3.10.15:
[BASH]
conda create --name pasah_env python=3.10.15 conda activate pasah_envconda create --name pasah_env python=3.10.15
conda activate pasah_env

2.	Install the required packages:
[BASH]
conda install pandas
conda install matplotlib
pip install requests
pip install beautifulsoup4

tkinter, PIL, and webbrowser are included in Python by default, so no additional installation is required for these.

Step 3: Running the Application

1.	Once all dependencies are installed, you can run the program by executing:
[BASH]
python main.py

2.	This will open the PASAH GUI, where you can enter city names to get data and view visualizations.
3.	Program Composition
•	Graphical User Interface (GUI): Built with Tkinter for displaying city metrics, search functionality, and visualization.
•	Data Processing: The program uses pandas to load and manipulate data from CSV files, including Walk Score, Population, Crime Index, and House Values.
•	Visualization: Dynamic pie charts and bar charts are created using matplotlib to display city comparisons, as well as line charts to show house value trends over time.

Key Files:
•	data_processing.py: Handles the data scraping and loading for city metrics like Walk Score, Crime Index, and House Values.
•	graph_maker.py: Contains the functions responsible for generating pie charts, bar charts, and house value trend charts.

#Workflow
1. Initialize Environment:
•	Import necessary libraries like tkinter, pandas, matplotlib, requests, and beautifulsoup
•	Set up the main application window using tkinter.

2. Data Loading:
•	Use data_processing.py to scrape or load city data (Walk Score, Population, Crime Index, House Values) from CSV files.
•	Load the data using pandas into appropriate DataFrames.

3. Search for a City:
•	The user enters a city name in the search box.
•	data_processing.get_city_data() retrieves the city's data from the DataFrame, matching the input city name.

4. Display City Data:
•	Display the city's metrics in a grid layout (Walk Score, Transit Score, Bike Score, Population, Crime Index, and House Values).
•	Compare these metrics to Pennsylvania averages using a dynamically generated table.

5. Visualization:
•	Use graph_maker.plot_population_pie_chart() to generate a pie chart comparing the selected city's population to the top or bottom 5 cities in Pennsylvania.
•	Use graph_maker.plot_comparison_bar_chart() to generate a bar chart comparing the city's Walk Score, Transit Score, Bike Score, and Crime Index against state averages.
•	Use graph_maker.plot_home_value_trends() to generate a line chart showing the house value trends over the past 10 years.

6. Toggle Views:
•	Provide the user with a toggle button to switch between viewing the top 5 or bottom 5 cities for the population comparison chart.

7. Interaction:
•	Allow the user to navigate and interact with the app, including switching between different visualizations and returning to the search function.
•	The app runs continuously, awaiting user input via the tkinter event loop.

#Usage Flow:
1.	Search for a City: Enter a city name into the search box.
2.	Display City Data: The application retrieves and displays city data such as Walk Score, Transit Score, Population, Crime Index, and House Values.
3.	Visualization: Visualize the selected city's metrics in relation to top or bottom cities using pie charts and bar charts. View house value trends over time using line charts.
4.	Toggle Views: Toggle between viewing the top 5 or bottom 5 cities in terms of population comparison.

![image](https://github.com/user-attachments/assets/bc449813-fd74-4557-b8f9-daf045ac92dd)
