
# Gemini AI Webapp Deployment

This project demonstrates how to create and deploy a web application that interacts with Gemini AI on a Google Kubernetes Engine (GKE) cluster. The application is built using Flask and integrates with Google's AI platform to generate text based on user input.

## Project Overview

The application leverages the Google AI Studio and Google Cloud AI Platform to access the Gemini model for natural language processing. The web app allows users to input prompts and receive generated text responses from the Gemini AI model.

## Features

- **Flask Web Application**: Provides a simple web interface for users to interact with the Gemini AI model.
- **Google Cloud Integration**: Utilizes the Google AI Platform to authenticate and communicate with the Gemini AI model.
- **GKE Deployment**: The application is containerized and deployed on a GKE cluster, ensuring scalability and high availability.
- **CI/CD Pipeline**: Implements a continuous integration and continuous deployment pipeline to automate the build, test, and deployment process.

## Project Structure

- `app/`: Contains the Flask application code and related files.
- `Dockerfile`: Defines the Docker image used for deploying the application.
- `k8s/`: Kubernetes manifests for deploying the application on GKE.
- `ci-cd/`: Configuration files for the CI/CD pipeline.
- `README.md`: Project documentation.

## Getting Started

### Prerequisites

- Google Cloud Platform account with access to AI services.
- API key generated from Google AI Studio with appropriate permissions.
- Google Cloud SDK installed and configured.
- Docker installed for containerization.
- Kubernetes command-line tool (kubectl) installed for managing the GKE cluster.

### Setup Instructions

1. **Create an API Key:**

   - Go to the Google AI Studio and create a new API key.
   - Assign appropriate permissions to the key.

2. **Securely Store the API Key:**

   - Use environment variables or Google Secret Manager to store the API key securely.
   - Do not hardcode the API key in your code.

3. **Deploy the Application:**

   - Build the Docker image using the provided `Dockerfile`.
   - Push the Docker image to a container registry.
   - Deploy the application on GKE using the Kubernetes manifests in the `k8s/` directory.

4. **Set Up the CI/CD Pipeline:**

   - Use the configuration files in the `ci-cd/` directory to set up the pipeline.
   - Ensure the pipeline includes stages for building, testing, and deploying the application.

## Additional Considerations

- For production environments, consider using Google Secret Manager for managing sensitive information.
- Implement error handling for API key issues and other potential errors.
- Explore using service accounts for more granular permissions and security.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue if you have suggestions or improvements.


