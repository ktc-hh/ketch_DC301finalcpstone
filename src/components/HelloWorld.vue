<script setup>
const menuItems = [
  {
    name: 'Hot Chicken Sando',
    badge: 'Best seller',
    price: '$14.90',
    note: 'Crispy chicken, slaw, and a smoky aioli on toasted brioche.',
    emoji: '🍗',
    accent: 'sandwich'
  },
  {
    name: 'Citrus Burrito Bowl',
    badge: 'Fresh pick',
    price: '$12.50',
    note: 'Grilled veggies, cilantro rice, black beans, and lime crema.',
    emoji: '🌮',
    accent: 'bowl'
  },
  {
    name: 'Sunset Salmon',
    badge: 'Chef special',
    price: '$18.40',
    note: 'Charred salmon with quinoa, greens, and a bright citrus glaze.',
    emoji: '🐟',
    accent: 'salmon'
  }
]

const features = [
  { label: 'Fast delivery', text: 'Brought to your door in under 20 minutes.', icon: '⚡' },
  { label: 'Fresh ingredients', text: 'Locally sourced produce and quality proteins.', icon: '🥬' },
  { label: 'Easy ordering', text: 'Simple checkout, smart returns, and live updates.', icon: '📦' }
]
</script>

<template>
  <div class="quickbite-app">
    <header class="topbar">
      <div class="brand" aria-label="QuickBite home">
        <div class="brand-mark">Q</div>
        <span>QuickBite</span>
      </div>

      <nav class="nav" aria-label="Main navigation">
        <a href="#">Home</a>
        <a href="#">Menu</a>
        <a href="#">Offers</a>
        <a href="#">Reviews</a>
      </nav>

      <div class="header-actions">
        <button class="ghost-button" type="button">Sign in</button>
        <button class="primary-button" type="button">Order now</button>
      </div>
    </header>

    <main class="page-shell">
      <section class="hero-section">
        <div class="hero-copy">
          <p class="eyebrow">Fast • Fresh • Flavorful</p>
          <h1>Crave-worthy meals, delivered with a smile.</h1>
          <p class="subcopy">
            From comfort classics to chef-crafted bowls, QuickBite brings restaurant-level flavor
            straight to your door whenever the appetite hits.
          </p>

          <div class="cta-row">
            <button class="primary-button large" type="button">Explore menu</button>
            <button class="secondary-button" type="button">View deals</button>
          </div>

          <div class="mini-stats">
            <div>
              <strong>12k+</strong>
              <span>happy diners</span>
            </div>
            <div>
              <strong>4.9/5</strong>
              <span>average rating</span>
            </div>
            <div>
              <strong>18 min</strong>
              <span>average delivery</span>
            </div>
          </div>
        </div>

        <div class="hero-visual" aria-label="Featured meal illustration">
          <div class="dish-scene">
            <div class="plate-glow"></div>
            <div class="food-stack">
              <span class="bun bun-top"></span>
              <span class="lettuce"></span>
              <span class="tomato"></span>
              <span class="patty"></span>
              <span class="bun bun-bottom"></span>
            </div>
          </div>

          <div class="floating-card rating-card">
            <div class="stars">★★★★★</div>
            <strong>4.9 rating</strong>
            <span>1.8k reviews</span>
          </div>

          <div class="floating-card delivery-card">
            <span class="badge-pill">On the way</span>
            <strong>12 min</strong>
            <span>delivery window</span>
          </div>
        </div>
      </section>

      <section class="feature-strip" aria-label="QuickBite features">
        <article v-for="feature in features" :key="feature.label" class="feature-item">
          <span class="feature-icon">{{ feature.icon }}</span>
          <div>
            <h3>{{ feature.label }}</h3>
            <p>{{ feature.text }}</p>
          </div>
        </article>
      </section>

      <section class="menu-section">
        <div class="section-head">
          <div>
            <p class="eyebrow">Popular picks</p>
            <h2>Top dishes this week</h2>
          </div>
          <a href="#">See full menu</a>
        </div>

        <div class="menu-grid">
          <article v-for="item in menuItems" :key="item.name" class="menu-card">
            <div class="food-art" :class="item.accent">
              <span>{{ item.emoji }}</span>
            </div>

            <div class="card-body">
              <div class="card-row">
                <h3>{{ item.name }}</h3>
                <span class="price">{{ item.price }}</span>
              </div>
              <p>{{ item.note }}</p>

              <div class="card-footer">
                <span class="menu-tag">{{ item.badge }}</span>
                <button type="button">Add</button>
              </div>
            </div>
          </article>
        </div>
      </section>

      <section class="benefits-panel">
        <div class="panel-copy">
          <p class="eyebrow">Why people choose us</p>
          <h2>Made for busy days and good cravings.</h2>
          <p>
            QuickBite blends convenience and quality so your next bite feels satisfying, effortless,
            and genuinely worth ordering again.
          </p>
        </div>

        <div class="benefit-list">
          <div>
            <strong>Curated menu</strong>
            <span>Balanced classics and fresh seasonal favorites.</span>
          </div>
          <div>
            <strong>Built for speed</strong>
            <span>Live status updates from kitchen to doorstep.</span>
          </div>
          <div>
            <strong>Better every time</strong>
            <span>Tailored recommendations based on your taste.</span>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>
