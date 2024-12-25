# Twitter Trends Viewer

Twitter Trends Viewer is a web application that fetches the top trending topics on Twitter using Selenium, ProxyMesh, and MongoDB, and displays them on a simple and elegant HTML page.

## Features

- **Fetch Twitter Trends**: Automatically logs into Twitter, fetches the latest trending topics, and stores them in a MongoDB database.
- **Proxy Support**: Uses ProxyMesh for secure and anonymous web scraping.
- **Responsive UI**: Displays the fetched trends, including the timestamp, IP address, and JSON record, in a clean and user-friendly interface.
- **MongoDB Integration**: Trends are stored in a MongoDB database with unique IDs for easy access.

---

## Installation and Setup

### Prerequisites

- Python 3.8+
- MongoDB instance (local or cloud)
- Selenium WebDriver (Microsoft Edge)
- Node.js (optional for further customization)
- ProxyMesh credentials

### Clone the Repository

```bash
$ git clone [<repository-url>](https://github.com/TheCoderAdi/stir-webscrape-intern
$ cd stir-webscrape-intern
```

### Install Dependencies

   Install Python dependencies:
   ```bash
   $ pip install -r requirements.txt
   ```

### Configure Environment

1. Create a `.env` file in the `root` folder:

   ```python
       TWITTER_USERNAME = "your-twitter-username"
       TWITTER_PASSWORD = "your-twitter-password"
       MONGO_URI = "mongodb://localhost:27017"
       PROXYMESH_USERNAME = "your-proxymesh-username"
       PROXYMESH_PASSWORD = "your-proxymesh-password"
   ```

### Run the Application

1. Start the Flask server:
   ```bash
   $ python app.py
   ```
2. Open your browser and navigate to:
   ```
   http://127.0.0.1:5000
   ```

---

## File Structure

```
.
├── app.py                # Flask app to serve the frontend and backend
├── src
│   ├── selenium_script.py # Selenium script for web scraping
│   ├── config.py          # Configuration file for credentials
├── static
│   ├── index.html         # Main HTML file for the UI
├── requirements.txt      # Python dependencies
└── README.md             # Project documentation
```

---

## How It Works

1. **Proxy and IP Setup**:

   - The application uses ProxyMesh for secure access to Twitter.
   - IP testing ensures the proxy is functional.

2. **Selenium Web Scraping**:

   - Logs into Twitter using credentials.
   - Fetches trending topics using XPath selectors.

3. **Data Storage**:

   - Trends are stored in MongoDB with a unique ID and timestamp.

4. **Frontend Display**:

   - Trends are fetched from the backend and displayed in a user-friendly interface.

---

## Technologies Used

- **Backend**: Python, Flask
- **Frontend**: HTML, CSS, JavaScript
- **Database**: MongoDB
- **Web Scraping**: Selenium
- **Proxy Management**: ProxyMesh

---

## Known Issues

- Twitter may restrict access if the scraping frequency is too high.
- ProxyMesh limits may apply depending on your subscription.
- Ensure that your Selenium WebDriver version matches your browser version.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

## Acknowledgments

- [Selenium](https://www.selenium.dev/)
- [ProxyMesh](https://proxymesh.com/)
- [MongoDB](https://www.mongodb.com/)
