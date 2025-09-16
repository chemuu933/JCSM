 # Jesus Christ Solution Ministry (JCSM)

**JCSM** is a modern church ministry web application built with Vue 3, Vite, and Tailwind CSS. The application serves as a digital platform for the Jesus Christ Solution Ministry, featuring sermons, events, and church information.

[![Vue.js](https://img.shields.io/badge/vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D)](https://vuejs.org/)
[![Vite](https://img.shields.io/badge/vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/tailwindcss-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)

## Features

- **Modern UI/UX** - Clean, responsive design built with Tailwind CSS
- **Fast Development** - Lightning fast development experience with Vite
- **Sermon Library** - Browse and listen to past sermons
- **Events Calendar** - Stay updated with upcoming church events
- **Responsive Design** - Works on all devices from mobile to desktop
- **Performance Optimized** - Fast loading times and smooth animations

## Live Demo

Check out the live demo: [JCSM Live](https://jcsm.vercel.app)

## Tech Stack

- **Frontend Framework**: [Vue.js 3](https://vuejs.org/)
- **Build Tool**: [Vite](https://vitejs.dev/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **Icons**: [Font Awesome](https://fontawesome.com/)
- **Deployment**: [Vercel](https://vercel.com/)

## Getting Started

### Prerequisites

- Node.js 16+ (LTS recommended)
- npm 7+ or yarn 1.22+

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/chemuu933/JCSM.git
   cd JCSM
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn
   ```

3. **Start development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```
   Open [http://localhost:5173](http://localhost:5173) to view it in the browser.

4. **Build for production**
   ```bash
   npm run build
   # or
   yarn build
   ```

5. **Preview production build**
   ```bash
   npm run preview
   # or
   yarn preview
   ```

## Project Structure

```
/JCSM
├── public/                 # Static files
├── src/
│   ├── assets/             # Images, fonts, etc.
│   ├── components/         # Reusable Vue components
│   ├── views/              # Page components
│   ├── App.vue             # Root Vue component
│   └── main.js             # Application entry point
├── .gitignore              # Git ignore file
├── index.html              # Main HTML file
├── package.json            # Project metadata and dependencies
├── postcss.config.js       # PostCSS configuration
├── tailwind.config.js      # Tailwind CSS configuration
└── vite.config.js          # Vite configuration
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
