# Vulnerable Web Applications Lab - Docker Compose

This repository provides a ready-to-use Docker Compose configuration for running multiple intentionally vulnerable web applications and penetration testing targets. It is ideal for learning, practicing ethical hacking, and cybersecurity training in a safe, isolated environment.

## Included Services

| Service           | Port(s)         | Description                                                                 |
|-------------------|-----------------|-----------------------------------------------------------------------------|
| **DVWA**          | 8001            | [Damn Vulnerable Web Application](http://www.dvwa.co.uk/) - PHP/MySQL app for security training. |
| **bWAPP**         | 8002            | [bWAPP](http://www.itsecgames.com/) - Buggy Web Application for web security testing. |
| **Juice Shop**    | 3000            | [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/) - Modern insecure web app. |
| **Metasploitable2** | 21, 22, 23, 80, 445, 3306, 5432 | Linux VM with multiple vulnerable services for exploitation practice. |

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Usage

1. **Clone the Repository**

   ```sh
   https://github.com/hidayat-tanjung/Vulnerable-Lab.git
   cd Vulnerable-Lab
   ```

2. **Start All Services**

   ```sh
   docker-compose up -d
   ```

3. **Access the Applications**

   - **DVWA:** [http://localhost:8001](http://localhost:8001)
   - **bWAPP:** [http://localhost:8002](http://localhost:8002)
   - **Juice Shop:** [http://localhost:3000](http://localhost:3000)
   - **Metasploitable2:**  
     - FTP: `localhost:21`  
     - SSH: `localhost:22`  
     - Telnet: `localhost:23`  
     - HTTP: [http://localhost:80](http://localhost:80)  
     - SMB: `localhost:445`  
     - MySQL: `localhost:3306`  
     - PostgreSQL: `localhost:5432`

4. **Stop All Services**

   ```sh
   docker-compose down
   ```

## Notes

- All services are connected to an internal Docker bridge network for isolation.
- **Metasploitable2** exposes several ports for multi-vector exploitation.
- Default credentials may be required; refer to each project’s documentation for login details.

## Security Warning

**Do not expose these containers to the public internet.**  
They are intentionally vulnerable and should only be used in a controlled, private lab environment.

## References

- [DVWA Documentation](https://github.com/digininja/DVWA)
- [bWAPP Documentation](https://github.com/raesene/bwapp)
- [OWASP Juice Shop](https://github.com/bkimminich/juice-shop)
- [Metasploitable2 Info](https://github.com/rapid7/metasploitable3)

---

**Happy Hacking! Practice responsibly.**
