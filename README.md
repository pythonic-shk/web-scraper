# web-scraper

A flexible, extendable Python web scraping framework for distributed and single-node use in Kubernetes.

## Features
- **Distributed scraping** (for high throughput), deployable via Kubernetes (`distributed/`)
- **Single-node scraping** as a Kubernetes job or service (`single-node/`)
- **Core abstract scraping engine** (Python, SOLID-principled, dynamic/static HTML, extendable; `core/`)
- **Flexible output storage**: object storage (S3/MinIO), DB, or Streams (Kafka, etc.; `storage/`)
- **UI interface** to monitor metrics of your scraping jobs (`ui/`)

## Repository structure
```
web-scraper/
├── core/           # Python abstractions, base classes, jobs, and orchestration
├── distributed/    # Deployment for distributed scraping on Kubernetes
├── single-node/    # Job/service for single node in Kubernetes
├── storage/        # Backends for storing scraped data
├── ui/             # Metrics monitoring and dashboard
└── README.md       # Project overview
```

## Goal
- Support for scraping static (requests/httpx/BeautifulSoup) and dynamic (Selenium/playwright) HTML.
- Metrics collector and flexible output targets.
- Abstract, extendable, follows SOLID principle for easy maintenance/extension.
- All major code in `core/`.

---
After this, folder and initial code scaffolding for each section will follow.