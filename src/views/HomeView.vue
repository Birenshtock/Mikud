<template>
  <div class="home-page">
    <img class="home-image-img" src="../../src/styles/imgs/222.png" alt="" />
    <div class="img-text">
      <h1>header text</h1>
      <h5>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque quae facere doloremque nostrum debitis voluptate? Laudantium
        dolorum, ad id ut quibusdam praesentium repellat, aperiam eum nemo neque ex ab consectetur!
      </h5>
      <button>Let`s Start !</button>
    </div>

    <div class="red">
      <div class="title-background"></div>

      <div class="bi">
        <h1 class="hi main-layout">?מי אנחנו</h1>
      </div>

      <div class="about-container main-layout">
        <img class="student-sticker" src="../../src/styles/imgs/סטיקר.png" alt="" />
        <p class="about">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Vel fugiat sint exercitationem provident molestiae esse autem
          necessitatibus, cum consequuntur earum repellat laudantium, velit, modi corrupti! Asperiores similique neque laborum id? Lorem
          ipsum dolor, sit amet consectetur adipisicing elit. Eligendi quod quas placeat in maxime explicabo. Ab ullam consequuntur,
          provident sed reprehenderit consectetur necessitatibus culpa explicabo pariatur! Placeat rem facere sunt.
        </p>
      </div>
    </div>

    <main class="learning-types main-layout">
      <div>
        <div class="learning-titles">
          <h1>צורות הלמידה אצלינו</h1>
          <h6 class="sub-title">כל המורים עוברים הסמכה אצלינו במרכז</h6>

          <div><i class="fa-sharp fa-solid fa-graduation-cap"></i></div>
        </div>

        <div class="learning-items">
          <div class="learning-item">
            <img src="../../src/styles/imgs/private-lesson.png" alt="" />
            <h3>שיעורים פרטיים</h3>
            <div class="flex space-between">
              <h6>מספר תלמידים: 1</h6>
              <h6>ע"י: עדי</h6>
            </div>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi eveniet quo odio aperiam eligendi, vel soluta, voluptatibus
              alias voluptate tenetur enim deserunt facilis a nobis id rerum ipsa corporis odit.
            </p>
            <button class="learning-btn">למד עוד</button>
            <RouterLink to="/contactUs"><button class="learning-btn">הרשם</button></RouterLink>
          </div>
          <div class="learning-item">
            <img src="../../src/styles/imgs/wwww.png" alt="" />
            <h3>קבוצות למידה</h3>

            <div class="flex space-between">
              <h6>מספר תלמידים: עד 5</h6>
              <h6>ע"י: עדי</h6>
            </div>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi eveniet quo odio aperiam eligendi, vel soluta, voluptatibus
              alias voluptate tenetur enim deserunt facilis a nobis id rerum ipsa corporis odit.
            </p>
            <button class="learning-btn">למד עוד</button>
<<<<<<< HEAD
=======
            <RouterLink to="/contactUs"><button class="learning-btn">הרשם</button></RouterLink>
>>>>>>> 903d5542bd4edd2d9df564799aa0aba5a1961076
          </div>
          <div class="learning-item">
            <img src="../../src/styles/imgs/zoom-call.png" alt="" />
            <h3>למידה מרחוק</h3>

            <div class="flex space-between">
              <h6>מספר תלמידים: 1</h6>
              <h6>ע"י: עדי</h6>
            </div>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi eveniet quo odio aperiam eligendi, vel soluta, voluptatibus
              alias voluptate tenetur enim deserunt facilis a nobis id rerum ipsa corporis odit.
            </p>
            <button class="learning-btn">למד עוד</button>
            <RouterLink to="/contactUs"><button class="learning-btn">הרשם</button></RouterLink>
          </div>
        </div>
      </div>
    </main>

    <div class="main-layout flex review-container">
      <button class="left-btn btn" @click="moveReview(-1)">left</button>
      <div class="flex">
        <!-- <img src="../../src/styles/imgs/review0.jpeg" alt="" /> -->
        <img :src="reviewImg" alt="no" />
        <div>{{ reviews[i] }}</div>
      </div>
      <button class="right-btn btn" @click="moveReview(+1)">right</button>
    </div>
  </div>
</template>
<script>
export default {
  components: {},
  data: () => {
    return {
      i: 0,

      reviews: ['אמא של תלמיד כיתה ד עולה חדש ממקסיקו', 22222222222, 33],
    }
  },
  methods: {
    moveReview(dif) {
      var currNum = this.i + dif
      console.log('currNum', currNum)
      if (currNum === 3) {
        this.i = 0
      } else if (currNum === -1) {
        this.i = 2
      } else {
        this.i = currNum
      }
    },
  },
  computed: {
    reviewImg() {
      return `../../src/styles/imgs/review${this.i}.jpeg`
    },
  },
<<<<<<< HEAD
=======
  methods: {
  },
  computed: {},
>>>>>>> 903d5542bd4edd2d9df564799aa0aba5a1961076
}
</script>

<style></style>
