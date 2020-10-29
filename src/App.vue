<template>
  <div id="app">


    <i-container class="container">
  <img alt="Vue logo" src="./assets/logo.png" class="text-center">
      <i-row>
        <i-column class="border-right" sm="6">
          <h1>Markdown</h1>
<i-textarea 

 :class="$style.textarea"
 v-model="text"
  placeholder="##Entrez votre texte en markdown ici.."
 
  />
  <hr>
        </i-column>
          <i-column sm="6">
            <h1>Texte formaté exemples</h1>

<div class="block">
<vue-markdown :source="text1" > 
</vue-markdown>


    </div>
  
     <div class="block">
     <vue-markdown :source="text2" >
</vue-markdown>
  </div>
  <h1>Résultat</h1>

     <div class="block">
     <vue-markdown :source="text" >
</vue-markdown>
  </div>


          </i-column>
          
    </i-row> 
   <p>&copy; 2020 <a href="https://rismo.fr">rismo.fr</a></p>
    </i-container>  

  </div>

</template>
 
<script>
import VueMarkdown from 'vue-markdown'
export default {
  name: 'App',
  components: {
    VueMarkdown
  
  },
  data(){


    return {
      text:'',
       titre:'Example1 ',
      text1:'*Un texte en italique avec un lien  [Markdown](https://guides.github.com/features/mastering-markdown/)*',
       titre2:'Example2 ',
      text2:'Insertion de code `<h1 class="text-muted">code</h1>`'
    }
  }
}
</script>



<style scoped>


.container{
  margin-top: 40px;
  align-items: center;
  
}
.block

{

  background-color:rgba(238, 238, 238, 0.829) ;
 color:rgb(51, 65, 4);
}

.border-right {

  border-right: 5px solid rgba(0, 255, 157, 0.623) ;
}
p, a
{

  color:rgb(6, 194, 131);
  background-color: black;
}

</style>

<style module>


  textarea{

  height: 400px;

  width:100% ;
  resize: none;
  outline: none;

 
}


</style>


