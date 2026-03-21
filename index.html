import { useState, useRef, useEffect, useCallback } from "react";

// ─── DATA ────────────────────────────────────────────────────────────────────

const CATEGORIES = [
  {
    name: "Restaurantes",
    icon: "🍽️",
    subs: [
      { group: "Cozinha", items: ["Brasileira", "Japonesa", "Italiana", "Portuguesa", "Árabe", "Mexicana", "Chinesa", "Francesa"] },
      { group: "Tipo", items: ["Buffet", "À la carte", "Self-service", "Rodízio", "Fast food", "Food truck"] },
      { group: "Ocasião", items: ["Romântico", "Família", "Negócios", "Casual", "Happy hour"] },
    ],
  },
  {
    name: "Cafés & Padarias",
    icon: "☕",
    subs: [
      { group: "Cafeterias", items: ["Café especial", "Café coado", "Espresso bar", "Café da manhã"] },
      { group: "Padarias", items: ["Pão artesanal", "Confeitaria", "Salgados", "Doces finos"] },
      { group: "Mais", items: ["Açaí", "Sucos naturais", "Sorveteria", "Casa de chá"] },
    ],
  },
  {
    name: "Mercados",
    icon: "🛒",
    subs: [
      { group: "Tipo", items: ["Supermercado", "Minimercado", "Hortifrúti", "Empório", "Atacarejo"] },
      { group: "Especialidade", items: ["Orgânicos", "Importados", "Bebidas", "Frios e laticínios"] },
      { group: "Conveniência", items: ["24 horas", "Delivery", "Adega", "Produtos naturais"] },
    ],
  },
  {
    name: "Saúde & Bem-estar",
    icon: "💊",
    subs: [
      { group: "Farmácia", items: ["Drogaria", "Manipulação", "Homeopatia", "Produtos naturais"] },
      { group: "Corpo", items: ["Academia", "Pilates", "Yoga", "CrossFit", "Natação"] },
      { group: "Beleza", items: ["Salão", "Barbearia", "Estética", "Spa", "Manicure"] },
    ],
  },
  {
    name: "Moda & Acessórios",
    icon: "👗",
    subs: [
      { group: "Roupas", items: ["Feminina", "Masculina", "Infantil", "Plus size", "Moda praia"] },
      { group: "Acessórios", items: ["Joalheria", "Bijuteria", "Bolsas", "Relógios", "Óculos"] },
      { group: "Calçados", items: ["Tênis", "Sapatos", "Sandálias", "Chinelos"] },
    ],
  },
  {
    name: "Serviços",
    icon: "🔧",
    subs: [
      { group: "Casa", items: ["Eletricista", "Encanador", "Pintor", "Chaveiro", "Limpeza"] },
      { group: "Pet", items: ["Pet shop", "Veterinário", "Banho e tosa", "Dog walker"] },
      { group: "Diversos", items: ["Lavanderia", "Costura", "Sapateiro", "Gráfica", "Cartório"] },
    ],
  },
  {
    name: "Educação",
    icon: "📚",
    subs: [
      { group: "Ensino", items: ["Idiomas", "Reforço escolar", "Pré-vestibular", "Informática"] },
      { group: "Cultura", items: ["Livraria", "Papelaria", "Escola de música", "Escola de dança"] },
      { group: "Kids", items: ["Creche", "Escola infantil", "Brinquedoteca", "Atividades extracurriculares"] },
    ],
  },
  {
    name: "Vida Noturna",
    icon: "🍸",
    subs: [
      { group: "Bares", items: ["Bar de praia", "Boteco", "Rooftop", "Pub", "Wine bar"] },
      { group: "Baladas", items: ["Sertanejo", "Funk", "Eletrônica", "Pagode", "Samba"] },
      { group: "Diversão", items: ["Karaokê", "Bilhar", "Boliche", "Fliperamas"] },
    ],
  },
];

const STREET_NAMES = [
  "Av. Atlântica", "R. Barata Ribeiro", "R. Santa Clara", "Av. Nossa Sra. de Copacabana",
  "R. Figueiredo Magalhães", "R. Siqueira Campos", "R. Tonelero", "R. Ministro Viveiros de Castro",
  "R. Domingos Ferreira", "R. Bolívar", "R. Duvivier", "R. Xavier da Silveira",
  "R. Paula Freitas", "R. Hilário de Gouveia", "R. Constante Ramos", "R. Pompeu Loureiro",
];

const FIRST_NAMES = [
  "Cantina da", "Sabor do", "Empório", "Bistrô", "Café", "Padaria", "Mercado",
  "Ateliê", "Espaço", "Ponto do", "Casa da", "Recanto do", "Boteco do",
  "Delícias da", "Canto do", "Armazém",
];

const LAST_NAMES = [
  "Dona Maria", "Seu Zé", "Copa", "Praia", "Leme", "Atlântica", "Mar",
  "Sol", "Areia", "Carioca", "Ipanema", "Bossa", "Harmonia", "Sabor",
  "Vovó", "Mineiro",
];

function seededRandom(seed) {
  let s = seed;
  return () => {
    s = (s * 16807) % 2147483647;
    return (s - 1) / 2147483646;
  };
}

function generateListings() {
  const rng = seededRandom(42);
  const catIcons = ["🍽️", "☕", "🛒", "💊", "👗", "🔧", "📚", "🍸"];
  const catNames = CATEGORIES.map((c) => c.name);
  const listings = [];
  const COPA_CENTER = { lat: -22.9711, lng: -43.1822 };

  for (let i = 0; i < 48; i++) {
    const catIdx = Math.floor(rng() * catNames.length);
    const cat = CATEGORIES[catIdx];
    const subGroup = cat.subs[Math.floor(rng() * cat.subs.length)];
    const subItem = subGroup.items[Math.floor(rng() * subGroup.items.length)];
    const rating = (3.5 + rng() * 1.5).toFixed(1);
    const reviews = Math.floor(10 + rng() * 490);
    const street = STREET_NAMES[Math.floor(rng() * STREET_NAMES.length)];
    const num = Math.floor(100 + rng() * 2000);
    const firstName = FIRST_NAMES[Math.floor(rng() * FIRST_NAMES.length)];
    const lastName = LAST_NAMES[Math.floor(rng() * LAST_NAMES.length)];
    const hue = Math.floor(rng() * 360);
    const lat = COPA_CENTER.lat + (rng() - 0.5) * 0.018;
    const lng = COPA_CENTER.lng + (rng() - 0.5) * 0.012;

    listings.push({
      id: i,
      name: `${firstName} ${lastName}`,
      category: catNames[catIdx],
      subcategory: subItem,
      icon: catIcons[catIdx],
      rating: parseFloat(rating),
      reviews,
      address: `${street}, ${num} - Copacabana`,
      hue,
      lat,
      lng,
      open: rng() > 0.2,
      whatsapp: true,
    });
  }
  return listings;
}

const ALL_LISTINGS = generateListings();

// ─── COLORS / THEME ──────────────────────────────────────────────────────────

const T = {
  bg: "#FAFAF8",
  surface: "#FFFFFF",
  text: "#1A1A1A",
  textMuted: "#6B6B6B",
  textLight: "#999999",
  brand: "#00A86B",
  brandDark: "#008F5A",
  brandLight: "#E6F7EF",
  accent: "#FF6B35",
  border: "#E8E8E4",
  borderLight: "#F0F0EC",
  shadow: "0 2px 12px rgba(0,0,0,0.08)",
  shadowHover: "0 8px 28px rgba(0,0,0,0.12)",
  megaBg: "#FFFFFF",
  headerBg: "#FFFFFF",
  topBarBg: "#00A86B",
  radius: "14px",
  radiusSm: "8px",
};

// ─── STYLES (CSS-in-JS) ─────────────────────────────────────────────────────

const styles = {
  app: {
    fontFamily: "'DM Sans', 'Nunito', sans-serif",
    background: T.bg,
    color: T.text,
    minHeight: "100vh",
    position: "relative",
  },

  // TOP BAR
  topBar: {
    background: T.topBarBg,
    padding: "10px 0",
    position: "sticky",
    top: 0,
    zIndex: 1000,
  },
  topBarInner: {
    maxWidth: 1280,
    margin: "0 auto",
    padding: "0 24px",
    display: "flex",
    alignItems: "center",
    gap: 16,
  },
  logo: {
    display: "flex",
    alignItems: "center",
    gap: 8,
    color: "#fff",
    fontWeight: 800,
    fontSize: 22,
    letterSpacing: "-0.5px",
    textDecoration: "none",
    flexShrink: 0,
    cursor: "pointer",
  },
  logoSub: {
    fontSize: 10,
    fontWeight: 500,
    opacity: 0.85,
    letterSpacing: "0.5px",
    textTransform: "uppercase",
    marginTop: -2,
  },
  searchWrap: {
    flex: 1,
    maxWidth: 600,
    position: "relative",
  },
  searchInput: {
    width: "100%",
    padding: "10px 44px 10px 16px",
    border: "none",
    borderRadius: 50,
    fontSize: 14,
    background: "rgba(255,255,255,0.95)",
    color: T.text,
    outline: "none",
    boxSizing: "border-box",
  },
  searchIcon: {
    position: "absolute",
    right: 14,
    top: "50%",
    transform: "translateY(-50%)",
    color: T.textMuted,
    fontSize: 16,
    pointerEvents: "none",
  },
  topBarActions: {
    display: "flex",
    alignItems: "center",
    gap: 12,
    flexShrink: 0,
  },
  topBarBtn: {
    background: "rgba(255,255,255,0.18)",
    border: "none",
    borderRadius: 50,
    padding: "8px 16px",
    color: "#fff",
    fontSize: 13,
    fontWeight: 600,
    cursor: "pointer",
    display: "flex",
    alignItems: "center",
    gap: 6,
    transition: "background 0.2s",
  },

  // CATEGORY BAR
  catBar: {
    background: T.headerBg,
    borderBottom: `1px solid ${T.border}`,
    position: "sticky",
    top: 48,
    zIndex: 999,
  },
  catBarInner: {
    maxWidth: 1280,
    margin: "0 auto",
    padding: "0 24px",
    display: "flex",
    alignItems: "stretch",
    gap: 0,
    overflowX: "auto",
  },
  catItem: (active) => ({
    padding: "14px 18px",
    fontSize: 13.5,
    fontWeight: 600,
    color: active ? T.brand : T.text,
    cursor: "pointer",
    whiteSpace: "nowrap",
    borderBottom: active ? `3px solid ${T.brand}` : "3px solid transparent",
    transition: "all 0.2s",
    display: "flex",
    alignItems: "center",
    gap: 6,
    position: "relative",
    userSelect: "none",
    background: "transparent",
    borderTop: "none",
    borderLeft: "none",
    borderRight: "none",
  }),

  // MEGA DROPDOWN
  megaOverlay: {
    position: "fixed",
    top: 0,
    left: 0,
    right: 0,
    bottom: 0,
    background: "rgba(0,0,0,0.15)",
    zIndex: 998,
  },
  megaDrop: {
    position: "absolute",
    top: "100%",
    left: 0,
    right: 0,
    background: T.megaBg,
    borderBottom: `1px solid ${T.border}`,
    boxShadow: "0 16px 48px rgba(0,0,0,0.1)",
    zIndex: 999,
    animation: "megaIn 0.2s ease",
  },
  megaInner: {
    maxWidth: 1280,
    margin: "0 auto",
    padding: "28px 24px 32px",
    display: "flex",
    gap: 48,
  },
  megaGroup: {
    flex: 1,
    minWidth: 160,
  },
  megaGroupTitle: {
    fontSize: 11,
    fontWeight: 700,
    textTransform: "uppercase",
    letterSpacing: "1px",
    color: T.brand,
    marginBottom: 14,
  },
  megaLink: {
    display: "block",
    fontSize: 13.5,
    color: T.text,
    padding: "5px 0",
    cursor: "pointer",
    transition: "color 0.15s",
    textDecoration: "none",
  },

  // BODY
  body: {
    maxWidth: 1280,
    margin: "0 auto",
    padding: "32px 24px",
  },
  sectionTitle: {
    fontSize: 24,
    fontWeight: 800,
    marginBottom: 4,
    letterSpacing: "-0.5px",
  },
  sectionSub: {
    fontSize: 14,
    color: T.textMuted,
    marginBottom: 24,
  },

  // GRID
  grid: {
    display: "grid",
    gridTemplateColumns: "repeat(auto-fill, minmax(270px, 1fr))",
    gap: 24,
  },

  // CARD
  card: {
    background: T.surface,
    borderRadius: T.radius,
    overflow: "hidden",
    cursor: "pointer",
    transition: "box-shadow 0.25s, transform 0.25s",
    border: `1px solid ${T.borderLight}`,
  },
  cardThumb: (hue) => ({
    height: 180,
    background: `linear-gradient(135deg, hsl(${hue},55%,65%), hsl(${(hue + 40) % 360},45%,55%))`,
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    fontSize: 52,
    position: "relative",
  }),
  cardBadge: (open) => ({
    position: "absolute",
    top: 12,
    left: 12,
    background: open ? "rgba(0,168,107,0.92)" : "rgba(180,40,40,0.88)",
    color: "#fff",
    fontSize: 10.5,
    fontWeight: 700,
    padding: "4px 10px",
    borderRadius: 50,
    letterSpacing: "0.3px",
  }),
  cardWhatsapp: {
    position: "absolute",
    top: 12,
    right: 12,
    background: "rgba(37,211,102,0.92)",
    color: "#fff",
    fontSize: 10.5,
    fontWeight: 700,
    padding: "4px 10px",
    borderRadius: 50,
    display: "flex",
    alignItems: "center",
    gap: 4,
  },
  cardBody: {
    padding: "14px 16px 16px",
  },
  cardName: {
    fontSize: 15,
    fontWeight: 700,
    marginBottom: 2,
    lineHeight: 1.3,
  },
  cardCat: {
    fontSize: 12,
    color: T.textMuted,
    marginBottom: 8,
  },
  cardBottom: {
    display: "flex",
    alignItems: "center",
    justifyContent: "space-between",
  },
  cardRating: {
    display: "flex",
    alignItems: "center",
    gap: 4,
    fontSize: 13,
    fontWeight: 600,
  },
  cardReviews: {
    fontSize: 12,
    color: T.textLight,
  },
  cardAddress: {
    fontSize: 11.5,
    color: T.textLight,
    marginTop: 8,
    lineHeight: 1.4,
  },

  // VER MAIS
  verMaisWrap: {
    textAlign: "center",
    marginTop: 40,
    marginBottom: 20,
  },
  verMaisBtn: {
    background: T.text,
    color: "#fff",
    border: "none",
    borderRadius: 50,
    padding: "14px 48px",
    fontSize: 15,
    fontWeight: 700,
    cursor: "pointer",
    transition: "transform 0.2s, box-shadow 0.2s",
    letterSpacing: "0.3px",
  },

  // EXPLORE PAGE
  exploreContainer: {
    display: "flex",
    height: "calc(100vh - 49px)",
    overflow: "hidden",
  },
  exploreList: {
    flex: "0 0 55%",
    overflowY: "auto",
    padding: "20px 24px",
    background: T.bg,
  },
  exploreMap: {
    flex: 1,
    background: "#E8EDE4",
    position: "relative",
    overflow: "hidden",
  },
  exploreCard: {
    display: "flex",
    gap: 16,
    padding: "16px",
    background: T.surface,
    borderRadius: T.radiusSm,
    marginBottom: 12,
    border: `1px solid ${T.borderLight}`,
    cursor: "pointer",
    transition: "box-shadow 0.2s",
  },
  exploreCardThumb: (hue) => ({
    width: 110,
    height: 90,
    borderRadius: T.radiusSm,
    background: `linear-gradient(135deg, hsl(${hue},55%,65%), hsl(${(hue + 40) % 360},45%,55%))`,
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    fontSize: 30,
    flexShrink: 0,
  }),
  exploreCardBody: {
    flex: 1,
    display: "flex",
    flexDirection: "column",
    justifyContent: "center",
  },

  // MAP
  mapSvg: {
    width: "100%",
    height: "100%",
  },
  mapPin: {
    cursor: "pointer",
    transition: "transform 0.2s",
  },
  mapTooltip: {
    position: "absolute",
    background: T.surface,
    padding: "10px 14px",
    borderRadius: T.radiusSm,
    boxShadow: T.shadowHover,
    fontSize: 12,
    zIndex: 10,
    pointerEvents: "none",
    maxWidth: 200,
    border: `1px solid ${T.border}`,
  },

  // BACK BUTTON
  backBtn: {
    background: "none",
    border: `1px solid ${T.border}`,
    borderRadius: 50,
    padding: "8px 20px",
    fontSize: 13,
    fontWeight: 600,
    cursor: "pointer",
    display: "flex",
    alignItems: "center",
    gap: 6,
    color: T.text,
    transition: "background 0.2s",
    marginBottom: 16,
  },

  filterBar: {
    display: "flex",
    gap: 8,
    marginBottom: 16,
    flexWrap: "wrap",
  },
  filterChip: (active) => ({
    padding: "6px 14px",
    borderRadius: 50,
    fontSize: 12,
    fontWeight: 600,
    border: active ? `2px solid ${T.brand}` : `1px solid ${T.border}`,
    background: active ? T.brandLight : T.surface,
    color: active ? T.brandDark : T.textMuted,
    cursor: "pointer",
    transition: "all 0.15s",
  }),
};

// ─── KEYFRAMES ───────────────────────────────────────────────────────────────

const GlobalStyles = () => (
  <style>{`
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,500;0,9..40,700;0,9..40,800;1,9..40,400&display=swap');
    
    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    @keyframes megaIn {
      from { opacity: 0; transform: translateY(-6px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(18px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    @keyframes slideIn {
      from { opacity: 0; transform: translateX(-20px); }
      to { opacity: 1; transform: translateX(0); }
    }

    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: transparent; }
    ::-webkit-scrollbar-thumb { background: #ccc; border-radius: 3px; }
    
    .copa-card:hover {
      box-shadow: ${T.shadowHover} !important;
      transform: translateY(-4px);
    }
    
    .mega-link:hover { color: ${T.brand} !important; }
    
    .explore-card:hover {
      box-shadow: ${T.shadow} !important;
    }
    
    .top-btn:hover { background: rgba(255,255,255,0.3) !important; }
    .ver-mais-btn:hover { transform: scale(1.04); box-shadow: 0 6px 20px rgba(0,0,0,0.18); }
    .back-btn:hover { background: ${T.borderLight} !important; }
    .filter-chip:hover { border-color: ${T.brand} !important; }
  `}</style>
);

// ─── COMPONENTS ──────────────────────────────────────────────────────────────

function Star({ filled }) {
  return (
    <span style={{ color: filled ? "#FFB800" : "#DDD", fontSize: 13 }}>★</span>
  );
}

function RatingStars({ rating }) {
  return (
    <span style={{ display: "inline-flex", gap: 1 }}>
      {[1, 2, 3, 4, 5].map((i) => (
        <Star key={i} filled={i <= Math.round(rating)} />
      ))}
    </span>
  );
}

function ListingCard({ listing, onClick, delay = 0 }) {
  return (
    <div
      className="copa-card"
      style={{ ...styles.card, animation: `fadeUp 0.4s ease ${delay}ms both` }}
      onClick={onClick}
    >
      <div style={styles.cardThumb(listing.hue)}>
        <span>{listing.icon}</span>
        <div style={styles.cardBadge(listing.open)}>
          {listing.open ? "Aberto" : "Fechado"}
        </div>
        {listing.whatsapp && (
          <div style={styles.cardWhatsapp}>
            <span>💬</span> Pedir
          </div>
        )}
      </div>
      <div style={styles.cardBody}>
        <div style={styles.cardName}>{listing.name}</div>
        <div style={styles.cardCat}>
          {listing.category} · {listing.subcategory}
        </div>
        <div style={styles.cardBottom}>
          <div style={styles.cardRating}>
            <RatingStars rating={listing.rating} />
            <span style={{ marginLeft: 2 }}>{listing.rating}</span>
          </div>
          <span style={styles.cardReviews}>{listing.reviews} avaliações</span>
        </div>
        <div style={styles.cardAddress}>📍 {listing.address}</div>
      </div>
    </div>
  );
}

function MiniMap({ listings, hoveredId, onHover, onLeave, mapRef }) {
  const LAT_MIN = -22.983;
  const LAT_MAX = -22.960;
  const LNG_MIN = -43.190;
  const LNG_MAX = -43.175;

  const toX = (lng) => ((lng - LNG_MIN) / (LNG_MAX - LNG_MIN)) * 100;
  const toY = (lat) => ((LAT_MAX - lat) / (LAT_MAX - LAT_MIN)) * 100;

  return (
    <div ref={mapRef} style={{ width: "100%", height: "100%", position: "relative" }}>
      {/* Map background */}
      <svg style={styles.mapSvg} viewBox="0 0 100 100" preserveAspectRatio="none">
        <defs>
          <pattern id="grid" width="5" height="5" patternUnits="userSpaceOnUse">
            <path d="M 5 0 L 0 0 0 5" fill="none" stroke="#d0d8cc" strokeWidth="0.15" />
          </pattern>
          <linearGradient id="ocean" x1="0" y1="0" x2="1" y2="1">
            <stop offset="0%" stopColor="#B8D4E3" />
            <stop offset="100%" stopColor="#A3C4D9" />
          </linearGradient>
        </defs>
        <rect width="100" height="100" fill="url(#ocean)" />
        {/* Copa land mass approximation */}
        <path
          d="M 0,15 Q 20,10 50,18 Q 80,25 100,20 L 100,100 L 0,100 Z"
          fill="#E8EDE4"
        />
        <path
          d="M 0,15 Q 20,10 50,18 Q 80,25 100,20 L 100,100 L 0,100 Z"
          fill="url(#grid)"
        />
        {/* Beach line */}
        <path
          d="M 0,15 Q 20,10 50,18 Q 80,25 100,20"
          fill="none"
          stroke="#F5E6C8"
          strokeWidth="1.5"
        />
        {/* Streets */}
        {[30, 45, 55, 65, 75, 85].map((y) => (
          <line key={`h${y}`} x1="0" y1={y} x2="100" y2={y} stroke="#D5DDD0" strokeWidth="0.3" />
        ))}
        {[15, 30, 45, 60, 75, 90].map((x) => (
          <line key={`v${x}`} x1={x} y1="20" x2={x} y2="100" stroke="#D5DDD0" strokeWidth="0.3" />
        ))}
        {/* Label */}
        <text x="50" y="8" textAnchor="middle" fontSize="3.5" fill="#7A9BBD" fontWeight="600" fontFamily="DM Sans">
          Praia de Copacabana
        </text>
        <text x="50" y="50" textAnchor="middle" fontSize="2.5" fill="#8B9B82" fontWeight="500" fontFamily="DM Sans" opacity="0.6">
          COPACABANA
        </text>
      </svg>
      {/* Pins */}
      {listings.map((l) => {
        const x = toX(l.lng);
        const y = toY(l.lat);
        const isHovered = hoveredId === l.id;
        if (x < 0 || x > 100 || y < 0 || y > 100) return null;
        return (
          <div
            key={l.id}
            onMouseEnter={() => onHover(l.id)}
            onMouseLeave={onLeave}
            style={{
              position: "absolute",
              left: `${x}%`,
              top: `${y}%`,
              transform: isHovered ? "translate(-50%,-100%) scale(1.3)" : "translate(-50%,-100%) scale(1)",
              transition: "transform 0.2s",
              zIndex: isHovered ? 5 : 1,
              cursor: "pointer",
            }}
          >
            <div
              style={{
                width: isHovered ? 30 : 22,
                height: isHovered ? 30 : 22,
                borderRadius: "50% 50% 50% 0",
                background: isHovered ? T.accent : T.brand,
                transform: "rotate(-45deg)",
                display: "flex",
                alignItems: "center",
                justifyContent: "center",
                boxShadow: isHovered ? "0 3px 10px rgba(0,0,0,0.3)" : "0 2px 6px rgba(0,0,0,0.2)",
                transition: "all 0.2s",
              }}
            >
              <span style={{ transform: "rotate(45deg)", fontSize: isHovered ? 13 : 10 }}>{l.icon}</span>
            </div>
            {isHovered && (
              <div
                style={{
                  position: "absolute",
                  bottom: "calc(100% + 8px)",
                  left: "50%",
                  transform: "translateX(-50%)",
                  background: T.surface,
                  padding: "8px 12px",
                  borderRadius: T.radiusSm,
                  boxShadow: T.shadowHover,
                  whiteSpace: "nowrap",
                  fontSize: 12,
                  fontWeight: 600,
                  border: `1px solid ${T.border}`,
                  pointerEvents: "none",
                }}
              >
                <div>{l.name}</div>
                <div style={{ fontSize: 10, color: T.textMuted, fontWeight: 400, marginTop: 2 }}>
                  ⭐ {l.rating} · {l.subcategory}
                </div>
              </div>
            )}
          </div>
        );
      })}
    </div>
  );
}

// ─── MAIN APP ────────────────────────────────────────────────────────────────

export default function CopaCommerce() {
  const [page, setPage] = useState("home"); // "home" | "explore"
  const [activeCat, setActiveCat] = useState(null);
  const [search, setSearch] = useState("");
  const [filterCat, setFilterCat] = useState(null);
  const [hoveredPin, setHoveredPin] = useState(null);
  const [selectedListing, setSelectedListing] = useState(null);
  const catBarRef = useRef(null);
  const megaTimeout = useRef(null);
  const mapRef = useRef(null);

  const handleCatEnter = useCallback((idx) => {
    clearTimeout(megaTimeout.current);
    setActiveCat(idx);
  }, []);

  const handleCatLeave = useCallback(() => {
    megaTimeout.current = setTimeout(() => setActiveCat(null), 200);
  }, []);

  const handleMegaEnter = useCallback(() => {
    clearTimeout(megaTimeout.current);
  }, []);

  const handleMegaLeave = useCallback(() => {
    megaTimeout.current = setTimeout(() => setActiveCat(null), 150);
  }, []);

  const filtered = ALL_LISTINGS.filter((l) => {
    const matchSearch =
      !search ||
      l.name.toLowerCase().includes(search.toLowerCase()) ||
      l.category.toLowerCase().includes(search.toLowerCase()) ||
      l.subcategory.toLowerCase().includes(search.toLowerCase()) ||
      l.address.toLowerCase().includes(search.toLowerCase());
    const matchCat = !filterCat || l.category === filterCat;
    return matchSearch && matchCat;
  });

  const homeListings = filtered.slice(0, 12);

  // ── LISTING DETAIL MODAL ──
  const DetailModal = ({ listing, onClose }) => {
    if (!listing) return null;
    return (
      <div
        onClick={onClose}
        style={{
          position: "fixed",
          inset: 0,
          background: "rgba(0,0,0,0.5)",
          zIndex: 2000,
          display: "flex",
          alignItems: "center",
          justifyContent: "center",
          padding: 24,
        }}
      >
        <div
          onClick={(e) => e.stopPropagation()}
          style={{
            background: T.surface,
            borderRadius: T.radius,
            maxWidth: 480,
            width: "100%",
            overflow: "hidden",
            animation: "fadeUp 0.3s ease",
          }}
        >
          <div style={styles.cardThumb(listing.hue)}>
            <span style={{ fontSize: 72 }}>{listing.icon}</span>
            <div style={styles.cardBadge(listing.open)}>
              {listing.open ? "Aberto agora" : "Fechado"}
            </div>
          </div>
          <div style={{ padding: "24px" }}>
            <h2 style={{ fontSize: 22, fontWeight: 800, marginBottom: 4 }}>{listing.name}</h2>
            <p style={{ fontSize: 13, color: T.textMuted, marginBottom: 16 }}>
              {listing.category} · {listing.subcategory}
            </p>
            <div style={{ display: "flex", alignItems: "center", gap: 8, marginBottom: 16 }}>
              <RatingStars rating={listing.rating} />
              <span style={{ fontSize: 14, fontWeight: 700 }}>{listing.rating}</span>
              <span style={{ fontSize: 12, color: T.textLight }}>({listing.reviews} avaliações)</span>
            </div>
            <p style={{ fontSize: 13, color: T.textMuted, marginBottom: 20 }}>📍 {listing.address}</p>
            <div style={{ display: "flex", gap: 12 }}>
              <button
                style={{
                  flex: 1,
                  background: "#25D366",
                  color: "#fff",
                  border: "none",
                  borderRadius: 50,
                  padding: "12px",
                  fontSize: 14,
                  fontWeight: 700,
                  cursor: "pointer",
                  display: "flex",
                  alignItems: "center",
                  justifyContent: "center",
                  gap: 8,
                }}
              >
                💬 Pedir via WhatsApp
              </button>
              <button
                onClick={onClose}
                style={{
                  background: T.bg,
                  border: `1px solid ${T.border}`,
                  borderRadius: 50,
                  padding: "12px 24px",
                  fontSize: 14,
                  fontWeight: 600,
                  cursor: "pointer",
                  color: T.text,
                }}
              >
                Fechar
              </button>
            </div>
          </div>
        </div>
      </div>
    );
  };

  // ── HOME PAGE ──
  if (page === "home") {
    return (
      <div style={styles.app}>
        <GlobalStyles />

        {/* TOP BAR */}
        <div style={styles.topBar}>
          <div style={styles.topBarInner}>
            <div style={styles.logo} onClick={() => { setPage("home"); setFilterCat(null); setSearch(""); }}>
              <span style={{ fontSize: 26 }}>🏪</span>
              <div>
                <div>CopaCommerce</div>
                <div style={styles.logoSub}>Copacabana · Rio de Janeiro</div>
              </div>
            </div>
            <div style={styles.searchWrap}>
              <input
                style={styles.searchInput}
                placeholder="Buscar estabelecimentos, categorias, endereços..."
                value={search}
                onChange={(e) => setSearch(e.target.value)}
              />
              <span style={styles.searchIcon}>🔍</span>
            </div>
            <div style={styles.topBarActions}>
              <button className="top-btn" style={styles.topBarBtn}>
                📍 Copacabana
              </button>
              <button className="top-btn" style={styles.topBarBtn}>
                Entrar
              </button>
            </div>
          </div>
        </div>

        {/* CATEGORY BAR */}
        <div style={styles.catBar} ref={catBarRef}>
          <div style={styles.catBarInner}>
            {CATEGORIES.map((cat, idx) => (
              <button
                key={cat.name}
                style={styles.catItem(activeCat === idx || filterCat === cat.name)}
                onMouseEnter={() => handleCatEnter(idx)}
                onMouseLeave={handleCatLeave}
                onClick={() => {
                  setFilterCat(filterCat === cat.name ? null : cat.name);
                  setActiveCat(null);
                }}
              >
                <span>{cat.icon}</span>
                {cat.name}
              </button>
            ))}
          </div>

          {/* MEGA DROPDOWN */}
          {activeCat !== null && (
            <div
              style={styles.megaDrop}
              onMouseEnter={handleMegaEnter}
              onMouseLeave={handleMegaLeave}
            >
              <div style={styles.megaInner}>
                {CATEGORIES[activeCat].subs.map((group) => (
                  <div key={group.group} style={styles.megaGroup}>
                    <div style={styles.megaGroupTitle}>{group.group}</div>
                    {group.items.map((item) => (
                      <a
                        key={item}
                        className="mega-link"
                        style={styles.megaLink}
                        onClick={() => {
                          setSearch(item);
                          setFilterCat(CATEGORIES[activeCat].name);
                          setActiveCat(null);
                        }}
                      >
                        {item}
                      </a>
                    ))}
                  </div>
                ))}
              </div>
            </div>
          )}
        </div>

        {activeCat !== null && (
          <div style={styles.megaOverlay} onClick={() => setActiveCat(null)} />
        )}

        {/* BODY */}
        <div style={styles.body}>
          <div style={styles.sectionTitle}>
            {filterCat ? `${filterCat} em Copacabana` : "Descubra Copacabana"}
          </div>
          <div style={styles.sectionSub}>
            {filtered.length} estabelecimentos
            {filterCat ? ` · ` : " mapeados · "}
            {filterCat && (
              <span
                onClick={() => setFilterCat(null)}
                style={{ color: T.brand, cursor: "pointer", fontWeight: 600 }}
              >
                Limpar filtro
              </span>
            )}
            {!filterCat && "Comissão zero · Pedidos via WhatsApp"}
          </div>

          <div style={styles.grid}>
            {homeListings.map((listing, i) => (
              <ListingCard
                key={listing.id}
                listing={listing}
                delay={i * 50}
                onClick={() => setSelectedListing(listing)}
              />
            ))}
          </div>

          {filtered.length > 12 && (
            <div style={styles.verMaisWrap}>
              <button
                className="ver-mais-btn"
                style={styles.verMaisBtn}
                onClick={() => setPage("explore")}
              >
                Ver todos os {filtered.length} estabelecimentos →
              </button>
            </div>
          )}

          {/* BANNER */}
          <div
            style={{
              marginTop: 48,
              background: `linear-gradient(135deg, ${T.brand}, #006B45)`,
              borderRadius: T.radius,
              padding: "36px 40px",
              color: "#fff",
              display: "flex",
              alignItems: "center",
              justifyContent: "space-between",
              gap: 24,
              flexWrap: "wrap",
            }}
          >
            <div>
              <div style={{ fontSize: 20, fontWeight: 800, marginBottom: 6 }}>
                Tem um negócio em Copacabana?
              </div>
              <div style={{ fontSize: 14, opacity: 0.9, maxWidth: 400 }}>
                Cadastre-se gratuitamente. Sem comissões, sem taxas. Seus clientes pedem direto no seu WhatsApp.
              </div>
            </div>
            <button
              style={{
                background: "#fff",
                color: T.brandDark,
                border: "none",
                borderRadius: 50,
                padding: "14px 32px",
                fontSize: 14,
                fontWeight: 700,
                cursor: "pointer",
                flexShrink: 0,
              }}
            >
              Cadastrar meu negócio
            </button>
          </div>
        </div>

        {/* FOOTER */}
        <footer
          style={{
            marginTop: 40,
            borderTop: `1px solid ${T.border}`,
            padding: "32px 24px",
            maxWidth: 1280,
            margin: "40px auto 0",
            display: "flex",
            justifyContent: "space-between",
            flexWrap: "wrap",
            gap: 24,
            fontSize: 13,
            color: T.textMuted,
          }}
        >
          <div>
            <div style={{ fontWeight: 700, color: T.text, marginBottom: 8 }}>CopaCommerce</div>
            <div>Plataforma hiperlocal de Copacabana</div>
            <div style={{ marginTop: 4 }}>Comissão zero · Isonomia · Dados abertos</div>
          </div>
          <div style={{ display: "flex", gap: 32 }}>
            <div>
              <div style={{ fontWeight: 600, color: T.text, marginBottom: 8 }}>Plataforma</div>
              <div>Como funciona</div>
              <div>Para comerciantes</div>
              <div>Dados do bairro</div>
            </div>
            <div>
              <div style={{ fontWeight: 600, color: T.text, marginBottom: 8 }}>Contato</div>
              <div>Instagram</div>
              <div>WhatsApp</div>
              <div>Email</div>
            </div>
          </div>
        </footer>

        <DetailModal listing={selectedListing} onClose={() => setSelectedListing(null)} />
      </div>
    );
  }

  // ── EXPLORE PAGE (VER MAIS) ──
  return (
    <div style={styles.app}>
      <GlobalStyles />

      {/* TOP BAR */}
      <div style={styles.topBar}>
        <div style={styles.topBarInner}>
          <div style={styles.logo} onClick={() => { setPage("home"); setFilterCat(null); setSearch(""); }}>
            <span style={{ fontSize: 26 }}>🏪</span>
            <div>
              <div>CopaCommerce</div>
              <div style={styles.logoSub}>Copacabana · Rio de Janeiro</div>
            </div>
          </div>
          <div style={styles.searchWrap}>
            <input
              style={styles.searchInput}
              placeholder="Buscar estabelecimentos, categorias, endereços..."
              value={search}
              onChange={(e) => setSearch(e.target.value)}
            />
            <span style={styles.searchIcon}>🔍</span>
          </div>
          <div style={styles.topBarActions}>
            <button className="top-btn" style={styles.topBarBtn}>
              📍 Copacabana
            </button>
          </div>
        </div>
      </div>

      {/* SPLIT VIEW */}
      <div style={styles.exploreContainer}>
        {/* LEFT: LISTING LIST */}
        <div style={styles.exploreList}>
          <button
            className="back-btn"
            style={styles.backBtn}
            onClick={() => setPage("home")}
          >
            ← Voltar
          </button>

          <h2 style={{ fontSize: 20, fontWeight: 800, marginBottom: 4 }}>
            {filterCat || "Todos os"} estabelecimentos
          </h2>
          <p style={{ fontSize: 13, color: T.textMuted, marginBottom: 16 }}>
            {filtered.length} resultados em Copacabana
          </p>

          {/* Category filter chips */}
          <div style={styles.filterBar}>
            <button
              className="filter-chip"
              style={styles.filterChip(!filterCat)}
              onClick={() => setFilterCat(null)}
            >
              Todos
            </button>
            {CATEGORIES.map((c) => (
              <button
                key={c.name}
                className="filter-chip"
                style={styles.filterChip(filterCat === c.name)}
                onClick={() => setFilterCat(filterCat === c.name ? null : c.name)}
              >
                {c.icon} {c.name}
              </button>
            ))}
          </div>

          {/* Listing rows */}
          {filtered.map((listing, i) => (
            <div
              key={listing.id}
              className="explore-card"
              style={{
                ...styles.exploreCard,
                animation: `slideIn 0.3s ease ${i * 30}ms both`,
                borderLeft: hoveredPin === listing.id ? `3px solid ${T.accent}` : "3px solid transparent",
              }}
              onMouseEnter={() => setHoveredPin(listing.id)}
              onMouseLeave={() => setHoveredPin(null)}
              onClick={() => setSelectedListing(listing)}
            >
              <div style={styles.exploreCardThumb(listing.hue)}>
                <span>{listing.icon}</span>
              </div>
              <div style={styles.exploreCardBody}>
                <div style={{ fontSize: 14, fontWeight: 700, marginBottom: 2 }}>{listing.name}</div>
                <div style={{ fontSize: 12, color: T.textMuted, marginBottom: 4 }}>
                  {listing.category} · {listing.subcategory}
                </div>
                <div style={{ display: "flex", alignItems: "center", gap: 6, fontSize: 12 }}>
                  <RatingStars rating={listing.rating} />
                  <span style={{ fontWeight: 600 }}>{listing.rating}</span>
                  <span style={{ color: T.textLight }}>({listing.reviews})</span>
                  <span
                    style={{
                      marginLeft: "auto",
                      fontSize: 10.5,
                      fontWeight: 600,
                      color: listing.open ? T.brand : "#C44",
                    }}
                  >
                    {listing.open ? "● Aberto" : "● Fechado"}
                  </span>
                </div>
                <div style={{ fontSize: 11, color: T.textLight, marginTop: 4 }}>📍 {listing.address}</div>
              </div>
            </div>
          ))}
        </div>

        {/* RIGHT: MAP */}
        <div style={styles.exploreMap}>
          <MiniMap
            listings={filtered}
            hoveredId={hoveredPin}
            onHover={setHoveredPin}
            onLeave={() => setHoveredPin(null)}
            mapRef={mapRef}
          />
          {/* Map overlay info */}
          <div
            style={{
              position: "absolute",
              bottom: 16,
              left: 16,
              background: "rgba(255,255,255,0.95)",
              borderRadius: T.radiusSm,
              padding: "10px 16px",
              fontSize: 12,
              color: T.textMuted,
              boxShadow: T.shadow,
              backdropFilter: "blur(8px)",
            }}
          >
            <span style={{ fontWeight: 700, color: T.text }}>{filtered.length}</span> estabelecimentos no mapa
            · Copacabana, RJ
          </div>
        </div>
      </div>

      <DetailModal listing={selectedListing} onClose={() => setSelectedListing(null)} />
    </div>
  );
}
