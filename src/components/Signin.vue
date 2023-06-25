<template>
    <div class="container mt-3 w-25 text-center">
        <form action="/">
            <div class="form-group">
                <input type="text" class="form-control mt-3" placeholder="Enter Username" />
            </div>
            <div class="form-group">
                <input type="Password" class="form-control mt-3" placeholder="Enter Password" />
            </div>
            <div class="form-group">
                <a class="form-control btn btn-primary mt-3" href="/" value="Log In">Login</a>
            </div>
        </form>
    </div>
  </template>
  
  <script>
  export default {
    name: 'SignIn',
  }
  </script>
  