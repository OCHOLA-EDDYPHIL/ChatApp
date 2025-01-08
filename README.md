# Django Realtime Chat Application

This is a Django-based real-time chat application that allows users to create chat rooms and exchange messages in
real-time. Users can join existing rooms or create new ones, and messages are updated dynamically using AJAX.

## Features

- **Create or Join Chat Rooms**: Users can either join an available chat room or create a new one by entering a room
  name and their username.
- **Realtime Messaging**: Messages sent in a room are dynamically updated for all users currently connected to the room
  without requiring a page refresh.
- **AJAX Integration**: Utilize AJAX to retrieve and send messages asynchronously for a better user experience.
- **User-Friendly Interface**: Clean and responsive UI for creating rooms and exchanging messages.

## Folder Structure

The core components of this application include:

1. **views.py**:
    - Contains the logic for handling user requests such as creating rooms, sending messages, and fetching messages in
      real-time.

2. **Templates**:
    - `home.html`: The landing page where users can enter a room name and username.
    - `room.html`: The chat room interface where real-time messaging happens.

3. **Models (`Room` and `Message`)**:
    - `Room`: Represents individual chat rooms.
    - `Message`: Stores messages sent by users in each room.

4. **Static/Frontend Assets**:
    - Included inline CSS and JavaScript for a responsive and dynamic experience.

## Prerequisites

To run the application, you need the following:

1. **Python 3.12.8**
   Make sure Python is installed. You can download it from the [official Python website]().
2. **Django Framework**
   Ensure Django is installed via pip. If not, use the following command:

``` bash
   pip install django
```

## Installation Guide

Follow these steps to set up and run the project:

1. **Clone Repository**:

``` bash
   git clone https://github.com/OCHOLA-EDDYPHIL/ChatApp.git
```

``` bash
   cd ChatApp
```

2. **Create Virtual Environment**:

``` bash
   python -m venv venv
```

3. **Activate Virtual Environment**:

``` bash
   .venv\Scripts\activate
```

4. **Install Dependencies**: Ensure all project dependencies are installed:

``` bash
   pip install -r requirements.txt
```

5. **Set Up Database**: Run migrations to set up the database:

``` bash
   python manage.py makemigrations
```

``` bash
   python manage.py migrate
```

6. **Run the Development Server**: Launch the server locally:

``` bash
   python manage.py runserver
```

7. **Access the Application**: Open your web browser and navigate to `http://127.0.0.1:8000`.

## How It Works

1. **Home Page**:
    - The application starts with the `home.html` page.
    - Enter a room name and username to create or join a chat room.

2. **Chat Room**:
    - Once inside a room, users can send and receive messages.
    - Messages are fetched dynamically every second using JavaScript and AJAX.

3. **Message Storage**:
    - Messages are stored in the database with room and sender details.

## AJAX Functionality

The application leverages AJAX for seamless real-time updates. The key JavaScript snippets include:

- **Fetching Messages**: Messages are fetched periodically from the server using an AJAX GET request.
- **Sending Messages**: Messages are posted asynchronously to the server without reloading the page.

## Project Example Pages

1. **Home Page**:
   Simple form allowing users to:
    - Enter a room name.
    - Enter a username.
    - Redirect to the specified room.

2. **Chat Room**:
    - Displays real-time messages in the room.
    - Allows sending new messages with an input form.

## Possible Enhancements

- Add user authentication for improved security.
- Display timestamps in a more user-friendly format.
- Add notifications for new messages.
- Incorporate WebSockets for even better real-time messaging.
- Improve CSS for more polished visual design.

## License

This project is open-source, and you are free to modify or use it for your own purposes.
Enjoy building and expanding on the Django Realtime Chat Application!
