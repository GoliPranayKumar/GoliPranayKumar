<div align="center">

<!-- ============================================================ -->
<!--  HERO BANNER — 100% inline SVG, zero external dependencies  -->
<!-- ============================================================ -->
<svg width="900" height="280" viewBox="0 0 900 280" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#03070F"/>
      <stop offset="45%" stop-color="#001829"/>
      <stop offset="100%" stop-color="#002a40"/>
    </linearGradient>
    <linearGradient id="nameGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00C2FF"/>
      <stop offset="100%" stop-color="#00FF94"/>
    </linearGradient>
    <linearGradient id="divGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00C2FF" stop-opacity="0"/>
      <stop offset="35%" stop-color="#00C2FF" stop-opacity="1"/>
      <stop offset="65%" stop-color="#00FF94" stop-opacity="1"/>
      <stop offset="100%" stop-color="#00FF94" stop-opacity="0"/>
    </linearGradient>
    <filter id="glow"><feGaussianBlur stdDeviation="4" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
    <filter id="orb"><feGaussianBlur stdDeviation="30"/></filter>
  </defs>

  <!-- BG -->
  <rect width="900" height="280" fill="url(#bgGrad)" rx="14"/>

  <!-- Grid -->
  <g stroke="#00C2FF" stroke-opacity="0.05" stroke-width="1">
    <line x1="0" y1="56" x2="900" y2="56"/><line x1="0" y1="112" x2="900" y2="112"/>
    <line x1="0" y1="168" x2="900" y2="168"/><line x1="0" y1="224" x2="900" y2="224"/>
    <line x1="180" y1="0" x2="180" y2="280"/><line x1="360" y1="0" x2="360" y2="280"/>
    <line x1="540" y1="0" x2="540" y2="280"/><line x1="720" y1="0" x2="720" y2="280"/>
  </g>

  <!-- Glow orbs -->
  <circle cx="100" cy="140" r="100" fill="#00C2FF" fill-opacity="0.07" filter="url(#orb)"/>
  <circle cx="800" cy="140" r="90" fill="#00FF94" fill-opacity="0.06" filter="url(#orb)"/>
  <circle cx="450" cy="260" r="70" fill="#00C2FF" fill-opacity="0.04" filter="url(#orb)"/>

  <!-- Corner brackets TL -->
  <polyline points="18,50 18,18 50,18" stroke="#00C2FF" stroke-width="2" fill="none" stroke-opacity="0.7"/>
  <!-- Corner brackets TR -->
  <polyline points="850,18 882,18 882,50" stroke="#00C2FF" stroke-width="2" fill="none" stroke-opacity="0.7"/>
  <!-- Corner brackets BL -->
  <polyline points="18,230 18,262 50,262" stroke="#00FF94" stroke-width="2" fill="none" stroke-opacity="0.7"/>
  <!-- Corner brackets BR -->
  <polyline points="850,262 882,262 882,230" stroke="#00FF94" stroke-width="2" fill="none" stroke-opacity="0.7"/>

  <!-- Top chip -->
  <rect x="310" y="26" width="280" height="22" rx="11" fill="#00C2FF" fill-opacity="0.1" stroke="#00C2FF" stroke-opacity="0.3" stroke-width="1"/>
  <text x="450" y="41" text-anchor="middle" font-family="'Courier New',monospace" font-size="10" fill="#00C2FF" letter-spacing="3">B.TECH AI &amp; DATA SCIENCE · 2023–2027</text>

  <!-- Main name -->
  <text x="450" y="135" text-anchor="middle" font-family="'Arial Black','Arial',sans-serif" font-size="58" font-weight="900" fill="url(#nameGrad)" filter="url(#glow)" letter-spacing="-1">Goli Pranay Kumar</text>

  <!-- Divider -->
  <line x1="150" y1="155" x2="750" y2="155" stroke="url(#divGrad)" stroke-width="1.5"/>

  <!-- Role line -->
  <text x="450" y="182" text-anchor="middle" font-family="'Courier New',monospace" font-size="14" fill="#E8F4FF" fill-opacity="0.85" letter-spacing="3">AI ENGINEER  ·  FULL STACK DEV  ·  DSA ENTHUSIAST</text>

  <!-- Tags row -->
  <!-- Tag 1: Python -->
  <rect x="168" y="200" width="70" height="22" rx="11" fill="#3776AB" fill-opacity="0.25" stroke="#3776AB" stroke-opacity="0.5" stroke-width="1"/>
  <text x="203" y="215" text-anchor="middle" font-family="'Courier New',monospace" font-size="10" fill="#7EC8FF" letter-spacing="1">Python</text>
  <!-- Tag 2: TensorFlow -->
  <rect x="248" y="200" width="90" height="22" rx="11" fill="#FF6F00" fill-opacity="0.2" stroke="#FF6F00" stroke-opacity="0.4" stroke-width="1"/>
  <text x="293" y="215" text-anchor="middle" font-family="'Courier New',monospace" font-size="10" fill="#FFB347" letter-spacing="1">TensorFlow</text>
  <!-- Tag 3: React -->
  <rect x="348" y="200" width="65" height="22" rx="11" fill="#61DAFB" fill-opacity="0.15" stroke="#61DAFB" stroke-opacity="0.4" stroke-width="1"/>
  <text x="380" y="215" text-anchor="middle" font-family="'Courier New',monospace" font-size="10" fill="#61DAFB" letter-spacing="1">React</text>
  <!-- Tag 4: PyTorch -->
  <rect x="423" y="200" width="70" height="22" rx="11" fill="#EE4C2C" fill-opacity="0.2" stroke="#EE4C2C" stroke-opacity="0.4" stroke-width="1"/>
  <text x="458" y="215" text-anchor="middle" font-family="'Courier New',monospace" font-size="10" fill="#FF8A70" letter-spacing="1">PyTorch</text>
  <!-- Tag 5: Java -->
  <rect x="503" y="200" width="55" height="22" rx="11" fill="#ED8B00" fill-opacity="0.2" stroke="#ED8B00" stroke-opacity="0.4" stroke-width="1"/>
  <text x="530" y="215" text-anchor="middle" font-family="'Courier New',monospace" font-size="10" fill="#FFB347" letter-spacing="1">Java</text>
  <!-- Tag 6: DSA -->
  <rect x="568" y="200" width="50" height="22" rx="11" fill="#00C2FF" fill-opacity="0.15" stroke="#00C2FF" stroke-opacity="0.4" stroke-width="1"/>
  <text x="593" y="215" text-anchor="middle" font-family="'Courier New',monospace" font-size="10" fill="#00C2FF" letter-spacing="1">DSA</text>
  <!-- Tag 7: Next.js -->
  <rect x="628" y="200" width="66" height="22" rx="11" fill="#ffffff" fill-opacity="0.06" stroke="#ffffff" stroke-opacity="0.2" stroke-width="1"/>
  <text x="661" y="215" text-anchor="middle" font-family="'Courier New',monospace" font-size="10" fill="#E8F4FF" letter-spacing="1">Next.js</text>

  <!-- Status dot -->
  <circle cx="270" cy="251" r="5" fill="#00FF94" fill-opacity="0.9">
    <animate attributeName="r" values="4;6;4" dur="2s" repeatCount="indefinite"/>
    <animate attributeName="fill-opacity" values="0.9;0.4;0.9" dur="2s" repeatCount="indefinite"/>
  </circle>
  <text x="283" y="256" font-family="'Courier New',monospace" font-size="12" fill="#00FF94" fill-opacity="0.95" letter-spacing="1">Available for Internships &amp; Collabs</text>

  <!-- Location -->
  <text x="700" y="256" text-anchor="middle" font-family="'Courier New',monospace" font-size="12" fill="#00C2FF" fill-opacity="0.7">📍 Hyderabad, India</text>
</svg>

<!-- BADGES ROW — shields.io is always reliable -->
<br/>
<a href="https://www.linkedin.com/in/golipranaykumar/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin"/></a>
&nbsp;
<a href="https://leetcode.com/u/golipranaykumar/"><img src="https://img.shields.io/badge/LeetCode-Solve-FFA116?style=flat-square&logo=leetcode&logoColor=black"/></a>
&nbsp;
<a href="mailto:golipranaykumar@gmail.com"><img src="https://img.shields.io/badge/Gmail-Mail_Me-EA4335?style=flat-square&logo=gmail&logoColor=white"/></a>
&nbsp;
<img src="https://komarev.com/ghpvc/?username=GoliPranayKumar&style=flat-square&color=00C2FF&label=views"/>
&nbsp;
<img src="https://img.shields.io/github/followers/GoliPranayKumar?style=flat-square&color=00FF94&label=followers"/>

</div>

---

<img align="right" width="370" src="https://github-readme-stats.vercel.app/api?username=GoliPranayKumar&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00C2FF&icon_color=00FF94&text_color=c9d1d9&border_radius=10"/>

### 🧑‍💻 `whoami`

```yaml
name:       Goli Pranay Kumar
role:       AI & Data Science Student
college:    Vignan Institute of Technology & Science
batch:      2023 – 2027
location:   Hyderabad, India 🇮🇳

passions:
  - Artificial Intelligence & Deep Learning
  - Data Structures & Algorithms
  - Full Stack Web Development
  - Building things that matter

currently:  Shipping AI + Web Applications 🚀
open_to:    Collaborations & Internships ✅
```

<br clear="right"/>

---

## ⚡ Tech Arsenal

<table>
<tr>
<td valign="top" width="33%">

**🐍 Languages**

![Python](https://img.shields.io/badge/Python-★★★★★-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-★★★★☆-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-★★★★☆-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![C](https://img.shields.io/badge/C-★★★☆☆-00599C?style=flat-square&logo=c&logoColor=white)
![HTML/CSS](https://img.shields.io/badge/HTML%2FCSS-★★★★☆-E34F26?style=flat-square&logo=html5&logoColor=white)

</td>
<td valign="top" width="33%">

**🧠 AI / ML**

![TensorFlow](https://img.shields.io/badge/TensorFlow-★★★★☆-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-★★★☆☆-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-★★★★☆-27338e?style=flat-square&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-★★★★☆-013243?style=flat-square&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-★★★☆☆-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)

</td>
<td valign="top" width="33%">

**🌐 Web / Tools**

![React](https://img.shields.io/badge/React-★★★★☆-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-★★★☆☆-white?style=flat-square&logo=nextdotjs&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-★★★☆☆-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-★★★☆☆-47A248?style=flat-square&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-★★★☆☆-4479A1?style=flat-square&logo=mysql&logoColor=white)

</td>
</tr>
</table>

---

## 🚀 Projects

<table>
<tr>
<td width="50%" valign="top">

### 🧠 MediScannerAI
> **Deep Learning X-Ray Analyzer**

AI system detecting abnormalities in Chest X-rays using convolutional neural networks with a React dashboard.

```
X-Ray → OpenCV Preprocess → CNN Model
      → Abnormality Score → React UI
```

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/-TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)
![OpenCV](https://img.shields.io/badge/-OpenCV-27338e?style=flat-square&logo=opencv&logoColor=white)

[![View](https://img.shields.io/badge/→_View_Project-00C2FF?style=for-the-badge)](https://github.com/GoliPranayKumar/MediScannerAi)

</td>
<td width="50%" valign="top">

### ⚔️ Yuddha Bhumi
> **Strategy Battle Simulation**

Real-time battlefield simulation with AI-driven opponents and strategic decision trees.

```
Player Input → Game Engine → AI Logic
             → Battle State → UI Render
```

![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

[![View](https://img.shields.io/badge/→_View_Project-00C2FF?style=for-the-badge)](https://github.com/GoliPranayKumar/YuddhaBhumi)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 📊 Credovia
> **Credibility Score Platform**

Full-stack platform with real-time credibility calculations and smooth animations.

```
User Data → Score Engine → Dashboard
          → Appwrite DB  → Analytics
```

![Next.js](https://img.shields.io/badge/-Next.js-white?style=flat-square&logo=nextdotjs&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/-Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![Appwrite](https://img.shields.io/badge/-Appwrite-F02E65?style=flat-square&logo=appwrite&logoColor=white)

[![View](https://img.shields.io/badge/→_View_Project-00C2FF?style=for-the-badge)](https://github.com/GoliPranayKumar/Credovia)

</td>
<td width="50%" valign="top">

### 📚 DSA in Java
> **Complete Algorithm Library**

Arrays, Stacks, Queues, Trees, Graphs, Dynamic Programming and more.

```
Arrays → Stacks → Queues → Trees
      → Graphs → DP → Sorting
```

![Java](https://img.shields.io/badge/-Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Algorithms](https://img.shields.io/badge/-Algorithms-00C2FF?style=flat-square)
![DSA](https://img.shields.io/badge/-DSA-00FF94?style=flat-square)

[![View](https://img.shields.io/badge/→_View_Project-00C2FF?style=for-the-badge)](https://github.com/GoliPranayKumar/DataStructures)

</td>
</tr>
</table>

---

## 📊 GitHub Analytics

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com/?user=GoliPranayKumar&theme=tokyonight&hide_border=true&background=0D1117&ring=00C2FF&fire=00FF94&currStreakLabel=00C2FF&border_radius=10" width="49%"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=GoliPranayKumar&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00C2FF&text_color=c9d1d9&border_radius=10" width="49%"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=GoliPranayKumar&theme=tokyo-night&bg_color=0D1117&color=00C2FF&line=00FF94&point=ffffff&area=true&hide_border=true" width="100%"/>

</div>

---

## 🏆 Trophies

<div align="center">
<img src="https://github-profile-trophy.vercel.app/?username=GoliPranayKumar&theme=tokyonight&no-frame=true&no-bg=true&column=7&margin-w=4"/>
</div>

---

## 🎯 2025 Roadmap

```
LeetCode 500+   ████████░░░░  Grinding Daily
Advanced DSA    ██████░░░░░░  Graphs & DP Next
AI SaaS MVP     ████░░░░░░░░  In Design Phase
Open Source     ██░░░░░░░░░░  First PRs Coming
```

---

<div align="center">

<!-- FOOTER SVG — inline, zero dependencies -->
<svg width="900" height="90" viewBox="0 0 900 90" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="fBg" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#03070F"/>
      <stop offset="50%" stop-color="#001829"/>
      <stop offset="100%" stop-color="#03070F"/>
    </linearGradient>
    <linearGradient id="fLine" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00C2FF" stop-opacity="0"/>
      <stop offset="50%" stop-color="#00FF94" stop-opacity="1"/>
      <stop offset="100%" stop-color="#00C2FF" stop-opacity="0"/>
    </linearGradient>
  </defs>
  <rect width="900" height="90" fill="url(#fBg)" rx="10"/>
  <line x1="0" y1="3" x2="900" y2="3" stroke="url(#fLine)" stroke-width="2"/>
  <text x="450" y="42" text-anchor="middle" font-family="'Courier New',monospace" font-size="14" fill="#00C2FF" letter-spacing="1">✨ Thanks for visiting — Let's build something awesome! 🚀</text>
  <text x="450" y="68" text-anchor="middle" font-family="'Courier New',monospace" font-size="11" fill="#E8F4FF" fill-opacity="0.4" letter-spacing="2">🎮 STRATEGY GAMES · 🎨 UI/UX · 🎬 VIDEO EDITING · 🤖 AI TOOLS</text>
</svg>

</div>
