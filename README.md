# URL Shortener

A simple URL shortener service to make an API to build short URLs. The functionality will be similar to Bitly. Using Node, Express, MongoDB, and Postman you can make your own URL Shortener service. 

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Postman Requests](#postman-requests)
- [Contributing](#contributing)

## Features

- Shorten long URLs into unique short-codes.
- Store URL mappings in a MongoDB database.
- Easy integration with Postman for testing and automation.

## Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- Node.js and npm
- Express.js
- MongoDB
- Postman

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/url-shortener-service.git
   cd url-shortener-service
2. Install dependencies:
   ```
   npm install
3. Configure MongoDB:
   - Create a MongoDB database and note the connection URI.
    
   - Update the config/default.json file with your MongoDB URI:
      ```bash
      {
        "mongoURI": "your-mongodb-connection-uri",
        "baseUrl": "http://localhost:5000"
      }
## Usage
### Postman Requests
 1. Open Postman and import the provided collection: URL Shortener Postman Collection.

 2. Set the base URL in Postman to http://localhost:5000 or your deployed URL.

 3. Use the following requests:

    - Shorten URL:
    
      - Method: POST
      - Endpoint: /api/url/shorten
      - Body (JSON):
        ```bash
        {
          "longUrl": "your-long-url-here"
        }
4. Send the Request. This request creates an entry in MongoDB, shortening the provided long URL and generating a unique short code.
   - Sample MongoDB Data:
     ```bash
     {
         _id : "unique id"
        longUrl : "your-long-url-here"
        shortUrl : "short-url"
        urlCode : "short-url-code"
        date : "Date-of-sending-request"
     }
## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.
