Certainly! Here's the README in English:

---

# Homelab Repository

Welcome to my homelab! This repository contains the configuration and scripts needed to set up my home environment with Traefik as a reverse proxy for my Docker containers.

## Objective

The main goal of this project is to provide a simple and flexible infrastructure to manage my self-hosted applications and services. Traefik is used as a reverse proxy to enable easy and secure access to these services, while simplifying SSL certificate management with Let's Encrypt, using OVH for the certificate challenge.

## Repository Structure

Each Docker container has its own folder at the root of the repository. Traefik-specific configurations can be found in the `traefik` folder.

- `/traefik`: Contains Traefik configuration files.
- `/service-name-1`: Folder for the first Docker service.
- `/service-name-2`: Folder for the second Docker service.
- ...

## Configuration

### Traefik

Traefik configuration is located in the `traefik` folder. You will find configuration files and rules that define the behavior of the reverse proxy. Make sure to adjust the settings according to your specific needs.

### Docker Containers

Each Docker service has its own folder at the root. Service-specific configurations, including the `docker-compose.yml` file, can be found in these respective folders.

## Certificate Challenge with OVH

This homelab uses OVH for the certificate challenge when configuring Let's Encrypt with Traefik. Ensure you have the necessary authentication information in your Traefik configuration.

## How to Use

1. Clone this repository to your homelab server:

   ```bash
   git clone https://github.com/DanielRicklin/homelab.git
   cd homelab
   ```

2. Configure Traefik by modifying the configuration files in the `traefik` folder.

3. Add new services by creating `docker-compose.yml` files in the respective service folders and linking them to Traefik using the appropriate labels.

4. Launch your services with Docker Compose:

   ```bash
   cd service-name
   docker-compose up -d
   ```

5. Access your services using the URLs defined in your Traefik configuration.

## Notes

- Ensure that the necessary ports are open on your firewall.
- Security is crucial; make sure to implement secure passwords and follow best security practices for your services.

Feel free to explore and customize this repository according to your needs. Happy homelabbing!

---

Make sure to provide the necessary OVH authentication information in your Traefik configuration files. Enjoy using your homelab!