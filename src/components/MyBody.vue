<template>
  <div class="body container">
    <div class="text_container">
      <div class="text">
        <h1>Мы любим животных
          и поддерживаем их</h1>
        <p>Один из проверенных способов это сделать
          — помочь благотворительному фонду</p>
        <button class="text-button">Кнопка добра</button>
      </div>
    </div>
    <div class="image_container">
      <img src="./../assets/svg/01.svg" alt="img">
    </div>
  </div>
</template>

<script>
export default {
  name: 'my-body'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.text-button {
  color: #FFFFFF;
  background-color: black;
  padding: 8px 40px;
  font-size: 20px;
  margin-top: 30px;
  margin-right: 460px;
  cursor: pointer;
  transition: 0.3s;
}
.text-button:hover {
  background-color: #FF6E1F;
  color: black;
  border-radius: 5px;
}
.body {
  display: flex;
  flex-direction: row;
  align-items: center;
}
.text_container {
  width: 45%;
  display: flex;
  flex-direction: column;
  margin-left: 100px;
}
.text h1 {
  font-size: 45px;
  text-align: left;
  margin-bottom: 30px;
}
.text p {
  font-size: 30px;
  text-align: left;
  line-height: 40px;
}
.image_container {
  width: 50%;
  border-left: 2px solid black;
}
.image_container img {
  width: 100%;
  padding: 40px 20px;
  transition: 0.5s ease-in-out;
}
.image_container img:hover {
  width: 98%;
}
.container {
  margin: 0 auto;
  margin-bottom: 20px;
  border: 2px black solid;
}
@media (min-width: 320px) and (max-width: 1400px) {
.body {
  flex-direction: column;
  padding-top: 90px;
}
  .image_container {
    border-left: 0px;
  }
  .text p {
    text-align: center;
  }
  .text h1 {
    text-align: center;
  }
  .text_container {
    margin-left: 0px;
  }
  .text-button {
    margin-right: 0px;
  }
  .image_container {
    width: 98%;
    padding-top: 30px;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .text_container {
    width: 90%;
  }
}
@media (min-width: 320px) and (max-width: 761px) {
.text h1 {
  text-align: left;
}
  .text p {
    text-align: left;
  }
  .text_container {
    width: 100%;
    padding-left: 30px;
  }
  .text-button {
    margin-right: 480px;
  }
}
</style>
