# Nginx Configuration for Open Banking API Gateway

This repository contains the Nginx configuration and related SSL certificates for proxying requests to the Open Banking API gateway. It includes configurations for routing traffic to various backend services such as the consent server, payment server, and identity server.

## Prerequisites

- **Nginx** must be installed on the server or local environment.
- SSL certificates (self-signed certificates are provided, but it is recommended to replace them with valid certificates for production environments).

## 1. Security Headers

The `nginx.conf` file includes several security headers to enhance security:

- `Content-Security-Policy`: Restricts the sources from which various types of content can be loaded.
- `X-Frame-Options`: Denies the embedding of the site in an iframe.
- `X-Content-Type-Options`: Prevents the browser from interpreting files as a different MIME type.
- `X-XSS-Protection`: Disables XSS filtering.
- `Access-Control-Allow-Origin`: Allows cross-origin requests from any origin.


## Best Practices for SSL Certificates

- For production environments, ensure you are using valid SSL certificates from a trusted certificate authority (CA).
- Secure your private key file with appropriate permissions to avoid unauthorized access.
