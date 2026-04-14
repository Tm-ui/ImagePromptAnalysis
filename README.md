# Chatlog Parser

Python script that parses HTML chat logs (from MidJourney or Discord exports) and extracts user IDs, timestamps, prompts, image URLs, and mentions into a structured CSV. Built with BeautifulSoup.

I used this to analyze prompt-image relationships in a dataset of 1,298 Midjourney interactions for a multimodal AI analysis project.

## Usage

Place your chatlog file as `sample.html` in the same directory, then:

```bash
pip install pandas beautifulsoup4
python chatlog_parser.py
```

Output is saved to `chatlog.csv`.

## Output fields

| Column | Description |
|--------|-------------|
| `user_id` | Pseudonymized identifier for the message sender |
| `timestamp` | Date and time of the message |
| `message_prompt` | Text content of the message (excluding @mentions) |
| `image_url` | URL of any associated image |
| `mentions` | List of mentioned user IDs |
