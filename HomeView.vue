<template>
<section class="h-100 bg-dark">
  <div class="container py-5 h-100" v-if="showform">
    <div class="row d-flex justify-content-center align-items-center h-100">
      <div class="col">
        <div class="card card-registration my-4">
          <div class="row g-0">
            <div class="col-xl-6 d-none d-xl-block">
              <img src="https://mdbcdn.b-cdn.net/img/Photos/new-templates/bootstrap-registration/img4.webp"
                alt="Sample photo" class="img-fluid"
                style="border-top-left-radius: .25rem; border-bottom-left-radius: .25rem;" />
            </div>
            <div class="col-xl-6">
              <div class="card-body p-md-5 text-black">
                <h3 class="mb-5 text-uppercase">Student card-maker form</h3>

                <div class="row">
                  <div class="col-md-6 mb-4">
                    <div class="form-outline">
                      <input type="text" id="form3Example1m" class="form-control form-control-lg" v-model="firstname" />
                      <label class="form-label" for="form3Example1m">First name</label>
                    </div>
                  </div>
                  <div class="col-md-6 mb-4">
                    <div class="form-outline">
                      <input type="text" id="form3Example1n" class="form-control form-control-lg" v-model="lastname" />
                      <label class="form-label" for="form3Example1n">Last name</label>
                    </div>
                  </div>
                </div>

                <div class="row">
                  <div class="col-md-6 mb-4">
                    <div class="form-outline">
                      <input type="text" id="form3Example1m1" class="form-control form-control-lg" v-model="grade" />
                      <label class="form-label" for="form3Example1m1">Grade</label>
                    </div>
                  </div>
                  <div class="col-md-6 mb-4">
                    <div class="form-outline">
                      <input type="text" id="form3Example1n1" class="form-control form-control-lg" v-model="gpa" />
                      <label class="form-label" for="form3Example1n1">GPA</label>
                    </div>
                  </div>
                </div>

                <div class="row">
                  <div class="col-md-6 mb-4">
                    <div class="form-outline">
                      <input type="text" id="form3Example1m1" class="form-control form-control-lg" v-model="phone" />
                      <label class="form-label" for="form3Example1m1">Phone</label>
                    </div>
                  </div>
                  <div class="col-md-6 mb-4">
                    <div class="form-outline">
                      <input type="text" id="form3Example1n1" class="form-control form-control-lg" v-model="email" />
                      <label class="form-label" for="form3Example1n1">E-mail</label>
                    </div>
                  </div>
                </div>

                <div class="form-outline mb-4">
                  <input type="text" id="form3Example8" class="form-control form-control-lg"  v-model="uni"/>
                  <label class="form-label" for="form3Example8">University</label>
                </div>

                <div class="d-md-flex justify-content-start align-items-center mb-4 py-2">

                  <h6 class="mb-0 me-4">Gender: </h6>

                  <div class="form-check form-check-inline mb-0 me-4">
                    <input class="form-check-input" type="radio" name="inlineRadioOptions" id="femaleGender"
                      value="female"  v-model="gender"/>
                    <label class="form-check-label" for="femaleGender">Female</label>
                  </div>

                  <div class="form-check form-check-inline mb-0 me-4">
                    <input class="form-check-input" type="radio" name="inlineRadioOptions" id="maleGender"
                      value="male" v-model="gender" />
                    <label class="form-check-label" for="maleGender">Male</label>
                  </div>

                  <div class="form-check form-check-inline mb-0">
                    <input class="form-check-input" type="radio" name="inlineRadioOptions" id="otherGender"
                      value="other" v-model="gender" />
                    <label class="form-check-label" for="otherGender">Other</label>
                  </div>

                </div>

                <div class="row">
                  <div class="col-md-6 mb-4">
                    <label for="select" class="label label-info">year of graduate</label>
                    <select class="select" v-model="graduate">
                      <option value="2023">2023</option>
                      <option value="2024">2024</option>
                      <option value="2024+">2024+</option>
                    </select>

                  </div>
                  <div class="col-md-6 mb-4">
                  </div>
                </div>
<!---
                <div class="form-outline mb-4">
                  <input type="text" id="form3Example9" class="form-control form-control-lg" />
                  <label class="form-label" for="form3Example9">DOB</label>
                </div>

                <div class="form-outline mb-4">
                  <input type="text" id="form3Example90" class="form-control form-control-lg" />
                  <label class="form-label" for="form3Example90">Pincode</label>
                </div>

                <div class="form-outline mb-4">
                  <input type="text" id="form3Example99" class="form-control form-control-lg" />
                  <label class="form-label" for="form3Example99">Course</label>
                </div>

                <div class="form-outline mb-4">
                  <input type="text" id="form3Example97" class="form-control form-control-lg" />
                  <label class="form-label" for="form3Example97">Email ID</label>
                </div>

                <div class="d-flex justify-content-end pt-3">
                  <button type="button" class="btn btn-light btn-lg">Reset all</button>
                  <button type="button" class="btn btn-warning btn-lg ms-2">Submit form</button>
                </div>
              -->
                <div class="d-flex justify-content-end pt-3">
                    <button type="button" class="btn btn-warning btn-lg ms-2" @click="ChangeVis">Convert to CARD format</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
    <div v-if="showcard">
      <Card :firstname="firstname" :lastname="lastname" :grade="grade" :gpa="gpa" :phone="phone" :email="email" :uni="uni" :gender="gender" :graduate="graduate">
      </Card>
    </div>
</section>


</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Card from '@/components/Card.vue'


export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    Card


  },
  data(){
    return{
      firstname:'',
      lastname:'',
      grade:'',
      gpa:'',
      phone:'',
      email:'',
      uni:'',
      gender:'',
      graduate:'',
      showcard:false,
      showform:true,
    }
  },
  methods:{
    ChangeVis(){
      this.showcard=!this.showcard
      this.showform=!this.showform
    }
  }
}
</script>

<style>
.card-registration .select-input.form-control[readonly]:not([disabled]) {
font-size: 1rem;
line-height: 2.15;
padding-left: .75em;
padding-right: .75em;
}
.card-registration .select-arrow {
top: 13px;
}
</style>
