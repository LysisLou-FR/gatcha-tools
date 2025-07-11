<template>
    <div class="page-content">
        <header class=""></header>
        <div class="content">
            <h1>{{ msg }}</h1>
            <div class="row stat-cards">
                <div class="col-md-6 col-xl-3">
                    <article class="stat-cards-item">
                        <div class="stat-cards-icon primary">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-feather" aria-hidden="true"><path d="M20.24 12.24a6 6 0 0 0-8.49-8.49L5 10.5V19h8.5z"></path><line x1="16" y1="8" x2="2" y2="22"></line><line x1="17.5" y1="15" x2="9" y2="15"></line></svg>
                        </div>
                        <div class="stat-cards-info">
                            <p class="stat-cards-info__num">3</p>
                            <p class="stat-cards-info__title">Espers</p>
                        </div>
                    </article>
                </div>
                <div class="col-md-6 col-xl-3">
                    <article class="stat-cards-item">
                        <div class="stat-cards-icon warning">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-file" aria-hidden="true"><path d="M13 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V9z"></path><polyline points="13 2 13 9 20 9"></polyline></svg>
                        </div>
                        <div class="stat-cards-info">
                            <p class="stat-cards-info__num">1478 286</p>
                            <p class="stat-cards-info__title">Total visits</p>
                        </div>
                    </article>
                </div>
                <div class="col-md-6 col-xl-3">
                    <article class="stat-cards-item">
                        <div class="stat-cards-icon purple">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-file" aria-hidden="true"><path d="M13 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V9z"></path><polyline points="13 2 13 9 20 9"></polyline></svg>
                        </div>
                        <div class="stat-cards-info">
                            <p class="stat-cards-info__num">1478 286</p>
                            <p class="stat-cards-info__title">Total visits</p>
                        </div>
                    </article>
                </div>
                <div class="col-md-6 col-xl-3">
                    <article class="stat-cards-item">
                        <div class="stat-cards-icon success">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-feather" aria-hidden="true"><path d="M20.24 12.24a6 6 0 0 0-8.49-8.49L5 10.5V19h8.5z"></path><line x1="16" y1="8" x2="2" y2="22"></line><line x1="17.5" y1="15" x2="9" y2="15"></line></svg>
                        </div>
                        <div class="stat-cards-info">
                            <p class="stat-cards-info__num">1478 286</p>
                            <p class="stat-cards-info__title">Total visits</p>
                        </div>
                    </article>
                </div>
            </div>
            <p>For a guide and recipes on how to configure / customize this project,<br>
            check out the<a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
            </p>
            <h3>Installed CLI Plugins</h3>
            <ul>
                <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
                <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
            </ul>
            <h3>Essential Links</h3>
            <ul>
                <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
                <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
                <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
                <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
                <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
            </ul>
            <h3>Ecosystem</h3>
            <ul>
                <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
                <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
                <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
                <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
                <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
            </ul>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
export default {
    name: 'PageContent',
    props: {
        msg: String
    },
    data () {
            return {
                info: null
            }
    },
    mounted () {
        axios
            .get('http://144.24.195.162:1337/api/espers')
            .then(response => (this.info = response.data))
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import '@/assets/css/variables.scss';
.page-content {
    flex: auto;
    background-color: rgba(255,255,255,0.05);
    background-image: url('../assets/mask-dislyte.svg');
    background-repeat: no-repeat;
    background-size: 40rem;
    background-position: bottom right;
}
header {
    display: block;
    width: 100%;
    height: 8rem;
    background: linear-gradient(90deg, #8F77FF 0%, #B8A8FF 100%);
}
.content {
    padding: 2.5rem 2rem;
}
h1 {
    margin: 0;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: $base-green;
}
.stat-cards {
    margin: 2rem -1rem 0 -1rem;
    > * {
        padding-left: 1rem;
        padding-right: 1rem;
        margin-bottom: 2rem;
    }
}
.stat-cards-item {
    padding: 1.2rem;
    background-color: rgba(255,255,255,0.05);
    box-shadow: 0 15px 50px rgba(160, 163, 189, 0.1);
    border-radius: 10px;
    height: 100%;
}
.stat-cards-icon {
    justify-content: center;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    margin-right: 9px;
}
.stat-cards-icon,
.stat-cards-item {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
}
.stat-cards-icon.primary {
    background-color: rgba(47,73,209,.1);
    color: #2f49d1;
}
.stat-cards-icon.purple {
    background-color: rgba(95,46,234,.1);
    color: #5f2eea;
}
.stat-cards-icon.warning {
    background-color: rgba(255,182,72,.1);
    color: #ffb648;
}
.stat-cards-icon.success {
    background-color: rgba(75,222,151,.1);
    color: #4bde97;
}
.stat-cards-info__num {
    font-weight: 600;
    font-size: 18px;
    line-height: 1.22;
    color: #b9b9b9;
    margin: 0 0 4px 0;
}
.stat-cards-info__title {
    font-weight: 500;
    font-size: 14px;
    line-height: 1.22;
    color: #b9b9b9;
    margin: 0;
}
</style>
