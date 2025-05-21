#  Self Care Microservice

This microservice analyzes user journal entries for sentiment and returns a positivity score along with a motivational message. It is designed to support the MoodMate app by providing emotional feedback through natural language processing.

---

##  Setup Instructions

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd your-repo-folder
```

2. Create a Virtual Environment
 ```bash  
python -m venv venv
.\venv\Scripts\activate   # On Windows
```

3. Install Dependencies
```bash
pip install -r requirements.txt
```
4. Running the FastAPI Server
```bash
uvicorn main:app --reload
```
Server will start at: http://127.0.0.1:8000

API Usage
POST /api/analyze

Request Headers
```bash
Content-Type: application/json
```
Request Body
```bash
{
  "mood": "neutral",
  "journal_text": "Today was tough, but I didn’t give up."
}
```

Response Body
```bash
{
  "positivity_score": 0.4215,
  "motivational_message": "You are stronger than you think."
}
```

 Test Program
To test the service programmatically, run:
```bash
python test_program.py
```
The test will POST a sample journal entry to the microservice and print the returned JSON result.

UML Diagram
```markdown

![UML Diagram](路径/或/GitHub链接)
```
Notes：
```bash
Sentiment analysis is done using the VADER sentiment intensity analyzer.
Messages are not tied to score ranges, but are randomly selected.
```
License：
This microservice is for educational purposes only. No license is provided.
