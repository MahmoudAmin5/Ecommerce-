
##  Talabaty Ecommerce Project

A full-stack Ecommerce web application built with **.NET Core Web API** for the backend, **Angular** for the frontend, and containerized with **Docker**.

---

##  Table of Contents

* [About the Project](#about-the-project)
* [Tech Stack](#tech-stack)
* [Prerequisites](#prerequisites)
* [Project Structure](#project-structure)
* [Setup Instructions](#setup-instructions)

  * [Backend (.NET)](#backend-net)
  * [Frontend (Angular)](#frontend-angular)
  * [Docker Compose](#docker-compose)
* [Usage](#usage)
* [Screenshots](#screenshots)
* [Author](#author)

---

##  About the Project

**Talabaty** is a simple ecommerce system allowing users to browse products, add them to a cart, and place orders.
It demonstrates the integration between a .NET Core Web API backend and an Angular frontend — both containerized using Docker for easy deployment.

---

##  Tech Stack

* .NET 8 Web API
* Angular 17
* Docker & Docker Compose
* SQL Server (if applicable)

---

##  Prerequisites

Before you begin, ensure you have the following installed:

* [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
* [Node.js & npm](https://nodejs.org/)
* [Angular CLI](https://angular.io/cli)
* [Docker](https://www.docker.com/products/docker-desktop)

---

##  Project Structure

```
Ecommerce-/
│
├── Backend/
│   ├── TalabatyAPI/
│   └── Dockerfile
│
├── Frontend/
│   ├── talabaty-client/
│   └── Dockerfile
│
├── docker-compose.yml
└── README.md
```

---

##  Setup Instructions

###  Backend (.NET)

```bash
cd Backend/TalabatyAPI
dotnet restore
dotnet build
dotnet run
```

API will run on `http://localhost:5000` by default.

---

###  Frontend (Angular)

```bash
cd Frontend/talabaty-client
npm install
ng serve --open
```

App will run on `http://localhost:4200`

---

###  Docker Compose

To run both frontend and backend services via Docker:

```bash
docker-compose up --build
```

To stop services:

```bash
docker-compose down
```

---

##  Usage

* Access the **API** at `http://localhost:5000/api`
* Access the **Frontend UI** at `http://localhost:4200`

Test adding products, placing orders, and browsing the store!

---


##  Author


[**Mahmoud Amin**](https://github.com/MahmoudAmin5)
[**Karem Atef**](https://github.com/Karem3tef)
[**Ezzat Walid**](https://github.com/EZZATW12)
[**Muhamed Muhsen**](https://github.com/muhamedmuhsen)
---

##  Notes

* Ensure your Docker Desktop is running before using `docker-compose`.
* You can customize ports inside `docker-compose.yml` if needed.


