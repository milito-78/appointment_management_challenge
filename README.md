# 🎯 Laravel Mid-Level Developer Task

## 📝 Project Title: Appointment Management System

### 👤 Roles:

* **Admin**: Can view reports, manage users and appointments
* **Consultant**: Can define available time slots, view appointments
* **User**: Can view consultants and book available time slots

---

## 📌 Features to Implement:

### ✅ Availability Management (Consultant Only)

* A consultant can define weekly available time slots (e.g., Mondays 9:00-12:00)
* These slots are saved in DB (`availabilities` table)

### ✅ Appointment Booking (User)

* Users can select consultants and book appointments only in available slots
* Prevent overlapping bookings for the same consultant
* Cancellation allowed up to 24 hours before start time

### ✅ Role-Based Access Control (All roles)

* Use Laravel Policies or middleware
* Only users can book; only consultants see their appointments
* Admin can see all

### ✅ Admin Reports

* View monthly appointment counts per consultant
* Optionally export to Excel (not required)

---

## 📁 Suggested Tables:

* `users`: `name`, `email`, `role`, `password`
* `availabilities`: `consultant_id`, `day_of_week`, `start_time`, `end_time`
* `appointments`: `user_id`, `consultant_id`, `start_time`, `end_time`, `status`

---

## ⚙️ Technical Requirements:

* Laravel 10+
* Blade templating (no SPA or Vue)
* Laravel Auth (Breeze or UI package is okay)
* Use Eloquent relationships
* Use Form Request validation
* Use Policies or Middleware for access control
* Clean Blade views and layout (can be basic)

---

## 🧪 Deliverables:

* Complete Laravel project (GitHub or zip)
* DB setup using migrations and seeders
* At least:

  * 1 admin
  * 2 consultants
  * 2 regular users
* Sample login credentials in README
* `README.md` explaining setup:

  * how to run the project
  * example login info
  * structure explanation (optional)

---

## ⏱️ Estimated Time to Complete:

** 7 Days

---

## 🔍 Bonus Points:

* Export reports (Excel, CSV)
* Reusable blade components
* Blade layout with sections
* Flash messages

---

Good luck! This task evaluates your:

* Laravel architecture understanding
* Problem solving
* Eloquent and Blade skillset
* Code readability and organization
