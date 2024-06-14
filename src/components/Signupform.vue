<template>
    <h1>Registration Form</h1>
    <p>Please fill out this form with the required information</p>
   <form> </form>
    <fieldset>
         <label for="first-name">Enter Your First Name: 
            <input id="first-name"  type="text" required v-model="firstname">
        </label>
        <label for="last-name">Enter Your Last Name:
            <input id="last-name" type="text" required v-model="lastname">
        </label>
        <label for="email">Enter Your Email: 
            <input id="email" type="email" required v-model="email">
        </label>
        <label for="new-password">Create a New Password: 
            <input id="new-password" type="password"  pattern="[a-z0-5]{8,}" required v-model="password">
        </label>
    </fieldset>
    <fieldset>
        <legend>Account type (required)</legend>
        <label for="personal-account"><input class="inline" id="personal-account" type="radio" name="account-type" checked /> Personal</label>
        <label for="business-account"><input  class="inline" id="business-account" type="radio" name="account-type" /> Business</label>
      </fieldset>
      <fieldset>
        <label for="profile-picture">Upload a profile picture: <input id="profile-picture" type="file" /></label>
        <label for="age">Input your age (years): <input id="age" type="number" min="13" max="120" /></label>
        <label for="referrer">How did you hear about us?
          <select id="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
        <label for="bio">Provide a bio:
          <textarea id="bio" rows="3" cols="30" placeholder="I like coding on the beach...."></textarea>
        </label>
      </fieldset>
    <label for="terms-and-conditions">
        <input class="inline" id="terms-and-conditions" type="checkbox" required> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions </a>
    </label>
    <input  type="submit" value="Submit">
      
  
   <P>Email:{{ email }}</P>
   <p>Password:{{ password }}</p>
   <p> FirstName:{{ firstname }}</p>
   <p> LastName:{{  lastname }}</p>
</template>

<script>
export default {
  data(){
    return{
        email: '',
        password: '',
        firstname: '',
        lastname: '',

    }
  }
}
</script>

<style>


h1, p {
  margin: 1em auto;
  text-align: center;
}

form {
  width: 60vw;
  max-width: 500px;
  min-width: 300px;
  margin: 0 auto;
  padding-bottom: 2em;
  
}

fieldset {
  border: none;
  padding: 2rem 0;
  border-bottom: 3px solid #757578;
}

fieldset:last-of-type {
  border-bottom: none;
}
label {
  display: block;
  margin: 0.5rem 0;
}
input , textarea{
    background-color:#0a0a23 ;
    border: 1px solid #0a0a23;

}
input,
textarea,
select {
  margin: 10px 0 0 0;
  width: 100%;
  color:#ffffff ;
    min-height: 2em;
}

.inline {
  width: unset;
  margin: 0 0.5em 0 0;
  vertical-align: middle;
}
input[type="submit"]{
    display: block;
    width: 60%;
    min-width: 300px;
    margin: 1em auto 1em auto;
    height: 2em;
    font-size: 1.1rem;
    background-color:#3b3b4f;
    border-color: white;
    
}
input[type="file"]{
   padding:1px 2px ;
}
</style>