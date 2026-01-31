<h1 align="center">Library Management System: Enterprise Web Solution</h1>

<p align="center">
  <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white" />
  <img src="https://img.shields.io/badge/.NET%20MVC-512BD4?style=for-the-badge&logo=.net&logoColor=white" />
  <img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white" />
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" />
</p>

<p align="center">
  A comprehensive, full-stack <b>ASP.NET MVC</b> application designed for scalable library management. This project features a dual-panel ecosystem (Admin & Member), real-time transaction tracking, fine calculation logic, and an advanced dashboard powered by <b>AdminLTE</b>.
</p>

<p align="center">
  <a href="#technical-architecture">
    <img src="https://img.shields.io/badge/Architecture-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#project-structure">
    <img src="https://img.shields.io/badge/Structure-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#core-features">
    <img src="https://img.shields.io/badge/Features-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#technical-specifications">
    <img src="https://img.shields.io/badge/Specs-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#deployment--installation">
    <img src="https://img.shields.io/badge/Deploy-222222?style=flat" />
  </a>
</p>

---
<br>

<h2 align="center">Technical Architecture</h2>

The system leverages the **Model-View-Controller (MVC)** architectural pattern to ensure separation of concerns and maintainability. It utilizes a robust n-tier inspired approach:

1.  **Presentation Layer:** Dynamic web interface built with **Razor View Engine**, integrated with **Bootstrap** and **AdminLTE 3.0** for a modern, responsive user experience.
2.  **Logic Layer (Controllers):** 19+ specialized controllers (e.g., `KitapController`, `OduncController`) manage complex business logic, from book inventory to lending workflows.
3.  **Data Access Layer (Model/Entity):** Uses **Entity Framework (ORM)** for seamless database operations and state management, providing an abstraction over raw SQL queries.
4.  **Security Module:** Implements custom hashing algorithms and role-based access control (RBAC) to distinguish between regular members and administrative personnel.

---
<br>

<h2 align="center">Project Structure</h2>

```
Project_LibraryManagementSystem/
├── Database/                                 # SQL Data persistence
│   └── DBKUTUPHANE.bak                       # Full SQL Server Database backup
├── Project Documantation/                    # Scientific documentation
│   └── Project Documantation.pdf             # Comprehensive technical report
│
└── Project/                                  # Source Code (ASP.NET Solution)
    ├── Controllers/                          # Business Logic (C#)
    │   ├── AdminController.cs                # Management portal logic
    │   ├── OduncController.cs                # Borrowing & Transaction logic
    │   └── KitapController.cs                # Inventory management
    ├── Models/Entity/                        # Database Context & ORM Entities
    ├── Views/                                # UI Templates (Razor .cshtml)
    ├── AdminLTE-3.0.4/                       # Dashboard UI Framework
    ├── Web.config                            # Global application configuration
    └── MvcKutuphane.sln                      # Visual Studio Solution file
```

---
<br>

<h2 align="center">Core Features</h2>

- **Inventory Ecosystem**: Complete CRUD cycle for books, authors, and genres with real-time stock status.
- **Borrowing System**: Automated tracking of lending dates, return deadlines, and status updates.
- **Analytics Dashboard**: Visual summary of library performance, including most borrowed books and active users.
- **User Roles**: Distinct portal experiences for Librarians (Full access) and Members (Search & Read-only profiling).
- **Messaging System**: Intra-system communication between management and members.

---
<br>

<h2 align="center">Technical Specifications</h2>

<table align="center">
  <tr>
    <th align="center">Component</th>
    <th align="center">Technology Stack</th>
  </tr>
  <tr>
    <td align="center"><b>Framework</b></td>
    <td align="center">ASP.NET MVC 5.x</td>
  </tr>
  <tr>
    <td align="center"><b>Language</b></td>
    <td align="center">C# 7.0+</td>
  </tr>
  <tr>
    <td align="center"><b>Frontend</b></td>
    <td align="center">HTML5, CSS3, JavaScript, jQuery, AJAX</td>
  </tr>
  <tr>
    <td align="center"><b>Styling</b></td>
    <td align="center">Bootstrap 4 / AdminLTE 3.0.4</td>
  </tr>
  <tr>
    <td align="center"><b>ORM</b></td>
    <td align="center">Entity Framework 6</td>
  </tr>
  <tr>
    <td align="center"><b>Database</b></td>
    <td align="center">Microsoft SQL Server 2019+</td>
  </tr>
</table>

---
<br>

<h2 align="center">Deployment & Installation</h2>

### 1. Environment Requirements
- **Visual Studio 2019** (or later) with the *ASP.NET and web development* workload.
- **SQL Server Management Studio (SSMS)**.
- **.NET Framework 4.7.2** (or compatible).

### 2. Repository Acquisition & Initialization
```bash
git clone https://github.com/Zer0-Bug/Project_LibraryManagementSystem.git
cd Project_LibraryManagementSystem
```

### 3. Database Restoration
1. Open **SSMS** and connect to your local server.
2. Right-click **Databases > Restore Database**.
3. Select **Device** and navigate to `Database/DBKUTUPHANE.bak`.
4. Restore the database with the name `DBKUTUPHANE`.

### 4. Application Configuration
Open `Project/Web.config` and locate the `<connectionStrings>` section. Update the `connectionString` attribute with your local SQL Server credentials:

```xml
<add name="DBKUTUPHANEEntities" connectionString="data source=YOUR_SERVER_NAME;initial catalog=DBKUTUPHANE;integrated security=True;..." />
```

### 5. Launching the System
1. Open `Project/MvcKutuphane.sln` in Visual Studio.
2. Right-click the project `MvcKutuphane` and select **Restore NuGet Packages**.
3. Press `F5` to build and launch the application in your default browser.

---
<br>

<h2 align="center">Usage Guide</h2>

- **Administrator Portal**: Accessible via `/Login/Index`. Use the admin credentials to manage the library catalog, monitor personnel, and view system-wide analytics.
- **Member Portal**: Members can log in to search the catalog, view their current borrowing status, and check for outstanding fines.
- **Public Showcase**: The main landing page (`Vitrin`) provides a public view of available library assets without requiring authentication.

---
<br>

<h2 align="center">Contribution</h2>

Contributions are always appreciated. Open-source projects grow through collaboration, and any improvement—whether a bug fix, new feature, documentation update, or suggestion—is valuable.

To contribute, please follow the steps below:

1. Fork the repository.
2. Create a new branch for your change:  
   `git checkout -b feature/your-feature-name`
3. Commit your changes with a clear and descriptive message:  
   `git commit -m "Add: brief description of the change"`
4. Push your branch to your fork:  
   `git push origin feature/your-feature-name`
5. Open a Pull Request describing the changes made.
<br>
All contributions are reviewed before being merged. Please ensure that your changes follow the existing code style and include relevant documentation or tests where applicable.

---
<br>
<h2 align="center">References</h2>

1. **Microsoft Docs** - [ASP.NET MVC Overview](https://learn.microsoft.com/en-us/aspnet/mvc/overview/getting-started/introduction/getting-started).  
2. **Entity Framework** - [EF6 Documentation](https://learn.microsoft.com/en-us/ef/ef6/).  
3. **AdminLTE 3** - [Official Documentation](https://adminlte.io/docs/3.0/).  
4. **Bootstrap** - [Bootstrap 4.x Guide](https://getbootstrap.com/docs/4.0/getting-started/introduction/).

---
<br>
<p align="center">
  <a href="mailto:777eerol.exe@gmail.com">
    <img src="https://cdn.simpleicons.org/gmail/D14836" width="40" alt="Email">
  </a>
  <span> × </span>
  <a href="https://www.linkedin.com/in/eerolexe/">
    <img src="https://upload.wikimedia.org/wikipedia/commons/c/ca/LinkedIn_logo_initials.png"
         width="40"
         alt="LinkedIn">
  </a>
</p>

---

<p align="center" style="margin-top:10px; letter-spacing:4px;">
  ∞
</p>
