<template>
  <div class="home">

    <div class="container">
      <div class="card bg-light mb-3" style="max-width: 40rem;">
        <div class="card-header">resume.name</div>
        <div class="card-body">
          <h5 class="card-title">Education</h5>
          <p class="card-text">education.start_date</p>
          education.end_date
          education.title
        </div>
      </div>
    </div>

    <div class="container">
      <div class="card bg-light mb-3" style="max-width: 40rem;">
        <div class="card-header">resume.name</div>
        <div class="card-body">
          <h5 class="card-title">Education</h5>
          <p class="card-text">education.start_date</p>
          education.end_date
          education.title
        </div>
      </div>
    </div>

    <div class="container">
      <div class="card" style="width: 18rem;" id="name-card">
        <img class="card-img-top" src="" alt="Card image cap">
        <div class="card-body">
          <h5 class="card-title">Card title</h5>
          <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">Cras justo odio</li>
          <li class="list-group-item">Dapibus ac facilisis in</li>
          <li class="list-group-item">Vestibulum at eros</li>
        </ul>
        <div class="card-body">
          <a href="#" class="card-link">Card link</a>
          <a href="#" class="card-link">Another link</a>
        </div>
      </div>
    </div>

  </div>
</template>

<style>
#name-card{
  position: fixed;
  top: 100px;
  right: 40px;
}
</style>

<script>
export default {
  data: function() {
    return {
      resumes: [],
      message: "hello"
    };
  },
  // created: function() {
  //   axios.get("localhost:3000/resumes").then{function(response) {
  //     this.resumes = response.data
  //   }.bind(this)
  //   }
  // },
  methods: {},
  computed: {}
};
</script>