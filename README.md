# Flower Shop Config Repository for Microservices

![GitHub repo size](https://img.shields.io/github/repo-size/PisethMao/flower-shop-config-repository-microservices)
![GitHub last commit](https://img.shields.io/github/last-commit/PisethMao/flower-shop-config-repository-microservices)
![GitHub stars](https://img.shields.io/github/stars/PisethMao/flower-shop-config-repository-microservices?style=social)
![GitHub forks](https://img.shields.io/github/forks/PisethMao/flower-shop-config-repository-microservices?style=social)
![Spring Cloud Config](https://img.shields.io/badge/Spring%20Cloud-Config%20Server-brightgreen)
![YAML](https://img.shields.io/badge/Config-YAML-blue)

Centralized configuration repository for the **Flower Shop Microservices** project using **Spring Cloud Config Server**.

This repository stores externalized configuration files for each microservice and each environment profile. It allows all services to fetch configuration from a single source instead of hardcoding properties inside every application.

---

## Overview

In a microservices architecture, configuration should not live inside each service permanently.  
This repository solves that by acting as the **central config source** for the system.

It currently manages configuration for:

- `order-service`
- `product-service`

Supported profiles:

- `dev`
- `qa`
- `prod`

---

## Architecture

This repository works together with **Spring Cloud Config Server**.

### Flow

```text
Microservice -> Config Server -> Git Config Repository
