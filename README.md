
---
title: ASD Video Screening Backend
emoji: 🧠
colorFrom: blue
colorTo: indigo
sdk: docker
pinned: false
---

# ASD Video Screening Backend

This Space runs the Flask backend for the ASD video classification project using Docker.

## Notice

This is an academic experiment only. It is not a clinically validated diagnostic tool. Model scores are not clinical probabilities.

## Model

The trained model is stored at:

`models/ASD_VGG16_LSTM_model.keras`

## API Endpoints

- `GET /` - Backend welcome message
- `GET /health` - Check whether the backend is running
- `POST /upload` - Upload a video
- `POST /predict` - Process a video and return the prediction

## Prediction Request

Send a POST request to `/predict` using multipart form data.

The file field must be named `video`.

Supported formats: MP4, AVI, MOV, MKV, MPEG, MPG.

## Deployment

This Space uses Docker to run the Flask backend on port `7860`.

The backend must successfully install its dependencies, load the trained model, and process a video before real predictions can be confirmed.
