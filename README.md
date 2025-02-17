# Advanced-English-Writing

# Essay Correction API  

## Overview  
This project is a **FastAPI-based essay correction service** that utilizes **Google's Gemini AI** to correct spelling and grammar, provide suggestions, and assign a grade. The application integrates with **MySQL** to store correction history.  

## Features  
- Accepts an **essay topic** and **text** as input  
- Validates that the essay length  
- Uses **Gemini AI (Generative AI)** to:  
  - Correct grammar, spelling, and punctuation  
  - Provide suggestions for improvement  
  - Analyze text relevance to the topic  
  - Assign a grade (**Needs Improvement, Good, Great, Excellent**)  
- Stores correction results in a **MySQL database**  

## Tech Stack  
- **Backend Framework:** FastAPI  
- **AI Model:** Google Gemini API  
- **Database:** MySQL  
- **Data Validation:** Pydantic  

## API Endpoints  

### Correct Essay  
**Endpoint:** `POST /correct`  
**Request Body:**  
```json
{
  "topic": "Climate Change",
  "text": "Climate chnge is a big problem. It effect many peoples."
}
```  
**Response Example:**  
```json
{
  "corrected_text": "Climate change is a big problem. It affects many people.",
  "suggestions": "1. 'chnge' should be 'change'.\n2. 'effect' should be 'affects'.",
  "grade": "Good"
}
```  
