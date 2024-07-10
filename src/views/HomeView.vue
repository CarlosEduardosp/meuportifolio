<script>
import Projetos from '../components/projetos.vue';

export default {
  name: 'Home',

  components: {
    Projetos
  },

  data() {
    return {
      acesso_projetos: false,

    }
  },

  methods: {
    ativar_projetos() {
      this.acesso_projetos = !this.acesso_projetos
    },


  }
}
</script>

<template>
  <div class="main">

    <div class="titulo">
      <img class="imagem_inicial" src="../assets/logo-carlos-eduardo.png" alt="">
    </div>

    <div class="separador"></div>


    <div class="div_frase" v-show="acesso_projetos == false">
      <img class="imagem_perfil" src="../assets/kadu.jpg" alt="" v-show="acesso_projetos == false">
      <div class="frases">
      <p class="frase">

        Olá! Sou Carlos Eduardo, também conhecido como 'Kadu' entre amigos, possuo experiência como desenvolvedor
        Python especializado em backend. Com foco na criação de APIs seguindo os princípios da Clean
        Architecture. E no frontend possuo habilidades com Javascript, Css, HTML e VuesJS.       
      </p>
      <ul class="frase">
        Tecnologias e Habilidades Principais:

        <li class="topicos">Frameworks: Experiência com Flask e FastAPI.</li>
        <li class="topicos">Bancos de Dados: Utilização proficiente de ORMs como SQLAlchemy e psycopg2 para integração com PostgreSQL.</li>
        <li class="topicos">Contêineres e Deploy: Domínio em Docker para gerenciamento de contêineres e experiência em deploys no
        Google Cloud Platform (GCP) e outras plataformas como Render.</li>
        <li class="topicos">Testes e Automação: Familiaridade com Pytest para testes unitários e de integração, automação de processos com
        CI/CD utilizando GitHub Actions.</li>
        <li class="topicos">Arquitetura e Design: Aplicação dos princípios SOLID, arquiteturas modulares, injeção de dependência e design
        patterns.</li>
        <li class="topicos">Desenvolvimento de APIs: Implementação de REST APIs, seguindo boas práticas de desenvolvimento de software.</li>
        <li class="topicos">Testes de Integração: Experiência em testes de integração utilizando ferramentas como Postman.</li>
        <li class="topicos">Versionamento e Colaboração: Uso eficaz de Git e GitHub para versionamento de código e colaboração em equipe.</li>        
        </ul>
      <p class="frase">
        Estou sempre em busca de novos desafios no desenvolvimento de software, focado em criar soluções de qualidade e
        escaláveis.
      </p>
      </div>
    </div>

    <Projetos class="componente_projetos" v-show="acesso_projetos == true"></Projetos>



    <div class="final">

      <div class="decora_btn" @click="ativar_projetos()">
        <a class="projetos" href="#">
          <img class="icone_projeto" src="../assets/portifolio.png" alt="" v-show="acesso_projetos == false">
          <img class="icone_projeto" src="../assets/voltar.png" alt="" v-show="acesso_projetos == true">

          <p class="mensagem" v-show="acesso_projetos == false">Conheça meus Projetos</p>
          <p class="mensagem" v-show="acesso_projetos == true">Voltar a Página Anterior</p>
        </a>
      </div>

      <div class="btns">

        <div>
          <a href="https://www.linkedin.com/in/carlos-eduardo-padilha-0a105040/">
            <img class="icone" src="../assets/linkedin-112.svg" alt="">
          </a>
          <a href="https://www.facebook.com/?_rdc=2&_rdr">
            <img class="icone" src="../assets/facebook-logo.png" alt="">
          </a>
          <a href="https://www.instagram.com/kadu_spadilha/">
            <img class="icone" src="../assets/instagram.png" alt="">
          </a>
        </div>
        <div>
          <a href="https://wa.me/qr/VLUWS67P35KPN1">
            <img class="icone" src="../assets/whatsapp_1384023.png" alt="">
          </a>
          <a href="https://github.com/CarlosEduardosp">
            <img class="icone" src="../assets/github-logo.png" alt="">
          </a>
          <a href="mailto:carlos.spadilha@yahoo.com.br?subject=Olá, Vi o Seu Portifólio ! ">
            <img class="icone" src="../assets/o-email.png" alt="">
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
@media (max-width: 720px) {
  .main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
  }

  .nome {
    color: #fff;
    font-size: 1.5rem;
  }

  .separador {
    width: 100%;
    height: 1.5px;
    background-color: #fff;
  }

  .imagem_perfil {
    width: 80%;
    margin-top: 20px;
    border-radius: 20px;
    box-shadow: 0px 0px 10px 2px #ffffff;
  }

  .div_frase {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 83%;
  }

  .frase {
    text-align: justify;
    margin-top: 20px;
    font-size: 0.87rem;
    color: #c9c9c9;
  }

  .icone {
    width: 50px;
    border-radius: 10px;
    padding: 5px;
    margin: 5px;
    background-color: #fff;
  }

  .icone_projeto {
    width: 60px;
    border-radius: 10px;
    background-color: #fff;
  }

  .decora_btn {
    width: 150px;
    height: 115px;
    background-color: #fff;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .final {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 10px;
    margin-top: 10px;
    margin-bottom: 20px;
  }

  .mensagem {
    color: black;
    text-align: center;
    font-weight: bold;
  }

  .imagem_inicial {
    width: 80%;
    margin: 5px;
    margin-top: 10px;
  }

  .titulo {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 10px;
  }

  .projetos {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-decoration: none;
  }

  .componente_projetos {}

  p {
    color: #fff;
  }

  .topicos{
    font-size: 0.8rem;
    margin-left: 5%;
    color: #f1f1f1;
    line-height: 1.2rem;
  }
}

@media (min-width: 721px) {
  .main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
  }

  .nome {
    color: #fff;
    font-size: 1.5rem;
  }

  .separador {
    width: 100%;
    height: 1px;
    background-color: #fff;
  }

  .imagem_perfil {
    width: 30%;
    margin-top: 0%;
    border-radius: 20px;
    box-shadow: 0px 0px 10px 2px #ffffff;
  }

  .div_frase {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    width: 83%;
    margin-top: 2%;
    gap: 10%;
  }

  .frase {
    text-align: justify;
    margin-top: 0px;
    font-size: 0.85rem;
    color: #c9c9c9;
    line-height: 160%;
    margin: 0.5% 0%;
  }

  .icone {
    width: 50px;
    border-radius: 10px;
    padding: 5px;
    margin: 5px;
    background-color: #fff;
  }

  .icone_projeto {
    width: 60px;
    border-radius: 10px;
    background-color: #fff;
  }

  .decora_btn {
    width: 150px;
    height: 115px;
    background-color: #fff;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .final {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 10px;
    margin-top: 10px;
    margin-bottom: 20px;
  }

  .mensagem {
    color: black;
    text-align: center;
    font-weight: bold;
  }

  .imagem_inicial {
    width: 20%;
    margin: 5px;
    margin-top: 10px;
  }

  .titulo {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 10px;
  }

  .projetos {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-decoration: none;
  }

  .componente_projetos {}

  p {
    color: #fff;
  }

  .frases{
    display: flex;
    flex-direction: column;
    align-items:baseline;
    justify-content: center;
  }

  .topicos{
    font-size: 0.8rem;
    margin-left: 5%;
    color: #f1f1f1;
  }
}
</style>