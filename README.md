# Movie Reservation System 🎫

A high-performance, concurrent movie reservation system built with **Go** and **Docker**. This application manages the lifecycle of movie reservations, from seat selection to payment processing, ensuring data consistency and real-time availability.



## 🚀 Features

* **RESTful API:** Clean and predictable API surface for movie, theater, and booking management.
* **Concurrency Handling:** Leverages Go routines and mutexes (or database locking) to prevent double-booking of seats.
* **Containerized Environment:** Fully dockerized setup using `docker-compose` for easy deployment.
* **PostgreSQL Integration:** Robust relational data mapping for complex theater layouts and bookings.
* **Real-time Availability:** Efficient querying to reflect seat status instantly.

---

## 🛠 Tech Stack

* **Language:** Go (Golang)
* **Database:** PostgreSQL
* **Containerization:** Docker & Docker Compose
* **Orchestration:** (Optional) Kubernetes-ready configuration

---

## 🏗 Getting Started

### Prerequisites

* [Go](https://golang.org/doc/install) (version 1.20+)
* [Docker](https://www.docker.com/get-started)
* [Docker Compose](https://docs.docker.com/compose/install/)

### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/raymondoyondi/Movie-Reservation-System.git](https://github.com/raymondoyondi/Movie-Reservation-System.git)
    cd Movie-Reservation-System
    ```

2.  **Environment Configuration:**
    Create a `.env` file in the root directory and add your database credentials:
    ```env
    DB_HOST=db
    DB_PORT=5432
    DB_USER=postgres
    DB_PASSWORD=password
    DB_NAME=ticketing_db
    ```

3.  **Run with Docker Compose:**
    ```bash
    docker-compose up --build
    ```
    The API will be available at `http://localhost:8080`.

---

## 📋 API Endpoints

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `GET` | `/movies` | Fetch all currently showing movies |
| `GET` | `/theaters/:id/seats` | Check seat availability for a specific theater |
| `POST` | `/bookings` | Create a new ticket reservation |
| `GET` | `/bookings/:id` | Retrieve booking details and status |

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

### Guidelines
* Ensure your code follows standard Go formatting (`go fmt`).
* Include unit tests for any new logic.
* Update the documentation if you change API signatures.

---

## ⚖️ License

Distributed under the **MIT License**. See `LICENSE` for more information.
