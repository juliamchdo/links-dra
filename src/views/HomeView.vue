<script setup lang="ts">

const navigate = (url: string) => {
  window.open(url, '_blank')
}
</script>

<template>
  <div class="background">
    <div class="profile-card">
      <div class="cover"></div>
      <div class="profile">
        <div class="pic-container">
          <div class="pic"></div>
        </div>
        <div class="above-fold">
          <div class="name">Dra. Natália Bittencourt da Silva</div>
          <h2 class="subtitle mx-2">Olá, <b>links</b> que irão te ajudar</h2>

          <div class="profile-links">
            <div class="links">
              <div @click="navigate('https://dra-natalia-bittencourt.netlify.app/')" class=" d-flex align-items-center">
                Conheça meu trabalho
                <img class="icon" src="../assets/icons/web.svg" alt="web">
              </div>
            </div>
            <div class="links">
              <div @click="navigate('https://www.doctoralia.com.br/z/JdNo2V')"
                class="d-flex align-items-center">Agende sua consulta
                <img class="icon" src="../assets/icons/schedule.svg" alt="schedule">
              </div>
            </div>
            <div class="links">
              <div @click="navigate('https://api.whatsapp.com/send?phone=554899114373')"
                class="d-flex align-items-center">Mande sua dúvida
                <img class="icon" src="../assets/icons/whatsapp.svg" alt="whatsapp">
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.background {
  background-color: #FFFF;
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

@media (width <=767px) {
  .background {
    background-image: url('../assets/images/background.jpeg');
    background-repeat: no-repeat;
    background-position: top center;
    background-size: cover;
  }

  .profile-card {
    top: 65%;
  }

}

@media (width >=768px) {
  .profile-card {
    top: 50%;
  }
}

.profile-card {
  position: absolute;
  width: 20rem;
  left: 50%;
  transform: translate(-50%, -50%);
  letter-spacing: 0.025em;
  text-align: center;
  color: var(--black);
}

.profile-card .cover {
  background-image: url('../assets/images/profile.png'),
    linear-gradient(135deg, rgba(26, 166, 183, 0.2), rgba(255, 65, 77, 0.4));
  background-position: top center;
  background-size: cover;
  background-repeat: no-repeat;
  background-blend-mode: overlay;
  height: 14rem;
  width: 100%;
  border-radius: 2rem;
  margin-bottom: -14rem;
  transform: translateY(0);
  transition: transform 500ms ease-in-out, opacity 200ms 300ms;
  opacity: 0;
  box-shadow: 0 2rem 4rem -3rem rgba(0, 45, 64, 0.5), 0 0 8rem 0 rgba(0, 45, 64, 0.1);
}

.profile-card .pic-container {
  background-color: white;
  position: absolute;
  left: 50%;
  width: 9rem;
  height: 9rem;
  border-radius: 50%;
  transform: translate(-50%, -50%);
  border: 1px solid var(--pink);
  margin-top: -2rem;
  z-index: 2;
}

.profile-card .pic-container .pic {
  background-image: url('../assets/images/profile.png'),
    linear-gradient(135deg, rgba(26, 166, 183, 0.1), rgba(255, 65, 77, 0.2));
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  background-blend-mode: overlay;
  position: absolute;
  left: 50%;
  top: 50%;
  width: 8rem;
  height: 8rem;
  border-radius: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
}

.profile-card .profile {
  position: relative;
  background: white;
  width: 100%;
  border-radius: 2rem;
  border: 2px solid var(--pink);
  padding-top: 2rem;
  box-sizing: border-box;
  transition: transform 500ms ease-in-out;
  box-shadow: 0 2rem 4rem -3rem rgba(0, 45, 64, 0.5), 0 0 8rem 0 rgba(0, 45, 64, 0.1);
}

.profile-card .above-fold {
  padding: 3rem 0 1rem 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.profile-card .above-fold .name {
  font-size: 1rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  padding: .5rem;
  border: 1px solid var(--pink);
  border-radius: 2rem;
  width: 90%;
}

.subtitle {
  margin-top: 2rem;
  font-size: 1.6rem;
}

.links>div {
  cursor: pointer;
}

.profile-card .above-fold .profile-links {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  width: 100%;
  margin-top: 2rem;
}

.profile-card .above-fold .links {
  border: 1px solid var(--pink);
  border-radius: 2rem;
  padding: .5rem;
  width: 80%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: .5rem;
}

.profile-card .above-fold .links .icon {
  height: 1.5rem;
  width: 1.5rem;
  margin-left: .5rem;
  fill: var(--dark-yellow);
}

@keyframes bounce {

  0%,
  60%,
  100% {
    transform: translateY(0);
  }

  80% {
    transform: translateY(-8px);
  }

  90% {
    transform: translateY(8px);
  }
}
</style>
