<script setup>
const cards = [
  {
    title: 'Sound Engineer',
    description: 'Не профессиональная работа со звуком'
  },
  {
    title: 'DevOps',
    description: 'Автоматизация и инфраструктура'
  },
  {
    title: 'Network Administrator',
    description: 'Сетевые технологии и администрирование'
  }
]
</script>

<template>
  <div class="business-card">
    <div class="header">
      <div class="avatar">
        <img src="https://i.ibb.co/p6qThd2s/photo-2025-09-27-21-43-32.jpg" alt="nirotop" />
      </div>
      <h1 class="name">nirotop</h1>
      <p class="position">Junior Specialist</p>
    </div>

    <div class="cards-container">
      <div v-for="(card, index) in cards" :key="index" class="card">
        <h2 class="card-title">{{ card.title }}</h2>
        <p class="card-description">{{ card.description }}</p>
      </div>
    </div>

    <div class="footer">
      <div class="social-links">
        <a href="https://www.twitch.tv/nirotop" target="_blank" class="social-button twitch-button">
          <svg class="social-icon" viewBox="0 0 24 24" fill="currentColor">
            <path d="M11.571 4.714h1.715v5.143H11.57zm4.715 0H18v5.143h-1.714zM6 0L1.714 4.286v15.428h5.143V24l4.286-4.286h3.428L22.286 12V0zm14.571 11.143l-3.428 3.428h-3.429l-3 3v-3H6.857V1.714h13.714Z"/>
          </svg>
          Twitch
          <span class="button-subtitle">Стримы и контент</span>
        </a>

        <a href="https://t.me/video_nirotop_bot" target="_blank" class="social-button telegram-button">
          <svg class="social-icon" viewBox="0 0 24 24" fill="currentColor">
            <path d="M21.198 2.433a1.5 1.5 0 0 1 1.841 1.822l-3.346 19.75a1.5 1.5 0 0 1-2.405 1.003L7.965 13.08a.5.5 0 0 1 .016-.805l7.91-4.982a.5.5 0 1 0-.587-.789L7.385 11.486 2.63 9.44a1.5 1.5 0 0 1-.457-2.513L20.195 1.52c.47-.345 1.003.04.003.913Z"/>
          </svg>
          Telegram Bot
          <span class="button-subtitle">Для связи</span>
        </a>

        <a href="https://t.me/nirotopTwitch" target="_blank" class="social-button telegram-button personal">
          <svg class="social-icon" viewBox="0 0 24 24" fill="currentColor">
            <path d="M21.198 2.433a1.5 1.5 0 0 1 1.841 1.822l-3.346 19.75a1.5 1.5 0 0 1-2.405 1.003L7.965 13.08a.5.5 0 0 1 .016-.805l7.91-4.982a.5.5 0 1 0-.587-.789L7.385 11.486 2.63 9.44a1.5 1.5 0 0 1-.457-2.513L20.195 1.52c.47-.345 1.003.04.003.913Z"/>
          </svg>
          Telegram
          <span class="button-subtitle">Личный</span>
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.business-card {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 32px;
  gap: 48px;
}

.header {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 5px;
}

.avatar {
  width: 120px;
  height: 120px;
  animation: float 3s ease-in-out infinite;
}

@keyframes float {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
}

.avatar img {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  border: 4px solid rgba(102, 126, 234, 0.3);
  object-fit: cover;
  filter: drop-shadow(0 8px 24px rgba(102, 126, 234, 0.4));
}

.name {
  font-size: 4rem;
  font-weight: 700;
  margin: 0;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  letter-spacing: -0.02em;
}

.position {
  font-size: 1.5rem;
  margin: 16px 0 0 0;
  color: #94a3b8;
  font-weight: 500;
}

.cards-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 24px;
  width: 100%;
  max-width: 1000px;
}

.card {
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 16px;
  padding: 32px 24px;
  text-align: center;
  transition: all 0.3s ease;
  backdrop-filter: blur(10px);
}

.card:hover {
  transform: translateY(-4px);
  border-color: rgba(102, 126, 234, 0.4);
  box-shadow: 0 8px 32px rgba(102, 126, 234, 0.15);
  background: rgba(255, 255, 255, 0.05);
}

.card-title {
  font-size: 1.5rem;
  font-weight: 600;
  margin: 0 0 12px 0;
  color: #e2e8f0;
}

.card-description {
  font-size: 1rem;
  color: #94a3b8;
  margin: 0;
  line-height: 1.6;
}

.footer {
  margin-top: 16px;
}

.social-links {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}

.social-button {
  display: inline-flex;
  flex-direction: column;
  align-items: center;
  gap: 4px;
  padding: 16px 32px;
  color: white;
  text-decoration: none;
  border-radius: 12px;
  font-size: 1rem;
  font-weight: 600;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.social-button::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
  transition: left 0.5s;
}

.social-button:hover::before {
  left: 100%;
}

.social-button:hover {
  transform: translateY(-2px);
}

.twitch-button {
  background: #9146ff;
  box-shadow: 0 4px 16px rgba(145, 70, 255, 0.3);
}

.twitch-button:hover {
  box-shadow: 0 8px 24px rgba(145, 70, 255, 0.4);
  background: #7d3ddb;
}

.telegram-button {
  background: #0088cc;
  box-shadow: 0 4px 16px rgba(0, 136, 204, 0.3);
}

.telegram-button:hover {
  box-shadow: 0 8px 24px rgba(0, 136, 204, 0.4);
  background: #006ba3;
}

.telegram-button.personal {
  background: #229ed9;
  box-shadow: 0 4px 16px rgba(34, 158, 217, 0.3);
}

.telegram-button.personal:hover {
  box-shadow: 0 8px 24px rgba(34, 158, 217, 0.4);
  background: #1a7db0;
}

.social-icon {
  width: 24px;
  height: 24px;
  margin-bottom: 2px;
}

.button-subtitle {
  font-size: 0.75rem;
  font-weight: 400;
  opacity: 0.9;
}

@media (max-width: 768px) {
  .name {
    font-size: 3rem;
  }

  .position {
    font-size: 1.25rem;
  }

  .cards-container {
    grid-template-columns: 1fr;
    max-width: 400px;
  }

  .social-links {
    gap: 12px;
  }

  .social-button {
    padding: 14px 24px;
    font-size: 0.9rem;
  }

  .button-subtitle {
    font-size: 0.7rem;
  }
}
</style>
