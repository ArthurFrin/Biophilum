# Biophilum

## 🌟 Features

- **Expertise Sections**: Detailed sections on fauna, flora, wetlands, watersheds, and more.
- **Responsive Design**: Optimized for both desktop and mobile devices.
- **Interactive Navigation**: Smooth scrolling and section detection.
- **Contact Information**: Easy access to contact details and downloadable CV.
- **Multimedia Content**: Rich visuals and illustrations to enhance user experience.

## 🚀 Project Structure

```text
/
├── public/                # Static assets
├── src/
│   ├── components/        # Reusable components
│   │   ├── icons/         # Icon components
│   │   ├── Header.astro   # Header component
│   │   ├── NavBar.vue     # Navigation bar with Vue.js
│   │   ├── FloraAndFauna.astro  # Fauna and flora expertise section
│   │   ├── WeatArea.astro       # Wetlands expertise section
│   │   ├── Watershed.astro      # Watershed expertise section
│   │   ├── WhoIAm.astro         # About section
│   │   ├── News.astro           # News and updates
│   │   └── footerContact.astro  # Footer with contact details
│   ├── layouts/          # Layout components
│   └── pages/            # Application pages
└── package.json          # Project metadata and dependencies
```

## 🛠️ Technologies Used

- **Astro**: Static site generator for fast and modern web development.
- **Vue.js**: Interactive components and state management.
- **SCSS**: Styling with modular and reusable CSS.

## 🧞 Commands

All commands are run from the root of the project:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Builds the production site to `./dist/`          |
| `npm run preview`         | Previews the production build locally            |