# Network Security Project for Phishing Data

A comprehensive network security project focused on phishing data analysis and detection using machine learning.

## Project Overview

This project implements a machine learning-based system for detecting and analyzing phishing attempts in network data. It includes data processing, model training, and a web interface for predictions.

## Features

- Data processing and validation pipeline
- Machine learning model for phishing detection
- FastAPI-based web interface
- MongoDB integration for data storage
- MLflow integration for experiment tracking
- Docker support for containerization

## Prerequisites

- Python 3.8+
- MongoDB
- Docker (optional)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/nageshwarpatel7/networksecurity
cd NetworkSecurity
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Configuration

1. Create a `.env` file in the root directory with the following variables:
```
MONGODB_URI=your_mongodb_uri
```

## Usage

### Running the Web Application

```bash
uvicorn app:app --reload
```

The application will be available at `http://localhost:8000`

### API Endpoints

- `/predict`: Submit data for phishing prediction
- `/docs`: Swagger UI documentation
- `/redoc`: ReDoc documentation

### Data Processing

Use `push_data.py` to process and push data to MongoDB:
```bash
python push_data.py
```

## Project Structure

```
.
├── app.py                 # FastAPI application
├── main.py               # Main application logic
├── push_data.py          # Data processing script
├── requirements.txt      # Project dependencies
├── setup.py             # Package configuration
├── templates/           # Web templates
├── final_model/         # Trained model files
├── data_schema/         # Data schema definitions
├── Network_Data/        # Network data files
└── prediction_output/   # Prediction results
```

## Development

### Running Tests

```bash
python test_mongodb.py
```

### Docker Support

Build and run the Docker container:
```bash
docker build -t network-security .
docker run -p 8000:8000 network-security
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

