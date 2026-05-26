  # Wright Funeral Home Billing Statement Generator
  
  [![Live Demo](https://img.shields.io/badge/Live%20Demo-Visit%20App-4a7c59?style=for-the-badge)](https://wfh-billing-git-beta2.vercel.app/)
  ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5-6db33f?style=flat-square&logo=springboot&logoColor=white)
  ![React](https://img.shields.io/badge/React-19-61dafb?style=flat-square&logo=react&logoColor=black)
  ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-336791?style=flat-square&logo=postgresql&logoColor=white)
  ![Java](https://img.shields.io/badge/Java-21-f89820?style=flat-square&logo=openjdk&logoColor=white)
  ![Google Cloud Run](https://img.shields.io/badge/Cloud%20Run-deployed-4285f4?style=flat-square&logo=googlecloud&logoColor=white)
  ![Vercel](https://img.shields.io/badge/Vercel-deployed-000000?style=flat-square&logo=vercel&logoColor=white)
  
  A full-stack billing statement generator for funeral homes — build itemized statements, apply service packages, and export professional PDF invoices.
  
  ![App screenshot](screenshot.png)
  
  ## Live Demo
  
  **[https://wfh-billing-git-beta2.vercel.app/](https://wfh-billing-git-beta2.vercel.app/)**
  
  > Currently in beta. No account required — browse freely.
  
  ## Repositories
  
  | Repo | Description | Stack |
  |------|-------------|-------|
  | [wfh-billing-api](https://github.com/RyPalm04/wfh-billing-api) | REST API | Spring Boot 3.5, PostgreSQL, Cloud Run |
  | [wfh-billing-web](https://github.com/RyPalm04/wfh-billing-web) | Web frontend | React 19, Vite, Vercel | 
  | [wfh-billing-desktop](https://github.com/RyPalm04/wfh-billing-desktop) | Desktop app | JavaFX, jpackage |
  
  ## Architecture
  
  The web app and desktop app share a single REST API backed by a PostgreSQL database on Google Cloud Run. Statement line items are stored as JSONB snapshots — preserving name
  and price at the time of save regardless of future catalog changes. PDF generation runs server-side via JasperReports.

  The React web app and JavaFX desktop app both communicate with the Spring Boot API over HTTP. The API handles all business logic, database persistence, and PDF generation.
  
  ## Features

  - Build itemized statements across services, merchandise, special charges, and cash advances
  - Apply service packages with per-item inclusion tracking
  - Sales tax calculation with configurable rate
  - Server-side PDF export with professional layout
  - Full statement history with edit and delete
  
  ## Roadmap
  
  Multi-tenant SaaS — see [Epic #39](https://github.com/RyPalm04/wfh-billing/issues/39).
  
  ## License

  Proprietary. Source is visible for portfolio purposes. Commercial use, redistribution, or derivative works require written permission. See [LICENSE](LICENSE).
