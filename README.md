NeighborFund

A full-stack community crowdfunding platform built with PHP and MySQL, designed to let neighborhoods and communities propose, fund, and track local improvement projects with transparency and accountability at every stage.

Overview

NeighborFund allows community members to submit local projects (e.g. park renovations, community centers, local initiatives), collect donations toward a funding goal, and track fund usage through milestone-based releases — all backed by voting, verification, and audit mechanisms to keep the process transparent and trustworthy.

Features


User authentication & roles: Users, admins, auditors, and project leads, each with different permissions.
Project lifecycle management: Projects move through draft → pending → approved → live → funded/failed → completed states.
Milestone-based funding: Funds are released in stages as milestones are completed, rather than all at once.
Community voting: Backers can vote on milestones before funds are released, adding a layer of community oversight.
Donations & rewards: Users can donate to projects and receive tiered rewards based on their contribution.
Karma / reputation system: Tracks user reputation based on donations, volunteering, and community participation.
KYC verification: Identity verification workflow for project leads/organizations to build trust.
Organization support: Organizations can register, get verified, and manage multiple projects.
Disputes & moderation: Users can report/dispute comments or milestones; admins can resolve or dismiss disputes.
Volunteer tracking: Records volunteer hours contributed to projects.
Audit log: Every sensitive action is logged for transparency and accountability.
Notifications: In-app notifications for project and account activity.
Reporting & analytics: Fiscal reports and community analytics for oversight.


Tech Stack


Backend: PHP (OOP, class-based architecture)
Database: MySQL (PDO for database access)
Frontend: HTML, CSS, JavaScript
Architecture: MVC-inspired structure — classes/ (models & business logic), pages/ (controllers/views), includes/ (shared layout components), config/ (database configuration), sql/ (schema)


Project Structure

neighborfund/
├── classes/          # Core domain classes (User, Project, Donation, Milestone,
│                      # Vote, Karma, Dispute, Audit, Organization, Volunteer, etc.)
├── pages/             # Page controllers (dashboard, projects, donate, admin, etc.)
├── includes/          # Shared header, footer, navbar, auth checks
├── config/            # Database configuration
├── cron/              # Scheduled tasks (e.g. checking project deadlines/status)
├── sql/               # Database schema (schema.sql)
├── assets/            # CSS, JS, uploaded files
└── uploads/           # User-uploaded evidence/documents

Database

The schema (sql/schema.sql) includes tables for: users, organizations, projects, milestones, budget_items, donations, rewards, user_rewards, comments, disputes, votes, notifications, project_updates, volunteers, audit_log, reports, project_revisions, site_verifications, kyc_documents, settings, and rate_limits.

How to Run


Install PHP (7.4+) and MySQL, or use a local stack such as XAMPP/WAMP/MAMP.
Create the database by importing the schema:


bash   mysql -u root -p < sql/schema.sql


Update database credentials in config/database.php if needed (defaults to localhost, database neighborfund, user root).
Place the project folder inside your server's document root (e.g. htdocs/neighborfund for XAMPP).
Visit http://localhost/neighborfund/pages/index.php in your browser.


Future Improvements


Add automated email notifications for milestone votes and project updates.
Integrate a real payment gateway for donations.
Add unit tests for core classes (Project, Donation, Milestone, Vote).


Author

Yassin Mohamed — GitHub | LinkedIn
