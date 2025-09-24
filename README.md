# 🍔 FoodFunPlace

A modern **Food Delivery Web App** built with **Spring Boot, Thymeleaf, and MySQL**.  
This project lets users browse menus, place orders, and learn more about the restaurant — all with a simple and responsive interface.  

---

## ✨ Features
- 🏠 Homepage with welcome message and hero section  
- 📖 About Us page with mission, values, and location info  
- 📍 Embedded Google Map (Cincinnati, OH branch)  
- 🍽️ Dynamic Menu with editable prices  
- 🎨 Custom styling and branding (renamed from *FoodFrenzy* → *FoodFunPlace*)  
- 🔒 Spring Security-ready (optional login/authentication)  
- 🗄️ MySQL database integration with Hibernate/JPA  

---

## 🖼️ Screenshots

| Home Page | Menu Page |
|-----------|-----------|
| ![Home](./assets/home.png) | ![Menu](./assets/menu.png) |

| About Us | Location |
|----------|----------|
| ![About](./assets/about.png) | ![Location](./assets/location.png) |



---

## 🛠️ Tech Stack
- **Backend:** Spring Boot (3.1.3), Java 17, Spring MVC, Spring Data JPA  
- **Frontend:** Thymeleaf, HTML, CSS, JavaScript  
- **Database:** MySQL (local)  
- **Build Tool:** Maven  
- **IDE:** VS Code / IntelliJ / Eclipse  

---

## ⚙️ Installation & Setup

### 1. Clone the repo

git clone https://github.com/Durgarao13/FoodFunPlace.git
cd FoodFunPlace

2. Configure the database

Open MySQL and create a database + user:

CREATE DATABASE food_delivery CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'bm_user'@'localhost' IDENTIFIED BY 'Bm_pass_2025!';
GRANT ALL PRIVILEGES ON food_delivery.* TO 'bm_user'@'localhost';
FLUSH PRIVILEGES;

3. Edit application.properties

Located at: src/main/resources/application.properties

spring.datasource.url=jdbc:mysql://localhost:3306/food_delivery?createDatabaseIfNotExist=true&useSSL=false&serverTimezone=UTC
spring.datasource.username=bm_user
spring.datasource.password=Bm_pass_2025!
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.database-platform=org.hibernate.dialect.MySQLDialect
spring.jpa.show-sql=true

server.port=8080

4. Build and run
mvn clean package
mvn spring-boot:run
