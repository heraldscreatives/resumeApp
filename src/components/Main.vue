<template>
  <div class="container">
    <div class="grid-container">
      <!-- <Form /> -->
      <!-- Aside -->
      <div class="aside">
        <!-- contact information -->
        <div class="form" id="form1">
          <h3>
            Choose theme&nbsp;&nbsp;&nbsp;&nbsp;<i
              @click="firstTheme"
              class="fa-solid fa-circle theme1"
            ></i
            >&nbsp;&nbsp;
            <i @click="secondTheme" class="fa-solid fa-circle theme2"></i
            >&nbsp;&nbsp;
            <i @click="thirdTheme" class="fa-solid fa-circle theme3"></i
            >&nbsp;&nbsp;
            <i @click="fourthTheme" class="fa-solid fa-circle theme4"></i
            >&nbsp;&nbsp;
          </h3>
          <h2>Contact Information</h2>
          <label for="name">First and Last Name:</label>
          <input type="text" v-on:input="makeUpper" v-model="name" /><br />
          <label for="website">Portfolio website if any</label>
          <input type="text" v-model="website" v-on:input="listenFor1" /><br />
          <label for="email">Email Address:</label>
          <input type="email" v-model="email" v-on:input="listenFor2" /><br />
          <label for="phone">Phone Number</label>
          <input type="text" v-model="phone" v-on:input="listenFor3" /><br />
          <label for="location">Location/City & Country</label>
          <input type="text" v-model="location" v-on:input="listenFor4" /><br />
          <label for="linkedin">Linkedin Profile</label>
          <input type="text" v-model="linkedin" v-on:input="listenFor5" /><br />
          <label for="twitter">Twitter Profile</label>
          <input type="text" v-model="twitter" v-on:input="listenFor6" />
        </div>

        <!-- Education form -->
        <div class="form" id="form2">
          <h2>Education</h2>
          <label for="course">Course/Certificate Name</label>
          <input type="text" v-model="course" /><br />
          <label for="school">University/College/School</label>
          <input type="text" v-model="school" /><br />
          <label for="yearOfStart">Date Started</label>
          <input
            v-on:input="listenFor32"
            type="text"
            v-model="yearOfStart"
          /><br />
          <label for="yearOfGrad">Date Ended</label>
          <input type="text" v-model="yearOfGrad" /><br />
          <label for="schoolLocation">City/Country</label>
          <input
            v-on:input="listenFor33"
            type="text"
            v-model="schoolLocation"
          /><br />
        </div>

        <!-- Skills form -->
        <div class="form" id="form3">
          <h2>Skills</h2>
          <label for="skill1">Skill 1</label>
          <input v-on:input="listenFor7" type="text" v-model="skill1" /><br />
          <label for="skill2">Skill 2</label>
          <input v-on:input="listenFor8" type="text" v-model="skill2" /><br />
          <label for="skill3">Skill 3</label>
          <input v-on:input="listenFor9" type="text" v-model="skill3" /><br />
          <label for="skill4">Skill 4</label>
          <input v-on:input="listenFor10" type="text" v-model="skill4" /><br />
          <label for="skill5">Skill 5</label>
          <input v-on:input="listenFor11" type="text" v-model="skill5" /><br />
          <label for="skill6">Skill 6</label>
          <input v-on:input="listenFor12" type="text" v-model="skill6" /><br />
          <label for="skill7">Skill 7</label>
          <input v-on:input="listenFor13" type="text" v-model="skill7" /><br />
          <label for="skill8">Skill 8</label>
          <input v-on:input="listenFor14" type="text" v-model="skill8" /><br />
          <label for="skill9">Skill 9</label>
          <input v-on:input="listenFor15" type="text" v-model="skill9" /><br />
          <!-- <label for="skill10">Skill 10</label>
          <input v-on:input="listenFor16" type="text" v-model="skill10" /><br /> -->
        </div>

        <!-- Career Objectives Form -->
        <div class="form" id="form4">
          <h2>Career Objective</h2>
          <label for="objectives">Profile Summary </label><br />
          <textarea type="text" v-model="objectives"></textarea>
        </div>

        <!-- Work Experience Form -->
        <div class="form" id="form5">
          <h2>Work Experience</h2>

          <!-- First work experience -->
          <div class="first-experience">
            <label for="jobTitle1">Job Title</label><br />
            <input type="text" v-model="jobTitle1" />
            <label for="company1">Name of Company</label><br />
            <input type="text" v-model="company1" />
            <label for="workLocation1">Location of Company</label><br />
            <input type="text" v-model="workLocation1" />
            <label for="yearStarted1">Year Started</label><br />
            <input
              v-on:input="listenFor26"
              type="text"
              v-model="yearStarted1"
            />
            <label for="yearFinished1">Year Finished</label><br />
            <input
              v-on:input="listenFor27"
              type="text"
              v-model="yearFinished1"
            />
            <label for="jobTitle1">Responsibilities</label><br />
            <input
              v-on:input="listenFor17"
              class="input"
              type="text"
              v-model="responsibility1a"
            /><br />
            <input
              v-on:input="listenFor18"
              class="input"
              type="text"
              v-model="responsibility1b"
            /><br />
            <input
              v-on:input="listenFor19"
              class="input"
              type="text"
              v-model="responsibility1c"
            /><br />
          </div>

          <!-- Second work experience -->
          <div class="second-experience">
            <label for="jobTitle2">Job Title</label><br />
            <input type="text" v-model="jobTitle2" />
            <label for="company2">Name of Company</label><br />
            <input type="text" v-model="company2" />
            <label for="workLocation2">Location of Company</label><br />
            <input type="text" v-model="workLocation2" />
            <label for="yearStarted2">Year Started</label><br />
            <input
              v-on:input="listenFor28"
              type="text"
              v-model="yearStarted2"
            />
            <label for="yearFinished2">Year Finished</label><br />
            <input
              v-on:input="listenFor29"
              type="text"
              v-model="yearFinished2"
            />
            <label for="responsibilities">Responsibilities</label><br />
            <input
              v-on:input="listenFor20"
              class="input"
              type="text"
              v-model="responsibility2a"
            /><br />
            <input
              v-on:input="listenFor21"
              class="input"
              type="text"
              v-model="responsibility2b"
            /><br />
            <input
              v-on:input="listenFor22"
              class="input"
              type="text"
              v-model="responsibility2c"
            /><br />
          </div>

          <!-- Third work experience -->
          <div class="third-experience">
            <label for="jobTitle3">Job Title</label><br />
            <input type="text" v-model="jobTitle3" />
            <label for="company3">Name of Company</label><br />
            <input type="text" v-model="company3" />
            <label for="workLocation3">Location of Company</label><br />
            <input type="text" v-model="workLocation3" />
            <label for="yearStarted3">Year Started</label><br />
            <input
              v-on:input="listenFor30"
              type="text"
              v-model="yearStarted3"
            />
            <label for="yearFinished3">Year Finished</label><br />
            <input
              v-on:input="listenFor31"
              type="text"
              v-model="yearFinished3"
            />
            <label for="responsibilities">Responsibilities</label><br />
            <input
              v-on:input="listenFor23"
              class="input"
              type="text"
              v-model="responsibility3a"
            /><br />
            <input
              v-on:input="listenFor24"
              class="input"
              type="text"
              v-model="responsibility3b"
            /><br />
            <input
              v-on:input="listenFor25"
              class="input"
              type="text"
              v-model="responsibility3c"
            /><br />
          </div>
        </div>

        <div class="div-pagination">
          <button class="pagination">Previous</button>
          <button class="pagination" @click="changeForm">Next</button>
        </div>
      </div>

      <!-- Resume section -->

      <div class="resume" id="canvas">
        <div class="resume-aside">
          <!-- contact aside -->
          <div
            class="aside-contact"
            v-bind:style="{ 'background-color': this.color }"
          >
            <h2 class="contact-h2">
              {{ name }}
            </h2>
            <div class="div-con-para">
              <p class="contact-p">
                <span class="eduIcon" id="website"></span>{{ website }}
              </p>
              <p class="contact-p">
                <span class="eduIcon" id="email"></span>{{ email }}
              </p>
              <p class="contact-p">
                <span class="eduIcon" id="phone"></span>{{ phone }}
              </p>
              <p class="contact-p">
                <span class="eduIcon" id="location"></span>{{ location }}
              </p>
              <p class="contact-p">
                <span class="eduIcon" id="linkedin"></span>{{ linkedin }}
              </p>
              <p class="contact-p">
                <span class="eduIcon" id="twitter"></span>{{ twitter }}
              </p>
            </div>
          </div>

          <!-- education aside -->
          <div class="aside-education">
            <h2 class="education-h2">EDUCATION</h2>
            <div class="div-edu-para">
              <p class="education-p">{{ course }}</p>
              <p class="education-p" v-bind:style="{ color: this.color }">
                {{ school }}
              </p>
              <p class="education-p">
                <span class="eduIcon" id="eduIconCalender"></span>&nbsp;&nbsp;
                <!-- <i class="fa-solid fa-calendar-days"></i>&nbsp;&nbsp; -->
                {{ yearOfStart }}
                <span id="dash4"></span> {{ yearOfGrad }}
              </p>
              <p class="education-p">
                <span class="eduIcon" id="eduIconLocation"></span>&nbsp;&nbsp;
                <!-- <i class="fa-solid fa-location-dot con"></i>&nbsp;&nbsp; -->
                {{ schoolLocation }}
              </p>
            </div>
          </div>

          <!-- skills aside -->
          <div class="aside-skills">
            <h2>SKILLS</h2>
            <div class="div-skills-para">
              <span class="pointz" id="point1"></span>
              <p>{{ skill1 }}</p>
            </div>
            <div class="div-skills-para">
              <span class="pointz" id="point2"></span>
              <p>{{ skill2 }}</p>
            </div>
            <div class="div-skills-para">
              <span class="pointz" id="point3"></span>
              <p>{{ skill3 }}</p>
            </div>
            <div class="div-skills-para">
              <span class="pointz" id="point4"></span>
              <p>{{ skill4 }}</p>
            </div>
            <div class="div-skills-para">
              <span class="pointz" id="point5"></span>
              <p>{{ skill5 }}</p>
            </div>
            <div class="div-skills-para">
              <span class="pointz" id="point6"></span>
              <p>{{ skill6 }}</p>
            </div>
            <div class="div-skills-para">
              <span class="pointz" id="point7"></span>
              <p>{{ skill7 }}</p>
            </div>
            <div class="div-skills-para">
              <span class="pointz" id="point8"></span>
              <p>{{ skill8 }}</p>
            </div>
            <div class="div-skills-para">
              <span class="pointz" id="point9"></span>
              <p>{{ skill9 }}</p>
            </div>
          </div>
        </div>

        <!-- Career section -->
        <div class="aside-career">
          <div class="career-section">
            <h2>CAREER OBJECTIVE</h2>
            <p>{{ objectives }}</p>
          </div>

          <!-- Work experience -->
          <div class="work-experience">
            <h2>WORK EXPERIENCE</h2>

            <!-- first work experience -->
            <div class="first-experience">
              <h2>{{ jobTitle1 }}</h2>
              <p v-bind:style="{ color: this.color }">
                {{ company1 }}
              </p>
              <p>
                <span class="yearStartFinish" id="calender1"></span
                >&nbsp;&nbsp;&nbsp;&nbsp;{{ yearStarted1 }}
                <span id="dash1"></span>&nbsp;&nbsp;&nbsp;&nbsp;{{
                  yearFinished1
                }}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span
                  class="yearStartFinish"
                  id="location1"
                ></span
                >{{ workLocation1 }}
              </p>
              <div class="point-class">
                <div class="div-point1">
                  <span class="point div-point-child" id="res-point1a"></span>
                  <p>{{ responsibility1a }}</p>
                </div>
                <div class="div-point1">
                  <span class="point div-point-child" id="res-point1b"></span>
                  <p>{{ responsibility1b }}</p>
                </div>
                <div class="div-point1">
                  <span class="point div-point-child" id="res-point1c"></span>
                  <p>{{ responsibility1c }}</p>
                </div>
              </div>
            </div>

            <!-- second work experience -->
            <div class="second-experience">
              <h2>{{ jobTitle2 }}</h2>
              <p v-bind:style="{ color: this.color }">
                {{ company2 }}
              </p>
              <p>
                <span class="yearStartFinish" id="calender2"></span
                >&nbsp;&nbsp;&nbsp;&nbsp;{{ yearStarted2 }}
                <span id="dash2"></span>&nbsp;&nbsp;&nbsp;&nbsp;{{
                  yearFinished2
                }}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span
                  class="yearStartFinish"
                  id="location2"
                ></span
                >{{ workLocation2 }}
              </p>
              <div class="point-class">
                <div class="div-point1">
                  <span class="point div-point-child" id="res-point2a"></span>
                  <p>{{ responsibility2a }}</p>
                </div>
                <div class="div-point1">
                  <span class="point div-point-child" id="res-point2b"></span>
                  <p>{{ responsibility2b }}</p>
                </div>
                <div class="div-point1">
                  <span class="point div-point-child" id="res-point2c"></span>
                  <p>{{ responsibility2c }}</p>
                </div>
              </div>
            </div>

            <!-- third work experience -->
            <div class="third-experience">
              <h2>{{ jobTitle3 }}</h2>
              <p v-bind:style="{ color: this.color }">
                {{ company3 }}
              </p>
              <p>
                <span class="yearStartFinish" id="calender3"></span
                >&nbsp;&nbsp;&nbsp;&nbsp;{{ yearStarted3 }}
                <span id="dash3"></span>&nbsp;&nbsp;&nbsp;&nbsp;{{
                  yearFinished3
                }}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span
                  class="yearStartFinish"
                  id="location3"
                ></span
                >{{ workLocation3 }}
              </p>
              <div class="point-class">
                <div class="div-point1">
                  <span class="point div-point-child" id="res-point3a"></span>
                  <p>{{ responsibility3a }}</p>
                </div>
                <div class="div-point1">
                  <span class="point div-point-child" id="res-point3b"></span>
                  <p>{{ responsibility3b }}</p>
                </div>
                <div class="div-point1">
                  <span class="point div-point-child" id="res-point3c"></span>
                  <p>{{ responsibility3c }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="button">
          <button @click="download" class="btn">Click here to download</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import html2canvas from "html2canvas";
// import Form from "./Form.vue";
// import ""
export default {
  name: "ResumeAppMain",
  components: {
    // Form,
  },

  data() {
    return {
      form: 0,
      color: "#328078",
      name: "",
      website: "",
      email: "",
      phone: "",
      location: "",
      linkedin: "",
      twitter: "",
      course: "",
      school: "",
      yearOfStart: "",
      yearOfGrad: "",
      schoolLocation: "",
      skills: "",
      profileSummary: "",
      jobTitle1: "",
      jobTitle2: "",
      jobTitle3: "",
      company1: "",
      company2: "",
      company3: "",
      yearStarted1: "",
      yearStarted2: "",
      yearStarted3: "",
      yearFinished1: "",
      yearFinished2: "",
      yearFinished3: "",
      workLocation1: "",
      workLocation2: "",
      workLocation3: "",
      responsibility1a: "",
      responsibility1b: "",
      responsibility1c: "",
      responsibility2a: "",
      responsibility2b: "",
      responsibility2c: "",
      responsibility3a: "",
      responsibility3b: "",
      responsibility3c: "",
      skill1: "",
      skill2: "",
      skill3: "",
      skill4: "",
      skill5: "",
      skill6: "",
      skill7: "",
      skill8: "",
      skill9: "",
      skill10: "",
      objectives:
        "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur, vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?",
    };
  },

  mounted() {},

  computed: {},

  methods: {
    changeForm() {
      const form1 = document.getElementById("form1");

      console.log(form1);
    },

    download() {
      // console.log("im clicked");
      let element = document.querySelector("#canvas");
      html2canvas(element).then((canvas) => {
        // Convert the canvas to an image
        let image = canvas
          .toDataURL("image/png")
          .replace("image/png", "image/octet-stream");
        // Download the image
        let link = document.createElement("a");
        link.download = "your-resume.png";
        link.href = image;
        link.click();
      });
    },
    firstTheme() {
      this.color = "#328078";
    },
    secondTheme() {
      this.color = "#9d454c";
    },
    thirdTheme() {
      this.color = "#262c53";
    },
    fourthTheme() {
      this.color = "#6e462c";
    },
    changeColor() {},
    listenFor1() {
      const x = document.getElementById("website");
      x.innerHTML = `<i class="fa-solid fa-globe con"></i>&nbsp;&nbsp;`;
    },
    listenFor2() {
      const x = document.getElementById("email");
      x.innerHTML = `<i class="fa-solid fa-envelope"></i>&nbsp;&nbsp;`;
    },
    listenFor3() {
      const x = document.getElementById("phone");
      x.innerHTML = `<i class="fa-solid fa-phone con"></i>&nbsp;&nbsp;`;
    },
    listenFor4() {
      const x = document.getElementById("location");
      x.innerHTML = `<i class="fa-sharp fa-solid fa-location-dot con"></i>&nbsp;&nbsp;`;
    },
    listenFor5() {
      const x = document.getElementById("linkedin");
      x.innerHTML = `<i class="fa-brands fa-linkedin con"></i>&nbsp;&nbsp;`;
    },
    listenFor6() {
      const x = document.getElementById("twitter");
      x.innerHTML = `<i class="fa-brands fa-twitter con"></i>&nbsp;&nbsp;`;
    },
    makeUpper(event) {
      event.target.value = event.target.value.toUpperCase();
      // <i class="fa-solid fa-circle"></i>;
    },
    listenFor7() {
      const x = document.getElementById("point1");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor8() {
      const x = document.getElementById("point2");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor9() {
      const x = document.getElementById("point3");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor10() {
      const x = document.getElementById("point4");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor11() {
      const x = document.getElementById("point5");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor12() {
      const x = document.getElementById("point6");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor13() {
      const x = document.getElementById("point7");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor14() {
      const x = document.getElementById("point8");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor15() {
      const x = document.getElementById("point9");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor16() {
      const x = document.getElementById("point10");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor17() {
      const x = document.getElementById("res-point1a");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>`;
    },
    listenFor18() {
      const x = document.getElementById("res-point1b");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor19() {
      const x = document.getElementById("res-point1c");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor20() {
      const x = document.getElementById("res-point2a");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor21() {
      const x = document.getElementById("res-point2b");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor22() {
      const x = document.getElementById("res-point2c");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor23() {
      const x = document.getElementById("res-point3a");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor24() {
      const x = document.getElementById("res-point3b");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor25() {
      const x = document.getElementById("res-point3c");
      x.innerHTML = `<i class="fa-solid fa-circle"></i>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`;
    },
    listenFor26() {
      const x = document.getElementById("calender1");
      x.innerHTML = `<i class="fa-solid fa-calendar-days"></i>`;
      const y = document.getElementById("dash1");
      y.innerHTML = ` -`;
    },
    listenFor27() {
      const x = document.getElementById("location1");
      x.innerHTML = `<i class="fa-sharp fa-solid fa-location-dot"></i>&nbsp;&nbsp;`;
    },
    listenFor28() {
      const x = document.getElementById("calender2");
      x.innerHTML = `<i class="fa-solid fa-calendar-days"></i>`;
      const y = document.getElementById("dash2");
      y.innerHTML = ` -`;
    },
    listenFor29() {
      const x = document.getElementById("location2");
      x.innerHTML = `<i class="fa-sharp fa-solid fa-location-dot"></i>&nbsp;&nbsp;`;
    },
    listenFor30() {
      const x = document.getElementById("calender3");
      x.innerHTML = `<i class="fa-solid fa-calendar-days"></i>`;
      const y = document.getElementById("dash3");
      y.innerHTML = ` -`;
    },
    listenFor31() {
      const x = document.getElementById("location3");
      x.innerHTML = `<i class="fa-sharp fa-solid fa-location-dot"></i>&nbsp;&nbsp;`;
    },
    listenFor32() {
      const x = document.getElementById("eduIconCalender");
      x.innerHTML = `<i class="fa-solid fa-calendar-days"></i>&nbsp;&nbsp;`;
      const y = document.getElementById("dash4");
      y.innerHTML = ` -`;
    },
    listenFor33() {
      const x = document.getElementById("eduIconLocation");
      x.innerHTML = `<i class="fa-sharp fa-solid fa-location-dot"></i>&nbsp;&nbsp;`;
    },
  },
};
</script>

<style scoped>
.grid-container {
  /* max-width: 100%; */
  display: grid;
  grid-template-columns: 30% 70%;
  background: rgba(191, 188, 192, 0.2);
  /* grid-template-rows: repeat(1, 1fr); */
}
.resume-aside {
  /* max-width: 100%; */
  background: #f8f8f8;
  /* display: block; */
  margin: 0px;
  padding: 0px;
}

.aside {
  margin: 20px;
  padding: 10px;
  background: rgba(209, 215, 221, 0.4);
}
.resume {
  /* max-width: 100%; */
  display: grid;
  /* grid-template-columns: 323.3px 646.7px; */
  grid-template-columns: 33.33% 66.67%;
  margin: 20px 20px 10px 0px;
  height: 1255px;
  grid-template-rows: repeat(1 1fr);
}

label {
  margin-right: 10px;
}

input[type="text" i] {
  width: 100%;
}
input[type="email" i] {
  width: 100%;
}
.input {
  margin-bottom: 10px;
}
textarea[type="text" i] {
  width: 100%;
}

.form {
  margin-bottom: 20px;
  padding: 10px;
  display: block;
}

.aside-contact {
  margin: 0px;
  padding: 30px 20px 20px 40px;
  /* width: 323.3px; */
  height: 300px;
  background: #328078;
  color: #fff;
  /* padding: 0 20px; */
}

.aside-education {
  /* width: 323.3px; */
  height: 250px;
  background: #f8f8f8;
  padding: 20px;
}

.aside-skills {
  /* width: 323.3px; */
  height: 562px;
  background: #f8f8f8;
  padding: 20px;
}

.aside-career {
  max-width: 646.6px;
  height: 1255px;
  background: #fff;
  padding: 0 10px;
  text-align: justify;
}

.div-con-para {
  margin: 20px 0 0 0;
}
.contact-p,
.contact-h2 {
  margin: 0px;
  padding: 0px;
}

.contact-p {
  margin-bottom: 20px;
}

.career-section {
  height: 360px;
  padding: 10px 10px 0px 10px;
}

.work-experience {
  padding: 0 10px;
}
.point-class {
  margin: 10px 0 20px 20px;
}

.div-skills-para {
  display: grid;
  grid-template-columns: 10px 250px;
  column-gap: 15px;
  margin-bottom: 10px;
}

div.div-skills-para p {
  margin: 0px;
  /* margin-top: 10px; */
}
.pointz {
  margin-top: 4px;
  font-size: 8px;
  /* margin-top: 10px; */
}

.div-con-para {
  margin-top: 30px;
}

.div-point1 {
  display: grid;
  grid-template-columns: 10px 500px;
  column-gap: 30px;
  /* margin-bottom: 10px; */
}

div.div-point1 p {
  margin: 0px;
  margin-top: 10px;
}

.div-point-child {
  margin-top: 16px;
}

.point {
  font-size: 8px;
  margin-left: 20px;
}

.yearStartFinish {
  color: #e6e6e6;
}

.eduIcon {
  color: #e6e6e6;
}

.first-experience,
.second-experience,
.third-experience {
  margin-bottom: 50px;
}

button.btn {
  /* margin-left: auto;
  margin-right: auto; */
  /* align-content: center;
  align-items: center; */
  text-align: center;
  color: #328078;
  background: #fff;
  border: 1px #328078 solid;
  border-radius: 5px;
  padding: 10px;
  margin: 20px;
}

button.btn:hover {
  background: #328078;
  color: #fff;
  border: 1px #328078 solid;
}

/* div.button {
  position: relative;
  margin: 40px;
} */
/* button {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
} */
/* .button {
} */

.theme1 {
  color: #328078;
}
.theme2 {
  color: #9d454c;
}
.theme3 {
  color: #262c53;
}
.theme4 {
  color: #6e462c;
}

/* .div-pagination {
 
} */

.pagination {
  width: 80px;
  padding: 5px;
  margin: 0 10px;
}
</style>