<template>
  <div class="home-page">
    <img class="home-image-img" src="../../src/styles/imgs/websiteBackground.png" alt="" />
    <!-- <div class="ji"></div> -->
    <div class="img-text">
      <h1>header text</h1>
      <h5>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque quae facere doloremque nostrum debitis voluptate? dolorum, aperiam
        eum nemo neque ex ab consectetur!
      </h5>
      <button class="btn">Let`s Start !</button>
    </div>

    <div class="main-layout offer-container">
      <h1>מה אנחנו מציעים?</h1>
      <h4>אנו במיקוד מאמינים בהשגת פועלים מתחושת שליחות תוך יצירת בלה בלה ממש רציני</h4>
      <div class="offer-list">
        <div v-for="offer in offers" key="offers.indexOf(offer)" class="offer">
          <img :src="offer.icon" alt="" />
          <h4>{{ offer.title }}</h4>
          <h6 class="offer-description">{{ offer.description }}</h6>
        </div>
      </div>
    </div>

    <div class="about-us">
      <div class="main-layout">
        <h1>מי אנחנו?</h1>
        <h6 class="about-sub-title">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Facere libero veritatis quas ex ut commodi explicabo at ipsam dicta.
        </h6>

        <div class="flex about-info-cont">
          <div class="about-info">
            <p>
              {{ lorem }}
              {{ lorem }}
            </p>
            <button class="btn about-btn">learn more</button>
          </div>
          <img class="about-img" src="../../src/styles/imgs/cover.png" alt="" />
        </div>
      </div>
    </div>

    <!-- <div class="red">
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
    </div> -->

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
              {{ lorem }}
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
              {{ lorem }}
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
              {{ lorem }}
            </p>
            <button class="learning-btn">למד עוד</button>
            <RouterLink to="/contactUs"><button class="learning-btn">הרשם</button></RouterLink>
          </div>
        </div>
      </div>
    </main>

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
      offers: [
        {
          icon: '../../src/styles/imgs/icon0.png',
          title: 'ביהס לעברית',
          description: ' ביה"ס לעברית מציע מגוון רחב של שיעורים המלמדים בלה בלה',
        },
        {
          icon: '../../src/styles/imgs/icon0.png',
          title: 'סטודנטים',
          description: 'אנחנו כאן להציע מרתונים לפני המבחנים, ושיעורים פרטיים במהלך הסמסטר',
        },
        {
          icon: '../../src/styles/imgs/icon0.png',
          title: 'ביה"ס לאנגלית',
          description: 'ביה"ס לאנגלית מציע מגוון  שיעורי אנגלית לשיפור הדיבור  והכתיבה',
        },
        {
          icon: '../../src/styles/imgs/icon0.png',
          title: 'שיעורים פרטיים',
          description: 'צוות מורים מקצועיים המכינים מערכי שיעור מותאמים לרמת התלמיד ותכנית התקדמות',
        },
        { icon: '../../src/styles/imgs/icon0.png', title: 'מרכז בגבעת שמואל', description: 'המון דברים ממש כיפיים  ולימודיים מתרחשים פה' },
        { icon: '../../src/styles/imgs/icon0.png', title: 'היי למה לא', description: 'אני כאן כל הזמן' },
      ],
      lorem:
        ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex consequatur, quam ut optio quisquam dolorem maiores perspic totam cupiditate asperiores provident praesentium nesciunt aperiam ipsam reiciendis aliquid adipisci sit beatae',
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
