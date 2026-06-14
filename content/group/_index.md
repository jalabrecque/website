---
title: Group
date: 2024-01-01
type: page
---

<!--
============================================================
  HOW TO ADD A STUDENT
  1. Copy one "student-row" block below (from <div class="student-row">
     to its closing </div>) and paste it where you want it.
  2. Fill in the name, degree, thesis, and bio.
  3. For a photo: put the image in  static/img/students/  and point
     src to it, e.g.  src="/img/students/firstname_lastname.jpg".
     If there is no photo yet, just leave the src as-is or remove it —
     it will automatically show a neutral grey placeholder.
  4. The <a href="..."> around the name is optional (link to LinkedIn,
     a personal site, etc.). Delete it if you don't want a link.
  Ordering on the page = order of the blocks here.
============================================================
-->

<style>
.students-list { display: flex; flex-direction: column; margin-top: 1.5rem; }

.student-row {
  display: flex;
  align-items: flex-start;
  gap: 1.75rem;
  padding: 1.75rem 0;
  border-bottom: 1px solid;
  border-color: currentColor;
  border-bottom-color: rgba(128,128,128,.25);
}
.student-row:last-child { border-bottom: none; }

.student-photo,
.student-photo.student-photo--missing {
  flex: 0 0 100px;
  width: 100px;
  height: 100px;
  object-fit: cover;
  border-radius: 14px;
  background: rgba(128,128,128,.2);
  display: block;
}
/* When an image fails to load / has no src, hide the broken icon
   and show the grey box instead. */
.student-photo--missing { object-fit: none; }
.student-photo--missing::after { content: ""; }

.student-body { flex: 1; min-width: 0; }

.student-name {
  font-size: 1.05rem;
  font-weight: 600;
  margin: 0 0 0.15rem;
}
.student-name a { color: inherit; text-decoration: none; }
.student-name a:hover { text-decoration: underline; }

.student-degree {
  font-size: 0.85rem;
  opacity: .6;
  margin: 0 0 0.4rem;
}

.student-thesis {
  font-size: 0.92rem;
  font-style: italic;
  opacity: .75;
  margin: 0 0 0.45rem;
  line-height: 1.45;
}

.student-bio {
  font-size: 0.95rem;
  margin: 0;
  line-height: 1.65;
}

@media (max-width: 480px) {
  .student-row { flex-direction: column; gap: 1rem; }
}
</style>

I currently supervise the following students. Feel free to
[get in touch](mailto:j.labrecque@erasmusmc.nl) if you are interested in
joining the group.

<div class="students-list">

  <!-- ===== STUDENT (copy this whole block to add another) ===== -->
  <div class="student-row">
    <img class="student-photo" src="/img/group/keling.jpg" alt="Student name"
         onerror="this.classList.add('student-photo--missing'); this.removeAttribute('src');">
    <div class="student-body">
      <p class="student-name">
        <a href="https://example.com" target="_blank" rel="noopener">Keling Wang</a>
      </p>
      <p class="student-degree">PhD candidate</p>
      <p class="student-thesis">Causal triangulation and epidemiologic methods</p>
      <p class="student-bio">Keling is interested in novel causal thinking methods needed “before and after causal estimation”, namely asking good causal questions, and alternatives in the violation of causal assumptions. Keling's research primarily focuses on the formalization and application of [causal triangulation](https://link.springer.com/article/10.1007/s40471-023-00340-0) methods, with interdisciplinary applied interests in social epidemiology and transgender/queer health. </p>
    </div>
  </div>

  <!-- ===== STUDENT ===== -->
  <div class="student-row">
    <img class="student-photo" src="/img/students/student_two.jpg" alt="Student name"
         onerror="this.classList.add('student-photo--missing'); this.removeAttribute('src');">
    <div class="student-body">
      <p class="student-name">Student Name</p>
      <p class="student-degree">MSc student</p>
      <p class="student-thesis">Working thesis title goes here</p>
      <p class="student-bio">A short write-up describing the student's project
        and interests.</p>
    </div>
  </div>

  <!-- ===== STUDENT (example with no photo — shows grey placeholder) ===== -->
  <div class="student-row">
    <img class="student-photo" alt="Student name"
         onerror="this.classList.add('student-photo--missing'); this.removeAttribute('src');"
         class="student-photo student-photo--missing">
    <div class="student-body">
      <p class="student-name">Student Name</p>
      <p class="student-degree">Research master student</p>
      <p class="student-thesis">Working thesis title goes here</p>
      <p class="student-bio">A short write-up describing the student's project
        and interests.</p>
    </div>
  </div>

</div>
