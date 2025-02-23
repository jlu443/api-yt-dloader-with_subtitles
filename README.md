# YouTube Video Downloader API with Subtitle Support

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## Description
The YouTube Video Downloader and Info API is a Flask-based Python project that allows you to download YouTube videos and retrieve video information using Pytube. This versatile tool provides two main functionalities:

1. **Download Video:** You can specify the video URL and resolution to download YouTube videos directly to your local machine.

2. **Get Video Info:** You can retrieve detailed information about a YouTube video, including its title, author, length, views, description, and publish date.

This project is designed to simplify the process of interacting with YouTube content programmatically.

## Features
- Download YouTube videos in various resolutions.
- Retrieve comprehensive information about YouTube videos.
- Error handling for reliable performance.
- JSON API endpoints for easy integration into other applications.

## Libraries and Technologies Used
- Python 3.x
- Flask for building the API.
- yt_dlp for interacting with YouTube content.
- re for URL validation.

## Usage
1. Clone this repository: `git clone https://github.com/jlu443/api-yt-dloader-with_subtitles.git`
2. Install the required libraries: `pip install flask yt_dlp requests`
3. Run the Flask application: `python main.py`
4. Access the API endpoints using HTTP requests (e.g., POST requests in Postman).

## API Endpoints

### Subtitle Support
- **Subtitles:** This parameter is optional. Keep blank by not writing the "subtitles" field to not need to download subtitles.
- Writing "true", "false" or any type of string input will activate subtitles.

### Download Video by Resolution
- **Endpoint:** `/download/<resolution>`
- **HTTP Method:** POST
- **Request Body:** JSON
    ```json
    {
        "url": "https://www.youtube.com/watch?v=VIDEO_ID"
        "subtitles": "true"
    }
    ```

### Get Video Info
- **Endpoint:** `/video_info`
- **HTTP Method:** POST
- **Request Body:** JSON
    ```json
    {
        "url": "https://www.youtube.com/watch?v=VIDEO_ID"
        "subtitles": true
    }
    ```

## Screenshots
### Downloading a Video without Subtitles
![image](https://github.com/jlu443/api-yt-dloader-with_subtitles/blob/main/pictures/useCase1.png)

### Downloading a Video with Subtitles
![image](https://github.com/jlu443/api-yt-dloader-with_subtitles/blob/main/pictures/useCase2.png)

### Retrieving Info
![image](https://github.com/jlu443/api-yt-dloader-with_subtitles/blob/main/pictures/useCase3.png)


## Code Repository
You can access the source code for this project on [GitHub](https://github.com/jlu443/api-yt-dloader-with_subtitles/blob/main/main.py).

## License
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT). You are free to use, modify, and distribute the code while providing appropriate attribution.
