  # Wright Funeral Home Billing System
  
  A full-stack billing statement generator built for Wright Funeral Home. The system allows staff to create, manage, and export itemized billing statements as print-ready PDFs.

  ## Repositories

  | Repo | Description |                                                                                                                                  
  |------|-------------|
  | [wfh-billing-api](https://github.com/RyPalm04/wfh-billing-api) | Spring Boot REST API — statement persistence, catalog management, PDF generation |
  | [wfh-billing-web](https://github.com/RyPalm04/wfh-billing-web) | React web app — create, edit, and manage statements from any browser |
  | [wfh-billing-desktop](https://github.com/RyPalm04/wfh-billing-desktop) | JavaFX desktop app — standalone client for local use |

  ## Architecture

  ┌─────────────────┐     ┌─────────────────┐
  │  React Web App  │     │ JavaFX Desktop  │
  │   (Vercel)      │     │     App         │
  └────────┬────────┘     └────────┬────────┘
           │                       │
           └──────────┬────────────┘
                      │ HTTPS + API Key
           ┌──────────▼────────────┐
           │   Spring Boot API     │
           │  (Google Cloud Run)   │
           └──────────┬────────────┘
                      │
           ┌──────────▼────────────┐
           │     PostgreSQL        │
           │  (Cloud SQL)          │
           └───────────────────────┘

  ## Tech Stack

  **API**
  - Java 21, Spring Boot 3.5
  - Spring Data JDBC, Flyway migrations
  - JasperReports PDF generation
  - PostgreSQL (Cloud SQL)
  - Deployed on Google Cloud Run

  **Web**
  - React 19, Vite
  - React Router, react-hot-toast
  - Deployed on Vercel                                                                                                                                    

  **Desktop**
  - Java 21, JavaFX
  - Packaged with jpackage (macOS, Windows, Linux)
  
  ## Status

  Currently in beta. The web app is live at [wfh-billing-git-beta2.vercel.app](https://wfh-billing-git-beta2.vercel.app).
  
  ## Roadmap

  The long-term direction is a multi-tenant SaaS platform marketable to multiple funeral homes — with per-tenant catalogs, user authentication, admin portal, and custom branding
   on statements. See the [open issues](https://github.com/RyPalm04/wfh-billing/issues) for tracked work.
