<template>

    <div class="container bootdey">
    <div class="row">
     <div class="d-flex justify-content-center align-items-center" style="height:10px;">
       <div class="col-md-4 ">
          <!-- START widget-->
          <div class="panel widget ">
             <div class="half-float">
                <img src="https://bootdey.com/img/Content/bg1.jpg" alt="" class="img-responsive">
                <div class="half-float-bottom">
                   <img src="https://bootdey.com/img/Content/avatar/avatar7.png" alt="Image" class="img-thumbnail img-circle thumb128">
                </div>
             </div>
             <div class="panel-body text-center">
                <h3 class="m0">{{ firstname }} {{ lastname }}</h3>
                <p class="text-muted">Student</p>
                <p class="text-muted">University: {{ uni }}</p>
                <p class="text-muted">Grade: {{ grade }}</p>
                <p class="text-muted">GPA: {{ gpa }}</p>
                <p class="text-muted">Phone: {{ phone }}</p>
                <p class="text-muted">E-Mail:{{ email }}</p>
                <p class="text-muted">Sex:{{ gender }}</p>
                <p class="text-muted"> Graduate:{{ graduate }}</p>
             </div>
             <div class="panel-body text-center bg-gray-dark">
                <div class="row row-table">
                   <div class="col-xs-4">
                      <h3 class="m0">.</h3>
                      <p class="m0">.</p>
                   </div>
                   <div class="col-xs-4">
                      <h3 class="m0">.</h3>
                      <p class="m0">.</p>
                   </div>
                   <div class="col-xs-4">
                      <h3 class="m0">.</h3>
                      <p class="m0">.</p>
                   </div>
                </div>
             </div>
          </div>
          <!-- END widget-->
       </div>
    </div>
    </div>
    </div>

    </template>
    
    <script>
    export default {
         props:['firstname','lastname','grade','gpa','phone','email','uni','gender','graduate']
    }
    </script>
    
    <style>
        body {
      font-family: "Helvetica Neue",Helvetica,Arial,sans-serif;
      font-size: 14px;
      line-height: 1.52857143;
      color: #515253;
      background-color: #ddd;
      margin-top:20px;
    }
    
    .widget .panel, .widget.panel {
      overflow: hidden;
    }
    
    .widget {
      margin-bottom: 20px;
      border: 0;
    }
    
    .bg-gray-darker {
      background-color: #232735;
      color: #fff!important;
    }
    
    .half-float {
      position: relative;
      margin-bottom: 65px;
    }
    
    .half-float .half-float-bottom, .half-float .half-float-top {
      position: absolute;
      left: 50%;
      bottom: -60px;
      width: 120px;
      height: 120px;
      margin-left: -60px;
      z-index: 2;
    }
    
    .thumb128 {
      width: 128px!important;
      height: 128px!important;
    }
    
    .half-float+* {
      margin-top: -55px;
      padding-top: 65px;
    }
    
    .m0 {
      margin: 0!important;
    }
    
    .bg-gray-dark {
      background-color: #3a3f51;
      color: #fff!important;
    }
    
    .row-table {
      display: table;
      table-layout: fixed;
      height: 100%;
      width: 100%;
      margin: 0;
    }
    
    .row-table>[class*=col-] {
      display: table-cell;
      float: none;
      table-layout: fixed;
      vertical-align: middle;
    }
    </style>