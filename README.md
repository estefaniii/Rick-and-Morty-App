cat << 'EOF' > README.md
# 🌌 Rick & Morty Universe Explorer

<div align="center">
  <img src="https://github.com/user-attachments/assets/59f1872d-48e9-4a33-986b-c413f72afbaf"
  width="500" alt="Rick & Morty App Screenshot">
</div>

A dynamic React application that explores the Rick & Morty multiverse with stunning visuals and interactive features.

## ✨ Features

- **Multiverse Navigation**: Explore all dimensions in the Rick & Morty universe
- **Character Database**: Detailed profiles for every resident
- **Instant Search**: Find locations with real-time suggestions
- **Pagination System**: Smooth browsing through hundreds of characters
- **Dark Mode UI**: Eye-friendly interface with themed styling
- **Responsive Design**: Perfect experience on any device

## 🛠️ Tech Stack

- **React 18** (Hooks, Context API)
- **Axios** for API communication
- **CSS Modules** for scoped styling
- **React Icons** for beautiful SVG icons
- **Rick & Morty API** integration

## 🚀 Installation

1. Clone the repository:
```bash
git clone https://github.com/estefaniii/rick-morty-explorer.git
```
2. Install dependencies:
```bash
npm install
```
3. Launch the multiverse:
```bash
npm run dev
```

## 🔍 Code Highlights

```jsx
// Custom hook for API data fetching
export function useFetchApi() {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(false);
  
  const request = useCallback(async (url) => {
    setLoading(true);
    try {
      const response = await axios.get(url);
      setData(response.data);
    } catch (error) {
      console.error("Wubba Lubba Dub Dub!", error);
    } finally {
      setLoading(false);
    }
  }, []);

  return { data, loading, request };
}
```

## 🌟 Components Showcase

### Hero Section
```jsx
<div className="hero">
  <img src="portal.gif" alt="Rick & Morty portal" />
</div>
```

### Resident Card
```jsx
<article className="resident-card">
  <header>
    <img src={character.image} alt={character.name} />
    <span className="status-badge">{character.status}</span>
  </header>
  <div className="resident-info">
    <h3>{character.name}</h3>
    <p>Species: {character.species}</p>
  </div>
</article>
```

## 🤝 Contributing to the Multiverse

1. Fork this repository
2. Create your feature branch (\`git checkout -b feature/amazing-feature\`)
3. Commit your changes (\`git commit -m 'Add some schwifty feature'\`)
4. Push to the branch (\`git push origin feature/amazing-feature\`)
5. Open a Pull Request

## 💖 Support My Interdimensional Work

If you enjoy this portal to the Rick & Morty universe, consider supporting my development:

[![Support via PayPal](https://img.shields.io/badge/Donate-PayPal-blue?style=for-the-badge&logo=paypal)](https://paypal.me/estefanniii?country.x=PA&locale.x=es_XC)

---

⭐ Don't forget to star the repository if you think this app is "Get Schwifty" cool!
EOF
