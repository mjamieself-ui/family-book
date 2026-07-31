# Family Social Network Development Plan

## Project Overview
A private, ultra-local social network for the family, inspired by early-2000s Facebook (pre-ads and algorithms). Designed to be secure, nostalgic, lightweight, and expandable.

---

## Key Requirements & Specifications

### Hosting & Infrastructure
* **Deployment:** Free cloud tier (e.g., Render or Railway) scaling to a paid VPS/persistent storage tier as the family expands.
* **Security:** HTTPS enabled via cloud host; gated by a **single shared family password** stored securely in environment variables.

### Core Features (Version 1)
1. **The News Feed & Status Updates:** A central timeline for text posts and photo shares.
2. **Profile Walls:** Individual landing pages for each family member where others can post direct messages.
3. **Comments & Reactions:** Interaction layers on every post and wall message.
4. **The Birthday & Events Calendar:** A dedicated board tracking upcoming family milestones and gatherings.
5. **The Family Directory:** A nostalgic "MemberList" page listing everyone with their bios and contact info.

### Future Extensibility
* Designed with modular hooks for background worker processes (e.g., automated weekly email digests, media compression workers, or event reminders).

---

## Tech Stack
* **Backend / Server:** Node.js with Express
* **Template Engine:** EJS (Embedded JavaScript) for clean, fast server-side rendering
* **Database:** SQLite (local dev) / PostgreSQL (production cloud migration)
* **Styling:** Custom CSS / Tailwind CSS for an early-2000s clean blue-and-white aesthetic

---

## Step-by-Step Implementation Guide

### Step 1: Project Initialization & Structure
Initialize the Node.js project and install required dependencies:
```bash
mkdir family-book
cd family-book
npm init -y
npm install express sqlite3 bcrypt express-session multer ejs


