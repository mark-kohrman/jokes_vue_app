<template>
  <div id="app">
    <div id="nav">
          <nav class="navbar navbar-expand-lg navbar-light fixed-top py-3" id="mainNav">
            <div class="container">
                <a class="navbar-brand js-scroll-trigger" href="#page-top">(app)ropriate jokes</a>
                <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation"><span class="navbar-toggler-icon"></span></button>
                <div class="collapse navbar-collapse" id="navbarResponsive">
                    <ul class="navbar-nav ml-auto my-2 my-lg-0">
                        <li class="nav-item"><a class="nav-link js-scroll-trigger" href="#services">Home</a></li>
                        <li class="nav-item"><a class="nav-link js-scroll-trigger" href="/about">About</a></li>
                    </ul>
                </div>
            </div>
        </nav>
    </div>


    <router-view/>
    <footer class="bg-light py-5">
            <div class="container"><div class="small text-center text-muted">Copyright © 2020 - (app)ropriate Jokes</div></div>
    </footer>
  </div>
</template>

<style>
</style>
