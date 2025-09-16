 cd "church ministry"
 git add .
 git -m "updates"
 git push
npm run dev


---

# JCSM

**JCSM** is a church ministry web app built with Vue.js & Tailwind CSS, deployed on Vercel. It features pages like sermons, church calendar, and more to support church operations online.

---

## Table of Contents

* [Features](#features)
* [Demo](#demo)
* [Tech Stack](#tech-stack)
* [Getting Started](#getting-started)
* [Project Structure](#project-structure)
* [Deployment](#deployment)
* [Contributing](#contributing)

---

## Features

Here are some of the main features:

* Display sermons (videos or audio)
* Church events calendar
* Responsive UI using Tailwind CSS
* Fast development setup (Vite)
* Clean UI/UX layout

---

## Demo

You can see a live version here: [jcsm.vercel.app](https://jcsm.vercel.app) ([GitHub][1])

---

## Tech Stack

* **Frontend**: Vue.js ([GitHub][1])
* **Styling**: Tailwind CSS ([GitHub][1])
* **Build Tool**: Vite ([GitHub][1])

---

## Getting Started

Here’s how you can set up the project locally:

1. **Clone the repo**

   ```bash
   git clone https://github.com/chemuu933/JCSM.git
   cd JCSM
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Run in development mode**

   ```bash
   npm run dev
   ```

4. **Build for production**

   ```bash
   npm run build
   ```

5. **Preview production build locally** (optional)

   ```bash
   npm run preview
   ```

---

## Project Structure

Here’s a rough overview of the folder layout:

```
/JCSM
│
├── .vscode/                 # VSCode settings (if any)
├── src/                     # Main source folder
│   ├── components/          # Reusable Vue components
│   ├── views/               # Pages / views
│   ├── assets/              # Images, styles etc.
│   └── ...                  # Other source files
├── .gitignore
├── package.json
├── vite.config.js
├── tailwind.config.js
└── index.html
```

---

## Deployment

* Deployed using Vercel (`jcsm.vercel.app`) ([GitHub][1])
* Ensure environment variables are added via Vercel dashboard if needed
* Production build uses `npm run build`

---

## Contributing

If you want to contribute:

1. Fork the repo
2. Create a feature branch (`git checkout -b feature-name`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature-name`)
5. Open a Pull Request



[1]: https://github.com/chemuu933/JCSM "GitHub - chemuu933/JCSM"
