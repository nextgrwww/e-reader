# 📚 Kindle Reader Pro

A feature‑rich, browser‑based e‑reader that brings the Kindle experience to the web.  
Built with React, Tailwind CSS, and EPUB.js, it simulates an e‑ink device with a clean interface, advanced reading tools, and full local storage persistence.

---

## ✨ Features

- **Library Management** – Upload EPUB, PDF, MOBI, or AZW3 files; view your collection in grid or list layout.
- **Advanced Reader** – Paginated or continuous scrolling, landscape two‑page view, and keyboard navigation.
- **Customizable Themes** – Light, Dark, and Sepia modes with adjustable font size and family.
- **Word Wise** – Inline definitions for difficult words (auto‑fetched via a free dictionary API).
- **Notebook** – Save bookmarks and character names; search for character mentions across the book.
- **Context Menu** – Right‑click (or long‑press) any word to copy, bookmark, or add to characters.
- **Data Persistence** – All books, settings, and annotations are stored locally in your browser.
- **Import / Export** – Upload new books via the floating button; backup your data by exporting JSON.

---

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/nextgrwww/e-reader.git
   cd e-reader
   ```

2. **Open the application**  
   Since it’s a single HTML file, you can open `index.html` directly in your browser.  
   For the best experience, use a local server (e.g., VS Code Live Server or `python -m http.server`).

3. **Upload your books**  
   Click the floating **+** button (or the upload icon) to add EPUB/PDF/MOBI/AZW3 files.

4. **Start reading** – tap any book in the library to open it.

---

## 🧰 How It Works

- **EPUB Rendering** – Powered by [EPUB.js](https://github.com/futurepress/epub.js/) with custom hooks for Word Wise and context menus.
- **State Management** – React hooks manage UI state; all data is serialized to `localStorage` under the key `kindle_web_data_v2`.
- **Word Wise** – When enabled, difficult words are annotated with definitions fetched on‑demand from the [Free Dictionary API](https://dictionaryapi.dev/).
- **Notebook** – Bookmarks and character lists are stored per book. Selecting a character triggers a full‑text search across the book’s spine.

---

## 🔧 Customisation

All reader settings (font, theme, two‑page view, Word Wise) are controlled via the **Aa menu** (top‑right in the reader).  
You can also adjust the following CSS variables in the `<style>` block to change the overall look:

```css
:root {
  /* Add custom properties here */
}
```

---

## 📜 Changelog

Based on recent commits:

- **Jul 13, 2026** – Added a dedicated persistent button for the menu toggle; refactored reader toolkit (theming, context menu, notebook, search).
- **Mar 31, 2026** – Introduced split‑page view for landscape mode; added long‑press Word Wise support and unified localStorage schema.
- **Mar 30, 2026** – Initial project creation.

---

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request with your improvements.  
Make sure to test new features thoroughly across different screen sizes and file formats.

---

## 📄 License

This project is open‑source and available under the [MIT License](LICENSE).

---

## 🙏 Acknowledgements

- [EPUB.js](https://github.com/futurepress/epub.js/) for EPUB parsing and rendering.
- [Tailwind CSS](https://tailwindcss.com/) for rapid styling.
- [React](https://reactjs.org/) for UI architecture.
- [Free Dictionary API](https://dictionaryapi.dev/) for word definitions.
- Icons from [Lucide](https://lucide.dev/).

---

*Happy reading!* 📖
