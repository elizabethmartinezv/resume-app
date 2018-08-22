<template>
  <div class="home">

    <div class="container">
      <div class="card bg-light mb-3" style="max-width: 40rem;">
        <div class="card-header">student.first_name student.last_name</div>
        <div class="card-body">
          <h5 class="card-title">experience.job_title</h5>
          <p class="card-text">student.short_bio</p>
        </div>
      </div>
    </div>

    <div class="container">
      <div class="card bg-light mb-3" style="max-width: 40rem;">
        <div class="card-header">student.first_name student.last_name</div>
        <div class="card-body">
          <h5 class="card-title">student.job_title at student.company_name </h5>
          <p class="card-text">student.short_bio</p>
        </div>
      </div>
    </div>

    <div class="container">
          <div class="card bg-light mb-3" style="max-width: 40rem;">
            <div class="card-header">student.first_name student.last_name</div>
            <div class="card-body">
              <h5 class="card-title">experience.job_title</h5>
              <p class="card-text">student.short_bio</p>
            </div>
          </div>
    </div>


    <div class="container">
      <div class="card" style="width: 18rem;" id="name-card">
        <img class="card-img-top" src="http://www.personalbrandingblog.com/wp-content/uploads/2017/08/blank-profile-picture-973460_640-300x300.png" alt="Card image cap" id="picture">
        <div class="card-body">
          <h5 class="card-title">Jane Doe</h5>
          <p class="card-text">Currently attending Actualize Coding Bootcamp. I enjoy coding, coffee, and bikerides.</p>
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">Web Developer at Actualize</li>
          <li class="list-group-item">janedoe@email.com</li>
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
#name-card{
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
</style>

<script>
export default {
  data: function() {
    return {
      students: [],
      educations: [],
      experiences: [],
      skills:[]
    };
  },
  // created: function() {
  //   axios.get("localhost:3000/").then{function(response) {
  //     this.resumes = response.data
  //   }.bind(this)
  //   }
  // },
  methods: {},
  computed: {}
};
</script>