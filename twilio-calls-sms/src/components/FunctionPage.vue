<template>
    <div id="form__container">


    <form>

        <!-- Email input text -->
        <h3></h3>
        <div >
          <span id="emailId">{{email}}</span>
        </div>
        <h1></h1>
        <input type="text" required v-model="to" placeholder="Phone number to send text to with country code">

        
        <!-- Message input text -->
        <h3></h3>
        <input type="text" required v-model="message" placeholder="Message">

        <h3></h3>

        <div id="button_Container">
          <b-button id="button" v-bind:disabled= "!to || !message"
                  v-on:click="sendText(to, message)" >Send Text</b-button>
        </div>

        <h3></h3>
        <div >
          <span v-if="error" style="color:red">{{error}} </span>
        </div>

        
      </form>

      <div id="loginRegister">


            <b-button id="button" v-on:click="logout()" >Logout</b-button>

        
        </div>


    </div>

</template>


<script src="./Function.js" />





<style>
body{
  background: #6bd891;
}


#loginRegister {
    position: absolute;
    top: 0px;
    right: 0px;
    padding: 20px;
}

form{
  width: 30%;
  height: 50%;
  display: flex;
  border-radius: 5px;
  border: none;
  flex-direction: column;
  padding: 20px;
}

#button {
  font-family: "Merienda";
}

#form__container{
  background-color: #6bd891;
  align-items: center;
  display: flex;
  flex-direction: column;
  margin-top: 100px;
}

#emailId {
  color: white;
  font-family: "Merienda";

}


</style>

