<script setup>
import { products, sellers } from "./assets/mockData";
</script>

<template>
  <body class="skin">
    <div id="wrapper">
      <div class="main-container">
        <div class="container">
          <div class="row first-block">
            <div class="col-lg-8 page-content col-thin-right">
              <div class="inner inner-box items-details-wrapper pb-0" style="">
                <h1 class="h4 fw-bold enable-long-words">
                  <strong>
                    <a
                      href="http://helperbook.shop/test-testtesttest/1"
                      title="Test testtesttest"
                    >
                      Самсунг 0101
                    </a>
                  </strong>
                </h1>

                <div class="gallery-container">
                  <div class="swiper main-gallery">
                    <div class="swiper-wrapper">
                      <div class="swiper-slide">
                        <img
                          src="http://helperbook.shop/storage/files/ru/1/thumb-816x460-5795836f151bc90eb4cb81e6e665d16b.jpg"
                          alt="test-testtesttest-big-0"
                        />
                      </div>
                    </div>
                    <div class="swiper-button-next"></div>
                    <div class="swiper-button-prev"></div>
                  </div>
                  <div class="swiper thumbs-gallery">
                    <div class="swiper-wrapper">
                      <div class="swiper-slide">
                        <img
                          src="http://helperbook.shop/storage/files/ru/1/thumb-120x90-5795836f151bc90eb4cb81e6e665d16b.jpg"
                          alt="test-testtesttest-small-0"
                        />
                      </div>
                    </div>
                  </div>
                </div>

                <div class="items-details">
                  <ul class="nav nav-tabs" id="itemsDetailsTabs" role="tablist">
                    <li class="nav-item" role="presentation">
                      <div
                        class="nav-link active cursor-default"
                        id="item-details-tab"
                        data-bs-toggle="tab"
                        data-bs-target="#item-details"
                        role="tab"
                        aria-controls="item-details"
                        aria-selected="true"
                      >
                        <span class="title-3 lh-base">Характеристики</span>
                      </div>
                    </li>
                  </ul>

                  <div
                    class="p-3 mb-3 tab-content"
                    id="itemsDetailsTabsContent"
                  >
                    <ul class="about-list">
                      <li
                        v-for="param in products[0].params"
                        :key="param"
                        class="about-list-item"
                      >
                        {{ Object.keys(param)[0] }}......
                        {{ Object.values(param)[0] }}
                      </li>
                    </ul>
                  </div>
                </div>
              </div>
            </div>

            <div class="col-lg-4 page-sidebar-right">
              <div class="sidebar-header" id="sidebar-header-seller">
                <span class="title">Продавцы</span>
                <div>
                  <img
                    src="./assets/img/sort.svg"
                    alt="Sort"
                    id="sort-seller"
                  />
                  <img src="./assets/img/filter.svg" alt="Filter" />
                </div>
              </div>
              <div class="sidebar">
                <div v-for="item in sellers" :key="item.id" class="item">
                  <div class="item-sidebar-header">
                    <p class="title">{{ item.name }}</p>
                    <p class="price">{{ item.price }}</p>
                  </div>
                  <div class="details">
                    <div class="labels">
                      <p>Рейтинг</p>
                      <p>Количество продаж</p>
                      <p>Срок доставки</p>
                    </div>
                    <div class="values">
                      <p>{{ item.rang_main }} / {{ item.rang_secondary }}</p>
                      <p>
                        {{ item.count_sales }} / {{ item.count_sales_product }}
                      </p>
                      <p class="delivery">{{ item.delivery_date }}</p>
                    </div>
                  </div>
                  <div class="button-group">
                    <button class="secondary-button">Написать</button>
                    <button class="button">Купить</button>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="second-block row">
            <div class="product col-lg-8 page-content col-thin-right">
              <h3 class="product__title">Информация о товаре</h3>
              <div class="product__path">
                <p class="product__path_active">Телефон Самсунг 0101</p>
                <p>Телефон Самсунг</p>
                <p>Телефон</p>
                <p>Электроника</p>
                <p>Телефон Самсунг 0101</p>
                <p>Телефон Самсунг</p>
                <p>Телефон</p>
                <p>Электроника</p>
                <p>Телефон Самсунг 0101</p>
                <p>Телефон Самсунг</p>
                <p>Телефон</p>
                <p>Электроника</p>
                <p>Телефон Самсунг 0101</p>
                <p>Телефон Самсунг</p>
                <p>Телефон</p>
                <p>Электроника</p>
              </div>
              <div class="pruduct__main">
                <div class="product__item">
                  <h4 class="product__item_title">
                    Петров А.В. Телефон Самсунг 0101 - новинка среди смартфонов
                  </h4>
                  <p class="product__item_text">
                    Начало статьи, главная мысль, цитата, статистика, мнение
                    автора, вывод по статье, любой текст.Начало статьи, главная
                    мысль, цитата, статистика, мнение автора, вывод по статье,
                    любой текст.Начало статьи, главная мысль, цитата,
                    статистика, мнение автора, вывод по статье, любой
                  </p>
                  <img
                    src="./assets/img/image 3.jpg"
                    alt="pic"
                    class="product__item_img"
                  />
                  <div class="product__item_footer">
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/like.svg" alt="pic" />
                      <p>157</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/dislike.svg" alt="pic" />
                      <p>5</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/eye.svg" alt="pic" />
                      <p>10 256</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/commentsvg.svg" alt="pic" />
                      <p>12</p>
                    </div>
                  </div>
                </div>
                <div class="product__item">
                  <h4 class="product__item_title">
                    Петров А.В. Телефон Самсунг 0101 - новинка среди смартфонов
                  </h4>
                  <p class="product__item_text">
                    Начало статьи, главная мысль, цитата, статистика, мнение
                    автора, вывод по статье, любой текст.
                  </p>
                  <img
                    src="./assets/img/image 3.jpg"
                    alt="pic"
                    class="product__item_img"
                  />
                  <div class="product__item_footer">
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/like.svg" alt="pic" />
                      <p>157</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/dislike.svg" alt="pic" />
                      <p>5</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/eye.svg" alt="pic" />
                      <p>10 256</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/commentsvg.svg" alt="pic" />
                      <p>12</p>
                    </div>
                  </div>
                </div>
                <div class="product__item">
                  <h4 class="product__item_title">
                    Петров А.В. Телефон Самсунг 0101 - новинка среди смартфонов
                  </h4>
                  <p class="product__item_text">
                    Начало статьи, главная мысль, цитата, статистика, мнение
                    автора, вывод по статье, любой текст.
                  </p>
                  <img
                    src="./assets/img/image 3.jpg"
                    alt="pic"
                    class="product__item_img"
                  />
                  <div class="product__item_footer">
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/like.svg" alt="pic" />
                      <p>157</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/dislike.svg" alt="pic" />
                      <p>5</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/eye.svg" alt="pic" />
                      <p>10 256</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/commentsvg.svg" alt="pic" />
                      <p>12</p>
                    </div>
                  </div>
                </div>
                <div class="product__item">
                  <h4 class="product__item_title">
                    Петров А.В. Телефон Самсунг 0101 - новинка среди смартфонов
                  </h4>
                  <p class="product__item_text">
                    Начало статьи, главная мысль, цитата, статистика, мнение
                    автора, вывод по статье, любой текст.
                  </p>
                  <img
                    src="./assets/img/image 3.jpg"
                    alt="pic"
                    class="product__item_img"
                  />
                  <div class="product__item_footer">
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/like.svg" alt="pic" />
                      <p>157</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/dislike.svg" alt="pic" />
                      <p>5</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/eye.svg" alt="pic" />
                      <p>10 256</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/commentsvg.svg" alt="pic" />
                      <p>12</p>
                    </div>
                  </div>
                </div>
                <div class="product__item">
                  <h4 class="product__item_title">
                    Петров А.В. Телефон Самсунг 0101 - новинка среди смартфонов
                  </h4>
                  <p class="product__item_text">
                    Начало статьи, главная мысль, цитата, статистика, мнение
                    автора, вывод по статье, любой текст.
                  </p>
                  <img
                    src="./assets/img/image 3.jpg"
                    alt="pic"
                    class="product__item_img"
                  />
                  <div class="product__item_footer">
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/like.svg" alt="pic" />
                      <p>157</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/dislike.svg" alt="pic" />
                      <p>5</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/eye.svg" alt="pic" />
                      <p>10 256</p>
                    </div>
                    <div class="pruduct__item_icon-block">
                      <img src="./assets/img/commentsvg.svg" alt="pic" />
                      <p>12</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="consultant col-lg-4 page-sidebar-right">
              <div class="sidebar-header">
                <span class="title">Консультанты</span>
                <div>
                  <img src="./assets/img/sort.svg" alt="Sort" />
                  <img src="./assets/img/filter.svg" alt="Filter" />
                </div>
              </div>
              <div class="sidebar">
                <div class="item">
                  <div class="item-sidebar-header">
                    <p class="title">Иванов Иван Иванович</p>
                    <p class="price">5 000 руб.</p>
                  </div>
                  <div class="details">
                    <div class="labels">
                      <p>Рейтинг</p>
                      <p>Количество консультаций</p>
                    </div>
                    <div class="values">
                      <p>4.4 / 5.0</p>
                      <p>65 шт.</p>
                    </div>
                  </div>
                  <div class="button-group">
                    <button class="secondary-button">Написать</button>
                    <button class="button">Оплатить</button>
                  </div>
                </div>
                <div class="item">
                  <div class="item-sidebar-header">
                    <p class="title">Иванов Иван Иванович</p>
                    <p class="price">5 000 руб.</p>
                  </div>
                  <div class="details">
                    <div class="labels">
                      <p>Рейтинг</p>
                      <p>Количество консультаций</p>
                    </div>
                    <div class="values">
                      <p>4.4 / 5.0</p>
                      <p>65 шт.</p>
                    </div>
                  </div>
                  <div class="button-group">
                    <button class="secondary-button">Написать</button>
                    <button class="button">Оплатить</button>
                  </div>
                </div>
                <div class="item">
                  <div class="item-sidebar-header">
                    <p class="title">Иванов Иван Иванович</p>
                    <p class="price">5 000 руб.</p>
                  </div>
                  <div class="details">
                    <div class="labels">
                      <p>Рейтинг</p>
                      <p>Количество консультаций</p>
                    </div>
                    <div class="values">
                      <p>4.4 / 5.0</p>
                      <p>65 шт.</p>
                    </div>
                  </div>
                  <div class="button-group">
                    <button class="secondary-button">Написать</button>
                    <button class="button">Оплатить</button>
                  </div>
                </div>
                <div class="item">
                  <div class="item-sidebar-header">
                    <p class="title">Иванов Иван Иванович</p>
                    <p class="price">5 000 руб.</p>
                  </div>
                  <div class="details">
                    <div class="labels">
                      <p>Рейтинг</p>
                      <p>Количество консультаций</p>
                    </div>
                    <div class="values">
                      <p>4.4 / 5.0</p>
                      <p>65 шт.</p>
                    </div>
                  </div>
                  <div class="button-group">
                    <button class="secondary-button">Написать</button>
                    <button class="button">Оплатить</button>
                  </div>
                </div>
                <div class="item">
                  <div class="item-sidebar-header">
                    <p class="title">Иванов Иван Иванович</p>
                    <p class="price">5 000 руб.</p>
                  </div>
                  <div class="details">
                    <div class="labels">
                      <p>Рейтинг</p>
                      <p>Количество консультаций</p>
                    </div>
                    <div class="values">
                      <p>4.4 / 5.0</p>
                      <p>65 шт.</p>
                    </div>
                  </div>
                  <div class="button-group">
                    <button class="secondary-button">Написать</button>
                    <button class="button">Оплатить</button>
                  </div>
                </div>
                <div class="item">
                  <div class="item-sidebar-header">
                    <p class="title">Иванов Иван Иванович</p>
                    <p class="price">5 000 руб.</p>
                  </div>
                  <div class="details">
                    <div class="labels">
                      <p>Рейтинг</p>
                      <p>Количество консультаций</p>
                    </div>
                    <div class="values">
                      <p>4.4 / 5.0</p>
                      <p>65 шт.</p>
                    </div>
                  </div>
                  <div class="button-group">
                    <button class="secondary-button">Написать</button>
                    <button class="button">Оплатить</button>
                  </div>
                </div>
                <div class="item">
                  <div class="item-sidebar-header">
                    <p class="title">Иванов Иван Иванович</p>
                    <p class="price">5 000 руб.</p>
                  </div>
                  <div class="details">
                    <div class="labels">
                      <p>Рейтинг</p>
                      <p>Количество консультаций</p>
                    </div>
                    <div class="values">
                      <p>4.4 / 5.0</p>
                      <p>65 шт.</p>
                    </div>
                  </div>
                  <div class="button-group">
                    <button class="secondary-button">Написать</button>
                    <button class="button">Оплатить</button>
                  </div>
                </div>
                <div class="item">
                  <div class="item-sidebar-header">
                    <p class="title">Иванов Иван Иванович</p>
                    <p class="price">5 000 руб.</p>
                  </div>
                  <div class="details">
                    <div class="labels">
                      <p>Рейтинг</p>
                      <p>Количество консультаций</p>
                    </div>
                    <div class="values">
                      <p>4.4 / 5.0</p>
                      <p>65 шт.</p>
                    </div>
                  </div>
                  <div class="button-group">
                    <button class="secondary-button">Написать</button>
                    <button class="button">Оплатить</button>
                  </div>
                </div>
                <div class="item">
                  <div class="item-sidebar-header">
                    <p class="title">Иванов Иван Иванович</p>
                    <p class="price">5 000 руб.</p>
                  </div>
                  <div class="details">
                    <div class="labels">
                      <p>Рейтинг</p>
                      <p>Количество консультаций</p>
                    </div>
                    <div class="values">
                      <p>4.4 / 5.0</p>
                      <p>65 шт.</p>
                    </div>
                  </div>
                  <div class="button-group">
                    <button class="secondary-button">Написать</button>
                    <button class="button">Оплатить</button>
                  </div>
                </div>
                <div class="item">
                  <div class="item-sidebar-header">
                    <p class="title">Иванов Иван Иванович</p>
                    <p class="price">5 000 руб.</p>
                  </div>
                  <div class="details">
                    <div class="labels">
                      <p>Рейтинг</p>
                      <p>Количество консультаций</p>
                    </div>
                    <div class="values">
                      <p>4.4 / 5.0</p>
                      <p>65 шт.</p>
                    </div>
                  </div>
                  <div class="button-group">
                    <button class="secondary-button">Написать</button>
                    <button class="button">Оплатить</button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <footer class="main-footer">
        <div class="footer-content"></div>
      </footer>
    </div>
  </body>
</template>

<style scoped lang="scss">
.items-details .tab-content {
  background-color: #f5f5f5;
  border: none;
}

.nav-tabs {
  border: none;
}

.nav-tabs .nav-link {
  border: none;
}

.nav-tabs .nav-link.active {
  background-color: #f5f5f5;
}

.first-block {
  position: relative;
}

.about-list {
  display: grid;
  grid-template-columns: repeat(2, minmax(200px, 1fr));
}

.about-list-item {
  display: flex;
  gap: 10px;

  span {
    color: #999;
  }
}

.sidebar::-webkit-scrollbar {
  width: 8px;
}
.sidebar::-webkit-scrollbar-thumb {
  background-color: #ccc;
  border-radius: 4px;
}
.sidebar::-webkit-scrollbar-track {
  background-color: #f5f5f5;
}
.sidebar-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 0;
}
.sidebar-header img {
  width: 20px;
  height: 20px;
  cursor: pointer;
  margin-right: 15px;
}
.title {
  font-size: 24px;
  font-weight: bold;
}
.item {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  border-radius: 10px;
  padding: 5px 15px 15px;
  margin-bottom: 10px;
  border: 1px solid #eee;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.05);
  background-color: white;

  p {
    margin: 0;
  }
}
.item-sidebar-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0;
}
.item-sidebar-header .title {
  font-weight: bold;
  font-size: 18px;
  margin: 0;
}
.item-sidebar-header .price {
  font-size: 18px;
  font-weight: bold;
  color: #333;
  margin: 0;
}
.details {
  display: flex;
  justify-content: space-between;
  margin: 10px 0;
}
.details .labels,
.details .values {
  display: flex;
  flex-direction: column;
}
.details .labels p,
.details .values p {
  font-size: 14px;
  color: #666;
}
.button-group {
  display: flex;
  justify-content: space-between;
}
.button {
  background-color: #ffcc00;
  border: none;
  color: white;
  border-radius: 8px;
  cursor: pointer;
  width: 48%;
  height: 30px;
}
.button:hover {
  background-color: #e6b800;
}
.secondary-button {
  background-color: white;
  border: 1px solid #dedede;
  border-radius: 8px;
  cursor: pointer;
  width: 48%;
  height: 30px;
}
.secondary-button:hover {
  background-color: #fff0b3;
}

.second-block {
  border-top: 1px solid rgba(0, 0, 0, 0.2);
  margin-top: 30px;
  margin-bottom: 50px;
  padding-top: 30px;
  position: relative;
}

.consultant .item {
  background-color: #f5f5f5;
}

.product__title {
  font-family: "Roboto", sans-serif;
  font-size: 25px;
  font-weight: 500;
  line-height: 16px;
  margin-top: 20px;
}

.product__path {
  height: 55px;
  display: flex;
  align-items: center;
  gap: 18px;
  overflow-x: auto;
  margin-bottom: 30px;

  p {
    white-space: nowrap;
    margin: 0;
    font-family: "Roboto", sans-serif;
    font-size: 20px;
    font-weight: 400;
    line-height: 16px;
  }
}

.product__path_active {
  color: #336699;
}
.product__path::-webkit-scrollbar {
  height: 8px;
}
.product__path::-webkit-scrollbar-thumb {
  background-color: #ccc;
  border-radius: 4px;
}
.product__path::-webkit-scrollbar-track {
  background-color: #f5f5f5;
}

.pruduct__main {
  display: grid;
  grid-template-columns: repeat(2, minmax(200px, 1fr));
  gap: 20px;
}
.sidebar {
  position: absolute;
  height: 90%;
  width: 33.3333333333%;
  background-color: white;
  border-radius: 10px;
  overflow-y: auto;
}

.product__item {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 30px;
  align-items: center;
  border: 1px solid #ddd;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  border-radius: 10px;
  padding: 10px;
  position: relative;
}

.product__item_title {
  font-family: "Roboto", sans-serif;
  font-size: 20px;
  font-weight: 700;
  line-height: 20px;
}

.product__item_text {
  font-family: "Roboto", sans-serif;
  font-size: 20px;
  font-weight: 400;
  line-height: 20px;
}

.product__item_img {
  width: 60%;
  margin-bottom: 30px;
}

.product__item_footer {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: start;
  gap: 20px;
  margin-top: 20px;
  white-space: nowrap;
  position: absolute;
  bottom: 10px;
  left: 10px;
}

.pruduct__item_icon-block {
  display: flex;
  align-items: center;
  gap: 5px;

  p {
    margin: 4px 0 0 0;
    font-family: "Roboto", sans-serif;
    font-size: 16px;
    font-weight: 400;
    line-height: 16px;
    color: #999999;
  }
}

@media (max-width: 1000px) {
  .sidebar {
    position: static;
    width: 100%;
  }
}

@media (max-width: 768px) {
  .pruduct__main {
    display: grid;
    grid-template-columns: repeat(1, minmax(200px, 1fr));
    gap: 20px;
  }
}
</style>
