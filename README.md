# 🗓️ Google Calendar Clone  

A **high-fidelity full-stack clone** of Google Calendar that allows users to create, edit, and manage events with Month, Week, and Day views.  
This project replicates Google Calendar’s key functionalities and responsive UI using **Next.js**, **React**, and **Drizzle ORM** on a **PostgreSQL (Neon/Supabase)** backend.

---

## 🚀 Features

- **Add, Edit, Delete Events (Full CRUD)**  
  Create, update, and remove events with instant UI updates.

- **Multiple Views**  
  Switch between **Month**, **Week**, and **Day** views to plan effectively.

- **Responsive Design**  
  Optimized for mobile, tablet, and desktop devices.

- **Smooth Animations**  
  Transitions and modals powered by **Framer Motion** for realistic Google Calendar-like UX.

- **Database Persistence**  
  Events are stored in a **serverless PostgreSQL database (Neon/Supabase)** using **Drizzle ORM**.

---

## 🎯 Objective

To design a **realistic calendar system** with modern web technologies that:
1. Provides a visually and functionally accurate experience similar to Google Calendar.  
2. Implements **full CRUD** operations connected to a live database.  
3. Demonstrates clean architecture, modular design, and maintainable code.  

---

## 🧱 Architecture Overview

### **Frontend (Next.js + React)**
- **Next.js 14** used for hybrid rendering (Server + Client).  
- **Shadcn UI** + **TailwindCSS** for fast and consistent design.  
- **Zustand store** manages month navigation and state between components.  
- **Framer Motion** adds animations and transitions.  

### **Backend (Next.js Server Actions + Drizzle ORM)**
- Server Actions handle CRUD logic (`createEventAction`, `updateEventAction`, `deleteEventAction`).  
- **Drizzle ORM** communicates directly with PostgreSQL database.  
- **Database hosted on Neon / Supabase** (serverless Postgres).  

**Data Flow**
Client Form ➜ Next.js Server Action ➜ Drizzle ORM ➜ PostgreSQL
⤷ revalidatePath("/") ➜ UI Refresh

🛠️ **Tech Stack**

| Category    | Technology      | Description                                                                 |
|-------------|-----------------|-----------------------------------------------------------------------------|
| Frontend    | Reactjs         | JavaScript library for building user interfaces.                           |
| Framework   | Nextjs          | React framework for server-rendered and statically generated applications. |
| UI Library  | Shadcn UI       | Collection of reusable components for React.                               |
| Styling     | Tailwindcss     | Utility-first CSS framework for rapid UI development.                       |
| Database    | Neon/Postgresql DB | Serverless Postgres database.                                               |
| ORM         | Drizzle ORM     | TypeScript ORM for interacting with the database.                           |
| Date Handling | Day.js          | Minimalist JavaScript library for parsing, validating, and formatting dates.|

📦 **Getting Started**

### Prerequisites

*   Node.js (v18 or higher)
*   npm or yarn
*   Neon account and Postgres database setup

### Installation

1.  Clone the repository:

    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2.  Install dependencies:

    ```bash
    npm install # or yarn install
    ```

3.  Set up environment variables:

    Create a `.env.local` file in the root directory and add your Neon/Postgresql database connection string:

    ```
    DATABASE_URL="your_neon_postgresql_connection_string"
    ```

### Running Locally

1.  Start the development server:

    ```bash
    npm run dev # or yarn dev
    ```

2.  Open your browser and navigate to `http://localhost:3000`.

📂 **Project Structure**

```
google-calendar-clone/
├── .next/                # Next.js build output
├── app/                   # Contains the application's routes and components
│   ├── api/             # API routes
│   ├── components/      # Reusable React components
│   ├── lib/             # Utility functions and database connection logic
│   ├── page.tsx         # Home page
│   └── layout.tsx       # Root layout
├── public/                # Static assets (images, fonts, etc.)
│   └── gcclone.png      # Screenshot of the application
├── styles/                # Global styles and Tailwind CSS configuration
│   └── globals.css
├── .env.local             # Environment variables (database connection string)
├── next.config.js         # Next.js configuration file
├── package.json           # Project dependencies and scripts
├── README.md              # Project documentation
└── tsconfig.json          # TypeScript configuration
```
