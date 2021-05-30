<template>
  <div class="col-10 mt-5">
    <div id="info" class="mt-5">
      <h2>Olá, eu sou o Walmir Silva. ^</h2>
      <br>
      <p>Este pequeno projeto foi desenvolvido para praticar tecnicas de desenvolvimento web.</p>
      <br />
      <span>Você pode ver esse e mais projetos em: </span> <a href='https://github.com/WSilva99'> https://github.com/WSilva99 </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
  mounted() {
    var back = document.getElementById("app");
    back.classList.remove("animate-back");
    back.classList.remove("stop-back");
    back.classList.add("me-back");

    var infos = Array.prototype.slice.call(document.getElementById("info").children);
    var t_infos = []
    infos.forEach((info) => {
        t_infos.push(info.innerText);
    })
    infos.forEach((i) => i.innerText = "");

    var tap_time = 65;

    
    var typing = 0;
    infos.forEach((info, i) => {
      var text = t_infos[i].split("");
      setTimeout(() => {
        info.classList.add("typing");
        var time = 0;
        text.forEach((c, j) => {
          time = tap_time * j;
          setTimeout(() => {
            if(c == '^') {
              info.innerHTML += "👋🏼";
            } else {
              info.innerHTML += c;
            }
          }, time);
        });
        setTimeout(() => {
          info.classList.remove("typing");
        }, time + tap_time);
      }, typing);
      typing += text.length * tap_time;
    });
  },
};
</script>

<style lang="scss">
@import url("../assets/style.scss");

a {
  color: var(--light)
}

</style>
