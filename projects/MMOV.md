images/screencapture-mmov-replit-app-2025-09-17-19_24_25.png

# MMOV – Men's Group Management App

## 📖 Overview
MMOV is a private members-only application designed for men's groups. The app provides a secure platform where members can create accounts, complete required profiles, and access shared calendars and directories. A three-tier role-based system (Member, Admin, Super Admin) ensures that permissions and features are properly controlled.

---

## 🏗 System Architecture

### Frontend
- **Framework:** React with TypeScript + Vite
- **Routing:** Wouter (role-based navigation)
- **UI:** Shadcn/UI + Tailwind CSS
- **State Management:** TanStack React Query
- **Forms:** React Hook Form + Zod
- **File Uploads:** Custom ObjectUploader → Google Cloud Storage

### Backend
- **Runtime:** Node.js + Express.js (TypeScript, ES modules)
- **Database:** PostgreSQL via Drizzle ORM
- **Sessions:** Express sessions stored in PostgreSQL
- **Storage:** Google Cloud Storage for profile images and files
- **API:** RESTful endpoints with authentication middleware

### Authentication & Authorization
- **Identity Provider:** Replit OIDC
- **Sessions:** PostgreSQL-backed secure cookies
- **Roles:** Member, Admin, Super Admin
- **Profile Gating:** Users must complete profiles before gaining full access

---

## 🗄 Database Schema
- **Users Table:** profile info, roles, completion status
- **Events Table:** group events, creator, location
- **Sessions Table:** session persistence
- **Roles:** enum constraint for role enforcement

---

## ✅ Validation & Tooling
- **Validation:** Zod schemas shared across frontend & backend
- **Build Tool:** Vite with hot module replacement
- **Migrations:** Drizzle Kit
- **Type Safety:** Full strict TypeScript mode

---

## 🔧 External Dependencies
- **Database:** Neon PostgreSQL (serverless)
- **Storage:** Google Cloud Storage
- **Authentication:** Replit OIDC
- **UI Components:** Radix + shadcn/ui
- **Date Handling:** date-fns
- **Validation:** Zod

---

## 🚀 Development Tools
- **Build:** Vite + TypeScript
- **Database Tools:** Drizzle ORM + Drizzle Kit
- **Session Store:** connect-pg-simple
- **Plugins:** Replit-specific Vite plugins

---

[🔙 Back to Portfolio](../README.md)
