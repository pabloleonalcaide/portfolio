<template>
     <div id="articles">
        <h2 class="heading">Sometimes I Write...</h2>
        <div class="container">
            <div class="row">
                <div class="article-block shadow-large article">
                    <div class="article-image">
                        <img :src="image" />
                    </div>
                    <div class="article-info">
                        <h3>Una Introducción a la Programación Orientada a Aspectos</h3>
                        <p>
                            Article of the talk made during the <a href="https://informatica.iesgrancapitan.org/sysmanas/sysmana-xi/">Sysmana</a> event in February 2019 about Aspect Oriented Programming and its application in the Spring Framework
                        </p>
                        <a href="https://medium.com/@PabloLeonPsi/una-aproximaci%C3%B3n-a-la-programaci%C3%B3n-orientada-a-aspectos-a62d377ebe79">View Article</a>
                    </div>
                </div>
                <div class="article-block shadow-large article">
                    <div class="article-image">
                        <img :src="image" />
                    </div>
                    <div class="article-info">
                        <h3>Git histories</h3>
                        <p>
                            Articles about my experience with Git and Github, adding some initial tips and recommendations
                        </p>
                        <a href="https://medium.com/@PabloLeonPsi/mi-primer-d%C3%ADa-con-github-5a11ae2bd250">Mi primer día con Git</a> | 
                        <a href="https://medium.com/@PabloLeonPsi/descubriendo-git-mas-all%C3%A1-del-add-commit-push-6efaed8ae26e">Descubriendo Git</a>
                    </div>
                </div>
                                <div class="article-block shadow-large article">
                    <div class="article-image">
                        <img :src="image" />
                    </div>
                    <div class="article-info">
                        <h3>Apuntes sobre Arquitecturas Limpias</h3>
                        <p>
                            Introductory notes about clean architectures in software development
                        </p>
                        <a href="https://medium.com/@PabloLeonPsi/apuntes-sobre-arquitecturas-limpias-de-software-vol-1-1a91131933e2">View Article</a>
                    </div>
                </div>
            </div>
        </div>
    </div> 
</template>
<script>
export default {
  name: 'Articles',
  data () {
      return{
          image: require('@/assets/articles.png')
      }
  }
}
</script>
<style lang="scss">

$heading: #333333;
$text: #74808a;

#articles{
    text-align: center;
}
.article{
    flex-direction:row-reverse;
}
.article-block{
    position: relative;
    max-width: 900px;
    margin: 0 auto 30px auto;
    overflow: hidden;
    background: #fff;
    border-radius: 4px;
    display: flex;
    border-radius: 40px 4px 4px 40px;
}
.article-image {
    flex: 0 0 15em;
    img{
        width: 100%
    }
}

.article-info {
    padding: 15px;

    h3 {
        font-size: 1.5em;
        font-weight: 300;
        color: $heading;
        margin: 0 0 15px 0;
    }

    p {
        color: $text;
        margin: 0 0 15px 0;
        font-size: 0.9em;
    }
}
</style>
