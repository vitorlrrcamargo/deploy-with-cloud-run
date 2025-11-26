# 🌤️ Zip Code Weather API - Go + Google Cloud Run

This project is an API developed in **Go** that returns the temperature of a city based on a provided Zip Code (CEP). The application uses the [ViaCEP API](https://viacep.com.br/) to get the city and the [WeatherAPI](https://www.weatherapi.com/) to return current weather data. The deployment is done on **Google Cloud Run**.

---

## 🚀 Access the application

You can test the application directly online through the link:

👉 [https://cloudrun-goexpert-lardup467q-uc.a.run.app/weather?cep=13024091](https://cloudrun-goexpert-lardup467q-uc.a.run.app/weather?cep=13024091)

---

## 🔧 Technologies Used

- [Go](https://golang.org/)
- [Docker](https://www.docker.com/)
- [Google Cloud Run](https://cloud.google.com/run)
- [ViaCEP API](https://viacep.com.br/)
- [WeatherAPI](https://www.weatherapi.com/)

---

## 📦 How to run locally

### 1. Clone the repository

```bash
git clone https://github.com/seu-usuario/seu-repo.git
cd seu-repo
```

### 2. Run locally (without Docker)

```bash
go run main.go
```
Access at: http://localhost:8080/weather?cep=13024091

### 3. Run with Docker

Build and bring up the container:
```bash
docker-compose up --build
```
Access at: http://localhost:8080/weather?cep=13024091

## 🧪 Tests
Unit tests are located in the tests folder.

To run the tests:
```bash
go test ./...
```

## 📁 Project Structure

```bash
deploy-com-cloud-run/
├── handler/
│   └── weather.go
├── service/
│   ├── cep.go
│   └── weather.go
├── tests/
│   └── handler_test.go
├── Dockerfile
├── docker-compose.yml
├── go.mod
└── main.go
```

## 🌐 Endpoints
GET /weather?cep=XXXXXXXX
Returns the temperature of the city corresponding to the informed Zip Code (CEP).

Example:
GET /weather?cep=13024091
Response:
json
Copy
Edit
{
  "temp_C": 24.5,
  "temp_F": 76.1,
  "temp_K": 297.5
}

## ⚠️ Notes
The project makes external calls to public APIs, therefore it is subject to the availability and limits of these APIs.

The WeatherAPI key is hardcoded in the code for testing and learning purposes only. In production, it is ideal to use environment variables or secret managers.

## 👨‍💻 Author
Vitor Camargo

## ☁️ Deploy on Google Cloud Run
The deployment is done on the Google Cloud Run platform, ensuring automatic scalability and high availability.

URL: https://cloudrun-goexpert-lardup467q-uc.a.run.app/weather?cep=13024091
