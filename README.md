# Store
# https://t.me/Sudokuh
# Financial assistant based on telegram bot

This project is a telegram bot created using Python and aiogram that helps you keep track of your personal finances. The bot allows users to manage spending categories, set aliases for them, and also receive spending statistics in a convenient format.

The bot also has a version for deployment to pythonanywhere using flask (webhook)

Aiogram Flask template with webhooks to deploy to pythonanywhere free plan

# Main functions
- Adding spending categories: Users can create categories to track various expenses.
- Setting aliases: For ease of entry, users can set aliases for spending categories.
- Expense statistics: The bot provides detailed expense statistics by category.
- Email notifications: Using Celery and Redis, the bot can send notifications about financial transactions via email or provide a link to a Google spreadsheet.
- Implemented a webhook to work correctly on the free pythonanywhere plan


# Installation

1. Clone the repository

If you don't use Git, you can simply download the repository source code in a ZIP archive and extract it to your computer.

2. Create a virtual environment and activate it
```
python -m venv venv
for Mac
source venv/bin/activate
or
for Win
source venv/Skripts/activate
```

3. Rename .env.example to .env and follow the instructions inside this file

## If you are using Docker:

4. Run docker-compose

```
cd infra/

docker-compose up -d
```
5. If the telegram-budget container does not work correctly, restart the containers:

```
docker-compose stop
docker-compose up -d
```

## If you are not using Docker

6. In the telegram-budget directory, run the following commands:

```
python main.py

celery -A tasks.tasks:app worker --loglevel=INFO --pool=solo

celery -A tasks.tasks:app flower
```

# Ready!
You have successfully installed the bot and are ready to start using it!

# Contribution to the project
If you have suggestions for improvement or find a bug, feel free to create an issue, send a pull request, or write directly to the author. Your input is welcome!


#Author
[Diashov Makar](https://github.com/ForTeamEffect)
