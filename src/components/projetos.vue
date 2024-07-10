<script>
export default {
    name: 'Projetos',

    data() {
        return {
            acesso_back: false,
            acesso_front: false
        }
    },

    methods: {
        ativar_back() {
            this.acesso_back = !this.acesso_back
        },
        ativar_front() {
            this.acesso_front = !this.acesso_front
        }
    }
}
</script>

<template>
    <div class="main">
        <ul>
            <p class="text2"> "Navegue através dos projetos em meu portfólio, representando uma jornada de muito estudo
                e
                dedicação. Cada
                projeto é uma narrativa única de desafios superados e metas alcançadas, refletindo meu profundo amor por
                tecnologia e áreas afins. Convido você a mergulhar em cada realização, e sinta-se à vontade para
                esclarecer
                dúvidas ou explorar os links para compreender o funcionamento de cada projeto. Um grande Abraço."</p>
            <div class="ass">
                <p class="text3">Carlos Eduardo</p>
                <p class="text3">Desenvolvedor de Software</p>
            </div>
            <p class="titulo" @click="ativar_back()">Meus Projetos BackEnd
                <img class="icone_seta" src="../assets/seta-para-baixo.png" alt="" v-show="acesso_back == false">
                <img class="icone_seta" src="../assets/seta-para-cima.png" alt="" v-show="acesso_back == true">
            </p>

            <div class="lis">

                <li v-show="acesso_back == true">
                    <a href="https://apicadastropessoasdockerimage.onrender.com">
                        <img class="imagem_projeto" src="../assets/imagens_projetos/api_pessoas.png" alt="">
                        <p class="text">API completa para um sistema de
                            cadastro de Pessoas, com CRUD de dados pessoais e imagens, em banco SQL (PostgreSQL)</p>
                        <p class="ver_mais">Clique e Veja Mais Sobre Este Projeto </p>
                    </a>
                </li>

                <li v-show="acesso_back == true">
                    <a href="https://apipublicanaruto.onrender.com">
                        <img class="imagem_projeto" src="../assets/imagens_projetos/naruto.png" alt="">
                        <p class="text">API com personagens do Naruto</p>
                        <p class="ver_mais">Clique e Veja Mais Sobre Este Projeto</p>
                    </a>
                </li>
            </div>
            <div class="lis">
                <li v-show="acesso_back == true">
                    <a href="https://pessoasfaker.onrender.com">
                        <img class="imagem_projeto" src="../assets/imagens_projetos/pessoasfaker.png" alt="">
                        <p class="text">API dados fictícios de pessoas para
                            testes com chamadas de api.</p>
                        <p class="ver_mais">Clique e Veja Mais Sobre Este Projeto </p>
                    </a>
                </li>
                <li v-show="acesso_back == true">
                    <a href="https://rhpredict-github-backend.onrender.com/">
                        <img class="imagem_projeto" src="../assets/imagens_projetos/api_machine.png" alt="">
                        <p class="text">API para análisar a permanência de uma pessoa em uma empresa, utilizando
                            tecnicas de machine learning.</p>
                        <p class="ver_mais">Clique e Veja Mais Sobre Este Projeto </p>
                    </a>
                </li>
            </div>

            <p class="titulo" @click="ativar_front()">Meus Projetos FrontEnd
                <img class="icone_seta" src="../assets/seta-para-baixo.png" alt="" v-show="acesso_front == false">
                <img class="icone_seta" src="../assets/seta-para-cima.png" alt="" v-show="acesso_front == true">

            </p>

            <div class="lis">
                <li v-show="acesso_front == true">
                    <a href="https://icnvararuama.com.br">
                        <img class="imagem_projeto" src="../assets/imagens_projetos/igreja.png" alt="">
                        <p class="text">Site de informações, e aplicação de cadastro de membros de uma igreja.
                            Rodando perfeitamente. Hospedagem da API no render, e do front no Netlify.</p>
                        <p class="ver_mais">Clique e Veja Mais Sobre Este Projeto </p>
                    </a>
                </li>

                <li v-show="acesso_front == true">
                    <a href="https://exemplositeigreja.netlify.app/">
                        <img class="imagem_projeto" src="../assets/imagens_projetos/igrejaexemplo.png" alt="">
                        <p class="text">Site de informações, e aplicação de cadastro de membros de uma igreja.
                            Site Exemplo. Rodando perfeitamente. Hospedagem da API no render, e do front no Netlify.</p>
                        <p class="ver_mais">Clique e Veja Mais Sobre Este Projeto </p>
                    </a>
                </li>
            </div>


            <div class="lis">
                <li v-show="acesso_front == true">
                    <a href="https://academialandingpage.netlify.app/">
                        <img class="imagem_projeto" src="../assets/imagens_projetos/academia.png" alt="">
                        <p class="text">Landing Page para uma academia. Para Desktop, Site Exemplo. Hospedagem no
                            Netlify</p>
                        <p class="ver_mais">Clique e Veja Mais Sobre Este Projeto </p>
                    </a>
                </li>

                <li v-show="acesso_front == true">
                    <a href="https://eunocontrole.netlify.app/">
                        <img class="imagem_projeto" src="../assets/imagens_projetos/eunocontrole.png" alt="">
                        <p class="text">Esta aplicação é um gerenciador de listas de compras. Com ela, você pode criar e
                            organizar suas listas de produtos de maneira prática e eficiente.</p>
                        <p class="ver_mais">Clique e Veja Mais Sobre Este Projeto</p>
                    </a>
                </li>

            </div>
        </ul>
    </div>
</template>


<style scoped>
@media (max-width: 720px) {

    .main {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .lis {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    ul {
        color: #f3f3f3;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        list-style-type: none;
    }

    li {
        width: 85%;
        border: 0.05rem solid #f3f3f3;
        border-radius: 5px;
        margin: 10px 0px;
    }

    a {
        text-decoration: none;
        width: 100%;
    }

    .titulo {
        color: #000000;
        font-size: 1rem;
        padding: 15px;
        font-weight: bold;
        letter-spacing: 2px;
        border-radius: 10px;
        background-color: #e9ca65;
        margin: 10px 0px;
        cursor: pointer;
    }

    .text {
        color: #000000;
        font-size: 0.9rem;
        text-align: center;
        padding: 10px 7px;
        background-color: #c9c9c9;
    }

    .text2 {
        color: #c9c9c9;
        font-size: 1.1rem;
        text-align: justify;
        width: 85%;
        margin: 20px 0px 5px 0px;
        line-height: 1.3;

    }

    .ass {
        display: flex;
        flex-direction: column;
        align-items: end;
        justify-content: center;
        width: 90%;
        padding: 18px 0px;
    }

    .text3 {
        color: #e2e2e2;
        font-size: 0.9rem;
        text-align: justify;
        padding: 0px 7px;
    }

    .exemplo {
        color: aliceblue;
    }

    .imagem_projeto {
        border-radius: 10px 10px 0px 0px;
        width: 100%;
    }

    .ver_mais {
        color: #000000;
        background-color: #e2e1b8;
        padding: 6px;
        height: 40px;
        width: 100%;
        font-size: 0.4;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        font-weight: bold;
        text-align: center;

    }

    .icone_seta {
        width: 15px;
    }
}

@media (min-width: 721px) {

    .main {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    ul {
        color: #f3f3f3;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        list-style-type: none;
    }

    .lis {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        width: 100%;
        gap: 1%;
    }

    li {
        width: 30%;
        border: 0.05rem solid #f3f3f3;
        border-radius: 5px;
        margin: 10px 0px;
    }

    a {
        text-decoration: none;
        width: 100%;
    }

    .titulo {
        color: #000000;
        font-size: 1rem;
        padding: 15px;
        font-weight: bold;
        letter-spacing: 2px;
        border-radius: 10px;
        background-color: #e9ca65;
        margin: 10px 0px;
        cursor: pointer;

    }

    .text {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        color: #000000;
        font-size: 0.9rem;
        text-align: center;
        padding: 10px 7px;
        background-color: #c9c9c9;
        height: 80px;
    }

    .text2 {
        color: #c9c9c9;
        font-size: 1.1rem;
        text-align: justify;
        width: 85%;
        margin: 20px 0px 5px 0px;
        line-height: 1.3;

    }

    .ass {
        display: flex;
        flex-direction: column;
        align-items: end;
        justify-content: center;
        width: 90%;
        padding: 18px 0px;
    }

    .text3 {
        color: #e2e2e2;
        font-size: 0.9rem;
        text-align: justify;
        padding: 0px 7px;
    }

    .exemplo {
        color: aliceblue;
    }

    .imagem_projeto {
        border-radius: 10px 10px 0px 0px;
        width: 100%;
    }

    .ver_mais {
        color: #000000;
        background-color: #ffae00;
        padding: 6px;
        height: 40px;
        width: 100%;
        font-size: 0.4;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        font-weight: bold;
        text-align: center;

    }

    .icone_seta {
        width: 15px;
    }
}
</style>