<template lang="pug">

  div.main#card
    div.main__head
      img(class="main__img" src="https://static.platzi.com/media/user_upload/Page%201-d8d869f4-7130-4ae9-9907-2fa809bd136a.jpg" alt="altText")
    div.main__title.font-weight-medium
      h1.title Register App
    form
      div.main__body

        div.main__labels
          label(for="name|") Email:
          input(class="" id="name" type="text" placeholder="")
      
        div.main__labels
          label(for="lastname") User
          input(class="" id="lastname" type="text" placeholder="")
        div.main__labels
          label(for="lastname") Password:
          input(class="" id="lastname" type="text" placeholder="")

        div.main__footer
          label(for="check")
          input(class="" id="check" type="checkbox" v-model="check")
          p Acepto
          input(class="button" type="button" @click="" value="Registrar" )

</template>


<script>
export default {
  name: 'login-app',
  data(){
    return {
      check : false
    }
  },

  watch: {
    check(){
        const card = document.getElementById('card')
        card.classList.toggle('animation')
        console.log(card)
    }
  }
}
</script>

<style lang="sass" scoped>

  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap')

  .main   
    font-family: 'Roboto', sans-serif

  label   
    display: block
    color: #ff9300
    font-size: 16px


  .main__labels, .main__footer 
    padding: 10px
    width: 100%

  .button 
    float: right 
    border-radius: 5px   
    background-color: #00bfd6
    padding: 10px 20px
    color: white
    font-size: 16px
    font-weight: bold

  .main 
    width: 320px
    height: 432px
    padding: 20px 20px
    box-shadow: 20px 20px 30px rgba(0,0,0, 0.4)
    border-radius: 10px
    background-color: #fff
    box-sizing: border-box

  .main__head 
    position: relative
    height: 110px

  .main__img 
    position: absolute
    left: 50%
    transform: translateX(-50%)

  .main__title 
    text-align: center
    color: #00bfd6

  .main__body 
    display: flex
    justify-content: center
    align-items: flex-start
    padding: 0 20px
    flex-direction: column

  .main__labels input 
    border-bottom: 2px solid #EFB123
    width: 100%
    margin-top: 5px

  .main__footer
    display: flex
    justify-content: space-between
    align-items: center

  @media screen and (min-width: 600px)
    .animation 
      animation: .3s move linear alternate 2

    @keyframes move 
      to 
        transform: translatey(-10px)
      
</style>
