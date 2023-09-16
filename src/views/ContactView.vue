<script lang="ts">
import emailjs from '@emailjs/browser';
const button = document.querySelector('button');
export default {
  methods: {
    sendEmail() {
      emailjs.sendForm('service_66efai7', 'template_ft9cixc', this.$refs.form, 'DD8Ol59OC9ccPtQdh')
        .then((result) => {
            console.log('SUCCESS!', result.text);
            alert('Votre message a bien été envoyé');
            button ?  button.disabled = true : null;
        }, (error) => {
            console.log('FAILED...', error.text);
            alert('Vous avez déjà envoyé un message. Je vous recontacterai dès que possible');
            button ?  button.disabled = true : null;
        });
    }
  }
}
</script>

<template>
  <div class="Contact">
    <div class="title"> 
      <h2>Envoyez-moi un message</h2>
    </div>
    <form ref="form" @submit.prevent="sendEmail">
      <label for="name">Nom</label>
      <input type="text" id="name" name="name" placeholder="Votre nom" minlength="2" maxlength="256" pattern="\w" required>
      <label for="email">Email</label>
      <input type="email" id="email" name="email" placeholder="Votre email" pattern="\/^[^\s@]+@[^\s@]+\.[^\s@]+$\/" required>
      <label for="message">Message</label>
      <textarea id="message" name="message" placeholder="Votre message"></textarea>
      <button type="submit" value="Send">Envoyer</button>
    </form>
  </div>
</template>

<style scoped>
.Contact {
margin: auto 0;
}
.title {
  text-align: center;
  margin-top: 5rem;
}
form {
  display: flex;
  flex-direction: column;
  align-items: center;
}
input {
  border: 1px solid lightgray;
  border-radius: 5px;
  margin-bottom: 1rem;
  padding: 10px;
  width: 300px;
}

textarea{
  border: 1px solid lightgray;
  border-radius: 5px;
  margin-bottom: 1rem;
  padding: 10px;
  width: 300px;
  height: 200px;
}

button {
  background-color: rgb(0, 113, 189);
  border: none;
  border-radius: 5px;
  color: white;
  cursor: pointer;
  font-size: 16px;
  margin-bottom: 1rem;
  padding: 10px;
  width: 300px;
}

button:active {
  background-color: rgb(0, 113, 189, 0.8);
}
</style>
