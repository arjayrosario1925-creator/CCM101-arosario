# Multi-Tier Architecture

## What is a Two-Tier Architecture?

A two-tier architecture is a system that separates the application and database into two different parts. The application is responsible for handling the user interface and requests, while the database manages and stores the information used by the application.

## Web/Application Tier

The Web/Application Tier is responsible for displaying the application to users and processing their requests. In this activity, the Nextcloud container serves as the application tier. Users can access it through a web browser to manage their private cloud files and storage.

## Database Tier

The Database Tier handles the storage and management of information required by the application. For this activity, MariaDB serves as the database for Nextcloud. It stores information such as user accounts, application settings, and data related to stored files.

## Why Separate Them?

Keeping the application and database in separate containers makes the system easier to organize and manage. Each container has a specific role, so one can be restarted, updated, or checked without directly interfering with the other. This separation also makes maintenance and troubleshooting easier.
