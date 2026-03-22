---
title: Students
date: 2024-01-01
type: page
---

<style>
.students-list { display: flex; flex-direction: column; margin-top: 1.5rem; }

.student-row {
  display: flex;
  align-items: flex-start;
  gap: 1.75rem;
  padding: 1.75rem 0;
  border-bottom: 1px solid rgba(0,0,0,.1);
}
.student-row:last-child { border-bottom: none; }

.student-photo {
  flex: 0 0 100px;
  width: 100px;
  height: 100px;
  object-fit: cover;
  border-radius: 14px;
  background: #e0e0e0;
  display: block;
}

.student-photo-placeholder {
  flex: 0 0 100px;
  width: 100px;
  height: 100px;
  border-radius: 14px;
  background: #e0e0e0;
}

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

<div class="students-list">

  <div class="student-row">
    <img class="student-photo" src="/img/students/jane_smith.jpg" alt="Jane Smith">
    <div class="student-body">
      <p class="student-name"><a href="https://linkedin.com/in/janesmith" target="_blank" rel="noopener">Jane Smith</a></p>
      <p class="student-degree">PhD candidate</p>
      <p class="student-thesis">Causal inference methods in pharmacoepidemiology</p>
      <p class="student-bio">Jane is investigating the application of instrumental variable methods to large claims databases, with a focus on treatment effect heterogeneity in chronic disease populations.</p>
    </div>
  </div>

  <div class="student-row">
    <img class="student-photo" src="/img/students/tom_devries.jpg" alt="Tom de Vries">
    <div class="student-body">
      <p class="student-name">Tom de Vries</p>
      <p class="student-degree">MSc, graduated 2023</p>
      <p class="student-thesis">Directed acyclic graphs in nutritional epidemiology</p>
      <p class="student-bio">Tom's thesis examined how DAG-based covariate selection affects estimates of diet–disease associations in prospective cohort studies. He now works as a data analyst at RIVM.</p>
    </div>
  </div>

  <div class="student-row">
    <div class="student-photo-placeholder"></div>
    <div class="student-body">
      <p class="student-name">Aisha Bakker</p>
      <p class="student-degree">Research master student</p>
      <p class="student-thesis">Target trial emulation for vaccine effectiveness studies</p>
      <p class="student-bio">Aisha is applying the target trial framework to administrative data from the NIVEL primary care database to estimate COVID-19 vaccine effectiveness in elderly patients.</p>
    </div>
  </div>

</div>
