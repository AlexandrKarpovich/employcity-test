<template>
  <section class="banner">
    <div class="container">
      <div class="banner__inner">
        <h1 class="title-main"> Lorem ipsum
          <span class="title-main__color">dolor sit amet consectetur</span> adipiscing
        </h1>
        <span class="list__title">
          At vero eos et accusamus et iusto odio dignissimos ducimus!
        </span>
        <ul class="list__descr">
          <li class="list__descr__item">
            Totam rem aperiam eaque ipsa
          </li>
          <li class="list__descr__item">
            Sit voluptatem accusantium doloremque laudantium
          </li>
          <li class="list__descr__item">
            Sed ut perspiciatis, unde omnis iste natus error
          </li>
        </ul>
        <div class="buttons">
          <a href="" class="buttons__item">заказать</a>
          <a href="" class="buttons__item">подробнее</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  name: 'MainBanner',
  components: {
    
  }
}
</script>

<style lang="scss">
  .banner {
    width: 100%;
    background: url('../assets/banner.jpeg') top center no-repeat;
    background-size: cover;
    &__inner {
      padding: 203px 0;
      text-align: left;
    }
    .title-main {
      font-weight: 700;
      font-size: 3rem;
      line-height: 3.625rem;
      text-transform: uppercase;
      color: #3E9CDC;
      max-width: 600px;
      width: 100%;
      text-align: left;

      &__color {
        color: #000000;
      }
    }
    .list {
      &__title {
        font-weight: 700;
        font-size: 20px;
        line-height: 24px;
        color: #000000;
      }
      &__descr {
        margin-bottom: 80px;
        &__item {
          font-weight: 400;
          font-size: 20px;
          line-height: 24px;
          color: #000000;
        }
      }
    }
    .buttons {
      max-width: 398px;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;

      &__item {
        width: 100%;
        max-width: 183px;
        text-align: center;
        padding: 15px 10px;
        text-decoration: none;
        box-sizing: border-box;
        &:first-child {
          background: #3E9CDC;
          border: 1px solid #FFFFFF;
          border-radius: 4px;
          color: #FFFFFF;
        }
        &:last-child {
          background: #FFFFFF;
          border: 1px solid #6F6D7B;
          border-radius: 4px;
          color: #2A2B30;
        }
      }
    }
  }
</style>