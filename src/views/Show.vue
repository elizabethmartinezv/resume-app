<template>
  <div class="Show">
    <div class="container">
      <div class="card bg-light mb-3" style="max-width: 40rem;" >
      <img class="card-img-top" id="avatar" src="http://www.personalbrandingblog.com/wp-content/uploads/2017/08/blank-profile-picture-973460_640-300x300.png" height='300' width='10' >
      <div class="card-body" >
        <h5 class="card-title">{{student.first_name}} {{student.last_name}}</h5>
        <ul>
        <li><p class="card-text">{{student.phone_number}}</p></li>
        <li><p class="card-text">{{student.email}}</p></li>
        <li><p class="card-text">{{student.short_bio}}</p></li>
        <li><p class="card-text">Twitter: {{student.twitter_handle}}</p></li>
        <li><p class="card-text">{{student.personal_blog}}</p></li>
        <li><p class="card-text">{{student.online_resume_url}}</p></li>
        <li><p class="card-text">{{student.github_url}}</p></li>
        </ul>
      </div>
     </div>
    </div>  
    <div class="container" v-for="education in student.education">
              <div class="card bg-light mb-3" style="max-width: 40rem;" >
                <div class="card-header">Education</div>
                <div class="card-body">
                  <h5 class="card-title">Education</h5>
                  <ul>
                    <li><p class="card-text"> {{education.University_name}}</p></li>
                    <li><p class="card-text">From: {{education.start_date}} to: {{education.end_date}}</p></li>
                    <li><p class="card-text"> {{education.degree}}</p></li>
                    
                    <li><p class="card-text"> {{education.Details}}</p></li>
                  </ul>
                </div>
              </div>
            </div> 
          
      <div class="container" v-for="experience in student.experiences">
              <div class="card bg-light mb-3" style="max-width: 40rem;">
                <div class="card-header">Experience</div>
                <div class="card-body">
                  <h5 class="card-title">Experience</h5>
                  <ul>
                    <li><p class="card-text">{{experience.company_name}}</p></li>
                    <li><p class="card-text">From: {{experience.start_date}} to: {{experience.end_date}} </p></li>
                    <li><p class="card-text">{{experience.job_title}}</p></li>
                  </ul>
                </div>
              </div>
            </div> 
      <div class="container" v-for="skill in student.skills">
              <div class="card bg-light mb-3" style="max-width: 40rem;">
                <div class="card-header">Skills</div>
                <div class="card-body">
                  <h5 class="card-title">Skills</h5>
                  <ul>
                    <li><p class="card-text">{{skill.Name}}</p></li>
                  </ul>
                </div>
              </div>
            </div> 
      </div>
</template>

<style>
#avatar {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-left: 10px;
    margin-top: 10px;
},
#name-card{
  position: fixed;
  top: 100px;
  right: 40px;
}
</style>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      student: {},
    };
  },
  created: function() {
    axios.get('http://vue-tang-resume-api.herokuapp.com/students/' + this.$route.params.id).then(response =>{
      console.log(response.data);
      this.student = response.data;
    });
    // getEducationInfo: function(){

    // }
  },
  methods: {},
  computed: {}
};
</script>