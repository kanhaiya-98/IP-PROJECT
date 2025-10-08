AI-Powered Travel Itinerary PlannerAn intelligent travel planning application that allows users to create, save, and manage detailed day-by-day travel itineraries. This tool leverages a powerful AI to provide smart suggestions for trips, all wrapped in a sleek, modern user interface.✨ FeaturesDynamic Itinerary Creation: Automatically generates day-wise planning cards based on user-selected dates.Detailed Day Planning: Add multiple activities with specific timings for each day of the trip.AI-Powered Suggestions: Get intelligent travel ideas and suggestions using the integrated Groq API.Persistent Storage: Save and manage multiple travel itineraries, which are stored securely in a database.Sleek, Modern UI: A beautiful, responsive interface with glass-morphism effects and intuitive navigation.Project Insights: Includes dedicated sections explaining the project's architecture and the development team.🛠️ Technology StackThis project is built with a modern, minimal-setup technology stack:Frontend:HTML5Tailwind CSSVanilla JavaScriptBackend:Java 11+Spring Boot 2.7.xSpring Data JPADatabase:H2 In-Memory Database (No installation required)Build Tool:Maven Wrapper (Included in the project)AI Integration:Groq API🚀 Getting StartedFollow these instructions to get a copy of the project up and running on your local machine.PrerequisitesMake sure you have the following software installed on your system:GitJava Development Kit (JDK) - Version 11 or newer.Visual Studio CodeExtensions:Extension Pack for Java (by Microsoft)Live Server (by Ritwick Dey)Installation & SetupClone the RepositoryOpen your terminal or command prompt and run the following command:git clone [https://github.com/kanhaiya-98/IP-PROJECT.git](https://github.com/kanhaiya-98/IP-PROJECT.git)
Navigate to the Project Directorycd IP-PROJECT
Run the Backend ServerIn your terminal, navigate to the backend folder:cd TravelPlanner-Backend
Start the Spring Boot application using the Maven Wrapper:On Windows:mvnw spring-boot:run
On macOS/Linux:./mvnw spring-boot:run
The backend will start on http://localhost:8080.Run the Frontend ApplicationOpen the TravelPlanner-Frontend folder in a new VS Code window.Right-click on the index.html file.Select "Open with Live Server".The application will open in your default browser.Add Your API Key (Important!)In the TravelPlanner-Frontend folder, open the index.html file.Find the line (around line 377) that contains:const GROQ_API_KEY = 'YOUR_GROQ_API_KEY';
Replace 'YOUR_GROQ_API_KEY' with your actual Groq API key.Note: This API key will only be on your local machine and should not be committed to GitHub.📂 Project StructureThe project is organized into two main directories: TravelPlanner-Backend for the server-side logic and TravelPlanner-Frontend for the user interface..
├── .gitignore
├── TravelPlanner-Backend/
│   ├── src/main/java/com/travelplanner/
│   │   ├── config/
│   │   ├── controller/
│   │   ├── model/
│   │   ├── repository/
│   │   └── TravelItineraryPlannerApplication.java
│   ├── src/main/resources/
│   │   └── application.properties
│   └── pom.xml
└── TravelPlanner-Frontend/
    └── index.html
🧑‍💻 Created ByThis project was developed by a team of passionate students from the AI & DS Department.Aditya YadavAyush YadavIshita Yadav
