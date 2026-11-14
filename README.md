# Wildlife Sighting Map 🐾

A community-driven wildlife observation platform where users can upload animal and bird sightings, discover nearby wildlife, and contribute to species identification.

## Key Features

- **Interactive Map:** Explore wildlife sightings with location-based markers, clustering, and filters.
- **Sighting Uploads:** Upload photos with automatic GPS and timestamp extraction using EXIF data.
- **AI Species Identification:** ML service suggests the top 3 possible species for each uploaded photo.
- **Community Verification:** Users can confirm or suggest alternative species identifications.
- **User Profiles:** Maintain personal species life lists, earn badges, and compete on leaderboards.
- **Location Privacy:** Sensitive species sightings display approximate locations to protect wildlife.

## Tech Stack

- **Frontend:** React, TypeScript, Tailwind CSS, Leaflet
- **Backend:** Node.js, Express.js, TypeScript
- **Database:** PostgreSQL, PostGIS
- **Background Jobs:** Redis, BullMQ
- **ML Service:** Python, FastAPI (BioCLIP planned)
- **Storage:** Cloudinary / S3
- **Authentication:** JWT, bcrypt

## Architecture

A full-stack application with a separate Python-based ML microservice. Image uploads are handled directly through cloud storage, while BullMQ processes species identification asynchronously without blocking the main API.

## Project Goal

Build a scalable, location-aware wildlife community that combines geospatial technologies, asynchronous processing, and machine learning to make wildlife discovery and documentation accessible.

## Project Structure

- `client/` — React frontend built with TypeScript.
- `api/` — Node.js and Express backend.
- `ml/` — Python-based machine learning service.