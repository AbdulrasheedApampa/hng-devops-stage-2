# Full-Stack FastAPI and React Template

Welcome to the Full-Stack FastAPI and React repository. This repository demo application showcases how to set up and run a full-stack application with a FastAPI backend and a ReactJS frontend.

## Project Structure

The repository is organized into two main directories:

- **frontend**: Contains the ReactJS application.
- **backend**: Contains the FastAPI application and PostgreSQL database integration.

Each directory has its own README file with detailed instructions specific to that part of the application.

## Getting Started

To get started with this template, please follow the instructions in the respective directories:

- [Frontend README](./frontend/README.md)
- [Backend README](./backend/README.md)

## Application Deployment

### Running on Local Machine

To run the application on your local machine, execute the following command:

```bash
docker-compose --env-file ./backend/.env up -d
```

### Running in Production

To run the application in a production environment, use the following steps:

1. Set your email and password as environment variables:

    ```bash
    export EMAIL=your_email@example.com
    export PASSWORD=your_password
    ```

2. Generate a hashed password:

    ```bash
    export HASHED_PASSWORD=$(openssl passwd -apr1 $PASSWORD)
    ```

3. Start the application using Docker Compose with the Traefik configuration:

    ```bash
    docker-compose -f docker-compose.traefik.yml up -d
    ```

4. (Optional) To start the application without Traefik:

    ```bash
    docker-compose -f docker-compose.yml --env-file ./backend/.env up -d
    ```

## Application Endpoints

- **Backend**: Available at [rasheed-apampa.com.ng/api](https://rasheed-apampa.com.ng/api)
- **Frontend**: Available at [rasheed-apampa.com.ng](https://rasheed-apampa.com.ng)
- **Adminer**: Available at [proxy.rasheed-apampa.com.ng](https://proxy.rasheed-apampa.com.ng)
- **Database**: Available at [db.rasheed-apampa.com.ng](https://db.rasheed-apampa.com.ng)
- **ReDoc**: Available at [rasheed-apampa.com.ng/redoc](https://rasheed-apampa.com.ng/redoc)

By following these instructions, you can set up and run the full-stack application seamlessly in both local and production environments.
