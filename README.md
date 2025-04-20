# Robot Control API

This project demonstrates a FastAPI-based REST API for controlling a robot's movement. The API allows clients to send velocity commands to control the robot's linear and angular velocities via HTTP requests.

## Features

- **REST API**: A FastAPI-based server to receive and process velocity control commands.
- **Velocity Command**: Accepts a JSON payload to control the robot's linear and angular velocities.
- **External Communication**: The API sends the velocity commands to the robot (simulated or real) via an HTTP request.

## Prerequisites

To run this API, you will need Python and the following dependencies:

1. Install Python 3.8 or higher.
2. Install the required dependencies by using `pip`:
    ```bash
    pip install fastapi pydantic requests uvicorn
    ```

## Setup Instructions

1. **Clone the repository**:
    ```bash
    git clone https://github.com/Techboy-lab2025/robot_control_api.git
    cd robot_control_api
    ```

2. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the FastAPI server**:
    ```bash
    uvicorn robot_control_api:app --reload
    ```

This will start the FastAPI server, which will be available at `http://localhost:8000`.

## API Endpoints

### POST `/cmd_vel`

This endpoint accepts velocity commands in JSON format to control the robot's movement.

#### Request Body Example:
```json
{
  "linear_x": 0.5,
  "angular_z": 0.0
}
