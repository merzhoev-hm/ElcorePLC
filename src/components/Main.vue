<script setup>
import CardList from "./CardList.vue";
</script>

<template>
  <main class="main">
    <div class="container">
      <h2 class="main__title">Новости и статьи</h2>
      <div class="main__filter-btns">
        <button class="active">Все новости и статьи</button>
        <button>Новости</button>
        <button>Статьи</button>
      </div>
      <CardList />
      <div class="main__pagination">
        <div class="pagination__btn pagination__btn-prev"></div>
        <div class="pagination__nums">
          <span class="pagination__num active-num">1</span>
          <span class="pagination__num">2</span>
          <span class="pagination__num">3</span>
          <span class="pagination__num">4</span>
          <span class="pagination__num pagination__num-more">...</span>
          <span class="pagination__num">11</span>
        </div>
        <div class="pagination__btn pagination__btn-next active"></div>
      </div>
    </div>
  </main>
</template>

<style scoped lang="scss">
.main {
  padding: 70px 0;
  color: rgba(38, 38, 38, 1);

  &__title {
    font-size: 36px;
    font-weight: 700;
    line-height: 50.4px;
    text-align: center;

    margin-bottom: 50px;

    @media (max-width: 500px) {
      margin-bottom: 30px;
      font-size: 25px;
      line-height: 30px;
    }
  }
  &__filter-btns {
    display: flex;
    gap: 15px;
    margin-bottom: 34px;

    @media (max-width: 530px) {
      flex-direction: column;
    }

    button {
      font-size: 14px;
      font-weight: 400;
      line-height: 16.41px;
      text-align: center;

      border-radius: 20px;
      padding: 6px 14px;

      border: 1px solid rgba(66, 141, 38, 1);
      color: rgba(66, 141, 38, 1);
    }

    .active {
      background-color: rgba(66, 141, 38, 1);
      color: rgba(255, 255, 255, 1);
      border: none;
    }
  }

  &__pagination {
    display: flex;
    align-items: center;
    gap: 20px;
    justify-content: center;

    margin-top: 80px;

    @media (max-width: 700px) {
      margin-top: 20px;
      gap: 15px;
    }

    .pagination__btn {
      position: relative;
      height: 6.5px;
      width: 8px;
      cursor: pointer;

      &::before,
      &::after {
        position: absolute;
        content: "";
        width: 100%;
        height: 2px;
        left: 0;
        background-color: rgba(38, 38, 38, 1);
        border-radius: 10px;
      }

      &:hover {
        &::before,
        &::after {
          background: rgba(66, 141, 38, 1);
        }
      }
    }

    .pagination__btn-prev {
      &::before {
        transform: rotate(-45deg);
        top: 0;
      }
      &::after {
        transform: rotate(45deg);
        bottom: 0;
      }
    }

    .pagination__btn-next {
      &::before {
        transform: rotate(45deg);
        top: 0;
      }
      &::after {
        transform: rotate(-45deg);
        bottom: 0;
      }
    }

    .pagination__nums {
      display: flex;
      gap: 20px;

      @media (max-width: 700px) {
        gap: 10px;
      }

      .pagination__num {
        padding: 6px;
        border: 1px solid transparent;
        border-radius: 3px;
        cursor: pointer;

        &:hover {
          border: 1px solid rgba(66, 141, 38, 1);
        }
      }
      .active-num {
        background: rgba(66, 141, 38, 1);
        color: rgba(255, 255, 255, 1);
      }
    }
  }
}
</style>
