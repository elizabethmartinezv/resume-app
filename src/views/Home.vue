<template>
  <div class="home">

  <div class="container">
    <div class="card" style="width: 50rem;" v-for="student in filterBy(students, searchFilter, 'title')">
      <img class="card-img-top" src="http://www.personalbrandingblog.com/wp-content/uploads/2017/08/blank-profile-picture-973460_640-300x300.png" alt="Card image cap" id="small-pic">
      <div class="card-body">
        <h5 class="card-title">{{ student.first_name}} {{ student.last_name }}</h5>
        <p class="card-text"v-for="experience in student.experiences">{{ experience.job_title}}</p>
        <a v-bind:href="'/#/show/' + student.id" class="btn btn-primary">More Info</a>
      </div>
    </div>
  </div>

    <div class="container">
      <div class="card" style="width: 18rem;" id="name-card">
        <img class="card-img-top" src="http://www.personalbrandingblog.com/wp-content/uploads/2017/08/blank-profile-picture-973460_640-300x300.png" alt="Card image cap" id="picture">
        <div class="card-body">
          <h5 class="card-title">Sarah Jones</h5>
          <p class="card-text">Currently attending Actualize Coding Bootcamp. I enjoy coding, coffee, and bikerides.</p>
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">Cool gal</li>
          <li class="list-group-item">sarahjones@email.com</li>
        </ul>
        <div class="card-body">
          <a href="#" class="card-link">Edit Profile</a>
          <a href="#" class="card-link">More Info</a>
          <a href="#" class="card-link">Logout</a>
        </div>
      </div>
</div>

  </div>
</template>

<style>
#name-card {
  position: fixed;
  top: 100px;
  right: 40px;
}

#picture {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  margin-top: 20px;
  margin-left: 63px;
}

#small-pic {
  width: 90px;
  height: 90px;
  border-radius: 50%;
  margin-top: 10px;
  margin-left: 14px;
}
</style>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      students: []
    };
  },
  created: function() {
    axios.get("http://vue-tang-resume-api.herokuapp.com/students").then(
      function(response) {
        console.log(response.data);
        this.students = response.data;
      }.bind(this)
    );
  },
  methods: {},
  computed: {}
};
</script>
