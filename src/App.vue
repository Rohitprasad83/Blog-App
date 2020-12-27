<template>
  <div id="app">
    <div id="nav">
      <b-navbar toggleable="lg" type="light" variant="inverse">
        <b-container>
          <b-navbar-brand href="/">Blog App</b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
              <b-collapse id="nav-collapse" is-nav>
                <!-- Right aligned nav items -->
                    <b-navbar-nav class="ml-auto">
                      <router-link d-sm-none d-md-block to="/">Home</router-link> 
                      <router-link d-sm-none d-md-block to="/about">About</router-link>
                      </b-navbar-nav>
              </b-collapse>
          </b-container>
      </b-navbar>
    </div>
    <main>
      <router-view/>
    </main>

      <footer class="footer"> 
        <div class="container">
          <div row="col-lg-6">
            <nav class="footer-links">
              <ul id="footer-menu">
                <li><a href="/">About</a></li>
                <li><a href="/">Write for us</a></li>
                <li><a href="/">Contact us</a></li>

              </ul>
            </nav>
          </div>
          <div row="col-lg-6">
            <nav class="social-links">
              <ul>
              <li><a href="https://www.facebook.com/" target="_blank"><b-icon-facebook class="h2 mb-2"> </b-icon-facebook></a></li>
              <li><a href="https://twitter.com/" target="_blank"><b-icon-twitter class="h2 mb-2"> </b-icon-twitter></a></li>
              <li><a href="https://www.youtube.com/" target="_blank"><b-icon-youtube class="h2 mb-2"> </b-icon-youtube></a></li>
              <li><a href="https://instagram.com/" target="_blank"><b-icon-instagram class="h2 mb-2"> </b-icon-instagram></a></li>
              <li><a href="/" target="_blank"><b-icon-linkedin class="h2 mb-2"> </b-icon-linkedin></a></li>
              </ul>
            </nav>
          </div>

          
        </div>
      </footer>
  </div>
</template>

<style>
  @import url('https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.0/normalize.min.css');

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }

  #nav {
    background-color: #F5F5F5;
    color: #555555;
  }

  #nav a {
    color: #555555;
    text-decoration: none;
    display: inline-block;
    padding: .5rem;
  }

  #nav a:hover {
    text-decoration: underline;
  }

  
  .content-wrapper {
    max-width: 840px;
    margin: 42px auto;
    padding: 21px;
    padding-bottom: 120px;
  }

  a {
    text-decoration: none;
  }
  .footer
  { 
      text-align: center;
      bottom: 0;
      margin: 0;
      height: 150px;
      background-color: #283646;
      padding-top: 0px;
      position: relative;
      left: 0px;
      right: 0px;
  }
.footer p
{ 
  padding-top: 50px;
	color: white;
}
.footer-links {
    margin-bottom: 1rem;
} 

#footer-menu {
  float: left;
}
.footer-links ul li {
    padding-top: 40px;
    padding-left: 15px;
    float: left;
    margin-right: 1rem;
}

.footer-links ul li a {
  color: #ced4da;
  margin-top: 20px;
}

.footer-links ul li a:hover {
  color: white;
}


.footer-links ul {
    margin: 0;
    padding: 0;
    list-style: none;
}
.social-links {
    float: right;
    margin-bottom: 4rem;
}
.social-links ul {
    margin: 0;
    padding-top: 40px;
    list-style: none;
}

.social-links ul li {
    float: left;
    margin-left: 1.5rem;
}

.social-links ul li a {
    display: block;
    font-size: 200%;
    color: #ced4da;
}

.social-links ul li a:hover {
  color:white;
}

.footer-sublinks {
    margin-bottom: 1rem;
} 

.footer-sublinks ul {
    margin: 0;
    padding: 0;
    list-style: none;
}

.footer-sublinks ul li {
    float: left;
    margin-right: 1rem;
}

.footer-sublinks ul li a {
    font-family: Montserrat,helvetica neue,Helvetica,Arial,sans-serif;
    font-size: 80%;
    color: #adb5bd;

}



</style>
