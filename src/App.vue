<template>
  <div id="app">
    <div class="container">
      <div class="row g-5">
        <div class="col-lg-4 sticky-lg-top vh-100">
          <div
            class="d-flex flex-column h-100 text-center overflow-auto shadow"
          >
            <img
              class="w-100 img-fluid mb-4"
              src="img/profile.jpg"
              alt="Image"
            />
            <h1 class="text-primary mt-2">Barnabas Tinarwo</h1>
            <div class="mb-4" style="height: 22px">
              <h4 class="typed-text-output d-inline-block text-light"></h4>
              <div class="typed-text d-none">
                  Systems Engineer, AWS Cloud Practitioner, Christian
              </div>
            </div>
            <div class="d-flex justify-content-center mt-auto mb-3">
              <a class="btn btn-secondary btn-square mx-1" href="#"
                ><i class="fab fa-facebook-f"></i
              ></a>
              <a class="btn btn-secondary btn-square mx-1" href="#"
                ><i class="fab fa-linkedin-in"></i
              ></a>
            </div>
            <div
              class="d-flex align-items-end justify-content-between border-top"
            >
              <a href="https://btinarwo.online/Barnabas-Tinarwo-CV.pdf" class="btn w-50 border-end">Download CV</a>
              <a href="#contact" class="btn w-50 btn-scroll">Contact Me</a>
            </div>
          </div>
        </div>
        <div class="col-lg-8">
          <About />
          <Experience />
          <Skills />
          <References />
          <Footer />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import About from "./components/About.vue";
import Experience from "./components/Experience.vue";
import Footer from "./components/Footer.vue";
import References from "./components/References.vue";
import Skills from "./components/Skills.vue";

export default {
  name: "App",
  components: {
    About,
    Experience,
    Skills,
    References,
    Footer,
  },
};
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
