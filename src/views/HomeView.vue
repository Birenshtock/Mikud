<template>
  <div class="home-page">
    <div class="flex home-open main-layout">
      <open />
    </div>

    <div class="main-layout offer-container">
      <h1>מה אנחנו מציעים?</h1>
      <h4>אנו במיקוד מאמינים בהשגת פועלים מתחושת שליחות תוך יצירת בלה בלה ממש רציני</h4>
      <div class="offer-list">
        <div v-for="offer in offers" key="offers.indexOf(offer)" class="offer">
          <img class="offer-gif" :src="offer.icon" alt="" />
          <h4>{{ offer.title }}</h4>
          <h6 class="offer-description">{{ offer.description }}</h6>
        </div>
      </div>
    </div>

    <aboutUs></aboutUs>
    <learningTypes></learningTypes>

    <div class="main-layout flex review-container">
      <reviews />
    </div>
  </div>
</template>
<script>
import aboutUs from '../components/about.vue'
import learningTypes from '../components/learning-types.vue'
import svgg from '../components/svg-aboutus.vue'
import open from '../components/home-open.vue'
import reviews from '../components/reviews.vue'
export default {
  components: { svgg, open, reviews, aboutUs, learningTypes },
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
          icon: '../../src/styles/imgs/Reading-Book.gif',

          title: 'ביהס לעברית',
          description: ' ביה"ס לעברית מציע מגוון רחב של שיעורים המלמדים בלה בלה',
        },
        {
          icon: '../../src/styles/imgs/Creative-Thinking.gif',
          title: 'סטודנטים',
          description: 'אנחנו כאן להציע מרתונים לפני המבחנים, ושיעורים פרטיים במהלך הסמסטר',
        },
        {
          icon: '../../src/styles/imgs/Web-Browsing.gif',

          title: 'ביה"ס לאנגלית',
          description: 'ביה"ס לאנגלית מציע מגוון  שיעורי אנגלית לשיפור הדיבור  והכתיבה',
        },
        {
          icon: '../../src/styles/imgs/Form-Filling.gif',

          title: 'שיעורים פרטיים',
          description: 'צוות מורים מקצועיים המכינים מערכי שיעור מותאמים לרמת התלמיד ותכנית התקדמות',
        },
        {
          icon: '../../src/styles/imgs/Online-Study.gif',
          title: 'מרכז בגבעת שמואל',
          description: 'המון דברים ממש כיפיים  ולימודיים מתרחשים פה',
        },
        {
          icon: '../../src/styles/imgs/Telescope.gif',

          title: 'תוכנית גפן',
          description: 'אני כאן כל הזמן',
        },
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
