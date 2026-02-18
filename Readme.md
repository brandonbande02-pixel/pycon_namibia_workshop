# PyCon Namibia Workshop

A FastAPI-based application for the PyCon Namibia workshop, integrating Twilio messaging and Google Generative AI.

## Prerequisites

- Python 3.8 or higher
- Git
- Twilio account 
- Google API key 

## Clone the Repository

```bash
git clone https://github.com/brandonbande02-pixel/pycon_namibia_workshop.git
cd pycon_namibia_workshop
```

## Setup Instructions

### 1. Create and Activate Virtual Environment

On **Windows (PowerShell)**:
```powershell
.\Scripts\Activate.ps1
```

On **Windows (Command Prompt)**:
```cmd
.\Scripts\activate.bat
```

On **macOS/Linux**:
```bash
source bin/activate
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure Environment Variables

Create a `.env` file in the root directory and add your configuration:

```env
# Twilio Configuration (optional)
TWILIO_ACCOUNT_SID=your_twilio_account_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_PHONE_NUMBER=your_twilio_phone_number

# Google Generative AI Configuration (optional)
GOOGLE_API_KEY=your_google_api_key

# Server Configuration
HOST=127.0.0.1
PORT=8000
```

### 4. Run the Application

```bash
uvicorn main:app --reload
```

The application will be available at `http://127.0.0.1:8000`

## API Documentation

Once the server is running, you can access:
- **Swagger UI**: `http://127.0.0.1:8000/docs`
- **ReDoc**: `http://127.0.0.1:8000/redoc`

## Project Structure

```
pycon_namibia_workshop/
├── main.py                  # FastAPI application entry point
├── requirements.txt         # Python dependencies
├── .env                     # Environment variables (not version controlled)
├── pyvenv.cfg              # Virtual environment configuration
└── README.md               # This file
```

## Dependencies

- **uvicorn**: ASGI server
- **fastapi**: Web framework
- **pydantic**: Data validation
- **twilio**: SMS/messaging services
- **google-genai**: Google Generative AI integration
- **python-dotenv**: Environment variable management

## Troubleshooting

### Virtual Environment Issues
If the activation script doesn't work, try creating a new virtual environment:
```bash
python -m venv .
```

### Missing Dependencies
Make sure you're in the activated virtual environment before installing:
```bash
pip list  # Verify you see installed packages
pip install -r requirements.txt
```

### Port Already in Use
If port 8000 is already in use, specify a different port:
```bash
uvicorn main:app --reload --port 8001
```

## Contributing

Follow PEP 8 guidelines and ensure all dependencies are documented in `requirements.txt`.

## License

MIT

