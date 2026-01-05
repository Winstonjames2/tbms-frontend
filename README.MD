# Twin Brothers Logistics System (TBLS) - Frontend Build

## Overview
> [!IMPORTANT]
> **DEMO VERSION ONLY**
> This build is intended for demonstration purposes only. It simulates the functionality of the Twin Brothers Logistics System and should not be used for production operations without a valid license.

This directory contains the **production build** of the Twin Brothers Logistics System frontend application. This program serves as the user interface for managing logistics operations, including:
- **Truck Dispatching**: Managing and tracking truck assignments.
- **Customer Management**: Handling customer details and grouping.
- **Voucher & Consignment Management**: Processing and printing vouchers.
- **Goods Tracking**: Managing inventory and goods details.
- **Chatbot Support**: Integrated AI assistant for operations.

## Build Information
This artifact was generated using the **Quasar Framework** (Vue.js) in **Single Page Application (SPA)** mode.

### Contents
- **index.html**: The entry point of the application.
- **css/**: Compiled stylesheets.
- **js/**: Transpiled and bundled JavaScript logic.
- **fonts/**: Web fonts used in the application.
- **icons/**: App icons and assets.

## How to Deploy
Since this is a static SPA build, these files can be served by any static web server.

### Local Testing
You can serve this folder using a simple HTTP server like `http-server`:
```bash
# Install http-server
npm install -g http-server

# Serve the current directory
http-server .
```

### Production Deployment
Deploy the contents of this folder to the root of your web server (e.g., Nginx, Apache, Caddy).

**Nginx Configuration Example:**
```nginx
server {
    listen 80;
    server_name specific-domain.com;
    root /path/to/dist/spa;
    index index.html;

    # Important for SPA routing: redirect 404s to index.html
    location / {
        try_files $uri $uri/ /index.html;
    }
}
``