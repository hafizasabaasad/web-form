<template>
  
  <div class="bg-img container">
    <h1 class="header h1">Account Registeration Form</h1>
    <form @submit.prevent="Submit">
        <h2>Create an ABC Account</h2>
        <fieldset>
            <label for="first-name">Enter Your First Name:
                <input id="first-name" type="text" required v-model="firstname" />
            </label>
            <label for="last-name">Enter Your Last Name:
                <input id="last-name" type="text" required v-model="lastname" />
            </label>
            <label for="email">Enter Your Email:
                <input id="email" type="email" required v-model="email" />
            </label>
            <label for="new-password">Create a New Password:
                <input id="new-password" type="password" pattern="[a-z0-5]{8,}" required v-model="password" />
            </label>
        </fieldset>
        <br />
        <fieldset>
            <legend>Account type (required)</legend>
            <label for="personal-account"><input class="inline" id="personal-account" type="radio" name="account-type"
                    checked />
                Personal</label>
            <label for="business-account"><input class="inline" id="business-account" type="radio"
                    name="account-type" />
                Business</label>
        </fieldset>
        <input type="submit" value="Submit" />
    </form>
    <p class="footer">Copyright © Hafiz Saba Asad, Developed in 2024</p>
  </div>


  <!-- <P>Email:{{ email }}</P>
  <p>Password:{{ password }}</p>
  <p>FirstName:{{ firstname }}</p>
  <p>LastName:{{ lastname }}</p> -->
</template>

<script>
export default {
  data() {
    return {
      email: "",
      password: "",
      firstname: "",
      lastname: "",
    };
  },
};
</script>

<style>
html {
display: grid;
height: 100%; /* OR min-height: 100% */
}
.container {
display: grid;
min-height: 0;
grid-template-rows: 1fr;
grid-template-columns: 1fr; /* 1 columns */
}
.header,
.footer {

grid-column: 1/-1; /* header and footer takes both columns */
text-align: center;
padding: 20px;

}
.bg-img {
  /* The image used */
  background-image: url("../../public/background-image-2.jpeg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  min-height: 100vh;
  
}
h1 {
  /* margin: 1em auto; */
  margin: 20px;
  padding: 20px;
  color: white;
  text-align: center;
}
h2 {
  margin: 50px;
  /* padding: 10px; */
  color: black;
  text-align: center;
}

form {
  border: 1px solid;
  border-radius: 20px;
  border-color: white;
  background-color: white;
  /* width: 100vw;
  max-width: 700px;
  min-width: 300px; */
  margin: auto;
  padding-bottom: 1em;
  
}

fieldset {
  border: none;
  padding: 1rem 3rem;
}

/* fieldset:last-of-type {
  border-bottom: none;
} */
label {
  display: block;
  /* margin: 1rem 0; */
}
input,
textarea {
  background-color: white;
  border: 1px solid #0a0a23;
  margin: 10px 0 0 0;
  width: 100%;
  color: black;
  min-height: 2em;
}

.inline {
  width: unset;
  margin: 0 0em 0 0;
  vertical-align: middle;
}
input[type="submit"] {
  display: block;
  width: 40%;
  min-width: 20px;
  margin: 2em auto 3em auto;
  height: 2em;
  font-size: 1.1rem;
  background-color: rgb(12, 107, 223);
  color: white;
  border-color: white;
}

/* Full-width input fields */
input[type="text"],
input[type="password"],
input[type="email"] {
  border-radius:10px;
  width: 100%;
  padding: 5px;
  margin: auto;
  border: none;
  background: #f1f1f1;
}

input[type="text"]:focus,
input[type="password"]:focus {
  background-color: white;
  outline: none;
}

</style>