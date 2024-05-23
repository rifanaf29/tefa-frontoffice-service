# TEFA FrontOffice Service

## Environment Variables
Name     | Desc
---------|-------------
AMQP_URL | RabbitMQ URL
PORT     | App Port

## Prerequisite
> * NodeJS 20
> * RabbitMQ

## Getting Started
> * Clone the repository
```bash
git clone https://github.com/Join-Sistem/tefa-frontoffice-service.git
```
> * Install dependencies
```bash
cd tefa-frontoffice-service
npm install
```
> * Run the project
```bash
npm start
```

## Usages

> * Post order request
```bash
curl --location 'http://localhost:3000/order' \
--header 'Content-Type: application/json' \
--data '{
    "order": {
        "name": "Bambang",
        "food": "Mie Ayam",
        "beverage": "Jeruk Es",
        "table_number": "01"
    }
}'
```

> * Expected Response
```bash
{
    "name": "Bambang",
    "food": "Mie Goreng",
    "beverage": "Jeruk Es",
    "table_number": "01"
}
```