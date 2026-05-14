# Build a Flask Selling Website
##For a basic Flask app, you mainly need:

Install Flask
Create app.py
Define routes
Run the server
Return HTML or JSON
## Goal
Build and deploy a simple selling website using Flask, SQLite, HTML/CSS, and image uploads.

---

# Module 1 — Website Structure
## Objective
Create a basic Flask website.

## Learning Outcomes
- Run Flask
- Use routes
- Render templates
- Serve CSS files

## Reflection
- What does a route do?
- Why use templates?

---

# Module 2 — SQLite Database
## Objective
Store items in SQLite.

## Learning Outcomes
- Create tables
- Insert/query records
- Connect Flask to SQLite

## Reflection
- Why use a database?
- What is persistence?

---

# Module 3 — Dynamic Listings
## Objective
Display database items dynamically.

## Learning Outcomes
- Query items
- Use Jinja loops
- Create detail pages

## Reflection
- What makes a page dynamic?
- How does Flask pass data to HTML?

---

# Module 4 — Image Uploads
## Objective
Upload item images.

## Learning Outcomes
- Handle uploads
- Save files securely
- Display uploaded images

## Reflection
- Why sanitize filenames?
- How do uploads work?

---

# Module 5 — Authentication
## Objective
Protect admin pages.

## Learning Outcomes
- Use sessions
- Build login/logout
- Restrict routes

## Reflection
- What is a session?
- Why protect admin pages?

---

# Module 6 — Item Management
## Objective
Edit and delete items.

## Learning Outcomes
- Update records
- Delete records
- Mark items sold

## Reflection
- What is CRUD?
- Why separate update and insert?

---

# Module 7 — Mobile Design
## Objective
Improve mobile usability.

## Learning Outcomes
- Use responsive CSS
- Build flexible layouts
- Optimize for phones

## Reflection
- Why design mobile-first?
- What improves usability?

---

# Module 8 — Deployment
## Objective
Deploy online.

## Learning Outcomes
- Deploy Flask apps
- Configure production settings
- Use free hosting

# Module 1 — Website Structure

## Goal
Create a running Flask website.

## Steps
1. Create project folder
2. Create virtual environment
3. Install Flask
4. Create `app.py`
5. Create `templates/`
6. Create `static/`
7. Run Flask server

## Structure

project/
├── app.py
├── templates/
└── static/

## Checkpoint
Homepage loads at localhost:5000

# Module 2 — SQLite Database

## Goal
Store item data permanently.

## Steps
1. Create `database.db`
2. Create `items` table
3. Insert sample data
4. Query items in Flask

## Schema

CREATE TABLE items (
    id INTEGER PRIMARY KEY,
    title TEXT,
    price TEXT
);

## Checkpoint
Items load from SQLite

# Module 3 — Dynamic Listings

## Goal
Display items dynamically.

## Steps
1. Query database
2. Pass items to template
3. Use Jinja loop
4. Create item detail route

## Example

{% for item in items %}
<h2>{{ item.title }}</h2>
{% endfor %}

## Checkpoint
New database items appear automatically

# Module 4 — Image Uploads

## Goal
Upload and display images.

## Steps
1. Create upload form
2. Create uploads folder
3. Save uploaded files
4. Store filenames in SQLite
5. Display images

## Upload Folder

uploads/

## Checkpoint
Phone uploads work correctly

# Module 5 — Authentication

## Goal
Protect admin routes.

## Steps
1. Create login page
2. Use Flask sessions
3. Add password check
4. Protect admin route
5. Add logout route

## Checkpoint
Only logged-in users access /admin

# Module 6 — Item Management

## Goal
Manage listings.

## Steps
1. Create edit form
2. Update records
3. Delete items
4. Add sold status

## Example

UPDATE items
SET sold = 1
WHERE id = ?;

## Checkpoint
Items can be edited and deleted

# Module 7 — Mobile Design

## Goal
Improve mobile usability.

## Steps
1. Use CSS Grid
2. Add responsive layout
3. Improve spacing
4. Resize images properly
5. Test on phone

## Example

.grid {
  display: grid;
}

## Checkpoint
Website works well on phones

# Module 8 — Deployment

## Goal
Deploy online.

## Steps
1. Push project to GitHub
2. Create hosting account
3. Connect repository
4. Configure startup command
5. Deploy app

## Recommended Hosts
- Render
- Railway
- PythonAnywhere

## Checkpoint
Website is publicly accessible

## Reflection
- Why not use debug mode publicly?
- What does hosting provide?
