# Football Team Management System

## Overview
The Football Team Management System is a Python-based application designed to manage football teams and their players. This project uses SQLite3 as the database backend and SQLAlchemy as the Object-Relational Mapping (ORM) tool. The system allows users to add teams and players, retrieve information about teams and players, and display this information in a structured format.

## Features
- Add, delete, and display football teams.
- Add, delete, and display football players.
- Find teams and players by ID.
- View related players for a team.

## Technology Stack
- Programming Language: Python
- Database: SQLite3
- ORM: SQLAlchemy

## Requirements
- Python 3.8 or above
- SQLAlchemy

## Installation
1. Clone the repository:
    ```sh
    git clone <repository_url>
    ```

2. Install dependencies:
    ```sh
    pipenv -- python 3.10 install
    ```

3. Activate the virtual environment:
    ```sh
    pipenv shell
    ```

4.  Reseting database schema:
    ```sh
    python3 lib/reset_db.py
    ```
5. Run the application:
    ```sh
    python3 lib/cli.py
    ```

## Usage
Follow the on-screen instructions to interact with the application via the CLI.

## Database Schema
The project consists of two main tables: `teams` and `players`.

- `teams`
  - `id` (Primary Key, Integer):Unigue identifier for each team.
  - `name` (String):Name of the team.
  - `city` (String):City the team is based in.
  - `stadium`(String):Name of the team`s stadium.

- `players`
  - `id` (Primary Key, Integer, Auto-increment):Unique identifier for each team.
  - `name` (String):Name of player.
  - `position` (String):Position of the player in the team.
  - `team_id` (Foreign Key, Integer):The ID of the team the player belongs to.

## DB Diagram
│+--------------------+         +--------------------+
|      Teams         |         |      Players       |
+--------------------+         +--------------------+
| id (PK)            |         | id (PK)            |
| name               |         | name               |
| city               |         | position           |
| stadium            |         | team_id (FK)       |
+--------------------+         +--------------------+


