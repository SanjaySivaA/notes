# Timetable

|           | 8:00-8:50 | 9:00-9:50 | 10:00-10:50 | 11:00-11:50 | 12:05-12:55 | Break   | 14:00-16:45 | 17:10-18:00 |
| :---      | :---:     | :---:     | :---:       | :---:       | :---:       | :---:   | :---:       | :---:       |
| Monday    |           | <span class="dbms">DBMS</span>       | <span class="cd">CD</span>         |             |             |         | <span class="cd">CD Lab</span>       |             |
| Wednesday | <span class="cd">CD</span>        |           |             |             |             |         |             |             |
| Friday    |           |           | <span class="dbms">DBMS</span>        | <span class="cd">CD</span>           |             |         | <span class="dbms">DBMS Lab</span>    |             |

<br/>

|           | 8:00-8:50 | 9:00-10:15 | 10:30-11:45 | 12:00-12:50 | Break   | 14:00-15:15 | 15:30-16:45 | 17:10-18:00 |
| :---      | :---:     | :---:      | :---:       | :---:       | :---:   | :---:       | :---:       | :---:       |
| Tuesday   | <span class="dbms">DBMS</span>      | <span class="nlp">NLP</span>        |             |             |         | <span class="mc">MC</span>          | <span class="gtm">GTM</span>         |             |
| Thursday  |           |            | <span class="nlp">NLP</span>         |             |         | <span class="gtm">GTM</span>         | <span class="mc">MC</span>          | <span class="mc">MC</span>          |


<style>

/* Sharp High-Contrast Light Theme */
:root {
  --bg-color: #ffffff;
  --text-main: #000000;
  --text-muted: #666666;
  --border-grey: #d3d3d3; /* Darker, crisper grey */
  --border-radius: 10px;
  
  /* Intense Sharp Shadow */
  --sharp-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 
                  0 4px 6px -2px rgba(0, 0, 0, 0.05),
                  0 0 1px 0 rgba(0, 0, 0, 0.3); /* The "edge" shadow */
  
  /* Today Highlight */
  --today-bg: #fffceb;
  --today-accent:rgb(226, 27, 27);

  /* Subject Palette */
  --dbms: #0070f3;
  --cd: #7928ca;
  --nlp: #d97706;
  --mc: #059669;
  --gtm: #db2777;
}

body {
  background-color: var(--bg-color);
  color: var(--text-main);
  font-family: 'Inter', -apple-system, system-ui, sans-serif;
  -webkit-font-smoothing: antialiased;
  padding: 50px;
}

h1 {
  font-weight: 800;
  letter-spacing: -0.05em;
  font-size: 2.5rem;
  margin-bottom: 2rem;
}

table {
  width: 100%;
  border-collapse: separate; 
  border-spacing: 0;
  border-radius: var(--border-radius);
  box-shadow: var(--sharp-shadow);
  border: 1px solid var(--border-grey);
  overflow: hidden;
  margin-bottom: 4rem;
}

th, td {
  padding: 16px 20px; 
  font-size: 0.9rem;
}

th:last-child, td:last-child {
  border-right: none;
}

tr:last-child td {
  border-bottom: none;
}

th {
  background-color: #f8f8f8;
  color: var(--text-main);
  font-weight: 700;
  letter-spacing: -0.02em;
}

td:first-child {
  font-weight: 700;
  background-color: #fcfcfc;
  width: 120px;
}

/* Today's Highlight Class */
.today {
  background-color: var(--today-bg) !important;
}
.today td:first-child {
  background-color: var(--today-bg) !important;
  border-left: 5px solid var(--today-accent);
}

/* Subject Styling */
span {
  font-weight: 700;
}

.dbms { color: var(--dbms); }
.cd   { color: var(--cd); }
.nlp  { color: var(--nlp); }
.mc   { color: var(--mc); }
.gtm  { color: var(--gtm); }

</style>