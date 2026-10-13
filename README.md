# EXP-15
# Multimodal Receipt Information Extraction

## Aim
To explore multimodal prompting using a vision-capable LLM to extract structured information from a restaurant receipt image and validate the total.

## Problem Statement
Analyze a restaurant receipt image and extract the restaurant name, date, ordered items, subtotal, tax, and total. Return the extracted information as JSON and check whether subtotal plus tax equals the total.

## Technologies Used
- Python
- OpenAI API
- GPT-4o-mini vision model
- Base64 image encoding
- JSON

## Algorithm
1. Install the required OpenAI Python package.
2. Set the OpenAI API key as an environment variable.
3. Load the receipt image.
4. Encode the image in Base64.
5. Create a multimodal prompt requesting structured JSON.
6. Send the prompt and image to the vision model.
7. Parse and display the returned JSON.
8. Validate whether subtotal plus tax equals total.
9. Print the validation result.

## Project Structure
```text
Multimodal_Receipt_Extraction/
├── main.py
├── receipt.jpg
├── README.md
├── requirements.txt
└── .gitignore
```

## Installation
```bash
pip install -r requirements.txt
```

## API Key Setup

Windows PowerShell:
```powershell
$env:OPENAI_API_KEY="your_api_key_here"
```

Linux/macOS:
```bash
export OPENAI_API_KEY="your_api_key_here"
```

Replace the placeholder with your valid OpenAI API key.

## Run the Experiment
Place `receipt.jpg` in the project directory and run:

```bash
python main.py
```

## Expected Output
The program displays the extracted receipt data as a JSON object, followed by a validation result:
- `PASSED` when subtotal plus tax equals the total.
- `FAILED` when the values do not match.
- `INCOMPLETE` when any required amount is unavailable.

The extracted values depend on the actual receipt image.

## Conclusion
This experiment demonstrates multimodal prompting, image encoding, structured JSON extraction, and arithmetic validation using a vision-capable large language model.
