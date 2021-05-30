<template>
  <div class="col-8 offset-1">
    <div id="display" class="typing"></div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      frase: "",
      frases: [
        "Cientificamente falando, tradições são uma coisa idiota.",
        "Eu odeio dizer isso a você, mas o que as pessoas c… reação química que obriga os animais a procriar.",
        "Casamentos são, basicamente, funerais com bolo.",
        "Existência é dor.",
        "Ninguém existe por um propósito. Ninguém pertence a lugar nenhum. Todo mundo vai morrer.",
        "A vida é esforço e vou parar quando morrer!",
        "Quando você tem noção de que nada importa, o universo é seu.",
        "Ter uma família não significa que você deixa de ser um indivíduo.",
        "Você sabe o melhor que pode fazer pelas pessoas qu… com elas, mesmo que isso signifique libertá-las.",
        "Eu riria, mas sou biologicamente incapaz.",
        "Então todo mundo deveria dormir todas as noites ag… Você percebe que a noite compõe metade do tempo?",
        "Vou lhe contar como me sinto em relação à escola, Jerry: é uma perda de tempo.",
        "Eles são burocratas. Eu não respeito eles.",
        "Deus não existe. Tem que arrancar esse curativo agora. Você vai me agradecer depois.",
        "Eu acho que você tem que pensar no futuro e viver o momento.",
        "Eu não respeito a terapia, porque sou cientista.",
        "Há uma lição aqui e não vou ser o único a descobrir isso.",
        "Se eu aprendi uma coisa hoje, é que às vezes você não precisa se importar!",
        "Se eu quisesse ficar sóbrio, não teria ficado bêbado.",
        "Planejar o fracasso é ainda mais idiota do que simplesmente planejar.",
        "Ouça, eu não sou o cara mais legal do Universo por…ssoas estúpidas fazem para proteger suas apostas.",
        "Escola não é um lugar para pessoas inteligentes.",
        "Minha geração fica traumatizada logo no café da manhã.",
        "Você é o caçula. Você não é a causa da tristeza dos seus pais, você é só um sintoma disso.",
        "Minha vida tem sido uma mentira!",
        "Eu sei que novas situações podem ser intimidadoras…mo um touro - é assim que crescemos como pessoas.",
        "Parece um bom momento para uma bebida e um discurso frio e calculado com um tom sinistro.",
        "É sua escolha tornar isso pessoal.",
        "Eu pensei que o objetivo de ter um cachorro era se sentir superior.",
        "Algumas pessoas não aguentam a verdade.",
        "Nada do que você faz importa.",
        "Minha vida é uma piada!",
        "O governo é ridículo!",
        "Desculpe, mas sua opinião significa muito pouco para mim.",
        "Viver é arriscar tudo!",
        "Rosas estão mortas. O amor é falso.",
        "A ciência é sábia, siga seus conselhos.",
        "Eu não faço mágica, eu faço ciência.",
        "Isso acontece porque os perdedores buscam coisas enquanto o resto de nós trabalha diariamente.",
        "Você é um pedaço de merda e eu posso provar matematicamente.",
        "Se você brincar um pouco com as palavras, consegue fazer qualquer coisa soar bem (ou mal).",
        "Viver é arriscar tudo. Caso contrário você é apena…aleatoriamente à deriva onde o universo te sopra.",
        "Ninguém existe de propósito, ninguém pertence a lugar nenhum.",
        "O amor é apenas uma reação química.",
        "Planejar o fracasso é ainda mais idiota do que simplesmente planejar.",
        "Casamentos são como velórios com bolo.",
        "Então é suposto todo mundo dormir todas as noites …que metade de todo o tempo que existe é de noite?",
        "Ninguém existe de propósito. Ninguém pertence a qu…lugar. Todo mundo vai morrer... Venha assistir TV",
        "Eu vou te dizer o que eu acho das escolas, Jerry: … Escola não é um lugar para pessoas inteligentes.",
        "Ninguém existe por um propósito. Ninguém pertence a lugar nenhum. Todo mundo vai morrer. Vem ver TV.",
        "Você é tipo Hitler, mas pelo menos Hitler se importava com a Alemanha ou algo do tipo.",
        "Se Deus existe, eu sou Ele!",
        "Qual a chance de ser legítimo e não uma mentira qu…a nós mesmo porque temos medo de morrer sozinhos?",
      ],
    };
  },
  beforeMount() {
    let sort = Math.floor(Math.random() * this.frases.length);
    this.frase = this.frases[sort];
  },
  mounted() {
    var animate = document.getElementById("app");
    animate.classList.remove("me-back")
    animate.classList.add("animate-back")
    const frase = this.frase.split("");
    var display = document.getElementById("display");
    var time = 0;
    var tap_time = 75;
    frase.forEach((letra, i) => {
      time = tap_time * i;
      setTimeout(() => (display.innerHTML += letra), time);
    });
    setTimeout(() => {
      display.classList.remove("typing");
    }, time + 2*tap_time);
    setTimeout(() => {
      animate.classList.replace("animate-back", "stop-back");
    }, time);
  },
};
</script>

<style lang="scss">
@import url("../assets/style.scss");
</style>
