# PetshopRestAPI

Welcome to the **PetshopRestAPI** documentation! This API allows you to manage pet-related data, including pet profiles, adoption status, and owner information.

![Petshop Logo](https://via.placeholder.com/150)

---

## Table of Contents
1. [Overview](#overview)
2. [API Endpoints](#api-endpoints)
3. [Authentication](#authentication)
4. [Usage Examples](#usage-examples)
5. [Installation](#installation)
6. [Contributing](#contributing)

---

## Overview

PetshopRestAPI is designed to provide a seamless experience for managing pet data. This service includes endpoints to:
- Retrieve pet profiles
- Update adoption statuses
- Manage owner details

**Key Features:**
- RESTful API structure
- JSON responses
- Authentication via API key

## API Endpoints

| Endpoint                   | Method | Description                        |
|----------------------------|--------|------------------------------------|
| `/pets`                    | GET    | Retrieve all pets                  |
| `/pets/{pet_id}`           | GET    | Retrieve a single pet by ID        |
| `/pets`                    | POST   | Create a new pet profile           |
| `/pets/{pet_id}`           | PUT    | Update a pet profile               |
| `/pets/{pet_id}/adopt`     | PATCH  | Mark a pet as adopted              |
| `/owners`                  | GET    | Retrieve all owners                |
| `/owners/{owner_id}`       | GET    | Retrieve a single owner by ID      |

## Authentication

To access the API, use the API key provided. Include it as a header in your requests:

```http
Authorization: Bearer <API_KEY>
```

Example:
```bash
curl -H "Authorization: Bearer YOUR_API_KEY" https://api.petshop.com/pets
```

## Usage Examples

### Example 1: Get All Pets

```bash
curl -X GET https://api.petshop.com/pets
```

**Response:**
```json
[
  {
    "id": "1",
    "name": "Buddy",
    "species": "Dog",
    "age": 5,
    "adopted": false
  },
  {
    "id": "2",
    "name": "Whiskers",
    "species": "Cat",
    "age": 3,
    "adopted": true
  }
]
```

### Example 2: Update Pet Adoption Status

```bash
curl -X PATCH -H "Authorization: Bearer YOUR_API_KEY" https://api.petshop.com/pets/1/adopt
```

## Installation

To get started with PetshopRestAPI locally, follow these steps:

1. Clone the repository:

    ```bash
    git clone https://github.com/Christensenkim/PetshopRestAPI.git
    cd PetshopRestAPI
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Start the server:

    ```bash
    npm start
    ```

Visit `http://localhost:3000` to access the API.

## Contributing

We welcome contributions! Here’s how you can get started:

- Fork the repository
- Create a new branch
- Submit a pull request with your changes

---

## FAQ

**Q: What data formats are supported?**

A: JSON is the primary data format supported by PetshopRestAPI.

**Q: How do I report an issue?**

A: Open an issue on our [GitHub Issues](https://github.com/Christensenkim/PetshopRestAPI/issues) page.

---

## License

Licensed under the MIT License. See `LICENSE` for details.
