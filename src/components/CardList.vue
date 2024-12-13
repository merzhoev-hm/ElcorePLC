<script setup></script>

<template>
  <div class="card__list">
    <div class="card__list-card">
      <img class="card__img" />

      <div class="card__info">
        <span>12 Июля 2024</span>
        /
        <span>Новость</span>
      </div>

      <h3 class="card__title">Новые технологии в сфере автоматизации</h3>

      <p class="card__desc">
        Какие инновации помогут улучшить производственные процессы и повысить
        эффективность работы предприятий
      </p>
    </div>
    <div class="card__list-card">
      <div class="card__img"></div>

      <div class="card__info">
        <span>Статья</span>
      </div>

      <h3 class="card__title">Влияние цифровизации</h3>

      <p class="card__desc">
        Вызовы и возможности появляются для компаний в результате цифровой
        трансформации производства
      </p>
    </div>
    <div class="card__list-card">
      <div class="card__img"></div>

      <div class="card__info">
        <span>5 Июля 2024</span>
        /
        <span>Новость</span>
      </div>

      <h3 class="card__title">Устойчивое развитие и ответственность</h3>

      <p class="card__desc">
        Какие методы и технологии помогают снизить негативное влияние
        производства
      </p>
    </div>
    <div class="card__list-card">
      <div class="card__img"></div>

      <div class="card__info">
        <span>12 Июля 2024</span>
        /
        <span>Новость</span>
      </div>

      <h3 class="card__title">Новые технологии в сфере автоматизации</h3>

      <p class="card__desc">
        Какие инновации помогут улучшить производственные процессы и повысить
        эффективность работы предприятий
      </p>
    </div>
    <div class="card__list-card">
      <div class="card__img"></div>

      <div class="card__info">
        <span>24 Мая 2024</span>
        /
        <span>Новость</span>
      </div>

      <h3 class="card__title">Устойчивое развитие и ответственность</h3>

      <p class="card__desc">
        Какие методы и технологии помогают снизить негативное влияние
        производства
      </p>
    </div>
    <div class="card__list-card">
      <div class="card__img"></div>

      <div class="card__info">
        <span>Статья</span>
      </div>

      <h3 class="card__title">Влияние цифровизации</h3>

      <p class="card__desc">
        Вызовы и возможности появляются для компаний в результате цифровой
        трансформации производства
      </p>
    </div>
    <div class="card__list-card">
      <div class="card__img"></div>

      <div class="card__info">
        <span>Статья</span>
      </div>

      <h3 class="card__title">Влияние цифровизации</h3>

      <p class="card__desc">
        Вызовы и возможности появляются для компаний в результате цифровой
        трансформации производства
      </p>
    </div>
    <div class="card__list-card">
      <div class="card__img"></div>

      <div class="card__info">
        <span>12 Июля 2024</span>
        /
        <span>Новость</span>
      </div>

      <h3 class="card__title">Новые технологии в сфере автоматизации</h3>

      <p class="card__desc">
        Какие инновации помогут улучшить производственные процессы и повысить
        эффективность работы предприятий
      </p>
    </div>
    <div class="card__list-card">
      <div class="card__img"></div>

      <div class="card__info">
        <span>24 апреля 2024</span>
        /
        <span>Новость</span>
      </div>

      <h3 class="card__title">Устойчивое развитие и ответственность</h3>

      <p class="card__desc">
        Какие методы и технологии помогают снизить негативное влияние
        производства
      </p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.card__list {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 60px 24px;

  @media (max-width: 880px) {
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 30px 20px;
  }

  @media (max-width: 700px) {
    grid-template-columns: repeat(1, minmax(0, 1fr));
    gap: 50px;
  }

  &-card {
    max-width: 408px;
    min-height: 426px;
    display: flex;
    flex-direction: column;
    gap: 10px;

    @media (max-width: 700px) {
      max-width: 100%;
    }

    .card__img {
      background-image: url("/main-icons/Превью.png");
      min-height: 220px;
      background-repeat: no-repeat;
      background-position: center;
      background-size: cover;
    }

    .card__info {
      color: rgba(108, 108, 108, 1);
      font-family: Roboto;
      font-size: 14px;
      font-weight: 400;
      line-height: 22.4px;
    }

    .card__title {
      font-size: 24px;
      font-weight: 700;
      line-height: 38.4px;
      color: rgba(38, 38, 38, 1);
    }

    .card__desc {
      font-size: 16px;
      font-weight: 400;
      line-height: 25.6px;
      color: rgba(38, 38, 38, 1);
    }
  }
}
</style>
