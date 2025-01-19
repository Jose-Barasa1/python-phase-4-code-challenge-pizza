# Pizza Restaurant API

## Overview

This repository contains a Flask-based API for managing a Pizza Restaurant domain. The backend is a Flask application that interacts with a SQLite database to manage restaurants, pizzas, and the relationship between them through a linking table (`RestaurantPizza`). The frontend is a fully built React application for testing the API in a realistic setting. This README provides setup instructions, usage guidelines, and details about the API functionality.

## Features

- **Flask-based API** for managing restaurants, pizzas, and restaurant-pizza associations.
- **React frontend** to interact with the API.
- **Testable routes** using Postman or pytest.
- **Database migrations and seeding** for testing data.
- **Validations** on restaurant-pizza relationships.
  
## Table of Contents

1. [Setup Instructions](#setup-instructions)
2. [API Routes](#api-routes)
3. [Testing](#testing)
4. [Database Models](#database-models)
5. [Validations](#validations)

## Setup Instructions

### Prerequisites

- Python 3.7 or higher
- Node.js and npm

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/pizza-restaurant-api.git
    cd pizza-restaurant-api
    ```

2. Install Python dependencies:

    ```bash
    pipenv install
    pipenv shell
    ```

3. Install React frontend dependencies:

    ```bash
    npm install --prefix client
    ```

4. Initialize and migrate the database:

    ```bash
    export FLASK_APP=server/app.py
    flask db init
    flask db migrate
    flask db upgrade head
    ```

5. Seed the database:

    ```bash
    python server/seed.py
    ```

6. Start the Flask backend:

    ```bash
    python server/app.py
    ```

7. Start the React frontend:

    ```bash
    npm start --prefix client
    ```

The API will be available at `localhost:5555`, and the frontend will be available at `localhost:4000`.

### Running Tests

To run the tests with `pytest`, use the following command:

```bash
pytest -x
