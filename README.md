# 🏛️ NPC Verification Desk

## 📌 Project Overview

**NPC Verification Desk** is a modern React web application built with Vite and managed via `pnpm`. Designed specifically for identity verification, demographic record lookups, certificate validation, and queue management, the system provides a streamlined interface for administrative personnel and verification officers.

The application follows a clean, modular architecture separating UI components, routed pages, authentication context, API services, and custom hooks.

---

## 📁 Directory Structure

```
.
├── .env                    # Local environment configuration
├── .env.example            # Environment template file
├── .gitignore              # Ignored files for version control
├── index.html              # Entry HTML template
├── package.json            # Scripts and dependency specifications
├── pnpm-lock.yaml          # PNPM locked dependencies
├── pnpm-workspace.yaml     # PNPM workspace configurations
├── vite.config.js          # Vite bundler & dev server configuration
├── README.md               # Project documentation
└── src/                    # Primary source code
    ├── main.jsx            # Application root mount point
    ├── App.jsx             # Top-level application layout & routing
    ├── auth.jsx            # Authentication state & provider context
    ├── format.js           # Data formatting & conversion utilities
    ├── hooks.js            # Shared custom React hooks
    ├── styles.css          # Global styling & layout definitions
    ├── api/                # Network service definitions
    │   └── client.js       # Base HTTP client configuration (Axios/Fetch)
    ├── components/         # Shared UI elements
    │   ├── Layout.jsx      # Navigation header, sidebar & frame wrapper
    │   ├── MapView.jsx     # Geolocation & map integration view
    │   └── ui.jsx          # Reusable design system primitives (Buttons, Inputs, Modals)
    └── pages/              # Primary view components
        ├── Admin.jsx       # Administrative settings & user role control
        ├── Certificates.jsx# Birth/Death/Attestation certificate management
        ├── Dashboard.jsx   # Core analytics & system health summary
        ├── Login.jsx       # Portal authentication & session initialization
        ├── Lookup.jsx      # Quick record search & verification lookup
        ├── Misc.jsx        # Auxiliary tools & secondary settings
        ├── Queue.jsx       # Verification queue & request processing stack
        ├── Records.jsx     # Master database record viewer & editor
        ├── Review.jsx      # Multi-stage review & approval workflows
        └── Verify.jsx      # Direct document & certificate verification panel
```

---

## 🛠️ Module & Feature Breakdown

### 🔐 System Core (`src/`)

* **`main.jsx`**: Initializes the React application tree.
* **`App.jsx`**: Manages top-level application routing, layout binding, and global state providers.
* **`auth.jsx`**: Manages authorization tokens, user roles, login state, and protected route access.
* **`api/client.js`**: Standardized HTTP client for executing backend API queries.

### 📄 Core Pages (`src/pages/`)

| Page Module | Role & Capability |
| :--- | :--- |
| **`Login.jsx`** | Secure user login, session management, and credential processing. |
| **`Dashboard.jsx`** | High-level metrics, verification statistics, and active queue counts. |
| **`Lookup.jsx`** | Rapid identity and registration search engine. |
| **`Verify.jsx`** | Primary verification interface for validating certificates and citizen records. |
| **`Review.jsx`** | Escalated review workflows for pending or flagged verification requests. |
| **`Certificates.jsx`** | Certificate generation, view, and print/download portal. |
| **`Queue.jsx`** | Task queue tracking incoming requests and assignment states. |
| **`Records.jsx`** | Detailed view and entry management for population data. |
| **`Admin.jsx`** | High-privilege admin panel for user roles and system flags. |
| **`Misc.jsx`** | Auxiliary system settings and fallback interface. |

---

## 🚀 Getting Started

### Prerequisites

* **Node.js**: `v18.0.0` or higher
* **pnpm**: `npm install -g pnpm`

### Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd npc-verification-desk
   ```

2. **Install project dependencies:**
   ```bash
   pnpm install
   ```

3. **Configure Environment Variables:**
   ```bash
   cp .env.example .env
   ```
   *Update parameters in `.env` (such as `VITE_API_BASE_URL`) according to your development target.*

4. **Run the local development server:**
   ```bash
   pnpm dev
   ```

5. **Build for production:**
   ```bash
   pnpm build
   ```

6. **Preview local production build:**
   ```bash
   pnpm preview
   ```