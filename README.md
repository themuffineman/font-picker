# 📚 Font Repository

A lightweight, open-source repository of font metadata and preview icons.
Perfect for building font pickers, design tools, or any app that needs quick access to fonts with visual previews.

---

## 🚀 Features

- ✅ **Easy-to-use data** – Fonts are exported as a simple array of objects.
- 🎨 **Visual previews** – Each font includes an image icon (how the font actaully looks like).
- 🌍 **Open-source** – Extend, modify, or integrate however you like.

---

## 📂 Repository Structure

```
.
├── fonts.js          # Exports an array of font objects
├── /font-images            # Folder containing font preview images and names
└── README.md
```

Each font object looks like this:

```js
{
  name: "Instrument Serif",
  icon: "https://raw.githubusercontent.com/themuffineman/font-picker/refs/heads/main/font-images/Instrument Serif.png"
}
```

---

## 📦 Installation

Clone or install the repository:

```bash
git clone https://github.com/themuffineman/font-picker.git
cd font-picker
```

---

## 🛠 Usage

Import the `fonts` array into your project:

```js
import { fonts } from "font-picker/fonts.js";

console.log(fonts);
/*
[
  {
    name: "Inter",
    icon: "https://raw.githubusercontent.com/themuffineman/font-picker/refs/heads/main/font-images/Inter.png"
  },
  {
    name: "DM Sans",
    icon: "https://raw.githubusercontent.com/themuffineman/font-picker/refs/heads/main/font-images/DM Sans.png"
  },
  ...
]
*/
```

You can then use this data to build a **font picker**:

```jsx
function FontPicker() {
  return (
    <div>
      {fonts.map((font) => (
        <div key={font.name}>
          <img src={font.icon} alt={font.name} width="100" />
          <p>{font.name}</p>
        </div>
      ))}
    </div>
  );
}
```

---

## 📜 License

MIT License – Free to use, share, and modify.
