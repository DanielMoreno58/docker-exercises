# Use NodeJS base image
FROM nginx:1.19.3

# Copy custom index html
COPY index.html /usr/share/nginx/html/

# Do healthcheck
HEALTHCHECK --interval=45s --timeout=5s --start-period=5s --retries=2 CMD curl --fail http://localhost/index.html || exit 1