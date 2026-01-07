## Concept-3: Cloud Deployments 101 – Docker → CI/CD → AWS/Azure

In this concept, I learned how a full-stack application can be taken from a local
development environment to the cloud using Docker, CI/CD pipelines, and cloud
platforms like AWS or Azure.

Docker helps by containerizing the application along with its dependencies,
ensuring that the application runs consistently across different environments.
By using containers, deployment issues caused by environment differences can be reduced.

CI/CD pipelines automate the process of building, testing, and deploying the
application whenever new code is pushed to the repository. This automation
reduces manual errors, improves deployment reliability, and speeds up delivery.

While deploying applications to AWS or Azure, environment variables and secrets
are handled securely using platform-specific configuration instead of hardcoding
them in the source code. This improves security and makes the application easier
to manage across development, staging, and production environments.

Overall, this concept helped me understand how automation and containerization
simplify cloud deployments and make applications more scalable and maintainable.

---

### Case Study: The Never-Ending Deployment Loop

The deployment issues in this scenario are mainly caused by improper environment
variable handling, port conflicts, and poor container lifecycle management.

Errors like “Environment variable not found” occur when required configuration
values are not correctly defined in the CI/CD pipeline or cloud environment.
Similarly, “Port already in use” errors happen when old containers are not stopped
before deploying new ones.

These issues can be resolved by properly containerizing the application using Docker,
defining all required environment variables securely in the CI/CD pipeline,
and ensuring that old containers are stopped or replaced before new deployments.

A well-configured CI/CD workflow ensures a clean handoff between each stage —
from code commit, to container build, to deployment — resulting in stable,
versioned, and secure deployments on AWS or Azure.