# AWS Highly Available Three-Tier Web Application

A highly available three-tier web application architecture implemented
using AWS services.

---

## 📌 Project Overview

This project demonstrates the design and implementation of a
**Highly Available Three-Tier Web Application on AWS**.

The architecture is divided into three main tiers:

- Web Tier
- Application Tier
- Database Tier

The project uses AWS networking, load balancing, auto scaling, EC2,
and Amazon RDS to build a highly available application environment.

---

## 🏗️ Architecture

![Three-Tier AWS Architecture](architecture/three-tier-architecture.png)

### Architecture Flow

```text
                         USERS
                           |
                           v
                  Internet Gateway
                           |
                           v
              Application Load Balancer
                           |
                 +---------+---------+
                 |                   |
                 v                   v
            Web Server 1        Web Server 2
             (EC2)               (EC2)
                 |                   |
                 +---------+---------+
                           |
                           v
                 Application Tier
                 Private EC2 Servers
                 |             |
                 +------+------+
                        |
                        v
                  Amazon RDS
                   Multi-AZ
                 MySQL Database
