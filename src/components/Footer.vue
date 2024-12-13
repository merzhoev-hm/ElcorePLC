<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const docWidth = ref(document.documentElement.clientWidth);

const updateWidth = () => {
  docWidth.value = document.documentElement.clientWidth;
};

const openSpoiler = (el) => {
  if (docWidth.value < 705) {
    el.nextElementSibling.classList.toggle("show");
    el.classList.toggle("active");
  }
};

onMounted(() => {
  window.addEventListener("resize", updateWidth);
});

onUnmounted(() => {
  window.removeEventListener("resize", updateWidth);
});
</script>

<template>
  <footer class="footer">
    <div class="footer__top">
      <div class="container">
        <div class="footer__top-content">
          <div class="footer__content-logo">
            <img src="/Лого.svg" alt="ElcorePLC" />
          </div>
          <p class="footer__content-desc">
            Платформа для автоматизации<br />ваших процессов
          </p>
          <div class="footer__content-install">
            <img src="/footer-icons/Скачать.svg" alt="i" />
          </div>
          <div class="footer__content-c">© ООО «НПО «Фарватер» 2024</div>
        </div>

        <div class="footer__platform footer__block">
          <h3 @click="openSpoiler($event.target)" class="footer__title">
            Платформа
          </h3>
          <ul class="footer__link-list">
            <li><a class="footer__link" href="#">ElcoreStore</a></li>
            <li><a class="footer__link" href="#">ElcoreCloud</a></li>
            <li><a class="footer__link" href="#">ElcoreIDE</a></li>
          </ul>
        </div>

        <div class="footer__resources footer__block">
          <h3 @click="openSpoiler($event.target)" class="footer__title">
            Обучение и ресурсы
          </h3>
          <ul class="footer__link-list">
            <li><a class="footer__link" href="#">Что такое ElcorePLC</a></li>
            <li><a class="footer__link" href="#">Документация</a></li>
            <li><a class="footer__link" href="#">Обучающие материалы</a></li>
            <li><a class="footer__link" href="#">Примеры использования</a></li>
            <li><a class="footer__link" href="#">База знаний</a></li>
          </ul>
        </div>

        <div class="footer__contact">
          <button class="footer__button">Личный кабинет</button>
          <ul class="footer__link-list">
            <li><a class="footer__link" href="#">Контакты</a></li>
            <li><a class="footer__link" href="#">Новости и статьи</a></li>
            <li><a class="footer__link" href="#">Сообщество (Форум)</a></li>
            <li><a class="footer__link" href="#">Тех поддержка</a></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="footer__bottom">
      <div class="container">
        <div class="footer__bottom-links">
          <a href="#"><img src="/header-icons/Тлг.svg" alt="Telegram" /></a>
          <a href="#"><img src="/header-icons/Дзен.svg" alt="Dzen" /></a>
          <a href="#"><img src="/header-icons/Ютуб.svg" alt="Youtube" /></a>
          <a href="#"><img src="/header-icons/Вк.svg" alt="VK" /></a>
        </div>
        <div class="footer__bottom-copyright">
          <ul>
            <li>
              <a class="footer__bottom-link" href="#"
                >Политика конфиденциальности</a
              >
            </li>
            <li><a class="footer__bottom-link" href="#">Карта сайта</a></li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
.footer {
  &__top {
    color: #fff;
    background: rgba(16, 16, 16, 1);

    .footer__block {
      @media (max-width: 705px) {
        .footer__title {
          position: relative;
          padding-left: 30px;
          cursor: pointer;

          &::before,
          &::after {
            content: "";
            width: 10px;
            height: 1px;
            background: #ffffff;
            position: absolute;
            top: 15px;
            transition: all 0.2s ease-in-out;
          }

          &::before {
            transform: rotate(40deg);
            left: 0;
          }

          &::after {
            transform: rotate(-40deg);
            left: 7px;
          }

          &.active::before {
            transform: rotate(-40deg);
          }

          &.active::after {
            transform: rotate(40deg);
          }
        }

        .footer__link-list {
          display: none;
        }

        .show {
          display: flex;
        }
      }
    }

    .container {
      padding-bottom: 100px;
      padding-top: 70px;

      display: grid;
      grid-template-columns: 2fr 1fr 1.5fr 1fr;

      gap: 40px 0;

      @media (max-width: 1150px) {
        grid-template-columns: 2fr 1fr 1.5fr;
      }

      @media (max-width: 880px) {
        grid-template-columns: 2fr 1fr;
      }

      @media (max-width: 705px) {
        display: flex;
        flex-direction: column;
        align-items: start;
        gap: 20px;
      }
    }

    &-content {
      display: flex;
      flex-direction: column;

      font-size: 18px;
      font-weight: 700;

      .footer__content-logo {
        margin-bottom: 29px;
      }

      .footer__content-install {
        margin-bottom: 33px;
      }

      .footer__content-desc {
        margin-bottom: 13px;

        line-height: 28.8px;
      }

      .footer__content-c {
        line-height: 21.09px;
      }
    }
  }

  &__platform {
  }

  &__title {
    font-size: 24px;
    font-weight: 700;
    line-height: 28.13px;
    color: rgba(108, 108, 108, 1);

    margin-bottom: 26px;
  }

  &__link-list {
    display: flex;
    flex-direction: column;
    gap: 18px;
  }

  &__link {
    font-size: 18px;
    font-weight: 400;
    line-height: 23.4px;
  }

  &__button {
    font-size: 18px;
    font-weight: 700;

    padding: 13px 17px;
    border: 1px solid rgba(255, 255, 255, 1);
    border-radius: 3px;
    margin-bottom: 26px;

    &:hover {
      border: 1px solid rgb(136, 136, 136);
    }
  }

  &__bottom {
    background: rgba(38, 38, 38, 1);

    .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-bottom: 26px;
      padding-top: 26px;

      @media (max-width: 700px) {
        flex-direction: column;
        gap: 20px;
      }
    }
    &-copyright {
      ul {
        display: flex;
        gap: 22px;

        @media (max-width: 500px) {
          flex-direction: column;
          align-items: center;
        }
      }
    }

    &-links {
      display: flex;
      gap: 21px;
      align-items: center;
    }

    &-link {
      font-size: 16px;
      font-weight: 400;
      line-height: 25.6px;
      color: rgba(171, 171, 171, 1);
    }
  }
}
</style>
