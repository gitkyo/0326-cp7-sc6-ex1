# Exercice Bootstrap : Créez votre portfolio de designer avec charte graphique

## Objectif pédagogique
Créer une page web portfolio professionnelle en utilisant Bootstrap et CSS personnalisé, en appliquant les principes de design et de charte graphique que vous connaissez déjà.

## Philosophie de travail
À chaque étape, respectez cette démarche :
1. **LIRE** le code avant de le copier
2. **COMPRENDRE** ce que fait chaque partie
3. **TESTER** chaque étape dans votre navigateur
4. **EXPÉRIMENTER** en modifiant des valeurs
5. **QUESTIONNER** tout ce qui n'est pas clair
6. **PARTAGER** vos découvertes avec les autres

---

## 🎨 Étape préliminaire : Définir votre charte graphique

### 🎯 Consignes
Avant de coder, définissons votre identité visuelle comme vous le feriez pour un client.

### 📋 Charte graphique à définir
1. **Couleurs principales** : 
   - Couleur primaire (votre couleur signature)
   - Couleur secondaire (couleur complémentaire)
   - Couleur d'accent (pour les CTA et highlights)
   - Couleurs neutres (gris, blanc cassé)

2. **Typographie** :
   - Police pour les titres (impact, lisibilité)
   - Police pour le texte courant (lisibilité, confort de lecture)

3. **Style visuel** :
   - Moderne et épuré / Créatif et artistique / Corporate et professionnel
   - Utilisation d'ombres, bordures arrondies, effets de survol

### 📖 Code CSS à créer (fichier `style.css`)
```css
/* === CHARTE GRAPHIQUE & DESIGN SYSTEM === */
/* Import des polices Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Poppins:wght@400;500;600;700&display=swap');

:root {
  /* === COULEURS === */
  /* Couleurs principales */
  --color-primary: #2C3E50;        /* Bleu ardoise élégant */
  --color-secondary: #E67E22;      /* Orange moderne */
  --color-accent: #F39C12;         /* Jaune doré */
  
  /* Couleurs neutres */
  --color-light: #F8F9FA;          /* Gris très clair */
  --color-white: #FFFFFF;          /* Blanc pur */
  --color-dark: #2C3E50;           /* Texte sombre */
  --color-muted: #6C757D;          /* Gris moyen */
  
  /* Couleurs supplémentaires */
  --color-success: #27AE60;        /* Vert succès */
  --color-warning: #F39C12;        /* Orange attention */
  --color-danger: #E74C3C;         /* Rouge erreur */
  --color-info: #3498DB;           /* Bleu information */
  
  /* === TYPOGRAPHIE === */
  --font-heading: 'Poppins', sans-serif;     /* Police moderne pour titres */
  --font-body: 'Inter', sans-serif;          /* Police lisible pour texte */
  
  /* Tailles de police */
  --font-size-xs: 0.75rem;         /* 12px */
  --font-size-sm: 0.875rem;        /* 14px */
  --font-size-base: 1rem;          /* 16px */
  --font-size-lg: 1.125rem;        /* 18px */
  --font-size-xl: 1.25rem;         /* 20px */
  --font-size-2xl: 1.5rem;         /* 24px */
  --font-size-3xl: 1.875rem;       /* 30px */
  --font-size-4xl: 2.25rem;        /* 36px */
  
  /* === ESPACEMENTS & DIMENSIONS === */
  --spacing-xs: 0.25rem;           /* 4px */
  --spacing-sm: 0.5rem;            /* 8px */
  --spacing-md: 1rem;              /* 16px */
  --spacing-lg: 1.5rem;            /* 24px */
  --spacing-xl: 2rem;              /* 32px */
  --spacing-2xl: 3rem;             /* 48px */
  --spacing-3xl: 4rem;             /* 64px */
  
  /* Rayons de bordure */
  --border-radius-sm: 0.375rem;    /* 6px */
  --border-radius: 0.75rem;        /* 12px */
  --border-radius-lg: 1rem;        /* 16px */
  --border-radius-xl: 1.5rem;      /* 24px */
  --border-radius-full: 9999px;    /* Cercle parfait */
  
  /* === OMBRES === */
  --shadow-sm: 0 1px 3px rgba(0,0,0,0.1);
  --shadow-light: 0 2px 10px rgba(0,0,0,0.1);
  --shadow-medium: 0 4px 20px rgba(0,0,0,0.15);
  --shadow-large: 0 10px 40px rgba(0,0,0,0.2);
  
  /* === TRANSITIONS === */
  --transition-fast: all 0.15s ease-in-out;
  --transition-smooth: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  --transition-slow: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
}

/* === STYLES DE BASE === */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: var(--font-body);
  font-size: var(--font-size-base);
  line-height: 1.6;
  color: var(--color-dark);
  background-color: var(--color-white);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

/* Typographie globale */
h1, h2, h3, h4, h5, h6 {
  font-family: var(--font-heading);
  font-weight: 600;
  line-height: 1.2;
  margin-bottom: var(--spacing-md);
}

h1 { font-size: var(--font-size-4xl); }
h2 { font-size: var(--font-size-3xl); }
h3 { font-size: var(--font-size-2xl); }
h4 { font-size: var(--font-size-xl); }
h5 { font-size: var(--font-size-lg); }
h6 { font-size: var(--font-size-base); font-weight: 600; }

p {
  margin-bottom: var(--spacing-md);
}

a {
  color: var(--color-primary);
  text-decoration: none;
  transition: var(--transition-smooth);
}

a:hover {
  color: var(--color-secondary);
}
```

### 🤔 Questions de réflexion design
1. **ANALYSER** : Quelles émotions vos couleurs choisies transmettent-elles ?
2. **COMPRENDRE** : Pourquoi utiliser des variables CSS plutôt que des couleurs en dur ?
3. **QUESTIONNER** : Comment votre charte graphique reflète-t-elle votre personnalité de designer ?
4. **EXPÉRIMENTER** : Testez différentes combinaisons de couleurs avec des outils comme Coolors.co

---

## Étape 1 : Structure HTML avec intégration CSS

### 🎯 Consignes
1. Créez un nouveau dossier pour votre projet
2. Créez `index.html` et `style.css`
3. Intégrez Bootstrap ET votre CSS personnalisé
### 🎯 Consignes
1. Créez un nouveau dossier pour votre projet (ex: `mon-portfolio`)
2. Créez un fichier `index.html` dans ce dossier
3. Ouvrez le fichier dans votre éditeur de code

### 📖 Code HTML à créer (`index.html`)
```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio | Votre Nom</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Bootstrap Icons -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.0/font/bootstrap-icons.css">
    <!-- Notre CSS personnalisé -->
    <link href="style.css" rel="stylesheet">
</head>
<body>
    <!-- Navigation fixe -->
    <nav class="navbar navbar-expand-lg navbar-dark fixed-top custom-navbar">
        <div class="container">
            <a class="navbar-brand fw-bold" href="#"><i class="bi bi-palette me-2"></i>Portfolio</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#accueil">Accueil</a></li>
                    <li class="nav-item"><a class="nav-link" href="#apropos">À propos</a></li>
                    <li class="nav-item"><a class="nav-link" href="#projets">Projets</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

### 🎨 CSS pour la navigation (ajout à `style.css`)
```css
/* === NAVIGATION === */
.custom-navbar {
  background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
  backdrop-filter: blur(10px);
  box-shadow: var(--shadow-light);
  transition: var(--transition-smooth);
  padding: var(--spacing-md) 0;
}

.custom-navbar.scrolled {
  background: rgba(44, 62, 80, 0.95);
  backdrop-filter: blur(20px);
}

.navbar-brand {
  font-family: var(--font-heading);
  font-size: var(--font-size-xl);
  font-weight: 700;
  color: white !important;
  text-decoration: none;
}

.nav-link {
  font-weight: 500;
  font-size: var(--font-size-sm);
  color: rgba(255,255,255,0.9) !important;
  transition: var(--transition-smooth);
  text-transform: uppercase;
  letter-spacing: 0.5px;
  position: relative;
}

.nav-link:hover,
.nav-link.active {
  color: var(--color-accent) !important;
  transform: translateY(-1px);
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 50%;
  width: 0;
  height: 2px;
  background: var(--color-accent);
  transition: var(--transition-smooth);
  transform: translateX(-50%);
}

.nav-link:hover::after,
.nav-link.active::after {
  width: 100%;
}
```

### 🤔 Questions de réflexion
1. **COMPRENDRE** : Pourquoi utiliser une navigation fixe (`fixed-top`) ?
2. **ANALYSER** : Comment le gradient crée-t-il un impact visuel ?
3. **TESTER** : Redimensionnez la fenêtre pour voir le menu responsive
4. **EXPÉRIMENTER** : Changez les couleurs du gradient

---

## Étape 2 : Section Hero avec slider (carousel Bootstrap)

### 🎯 Consignes
Créez une section d'accueil impactante avec un carousel pour présenter votre travail.

### 📖 Code HTML à ajouter (dans le `<body>`, après la navigation)
```html
<!-- Section Hero avec Carousel -->
<section id="accueil" class="hero-section">
    <div id="heroCarousel" class="carousel slide" data-bs-ride="carousel" data-bs-interval="5000">
        <div class="carousel-indicators">
            <button type="button" data-bs-target="#heroCarousel" data-bs-slide-to="0" class="active"></button>
            <button type="button" data-bs-target="#heroCarousel" data-bs-slide-to="1"></button>
            <button type="button" data-bs-target="#heroCarousel" data-bs-slide-to="2"></button>
        </div>
        
        <div class="carousel-inner">
            <!-- Slide 1 - Présentation -->
            <div class="carousel-item active">
                <div class="hero-slide" style="background: linear-gradient(135deg, rgba(44,62,80,0.8), rgba(230,126,34,0.7)), url('https://images.unsplash.com/photo-1586953208448-b95a79798f07?auto=format&fit=crop&w=1920&h=1080&q=80'); background-size: cover; background-position: center;">
                    <div class="container h-100">
                        <div class="row h-100 align-items-center">
                            <div class="col-lg-8 text-white">
                                <h1 class="display-3 fw-bold mb-4">Votre Nom</h1>
                                <p class="lead mb-4">Designer UI/UX passionné par la création d'expériences digitales exceptionnelles</p>
                                <a href="#projets" class="btn btn-accent btn-lg me-3">Voir mes projets</a>
                                <a href="#contact" class="btn btn-outline-light btn-lg">Me contacter</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Slide 2 - Compétences -->
            <div class="carousel-item">
                <div class="hero-slide" style="background: linear-gradient(135deg, rgba(230,126,34,0.8), rgba(243,156,18,0.7)), url('https://images.unsplash.com/photo-1586717791821-3f44a563fa4c?auto=format&fit=crop&w=1920&h=1080&q=80'); background-size: cover; background-position: center;">
                    <div class="container h-100">
                        <div class="row h-100 align-items-center">
                            <div class="col-lg-8 text-white">
                                <h2 class="display-4 fw-bold mb-4">Mes Compétences</h2>
                                <div class="row">
                                    <div class="col-md-6">
                                        <p><i class="bi bi-palette me-2"></i> Design UI/UX</p>
                                        <p><i class="bi bi-code-slash me-2"></i> HTML/CSS/JS</p>
                                        <p><i class="bi bi-bootstrap me-2"></i> Bootstrap & Frameworks</p>
                                    </div>
                                    <div class="col-md-6">
                                        <p><i class="bi bi-brush me-2"></i> Adobe Creative Suite</p>
                                        <p><i class="bi bi-phone me-2"></i> Design Responsive</p>
                                        <p><i class="bi bi-eye me-2"></i> Prototypage</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Slide 3 - Philosophie -->
            <div class="carousel-item">
                <div class="hero-slide" style="background: linear-gradient(135deg, rgba(243,156,18,0.8), rgba(44,62,80,0.7)), url('https://images.unsplash.com/photo-1581291518857-4e27b48ff24e?auto=format&fit=crop&w=1920&h=1080&q=80'); background-size: cover; background-position: center;">
                    <div class="container h-100">
                        <div class="row h-100 align-items-center">
                            <div class="col-lg-8 text-white">
                                <h2 class="display-4 fw-bold mb-4">Ma Philosophie</h2>
                                <blockquote class="blockquote">
                                    <p class="mb-4">"Le design n'est pas seulement à quoi ça ressemble. Le design, c'est comment ça fonctionne."</p>
                                    <footer class="blockquote-footer text-light">Steve Jobs</footer>
                                </blockquote>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Contrôles du carousel -->
        <button class="carousel-control-prev" type="button" data-bs-target="#heroCarousel" data-bs-slide="prev">
            <span class="carousel-control-prev-icon"></span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#heroCarousel" data-bs-slide="next">
            <span class="carousel-control-next-icon"></span>
        </button>
    </div>
</section>
```

### 🎨 CSS pour le Hero (ajout à `style.css`)
```css
/* === ÉLÉMENTS GÉNÉRAUX === */
.section-subtitle {
  color: var(--color-secondary);
  font-weight: 600;
  font-size: var(--font-size-sm);
  text-transform: uppercase;
  letter-spacing: 1px;
  display: block;
  margin-bottom: var(--spacing-sm);
}

.section-title {
  font-family: var(--font-heading);
  font-size: var(--font-size-4xl);
  font-weight: 700;
  color: var(--color-dark);
  margin-bottom: var(--spacing-lg);
  position: relative;
}

.section-title::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 80px;
  height: 4px;
  background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
  border-radius: var(--border-radius-full);
}

/* === SECTION HERO === */
.hero-section {
  margin-top: 76px; /* Compensation navbar fixe */
  height: 100vh;
  min-height: 600px;
}

.hero-slide {
  height: 100vh;
  min-height: 600px;
  display: flex;
  align-items: center;
  position: relative;
  background-attachment: fixed;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.hero-slide::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0,0,0,0.2);
  z-index: 1;
}

.hero-slide .container {
  position: relative;
  z-index: 2;
}

.hero-slide h1 {
  font-size: clamp(2.5rem, 5vw, 4rem);
  margin-bottom: var(--spacing-lg);
  text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
}

.hero-slide .lead {
  font-size: var(--font-size-xl);
  margin-bottom: var(--spacing-2xl);
  text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
  color: rgba(255,255,255,0.9);
}

/* Boutons personnalisés */
.btn-accent {
  background: linear-gradient(135deg, var(--color-accent), #e67e22);
  border: none;
  color: white;
  font-weight: 600;
  padding: var(--spacing-md) var(--spacing-xl);
  border-radius: var(--border-radius);
  font-size: var(--font-size-base);
  transition: var(--transition-smooth);
  text-transform: uppercase;
  letter-spacing: 0.5px;
  text-decoration: none;
  display: inline-block;
}

.btn-accent:hover {
  background: linear-gradient(135deg, #e67e22, var(--color-accent));
  transform: translateY(-3px);
  box-shadow: var(--shadow-large);
  color: white;
}

/* Indicateurs du carousel */
.carousel-indicators [data-bs-target] {
  background-color: var(--color-accent);
  border-radius: 50%;
  width: 12px;
  height: 12px;
  margin: 0 5px;
  opacity: 0.6;
  transition: var(--transition-smooth);
}

.carousel-indicators [data-bs-target].active {
  opacity: 1;
  transform: scale(1.2);
}
```

### 🤔 Questions de réflexion design
1. **ANALYSER** : Comment les gradients créent-ils une hiérarchie visuelle ?
2. **COMPRENDRE** : Pourquoi utiliser `z-index` et un overlay sombre ?
3. **TESTER** : Les transitions automatiques du carousel fonctionnent-elles ?
4. **EXPÉRIMENTER** : Changez les durées de transition, les images d'unsplash
5. **QUESTIONNER** : L'accessibilité du carousel est-elle respectée ?
6. **OBSERVER** : Comment les images de fond Unsplash renforcent-elles le message de chaque slide ?

Les slides utilisent maintenant des images de fond professionnelles d'Unsplash pour créer un impact visuel plus fort.
Cette technique combine **gradient overlay** + **image de fond** pour maintenir la lisibilité du texte.

---

## Étape 3 : Section "À propos" avec design card moderne
### 🎯 Consignes
Créez une section "À propos" avec des éléments design modernes et du contenu structuré.

### 📖 Code HTML à ajouter (après la section Hero)
```html
<!-- Section À propos -->
<section id="apropos" class="py-5">
    <div class="container">
        <div class="row align-items-center">
            <div class="col-lg-5 mb-4 mb-lg-0">
                <div class="about-image-wrapper">
                    <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?auto=format&fit=crop&w=400&h=500&q=80" 
                         class="img-fluid about-image" alt="Photo professionnelle - Designer créative">
                    <div class="image-decoration"></div>
                </div>
            </div>
            <div class="col-lg-7">
                <div class="about-content">
                    <span class="section-subtitle">Découvrez</span>
                    <h2 class="section-title mb-4">À propos de moi</h2>
                    <p class="lead mb-4">Designer passionné avec une approche centrée sur l'utilisateur, 
                       je transforme des idées complexes en expériences digitales intuitives et esthétiques.</p>
                    
                    <div class="row mb-4">
                        <div class="col-sm-6">
                            <div class="skill-item">
                                <i class="bi bi-palette skill-icon"></i>
                                <h5>Design UI/UX</h5>
                                <p>Création d'interfaces modernes et ergonomiques</p>
                            </div>
                        </div>
                        <div class="col-sm-6">
                            <div class="skill-item">
                                <i class="bi bi-code-slash skill-icon"></i>
                                <h5>Développement Front-end</h5>
                                <p>HTML, CSS, JavaScript et frameworks modernes</p>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Bouton Modal pour CV -->
                    <button type="button" class="btn btn-primary btn-lg me-3" data-bs-toggle="modal" data-bs-target="#cvModal">
                        <i class="bi bi-download me-2"></i>Voir mon CV
                    </button>
                    <a href="#contact" class="btn btn-outline-primary btn-lg">Me contacter</a>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Modal CV -->
<div class="modal fade" id="cvModal" tabindex="-1" aria-labelledby="cvModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-lg">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="cvModalLabel"><i class="bi bi-person-lines-fill me-2"></i>Mon CV</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Fermer"></button>
            </div>
            <div class="modal-body">
                <div class="row">
                    <div class="col-md-6">
                        <h6 class="text-primary mb-3"><i class="bi bi-briefcase me-2"></i>Expérience</h6>
                        <div class="timeline-item mb-3">
                            <strong>Designer UI Junior</strong><br>
                            <small class="text-muted">2023 - Aujourd'hui | Agence Créative</small>
                            <p class="mt-2 small">Conception d'interfaces web et mobile, prototypage, tests utilisateurs.</p>
                        </div>
                        <div class="timeline-item mb-3">
                            <strong>Stage Design</strong><br>
                            <small class="text-muted">2023 | Startup Tech</small>
                            <p class="mt-2 small">Refonte de l'application mobile, amélioration UX.</p>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <h6 class="text-primary mb-3"><i class="bi bi-mortarboard me-2"></i>Formation</h6>
                        <div class="timeline-item mb-3">
                            <strong>Formation Designer UI</strong><br>
                            <small class="text-muted">2022-2023 | École de Design</small>
                            <p class="mt-2 small">Spécialisation en design d'interfaces et expérience utilisateur.</p>
                        </div>
                        <div class="timeline-item mb-3">
                            <strong>BTS Design Graphique</strong><br>
                            <small class="text-muted">2020-2022 | Lycée Arts Appliqués</small>
                            <p class="mt-2 small">Fondamentaux du design, typographie, identité visuelle.</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="modal-footer">
                <a href="#" class="btn btn-primary"><i class="bi bi-download me-2"></i>Télécharger PDF</a>
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Fermer</button>
            </div>
        </div>
    </div>
</div>
```

### 🎨 CSS pour la section À propos (ajout à `style.css`)
```css
/* === SECTION À PROPOS === */
#apropos {
  background: linear-gradient(135deg, var(--color-light) 0%, #e9ecef 100%);
  position: relative;
}

#apropos::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="1" fill="%23000" opacity="0.02"/><circle cx="75" cy="75" r="1" fill="%23000" opacity="0.02"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
  opacity: 0.3;
  z-index: 1;
}

#apropos .container {
  position: relative;
  z-index: 2;
}

.about-image-wrapper {
  position: relative;
  max-width: 400px;
  margin: 0 auto;
}

.about-image {
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-medium);
  position: relative;
  z-index: 2;
  width: 100%;
  height: auto;
}

.image-decoration {
  position: absolute;
  top: -20px;
  left: -20px;
  width: calc(100% + 20px);
  height: calc(100% + 20px);
  background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
  border-radius: var(--border-radius-lg);
  z-index: 1;
  opacity: 0.8;
  transform: rotate(-2deg);
}

.skill-item {
  text-align: center;
  padding: var(--spacing-xl);
  background: white;
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-light);
  transition: var(--transition-smooth);
  height: 100%;
  border: 1px solid rgba(0,0,0,0.05);
}

.skill-item:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-medium);
  border-color: var(--color-primary);
}

.skill-icon {
  font-size: 3rem;
  color: var(--color-primary);
  margin-bottom: var(--spacing-md);
  display: block;
}

.skill-item h5 {
  color: var(--color-dark);
  font-weight: 600;
  margin-bottom: var(--spacing-sm);
}

.skill-item p {
  color: var(--color-muted);
  font-size: var(--font-size-sm);
  margin: 0;
}

/* === MODAL CV === */
.modal-content {
  border-radius: var(--border-radius-lg);
  border: none;
  box-shadow: var(--shadow-large);
}

.modal-header {
  background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
  color: white;
  border-radius: var(--border-radius-lg) var(--border-radius-lg) 0 0;
  border-bottom: none;
}

.modal-header .btn-close {
  filter: invert(1);
}

.timeline-item {
  padding-left: var(--spacing-lg);
  border-left: 3px solid var(--color-primary);
  position: relative;
  margin-bottom: var(--spacing-lg);
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: -6px;
  top: 5px;
  width: 10px;
  height: 10px;
  background: var(--color-secondary);
  border-radius: 50%;
}

.timeline-item:last-child {
  margin-bottom: 0;
}
```

### 🤔 Questions de réflexion design
1. **ANALYSER** : Comment la décoration d'image crée-t-elle de la profondeur ?
2. **COMPRENDRE** : Pourquoi utiliser une modale pour le CV plutôt qu'une nouvelle page ?
3. **TESTER** : Les animations hover sur les skill-items fonctionnent-elles ?
4. **EXPÉRIMENTER** : Modifiez les couleurs du gradient de fond, l'image de profil. Vous pouvez personaliser l'image de profil
5. **QUESTIONNER** : L'accessibilité de la modale est-elle respectée ?

### 🤔 Questions de réflexion technique
1. **LIRE** : Que signifient `col-md-4` et `col-md-8` ?
2. **COMPRENDRE** : Pourquoi `align-items-center` sur la `row` ?
3. **TESTER** : Redimensionnez la fenêtre. Comment se comporte la grille ?
4. **EXPÉRIMENTER** : Changez `col-md-4` en `col-lg-4`. Quelle différence ?
5. **QUESTIONNER** : Pourquoi utiliser `img-fluid` sur l'image ?

---

## Étape 4 : Galerie de projets avec modales interactives

### 🎯 Consignes
Créez une section projets avec des cartes interactives et des modales détaillées pour chaque projet.

### 📖 Code HTML pour la section projets
```html
<!-- Section Projets -->
<section id="projets" class="py-5">
    <div class="container">
        <div class="text-center mb-5">
            <span class="section-subtitle">Portfolio</span>
            <h2 class="section-title">Mes Réalisations</h2>
            <p class="lead">Découvrez une sélection de mes projets les plus représentatifs</p>
        </div>
        
        <div class="row g-4">
            <!-- Projet 1 -->
            <div class="col-lg-4 col-md-6">
                <div class="project-card" data-bs-toggle="modal" data-bs-target="#projectModal1">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&h=300&q=80" 
                                class="img-fluid" alt="Application mobile - Interface bancaire moderne">
                        <div class="project-overlay">
                            <div class="project-info">
                                <h5 class="text-white mb-2">Application Mobile Banking</h5>
                                <p class="text-white-50 mb-3">UI/UX Design • Figma</p>
                                <button class="btn btn-outline-light btn-sm">
                                    <i class="bi bi-eye me-2"></i>Voir détails
                                </button>
                            </div>
                        </div>
                    </div>
                    <div class="project-content">
                        <div class="d-flex justify-content-between align-items-center">
                            <span class="badge bg-primary">Mobile App</span>
                            <small class="text-muted">2024</small>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Projet 2 -->
            <div class="col-lg-4 col-md-6">
                <div class="project-card" data-bs-toggle="modal" data-bs-target="#projectModal2">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&h=300&q=80" 
                                class="img-fluid" alt="Site e-commerce - Dashboard analytics">
                        <div class="project-overlay">
                            <div class="project-info">
                                <h5 class="text-white mb-2">Site E-commerce</h5>
                                <p class="text-white-50 mb-3">Web Design • Bootstrap</p>
                                <button class="btn btn-outline-light btn-sm">
                                    <i class="bi bi-eye me-2"></i>Voir détails
                                </button>
                            </div>
                        </div>
                    </div>
                    <div class="project-content">
                        <div class="d-flex justify-content-between align-items-center">
                            <span class="badge bg-warning text-dark">Web Design</span>
                            <small class="text-muted">2024</small>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Projet 3 -->
            <div class="col-lg-4 col-md-6">
                <div class="project-card" data-bs-toggle="modal" data-bs-target="#projectModal3">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1558655146-9f40138edfeb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&h=300&q=80" 
                                class="img-fluid" alt="Identité visuelle - Design graphique créatif">
                        <div class="project-overlay">
                            <div class="project-info">
                                <h5 class="text-white mb-2">Identité Visuelle</h5>
                                <p class="text-white-50 mb-3">Branding • Illustrator</p>
                                <button class="btn btn-outline-light btn-sm">
                                    <i class="bi bi-eye me-2"></i>Voir détails
                                </button>
                            </div>
                        </div>
                    </div>
                    <div class="project-content">
                        <div class="d-flex justify-content-between align-items-center">
                            <span class="badge bg-success">Branding</span>
                            <small class="text-muted">2023</small>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Modal Projets (exemple pour Projet 1) -->
<div class="modal fade" id="projectModal1" tabindex="-1" aria-hidden="true">
    <div class="modal-dialog modal-xl">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Application Mobile Banking</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <div class="row">
                    <div class="col-md-8">
                        <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&h=600&q=80" 
                             class="img-fluid rounded mb-3" alt="Mockups application mobile - Interface utilisateur moderne">
                    </div>
                    <div class="col-md-4">
                        <h6 class="text-primary mb-3">Détails du projet</h6>
                        <p><strong>Client :</strong> FinanceApp Startup</p>
                        <p><strong>Durée :</strong> 3 mois</p>
                        <p><strong>Outils :</strong> Figma, Sketch, InVision</p>
                        <p><strong>Équipe :</strong> 1 Designer, 2 Développeurs</p>
                        
                        <h6 class="text-primary mb-3 mt-4">Problématique</h6>
                        <p>Créer une interface intuitive pour une application bancaire mobile, 
                           en respectant les contraintes de sécurité et d'accessibilité.</p>
                        
                        <h6 class="text-primary mb-3">Solution</h6>
                        <p>Design épuré avec navigation simplifiée et système de couleurs 
                           rassurant. Tests utilisateurs itératifs.</p>
                    </div>
                </div>
            </div>
            <div class="modal-footer">
                <a href="#" class="btn btn-primary">Voir prototype</a>
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Fermer</button>
            </div>
        </div>
    </div>
</div>

<!-- Modal Projet 2 - Site E-commerce -->
<div class="modal fade" id="projectModal2" tabindex="-1" aria-hidden="true">
    <div class="modal-dialog modal-xl">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Site E-commerce</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <div class="row">
                    <div class="col-md-8">
                        <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&h=600&q=80" 
                             class="img-fluid rounded mb-3" alt="Site e-commerce - Interface dashboard analytics moderne">
                    </div>
                    <div class="col-md-4">
                        <h6 class="text-primary mb-3">Détails du projet</h6>
                        <p><strong>Client :</strong> ShopTech Solutions</p>
                        <p><strong>Durée :</strong> 4 mois</p>
                        <p><strong>Outils :</strong> Bootstrap, CSS3, JavaScript</p>
                        <p><strong>Équipe :</strong> 2 Designers, 3 Développeurs</p>
                        
                        <h6 class="text-primary mb-3 mt-4">Problématique</h6>
                        <p>Refonte complète d'un site e-commerce existant pour améliorer 
                           l'expérience utilisateur et augmenter les conversions.</p>
                        
                        <h6 class="text-primary mb-3">Solution</h6>
                        <p>Design responsive moderne avec focus sur la performance 
                           et l'optimisation du parcours d'achat.</p>
                    </div>
                </div>
            </div>
            <div class="modal-footer">
                <a href="#" class="btn btn-primary">Voir le site</a>
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Fermer</button>
            </div>
        </div>
    </div>
</div>

<!-- Modal Projet 3 - Identité Visuelle -->
<div class="modal fade" id="projectModal3" tabindex="-1" aria-hidden="true">
    <div class="modal-dialog modal-xl">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Identité Visuelle</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <div class="row">
                    <div class="col-md-8">
                        <img src="https://images.unsplash.com/photo-1558655146-9f40138edfeb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&h=600&q=80" 
                             class="img-fluid rounded mb-3" alt="Identité visuelle - Éléments graphiques créatifs et logo design">
                    </div>
                    <div class="col-md-4">
                        <h6 class="text-primary mb-3">Détails du projet</h6>
                        <p><strong>Client :</strong> Creative Agency</p>
                        <p><strong>Durée :</strong> 2 mois</p>
                        <p><strong>Outils :</strong> Illustrator, Photoshop, InDesign</p>
                        <p><strong>Équipe :</strong> 1 Designer, 1 Directeur artistique</p>
                        
                        <h6 class="text-primary mb-3 mt-4">Problématique</h6>
                        <p>Création d'une identité visuelle complète pour une nouvelle 
                           agence créative, incluant logo, charte graphique et supports.</p>
                        
                        <h6 class="text-primary mb-3">Solution</h6>
                        <p>Design moderne et polyvalent reflétant l'esprit créatif 
                           de l'agence avec une approche minimaliste mais impactante.</p>
                    </div>
                </div>
            </div>
            <div class="modal-footer">
                <a href="#" class="btn btn-primary">Voir la charte</a>
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Fermer</button>
            </div>
        </div>
    </div>
</div>
```

### 🎨 CSS pour la section projets (ajout à `style.css`)
```css
/* === SECTION PROJETS === */
#projets {
  background: white;
  position: relative;
}

.project-card {
  background: white;
  border-radius: var(--border-radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow-light);
  transition: var(--transition-smooth);
  cursor: pointer;
  height: 100%;
  border: 1px solid rgba(0,0,0,0.05);
}

.project-card:hover {
  transform: translateY(-10px);
  box-shadow: var(--shadow-large);
}

.project-image {
  position: relative;
  overflow: hidden;
  height: 250px;
  background: var(--color-light);
}

.project-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: var(--transition-smooth);
}

.project-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(135deg, rgba(44,62,80,0.95), rgba(230,126,34,0.9));
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: var(--transition-smooth);
  backdrop-filter: blur(2px);
}

.project-card:hover .project-overlay {
  opacity: 1;
}

.project-card:hover .project-image img {
  transform: scale(1.1);
}

.project-info {
  text-align: center;
  padding: var(--spacing-xl);
}

.project-info h5 {
  font-size: var(--font-size-xl);
  margin-bottom: var(--spacing-sm);
}

.project-info p {
  margin-bottom: var(--spacing-lg);
}

.project-content {
  padding: var(--spacing-lg);
}

/* Badges personnalisés */
.badge {
  font-size: var(--font-size-xs);
  font-weight: 600;
  padding: var(--spacing-sm) var(--spacing-md);
  border-radius: var(--border-radius-full);
  text-transform: uppercase;
  letter-spacing: 0.5px;
}
```

### 🤔 Questions de réflexion design
1. **ANALYSER** : Comment l'effet hover améliore-t-il l'expérience utilisateur ?
2. **COMPRENDRE** : Pourquoi utiliser des modales plutôt qu'une page séparée ?
3. **QUESTIONNER** : Comment optimiser les performances avec ces images ?
4. **EXPÉRIMENTER** : Testez d'autres images d'Unsplash pour vos projets

### 🤔 Questions de réflexion technique
1. **LIRE** : Que fait la classe `h-100` sur les cartes ?
2. **COMPRENDRE** : À quoi sert `g-3` sur la `row` ?
3. **TESTER** : Supprimez `h-100` et observez la différence
4. **EXPÉRIMENTER** : Changez les couleurs des badges (`bg-primary`, `bg-success`, etc.). Essayer avec d'autres images
5. **QUESTIONNER** : Pourquoi utiliser `shadow-sm` sur les cartes ?

---

## Étape 6 : Section contact avec formulaire

### 🎯 Consignes
Ajoutez une section de contact professionnelle avec un formulaire complet.

### 📖 Code à ajouter (après les modales de projets)
```html
<!-- Section Contact -->
<section id="contact" class="py-5">
    <div class="container">
        <div class="text-center mb-5">
            <span class="section-subtitle">Collaboration</span>
            <h2 class="section-title">Travaillons Ensemble</h2>
            <p class="lead">Un projet en tête ? Discutons de vos besoins !</p>
        </div>
        
        <div class="row justify-content-center">
            <div class="col-lg-8">
                <div class="contact-form-wrapper">
                    <form class="contact-form">
                        <div class="row">
                            <div class="col-md-6 mb-3">
                                <label for="nom" class="form-label">Nom complet</label>
                                <input type="text" class="form-control" id="nom" required>
                            </div>
                            <div class="col-md-6 mb-3">
                                <label for="email" class="form-label">Email</label>
                                <input type="email" class="form-control" id="email" required>
                            </div>
                        </div>
                        <div class="mb-3">
                            <label for="sujet" class="form-label">Sujet</label>
                            <select class="form-select" id="sujet" required>
                                <option value="">Choisissez un sujet</option>
                                <option value="design">Projet Design UI/UX</option>
                                <option value="web">Développement Web</option>
                                <option value="branding">Identité Visuelle</option>
                                <option value="autre">Autre</option>
                            </select>
                        </div>
                        <div class="mb-4">
                            <label for="message" class="form-label">Message</label>
                            <textarea class="form-control" id="message" rows="5" required></textarea>
                        </div>
                        <div class="text-center">
                            <button type="submit" class="btn btn-primary btn-lg">
                                <i class="bi bi-send me-2"></i>Envoyer le message
                            </button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</section>
```

### 🎨 CSS pour la section contact (ajout à `style.css`)
```css
/* === SECTION CONTACT === */
#contact {
  background: linear-gradient(135deg, var(--color-light) 0%, #e9ecef 100%);
  position: relative;
}

#contact::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="1" fill="%23000" opacity="0.02"/><circle cx="75" cy="75" r="1" fill="%23000" opacity="0.02"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
  opacity: 0.3;
  z-index: 1;
}

#contact .container {
  position: relative;
  z-index: 2;
}

.contact-form-wrapper {
  background: white;
  padding: var(--spacing-2xl);
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-medium);
  border: 1px solid rgba(0,0,0,0.05);
}

.contact-form .form-label {
  font-weight: 600;
  color: var(--color-dark);
  margin-bottom: var(--spacing-sm);
}

.contact-form .form-control,
.contact-form .form-select {
  border: 2px solid #e9ecef;
  border-radius: var(--border-radius);
  padding: var(--spacing-md);
  font-size: var(--font-size-base);
  transition: var(--transition-smooth);
}

.contact-form .form-control:focus,
.contact-form .form-select:focus {
  border-color: var(--color-primary);
  box-shadow: 0 0 0 0.2rem rgba(44, 62, 80, 0.15);
  transform: translateY(-1px);
}

/* === FOOTER === */
.footer-custom {
  background: var(--color-dark);
  color: white;
  border-top: 4px solid var(--color-accent);
}

.footer-custom .container {
  padding: var(--spacing-xl) 0;
}

.social-links a {
  color: rgba(255,255,255,0.7);
  font-size: 1.5rem;
  transition: var(--transition-smooth);
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  text-decoration: none;
}

.social-links a:hover {
  color: var(--color-accent);
  background: rgba(243,156,18,0.1);
  transform: translateY(-3px);
}
```

### 🎨 CSS Responsive et Utilitaires (ajout final à `style.css`)
```css
/* === MEDIA QUERIES - RESPONSIVE === */
@media (max-width: 991.98px) {
  .section-title {
    font-size: var(--font-size-3xl);
  }
  
  .section-title::after {
    width: 60px;
    left: 0;
    transform: none;
  }
  
  .hero-slide h1 {
    font-size: var(--font-size-3xl);
  }
  
  .about-image-wrapper {
    margin-bottom: var(--spacing-xl);
  }
}

@media (max-width: 767.98px) {
  .navbar-nav {
    background: rgba(44, 62, 80, 0.95);
    padding: var(--spacing-md);
    border-radius: var(--border-radius);
    margin-top: var(--spacing-sm);
  }
  
  .hero-slide h1 {
    font-size: var(--font-size-2xl);
  }
  
  .skill-item {
    padding: var(--spacing-lg);
    margin-bottom: var(--spacing-lg);
  }
  
  .project-info {
    padding: var(--spacing-lg);
  }
  
  .contact-form-wrapper {
    padding: var(--spacing-xl);
  }
  
  .image-decoration {
    top: -10px;
    left: -10px;
    width: calc(100% + 10px);
    height: calc(100% + 10px);
  }
}

@media (max-width: 575.98px) {
  .btn-accent,
  .btn-outline-light {
    padding: var(--spacing-sm) var(--spacing-lg);
    font-size: var(--font-size-sm);
  }
  
  .hero-slide {
    min-height: 500px;
  }
  
  .section-title::after {
    width: 60px;
    height: 3px;
  }
}

/* === UTILITAIRES === */
.text-gradient {
  background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.bg-gradient-primary {
  background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
}

.bg-gradient-accent {
  background: linear-gradient(135deg, var(--color-secondary), var(--color-accent));
}

/* Smooth scroll */
html {
  scroll-behavior: smooth;
}

/* Focus visible pour l'accessibilité */
*:focus-visible {
  outline: 2px solid var(--color-accent);
  outline-offset: 2px;
}

/* Amélioration des performances */
img {
  max-width: 100%;
  height: auto;
}
```

### 🤔 Questions de réflexion
1. **LIRE** : Que font les classes `form-label` et `form-control` ?
2. **COMPRENDRE** : Pourquoi utiliser `mb-3` entre les champs ?
3. **TESTER** : Cliquez sur les labels. Que se passe-t-il ?
4. **EXPÉRIMENTER** : Changez `btn-primary` en `btn-success` ou `btn-danger`
5. **QUESTIONNER** : À quoi sert `list-unstyled` ?

---

## Étape 7 : Pied de page
### 🎯 Consignes
Terminez votre portfolio avec un pied de page élégant.

### 📖 Code à ajouter (après la section contact)
```html
<!-- Pied de page -->
<footer class="py-4 mt-5 footer-custom">
    <div class="container">
        <div class="row align-items-center">
            <div class="col-md-6">
                <p class="mb-0">&copy; 2024 Votre Nom. Tous droits réservés.</p>
                <small class="text-muted">Créé avec ❤️, Bootstrap et CSS</small>
            </div>
            <div class="col-md-6 text-md-end">
                <div class="social-links">
                    <a href="#" class="me-3"><i class="bi bi-linkedin"></i></a>
                    <a href="#" class="me-3"><i class="bi bi-behance"></i></a>
                    <a href="#" class="me-3"><i class="bi bi-dribbble"></i></a>
                    <a href="#"><i class="bi bi-github"></i></a>
                </div>
            </div>
        </div>
    </div>
</footer>
```

### 🤔 Questions de réflexion
1. **LIRE** : Que fait `border-top` ?
2. **COMPRENDRE** : Différence entre `py-4` et `my-5` ?
3. **TESTER** : Supprimez `text-center`. Que constatez-vous ?
4. **EXPÉRIMENTER** : Ajoutez une couleur de fond avec `bg-light`
5. **QUESTIONNER** : Pourquoi utiliser `&copy;` plutôt que le symbole © ?

---

## Étape 8 : Responsive et personnalisation
### 🎯 Consignes finales
1. **TESTER** votre portfolio sur différentes tailles d'écran
2. **EXPÉRIMENTER** avec les couleurs et espacements
3. **PERSONNALISER** le contenu avec vos vraies informations
4. **PARTAGER** vos découvertes avec le groupe

### 🤔 Questions finales
1. Quels aspects de Bootstrap vous ont le plus aidé ?
2. Quelles difficultés avez-vous rencontrées ?
3. Comment pourriez-vous améliorer ce portfolio ?
4. Quelles fonctionnalités Bootstrap aimeriez-vous explorer ?

---

## 🏆 Défis supplémentaires (optionnels)
- Ajoutez une barre de navigation fixe en haut
- Intégrez des icônes avec Bootstrap Icons
- Créez un carrousel pour vos projets
- Ajoutez des animations avec les classes Bootstrap
- Personaliser le portfolio

---

## 💡 Ressources pour aller plus loin
- [Documentation officielle Bootstrap](https://getbootstrap.com/docs/)
- [Bootstrap Icons](https://icons.getbootstrap.com/)
- [Générateur de thèmes Bootstrap](https://bootstrap.build/)
