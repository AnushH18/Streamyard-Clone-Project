# Streamyard Clone

This project aims to create a simplified clone of Streamyard, allowing users to stream audio and video via a web interface using Node.js, Express, Socket.IO, and ffmpeg for media processing and streaming.

## Features

- **Streaming Interface:** Provides a basic web interface to start streaming audio and video.
- **Real-time Communication:** Uses Socket.IO for real-time communication between clients and server.
- **Media Processing:** Utilizes ffmpeg for encoding and streaming media to an RTMP server.

## Prerequisites

Before you begin, ensure you have the following installed on your development machine:

- Node.js (version 18.x recommended)
- npm (normally comes with Node.js installation)
- ffmpeg (for media processing and streaming)

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/AnushH18/Streamyard-Clone-Project.git
    cd Streamyard-Clone
    ```

2. **Install dependencies:**

    ```bash
    npm install
    ```

3. **Build Docker image (optional):**

    If you prefer to run the application in a Docker container, follow these steps:

    ```bash
    docker build -t streamyard-clone .
    ```

## Usage

1. **Start the application:**

    To run the application locally without Docker, use:

    ```bash
    npm start
    ```

    This will start the Node.js server at `http://localhost:3000`.

2. **Access the application:**

    Open your web browser and go to [http://localhost:3000](http://localhost:3000) to access the Streamyard Clone interface.

3. **Start streaming:**

    - Click on the "Start" button to initiate streaming.
    - Grant necessary permissions when prompted to access your audio and video devices.

4. **Streaming to RTMP server:**

    By default, the application streams to `rtmp://a.rtmp.youtube.com/live2/dcfx-m7v2-j248-3185-9207`. Modify the `options` array in `index.js` to change the RTMP server configuration.

## Docker Deployment

If you opted to build a Docker image, run the following command to start the container:

```bash
docker run -p 3000:3000 streamyard-clone
