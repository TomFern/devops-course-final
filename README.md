# Final Project

**Goal**: assess DevOps skills. This project counts towards your final note.

## Deliverables

- A Continuous Integration pipeline with the following jobs:
  - Build or download dependencies. Cache the project dependencies.
  - Linter. Use pylint to lint your Python code
  - Dependency security scanning. Ensure there are no vulnerabilities
  - Static security scanning. Ensure there are no vulnerabilities
  - Unit tests
  - Integration tests. Use Docker-based environments in your CI to run the integration tests
  - Artifact signing. Upload the signature file as a **workflow artifact**. You may create your own GPG keypair for this.
  - Generation of SBOM. Upload the SBOM as a **workflow artifact**
  - Test reports should be enabled and configured to capture test data

- An **automated** Continuous Delivery pipeline with the following jobs:
  - Build Docker image for the application
  - Upload application image to DockerHub

The order of jobs/blocks are not necessary as listed above. Set up the pipeline following best practices. Remember that fast jobs should run first.

See the **Final project** assignment in the learning platform to learn how to submit your work.

## Resources

You have the following resources at your disposal:

- Application code
- Unit and integration tests for the application
- Docker compose configuration to test locally
- Dockerfile to build the application image
- Only files in the `app` directory have to pass security tests
- Tip: Your GitHub project must be public
- Tip: You may need to add dependencies to your `requirements.txt`
- Tip: You need to define the following environment variable in your jobs: `REDIS_PORT=6379`
- Use Python 3.9 to build, run and test the application —— NOTE: docker-based image testing -> registry.semaphoreci.com/python:3.12.1
