# AI-Powered Travel Itinerary Planner

[](https://opensource.org/licenses/MIT)

An intelligent travel planning application that allows users to create, save, and manage detailed day-by-day travel itineraries. This tool leverages a powerful AI to provide smart suggestions for trips, all wrapped in a sleek, modern user interface.

-----

## ✨ Core Features

  * **Dynamic Itinerary Creation:** Automatically generates day-wise planning cards based on user-selected dates.
  * **Detailed Day Planning:** Add multiple activities with specific timings for each day of the trip.
  * **AI-Powered Suggestions:** Get intelligent travel ideas and activity suggestions using the integrated Groq API.
  * **Persistent Storage:** Save and manage multiple travel itineraries, which are stored securely in a Spring Boot-powered backend.
  * **Sleek, Modern UI:** A beautiful, responsive interface built with Tailwind CSS, featuring glass-morphism effects and intuitive navigation.
  * **Project Insights:** Includes dedicated sections explaining the project's architecture and the development team.

-----

## 🏛️ System Architecture

This project follows a classic client-server architecture:

1.  **Frontend (Client):** A static application built with **HTML, Tailwind CSS, and Vanilla JavaScript**. It handles all user interactions and UI rendering.
2.  **Backend (Server):** A **Java Spring Boot** application that exposes a REST API. It manages all business logic, data validation, and communication with the database.
3.  **Database:** A **H2 In-Memory Database** is used for persistent storage of user itineraries.
4.  **AI Integration:** The frontend communicates **directly with the Groq API** to fetch AI-powered travel suggestions.

-----

## 🛠️ Technology Stack

This project is built with a modern, minimal-setup technology stack:

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Frontend** | HTML5, Tailwind CSS, Vanilla JavaScript | For the responsive user interface and client-side logic. |
| **Backend** | Java 11+, Spring Boot 2.7.x | For the robust server-side REST API. |
| **Data Persistence** | Spring Data JPA, H2 In-Memory DB | For saving and retrieving itinerary data. |
| **AI Integration** | Groq API | For generating intelligent travel suggestions. |
| **Build Tool** | Maven Wrapper (Included) | For managing backend dependencies and running the server. |

-----

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing.

### 1\. Prerequisites

Make sure you have the following software installed on your system:

  * [Git](https://git-scm.com/)
  * [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html) - Version 11 or newer.
  * [Visual Studio Code](https://code.visualstudio.com/)
      * **Recommended Extension:** [Extension Pack for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack) (by Microsoft)
      * **Recommended Extension:** [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) (by Ritwick Dey)

### 2\. Clone the Repository

Open your terminal or command prompt and run the following command:

```bash
git clone https://github.com/kanhaiya-98/IP-PROJECT.git
cd IP-PROJECT
```

### 3\. Run the Backend (Spring Boot)

The backend server must be running to save and load itineraries.

```bash
# Navigate to the backend folder
cd TravelPlanner-Backend

# Start the Spring Boot application using the Maven Wrapper
# On Windows:
./mvnw.cmd spring-boot:run

# On macOS/Linux:
./mvnw spring-boot:run
```

The backend will start and be accessible at `http://localhost:8080`.

### 4\. Run the Frontend (Vanilla JS)

**Important:** Do not simply open `index.html` in your browser. It must be served by a local server to handle API requests properly.

1.  **Add Your API Key (Securely):**

      * In the `TravelPlanner-Frontend` folder, create a new file named `config.js`.
      * Add the following content to `config.js`:

    <!-- end list -->

    ```javascript
    // This file is in .gitignore to protect your key!
    const GROQ_API_KEY = 'your-actual-groq-api-key-here';
    ```

      * Replace `'your-actual-groq-api-key-here'` with your actual Groq API key.
      * The `index.html` file is already set up to load this key. **Do not** paste your key directly into `index.html`.

2.  **Start the Live Server:**

      * Open the `TravelPlanner-Frontend` folder in a **new VS Code window**.
      * Right-click on the `index.html` file.
      * Select "**Open with Live Server**".

The application will automatically open in your default browser (e.g., at `http://127.0.0.1:5500`).

-----

## 🔌 API Endpoints

The backend server provides the following REST API endpoints for managing itineraries.

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/itineraries` | Creates a new travel itinerary. |
| `GET` | `/api/itineraries` | Retrieves a list of all saved itineraries. |
| `GET` | `/api/itineraries/{id}` | Retrieves a single itinerary by its unique ID. |
| `DELETE` | `/api/itineraries/{id}` | Deletes an itinerary by its unique ID. |

-----

## 📂 Project Structure

The project is organized into two main directories: `TravelPlanner-Backend` for the server-side logic and `TravelPlanner-Frontend` for the user interface.

```
.
├── .gitignore
├── TravelPlanner-Backend/
│   ├── .mvn/
│   ├── src/main/java/com/travelplanner/
│   │   ├── config/          # Spring configurations
│   │   ├── controller/      # REST API endpoints
│   │   ├── model/           # JPA entity classes (e.g., Itinerary, Day, Activity)
│   │   ├── repository/      # Spring Data JPA interfaces
│   │   └── TravelItineraryPlannerApplication.java  # Main application entry point
│   ├── src/main/resources/
│   │   └── application.properties   # Database and server configuration
│   ├── mvnw
│   ├── mvnw.cmd
│   └── pom.xml            # Maven project dependencies
│
└── TravelPlanner-Frontend/
    ├── config.js          # (You must create this) API key configuration
    └── index.html         # Main (and only) HTML file
```

-----

## 🤝 Contributing

Contributions are welcome\! If you have suggestions for improvements or find any bugs, please feel free to open an issue or submit a pull request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

-----

## 📄 License

This project is distributed under the MIT License. See `LICENSE` file for more information (if one exists), or check the [MIT License details](https://opensource.org/licenses/MIT).

-----
