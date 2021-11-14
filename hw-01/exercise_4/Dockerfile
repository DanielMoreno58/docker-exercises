# Use NodeJS base image
FROM nginx:1.19.3

# Do healthcheck
HEALTHCHECK --interval=45s --timeout=5s --start-period=60s --retries=2 CMD curl --fail http://localhost:8080/index.html