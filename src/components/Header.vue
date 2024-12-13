<script setup></script>

<template>
  <header class="header">
    <div class="container">
      <div class="header__top">
        <div class="header__top-social">
          <a href="#"><img src="/header-icons/Тлг.svg" alt="Telegram" /></a>
          <a href="#"><img src="/header-icons/Дзен.svg" alt="Dzen" /></a>
          <a href="#"><img src="/header-icons/Ютуб.svg" alt="Youtube" /></a>
          <a href="#"><img src="/header-icons/Вк.svg" alt="VK" /></a>
        </div>
        <div class="header__top-right">
          <nav class="header__top-nav">
            <a href="#">Форум</a>
            <a href="#">Поиск</a>
            <a href="#">Контакты</a>
          </nav>
          <div class="header__top-usermenu">
            <button>
              <img src="/header-icons/star.svg" alt="Favorites" />
            </button>
            <button>
              <img src="/header-icons/shopping-cart.svg" alt="Cart" />
            </button>
            <button class="usermenu__lk-btn">Личный кабинет</button>
          </div>
        </div>
      </div>
    </div>

    <div class="header__center">
      <div class="container">
        <div class="header__center-logo">
          <img src="/Лого.svg" alt="ElcorePLC" />
        </div>
        <nav class="header__center-nav">
          <ul class="header__center-ul">
            <li><a href="#">ElcoreStore</a></li>
            <li><a href="#">ElcoreCloud</a></li>
            <li><a href="#">ElcoreIDE</a></li>
            <li class="nav__dropdown-wrapper">
              <button href="#" class="nav__dropdown-btn">
                Обучение и ресурсы
                <img src="/header-icons/arrow.svg" alt="\/" />
              </button>
              <ul class="nav__dropdown-menu">
                <li>
                  <a class="footer__link" href="#">Что такое ElcorePLC</a>
                </li>
                <li><a class="footer__link" href="#">Документация</a></li>
                <li>
                  <a class="footer__link" href="#">Обучающие материалы</a>
                </li>
                <li>
                  <a class="footer__link" href="#">Примеры использования</a>
                </li>
                <li><a class="footer__link" href="#">База знаний</a></li>
              </ul>
            </li>
            <li><a href="#">Новости и статьи</a></li>
          </ul>
        </nav>
        <div class="header__center-menu">
          <span></span>
        </div>
      </div>
    </div>

    <div class="header__bottom">
      <div class="container">
        <div class="header__bottom-path">
          <span>Главная</span>
          /
          <span>Новости и Статьи</span>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
.header {
  background-color: #262626;
  color: rgba(255, 255, 255, 1);

  &__top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 12px 0;

    &-social {
      display: flex;
      gap: 22px;
      align-items: center;

      @media (max-width: 860px) {
        display: none;
      }
    }

    &-right {
      display: flex;
      align-items: center;
      gap: 56px;

      @media (max-width: 860px) {
        gap: 0;
        justify-content: space-between;
        width: 100%;
      }

      @media (max-width: 600px) {
        justify-content: center;
      }

      .header__top-nav {
        display: flex;
        gap: 30px;

        @media (max-width: 600px) {
          display: none;
        }

        & a {
          font-weight: 700;
          line-height: 24px;

          @media (max-width: 860px) {
            font-size: 13px;
            font-weight: 500;
          }

          &:hover {
            color: rgb(206, 206, 206);
          }
        }
      }

      .header__top-usermenu {
        display: flex;
        gap: 30px;

        .usermenu__lk-btn {
          padding: 6px 14px;
          background-color: #428d26;
          border-radius: 3px;

          font-size: 14px;
          font-weight: 400;
          line-height: 16.41px;

          &:hover {
            background-color: #36751f;
          }
        }
      }
    }
  }

  &__center {
    background-color: rgba(16, 16, 16, 1);

    .container {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding-top: 35px;
      padding-bottom: 35px;

      .header__center-logo {
        cursor: pointer;
      }

      .nav__dropdown-wrapper {
        position: relative;

        .nav__dropdown-menu {
          position: absolute;
          background-color: rgba(16, 16, 16, 1);
          left: -15px;
          display: flex;
          flex-direction: column;
          min-width: max-content;
          border-radius: 0px 0px 10px 10px;
          padding-top: 20px;
          display: none;

          & li {
            padding: 12px;
            border-radius: 10px;
            &:hover {
              background-color: #262626;
            }
          }
        }

        .nav__dropdown-btn {
          display: flex;
          align-items: center;
          gap: 8px;
        }

        &:hover .nav__dropdown-menu {
          display: flex;
        }
      }

      .header__center-nav {
        @media (max-width: 1150px) {
          display: none;
        }
      }

      .header__center-ul {
        display: flex;
        gap: 40px;

        font-size: 18px;
        line-height: 21.09px;

        & a {
          &:hover {
            color: rgb(206, 206, 206);
          }
        }
      }

      & .header__center-menu {
        display: none;
        position: relative;
        width: 33px;
        height: 28px;
        cursor: pointer;

        @media (max-width: 1150px) {
          display: block;
        }

        &::before,
        &::after {
          position: absolute;
          content: "";
          width: 100%;
          height: 2px;
          background: rgba(217, 217, 217, 1);
          left: 0;
          border-radius: 3px;
        }

        &::before {
          top: 0;
        }

        &::after {
          bottom: 0;
        }

        & span {
          position: absolute;
          width: 100%;
          height: 2px;
          background: rgba(217, 217, 217, 1);
          left: 0;
          top: 14px;
          border-radius: 3px;
        }
      }
    }
  }

  &__bottom {
    padding: 12px 0;

    &-path {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 12px;
      font-weight: 400;

      & span {
        color: rgba(217, 217, 217, 1);
        font-size: 12px;
        font-weight: 400;
        line-height: 19.2px;
        cursor: pointer;

        &:hover {
          color: rgb(182, 180, 180);
        }
      }
    }
  }
}
</style>
