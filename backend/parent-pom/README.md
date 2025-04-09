# Parent POM for SBL Platform

This project acts as the parent Maven module to manage all submodules and centralize dependencies.

## Modules

- api-collection
- backend/kunden-service
- backend/kalender-service
- backend/zahlung-service

## How to Build

First, install the parent-pom:

```bash
cd parent-pom
mvn clean install
```

Then, go back to your root project and build everything:

```bash
cd ..
mvn clean install -Pdev
```

This ensures that the api-collection and backend services can correctly inherit dependency versions.
