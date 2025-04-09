# API Collection Module

This module contains OpenAPI 3.0 YAML specifications for Sham Beauty Lounge Platform.

## How to Generate Java Code

Development (Internal APIs):

```bash
mvn clean install -Pdev
```

Production (External APIs):

```bash
mvn clean install -Pprod
```

Generated code will appear in `target/generated-sources/openapi/`.
