#📝 Chatlog Parser

This Python script parses HTML chat log data (e.g., from MidJourney or Discord exports) using `BeautifulSoup` and extracts key information, including user IDs, timestamps, prompts, image URLs, and mentions. The output is saved as a structured CSV, making it easy to analyze chat interactions and trends.

---

## 📦 Installation

Ensure you have Python installed, then install the required libraries:

```bash
pip install pandas beautifulsoup4

```
Output
The script prints the resulting DataFrame and saves it to chatlog.csv.

##  ▶️ Usage
Prepare your HTML file
Name your chatlog file sample.html and place it in the same directory as chatlog_parser.py.
python chatlog_parser.py

#Run the script

```bash
python chatlog_parser.py
```

## 📄 Output Fields
The script prints the resulting DataFrame and saves it to chatlog.csv.

##📄 Output Fields

| Column           | Description                                              |
| ---------------- | -------------------------------------------------------- |
| `user_id`        | Unique (pseudonymized) identifier for the message sender |
| `timestamp`      | Date and time of the message                             |
| `message_prompt` | Text content of the message (excluding `@mentions`)      |
| `image_url`      | URL of any image associated with the message             |
| `mentions`       | List of mentioned user IDs (if any)                      |


##💡Example Use Cases

-Analyzing how users prompt generative models

-Tracking prompt behavior over time

-Filtering for prompt-image relationships in multimodal systems

##📜 License
This project is licensed under the MIT License.
