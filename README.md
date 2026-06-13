# Number Guessing Game

A command-line number guessing game built with Bash and PostgreSQL.

## Description

This application generates a random secret number between 1 and 1000 and challenges the user to guess it.

User statistics are stored in a PostgreSQL database, including:

- Username
- Total games played
- Best game (fewest guesses)

Returning users can view their game history and best score before starting a new game.

## Features

- Random number generation
- Username-based player profiles
- PostgreSQL database integration
- Input validation for integers
- Tracks total games played
- Tracks best game score

## Technologies Used

- Bash
- PostgreSQL
- Git

## Database Structure

### users

| Column | Type |
|----------|----------|
| user_id | SERIAL PRIMARY KEY |
| username | VARCHAR(22) UNIQUE NOT NULL |

### games

| Column | Type |
|----------|----------|
| game_id | SERIAL PRIMARY KEY |
| user_id | INT REFERENCES users(user_id) |
| guesses | INT NOT NULL |

