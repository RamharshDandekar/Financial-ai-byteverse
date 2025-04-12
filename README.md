# GenAI-Powered Financial Assistant

## Project Description

This project is a GenAI-powered financial assistant designed to improve financial literacy and empower better investment decisions, particularly in regions with low financial literacy rates.  It provides users of all financial backgrounds with personalized guidance, investment product discovery, and tools to manage their finances effectively. By leveraging the power of Generative AI, we aim to bridge the financial literacy gap and make informed investing accessible to everyone for personal and educational use.

**This project is intended for personal, non-commercial use and educational purposes. Contributions are welcome to improve the project for the community.**

## Features

*   **Financial Question Resolver (AI Teacher):**  Engage in natural language conversations with an AI chatbot to get answers to basic and complex financial questions.
*   **Personalized Advice based on Financial Literacy Level:** The AI adapts its responses based on the user's self-declared financial knowledge (low, medium, advanced).
*   **Investment Product Discovery:** Find suitable investment options based on user preferences, risk tolerance, and investment goals.
*   **Live Share Market Data & Analysis:** Track live share prices, get AI-powered analysis of specific stocks, and receive investment recommendations based on price and risk.
*   **Financial Risk Finder (PDF Policy Analysis):** Upload insurance policies (PDF format) and receive AI-driven analysis highlighting potential loopholes and unfavorable clauses.
*   **Budget Planner:** Track income and expenses, get spending suggestions, and plan budgets aligned with life goals.
*   **Multilingual Support:**  (To be implemented/Specify languages) Access the assistant in multiple languages to reach a wider audience.
*   **User Authentication & Registration:** Secure login and registration system to personalize user experience and track progress.
*   **Terms & Conditions and Privacy Policy:**  Clearly defined terms of service and privacy policy for user transparency.

## Solution Technology Stack

This project leverages a modern and robust technology stack to deliver a powerful and scalable financial assistant platform.  Here's a breakdown of the key technologies used:

*   **Frontend:**
    *   **React:** A JavaScript library for building dynamic and interactive user interfaces, ensuring a user-friendly experience.

*   **Backend:**
    *   **Django:** A high-level Python web framework that enables rapid development of secure and maintainable backend APIs and data management.

*   **Database:**
    *   **MongoDB:** A NoSQL document database chosen for its flexibility and scalability in handling diverse data types, including user data, financial information, and AI-generated analysis.

*   **Fine-tune Models Training & AI/ML Services:**
    *   **Gemini (Google):**  The core Generative AI model driving the intelligent features of the assistant, including the chatbot, PDF risk analysis, and potentially aspects of share data analysis.
    *   **LangChain:** A framework designed to augment and orchestrate Large Language Models (LLMs) like Gemini, likely used to enhance the AI's reasoning capabilities, data integration, and overall performance within the financial domain.

*   **Authentication:**
    *   **Clerk:** A dedicated authentication and user management service, ensuring secure user registration, login, and session management with ease of implementation.

This technology stack is carefully selected to ensure scalability, maintainability, security, and optimal performance for delivering a cutting-edge GenAI-powered financial assistant.

## Installation

Follow these steps to set up the project locally:

**Prerequisites:**

*   [Node.js](https://nodejs.org/) (version >= 16.0.0 recommended) and npm (or yarn) installed (for frontend).
*   [Python](https://www.python.org/) (version >= 3.8 recommended) and pip installed (for backend).
*   [MongoDB](https://www.mongodb.com/docs/manual/installation/) installed and running (if using MongoDB locally).
*   API Keys:
    *   **GenAI API Key:** You will need to obtain an API key from (Specify AI provider - e.g., Google Gemini API, OpenAI). Set this as an environment variable (e.g., `GEMINI_API_KEY` or `OPENAI_API_KEY`).
    *   **Share Market Data API Key:** If using a share market data API, obtain an API key and set it as an environment variable (e.g., `MARKET_DATA_API_KEY`).

**Frontend Setup (React):**

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/RamharshDandekar/Financial-ai-byteverse.git
    cd Financial-ai-byteverse
    ```

2.  **Install frontend dependencies:**
    ```bash
    npm install  # or yarn install
    ```

3.  **Environment Variables (Frontend):**
    *   Create a `.env.local` file in the `frontend` directory.
    *   Add any frontend-specific environment variables here (if needed). For example:
        ```
        # Example: API Base URL if different from default
        # REACT_APP_API_BASE_URL=http://localhost:8000/api  (Django backend default port is often 8000)
        ```

4.  **Start the frontend development server:**
    ```bash
    npm start  # or yarn start
    ```
    The frontend application should now be running at `http://localhost:3000` (or a similar address).

**Backend Setup (Django):**

1.  **Navigate to the backend directory:**
    ```bash
    cd ../backend 
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Linux/macOS
    venv\Scripts\activate  # On Windows
    ```

3.  **Install backend dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Ensure you have a `requirements.txt` file listing Django and other Python dependencies)*

4.  **Environment Variables (Backend - Django):**
    *   Create a `.env` file in the `backend` directory.
    *   Add your API keys and database connection details to this file. For example:
        ```
        GEMINI_API_KEY=YOUR_GEMINI_API_KEY
        MARKET_DATA_API_KEY=YOUR_MARKET_DATA_API_KEY
        DATABASE_URL=mongodb://user:password@host:port/database_name  # Example for MongoDB (if using Django with MongoDB)
        SECRET_KEY=your_django_secret_key # Generate a strong secret key for Django
        DEBUG=True # Set to False for production
        ```

5.  **Database Setup (MongoDB):**
    *   Ensure MongoDB is running and accessible. Create a database named (Specify database name from `.env` or configuration).
    *   **Run Django Migrations:**  Apply database migrations to set up your database schema.
        ```bash
        python manage.py migrate
        ```

6.  **Start the backend server (Django):**
    ```bash
    python manage.py runserver
    ```
    The Django backend API should now be running at `http://localhost:8000` (default Django development server address).

## Usage

1.  **Access the application:** Open your web browser and go to the frontend URL (e.g., `http://localhost:3000`).
2.  **Login/Register:** Create a new account or log in with existing credentials.
3.  **Explore Features:** Use the navigation bar to access different features:
    *   **Financial Question Resolver:**  Start chatting with the AI by typing your financial questions in the chat interface.
    *   **PDF Risk Analysis:** Upload a PDF insurance policy document to get an analysis of potential risks and loopholes.
    *   **Share Market Data:** Search for specific stocks to view live data and AI-powered analysis.
    *   **Budget Planner:**  Input your income and expenses to create a budget and get spending insights.
    *   (And other features as implemented)
4.  **Interact with the AI:**  For features involving AI, provide clear and concise inputs to get the best responses.

## Contributing

We welcome contributions to improve this project for personal and educational use! To contribute:

1.  **Fork the repository.**
2.  **Create a new branch** for your feature or bug fix: `git checkout -b feature/your-feature-name` or `git checkout -b bugfix/your-bugfix-name`.
3.  **Make your changes and commit them:** `git commit -m "Add your descriptive commit message"`.
4.  **Push your branch to your forked repository:** `git push origin feature/your-feature-name`.
5.  **Create a Pull Request** to the main repository, describing your changes in detail.

## License

**Non-Commercial Use License**

**Permitted Uses:**

*   **Personal Use:** You are free to use, modify, and run this project for your own personal, non-commercial purposes.
*   **Educational Use:**  You may use this project for educational purposes, such as in classrooms, workshops, or for self-learning.
*   **Contribution:** You are encouraged to contribute to this project to enhance its features and functionality for the benefit of the community, under the same non-commercial license terms.

**Prohibited Uses:**

*   **Commercial Use:**  **Commercial use of this project is strictly prohibited.** This includes, but is not limited to:
    *   Selling or distributing this project or any part of it for commercial gain.
    *   Incorporating this project or any part of it into commercial products or services.
    *   Using this project or any part of it for business operations or revenue generation.
*   **Distribution for Commercial Purposes:** You may not distribute this project in any context where commercial gain is the primary objective.

**Disclaimer:**

This project is provided "as is" without warranty of any kind.  The authors and contributors are not responsible for any consequences arising from the use of this project.  Financial decisions should be made with due diligence and potentially with the advice of a qualified financial professional.

**By using, modifying, or contributing to this project, you agree to abide by the terms of this Non-Commercial Use License.**


## Contact

For questions or inquiries, please contact:

Team Nxt_Byte
