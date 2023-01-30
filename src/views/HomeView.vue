<template>
  <div class="home-page">
    <img class="home-image-img" src="../../src/styles/imgs/home-img.png" alt="" />
    <div class="img-text">
      <h1>header text</h1>
      <h5>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque quae facere doloremque nostrum debitis voluptate? dolorum, aperiam
        eum nemo neque ex ab consectetur!
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
            <RouterLink to="/contactUs"><button class="learning-btn">הרשם</button></RouterLink>
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

    <hr>

    <div class="main-layout flex review-container">
      <button class="left-btn btn" @click="moveReview(-1)"><i class="fa-solid fa-chevron-left"></i></button>
      <div class="flex img-txt-cont">
        <img class="review-img" :src="reviewImg" alt="no" />
        <div class="review-txt">
          <h6 class="review-txt-sub">{{ reviews[i].reviewDscription }}</h6>
          <h1 class="review-txt-title">{{ reviews[i].reviewInfo }}</h1>
          <!-- {{ reviews[i] }} -->
        </div>
      </div>
      <button class="right-btn btn" @click="moveReview(+1)"><i class="fa-solid fa-chevron-right"></i></button>
    </div>
    
  </div>

</template>
<script>
export default {
  components: {},
  data: () => {
    return {
      i: 0,

      reviews: [
        { reviewDscription: '4 שעות עברית בשבוע | במרכז למידה ברעננה', reviewInfo: 'אמא של תלמיד כיתה ד עולה חדש ממקסיקו' },
        { reviewDscription: 'שיעור אחד בשבוע | בבית בתלמידה', reviewInfo: 'שני תלמידת גיתה י"א, 4 יחידות מתמטיקה' },

        { reviewDscription: 'שיעור 1 בשבוע לאורך הסמסטר |   זום', reviewInfo: 'עדי, סטודנטית להנדסת חשמל בבר אילן אחרי מבחן בחדו"א 1' },

        ,
      ],
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
}
</script>

<style></style>


