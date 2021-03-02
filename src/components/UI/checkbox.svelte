


         <input type="checkbox" id="off" />
         <label for="off">
            <span class="handler"><span class="handler-inner"></span></span>
            <span class="title">3D</span>
            <span>2D</span>
            <span class="bg-on"></span>  
         </label>

         <style>
label {
   display: inline-block;
}

input[type="checkbox"] {
   display: none;
}

input[type="checkbox"] + label {
   position: relative;
   display: inline-block;
   width: 45.45454545%;
   padding: 0.7rem 1rem;
   text-align: right;
   border-radius: 22%/50%;
   box-sizing: border-box;
   box-shadow: inset 0 2px 2px 0 rgba(0,0,0,.3), inset 0 0 0 1px #d6d6d6, 0 2px 0 0 white;
   background: #e5e4e4;
   background: -webkit-linear-gradient(top, #e5e4e4 1%,#f1f1f1 100%);
   background: -moz-linear-gradient(top, #e5e4e4 1%, #f1f1f1 100%);
   background: -o-linear-gradient(top, #e5e4e4 1%,#f1f1f1 100%);
   background: -ms-linear-gradient(top, #e5e4e4 1%,#f1f1f1 100%);
   background: linear-gradient(to bottom, #e5e4e4 1%,#f1f1f1 100%);
   overflow: hidden;
   cursor: pointer;
   z-index: 1;
}

label[for="off"] {
   margin-right: 7.272727273%;
}


.bg-on {
   position: absolute;
   top: 0;
   left: -82%;
   display: inline-block;
   width: 100%;
   height: 100%;
   box-shadow: inset 0 0 4px 1px rgba(0,0,0,.3);
   border-radius: 18px;
   background: #e15e0f;
   background: -webkit-linear-gradient(top, #e15e0f 1%,#fc8516 100%);
   background: -moz-linear-gradient(top, #e15e0f 1%, #fc8516 100%);
   background: -o-linear-gradient(top, #e15e0f 1%,#fc8516 100%);
   background: -ms-linear-gradient(top, #e15e0f 1%,#fc8516 100%);
   background: linear-gradient(to bottom, #e15e0f 1%,#fc8516 100%);
   transition: all .4s ease-out;
   opacity: .99;
   z-index: 1;
}

input[type="checkbox"]:checked + label > .handler {
   left: 59%;
}

input[type="checkbox"]:checked + label > .title {
   opacity: 1;
}

input[type="checkbox"]:checked + label > .bg-on {
   left: 0;
}

.title {
   position: relative;
   left: -20%;
   color: white;
   opacity: 0;
   transition: all .6s;
   z-index: 2;
}

.handler {
   position: absolute;
   top: 0;
   left: -1%;
   display: block;
   padding: 21.0782%;
   border-radius: 50%;
   box-shadow: inset 0 5px 2px 0 rgba(255,255,255,.6), inset 0 0 0 1px #b8b8b8, 0 2px 2px 0 rgba(0,0,0,.4);
   background: #fbfbfb;
   background: -webkit-linear-gradient(top, #fbfbfb 0%,#dddddc 100%);
   background: -moz-linear-gradient(top, #fbfbfb 0%, #dddddc 100%);
   background: -o-linear-gradient(top, #fbfbfb 0%,#dddddc 100%);
   background: -ms-linear-gradient(top, #fbfbfb 0%,#dddddc 100%);   
   background: linear-gradient(to bottom, #fbfbfb 0%,#dddddc 100%);
   transition: all .4s;
   z-index: 3;
}

.handler-inner {
   position: absolute;
   top: 0;
   left: 0;
   right: 0;
   bottom: 0;   
   display: block;
   width: 41.66666667%;
   height: 41.66666667%;
   border-radius: 50%;
   margin: auto;
   box-shadow: inset 0 2px 2px 0 rgba(0,0,0,.3), inset 0 0 0 1px #d6d6d6, 0 2px 0 0 white;
   background: #e5e4e4;
   background: -webkit-linear-gradient(top, #e5e4e4 1%,#f1f1f1 100%);
   background: -moz-linear-gradient(top, #e5e4e4 1%, #f1f1f1 100%);
   background: -o-linear-gradient(top, #e5e4e4 1%,#f1f1f1 100%);
   background: -ms-linear-gradient(top, #e5e4e4 1%,#f1f1f1 100%);
   background: linear-gradient(to bottom, #e5e4e4 1%,#f1f1f1 100%);
   z-index: 4;
}

         </style>