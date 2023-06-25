<template>
    <div class="container mt-3 w-25 text-center">
        <form action="/">
            <div class="form-group">
                <input type="email" class="form-control mt-3" placeholder="Enter Username" required/>
            </div>
            <div class="form-group">
                <input type="Password" class="form-control mt-3" placeholder="Enter Password" required/>
            </div>
            <div class="form-group">
                <input class="form-control btn btn-primary mt-3" type="submit" href="/" value="Log In"/>
            </div>
        </form>
    </div>
  </template>
  
  <script>
  export default {
    name: 'SignIn',
  }
  </script>
  