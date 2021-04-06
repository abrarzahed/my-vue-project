<template>
  <div id="contact">
    <div class="contact-info"  v-if="submited">
        <h2>Contact info</h2>
        <p>Mobile : +00000000000</p>
        <p> Email : example@gmail.com</p>
        <p><Address>Road no:23, House no: 4 <br> Dhaka bangladesh</Address></p>

    </div>
    <div class="congrats"  v-if="!submited">
        <h2>Thank you {{ name }}</h2>
        <p>we will talk to very soon</p>
      <router-link to="/">  <button class="btn-contact">Back to home</button></router-link>
    </div>
    <div class="contact-form"  v-if="submited">
      <form>
        <div class="form-header">
          <!-- <slot name="form-header"></slot> -->
          <h2>Get in touch</h2>
        </div>
        <div class="form-fields">
          <!-- <slot name="form-fields"></slot> -->
          <input type="text" placeholder="Name" v-model="name" required />
          <input type="email" placeholder="example@.com" required />
          <textarea placeholder="Message"></textarea>
        </div>
        <div class="form-controls">
          <!-- <slot name="form-controls"></slot> -->
          <button class="btn-contact" @click.prevent="submitForm" :disabled="!name">Submit</button>
        </div>
        <div class="useful-links">
          <slot name="useful-links"></slot>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            name : '',
            submited: true
        }
    },
    methods:{
        submitForm(){
            if(this.name){
                
                this.submited = false
            }
        }
    }
};
</script>

<style scoped>
#contact{
display: flex;
max-width: 700px;
margin: 0 auto;
padding: 100px 0;
align-items: center;
justify-content: center;
gap: 80px;
min-height: 60vh
}
.congrats{
    text-align: center;
}
.congrats *{
    margin: 10px 0
}
form{
    padding: 20px;
    text-align: center;
  box-shadow: 0 0 10px rgba(234, 154, 63, 0.693);
    border-radius: 10px;
    width: 400px;
    background: url(../assets/blo.png);
    background-size: cover;
    background-repeat: no-repeat;
}
form *{
    margin: 20px 0
}
input,
textarea{
    display: block;
    padding: 20px;
    width: 100%
}
textarea{
    resize: none;
}
.contact-info{
    align-self: start;
    background: #EE9E40;
    padding: 10px;
    color: #fff;
    min-width: 300px;
    border-radius: 10px;
      box-shadow: 0 0 10px rgba(234, 154, 63, 0.693);
   text-align: center;
}
.contact-info *{
    margin: 20px 0
}
.btn-contact:disabled{
    background: #ddd;
    cursor:none
}
@media (max-width: 768px){
    #contact{
        flex-direction: column;
        padding: 100px 5%;
        text-align: center;
    }
    #contact *{
       max-width: 100%
    }
    .contact-info{
    align-self: center;
    order: 1
}
}

</style>
