<template>
  <div class="team-area pt-100 pb-70">
    <div class="container">
      <div class="section-title text-center">
        <span class="sp-color2">Our Team</span>
        <h2>Our Team Members</h2>
      </div>
      <div class="row pt-45" v-if="team.teams.length >= 1">
        <div
          v-for="member in team.teams"
          :key="member.id"
          class="col-sm-6 col-md-4 projects-col"
        >
          <div class="card">
            <div class="thumb">
              <img :src="member.image" alt="" />
              <div class="rollover"></div>
            </div>
            <div class="content">
              <h4>{{ member.name }}</h4>
              <h5>{{ member.job }}</h5>
              <h6>
                {{ member.description.substring(0, 200) }}
                {{ member.description.length > 200 ? "..." : "" }}
              </h6>
              <h5>{{ member.phone }}</h5>
              <h5>{{ member.email }}</h5>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppTeamMembers",
  props: ["team"],
};
</script>

<style>
.team-area .section-title {
  margin-bottom: 0;
}
.section-title span {
  margin-bottom: 8px;
  font-weight: 600;
  display: block;
  color: #ffa737;
}
.team-area .section-title h2 {
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
  font-size: 35px;
  font-weight: 600;
  margin-top: 0;
  line-height: 1.2;
  color: var(--main-color);
  margin-bottom: 0;
}
.projects-col {
  text-align: center;
  margin-bottom: 40px;
}
.projects-col .thumb {
  margin-bottom: 18px;
  text-align: center;
  display: inline-block;
}
.projects-col .thumb img {
  border-radius: 50%;
  width: 200px;
}
.projects-col .content h4 {
  color: var(--main-color);
  font-size: 20px;
  margin-bottom: 10px;
  letter-spacing: 1px;
  text-transform: uppercase;
}
.projects-col .content h5 {
  font-size: 16px;
  margin-bottom: 20px;
  letter-spacing: 1px;
  color: var(--main-color);
}
.projects-col .content h6 {
  color: #989898;
  font-family: Open Sans, sans-serif;
  font-size: 14px;
  text-transform: uppercase;
  margin-bottom: 15px;
  line-height: 28px;
  letter-spacing: 0.3px;
}
.projects-col .content h3 {
  color: #ffa737;
  text-transform: uppercase;
  font-size: 20px;
}
</style>
