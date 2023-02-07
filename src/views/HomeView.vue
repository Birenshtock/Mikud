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

    <div class="about-us">
      <div class="main-layout">
        <h1 class="about-title">? מי אנחנו</h1>
        <h6 class="about-sub-title">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Facere libero veritatis quas ex ut commodi explicabo
          at ipsam dicta.
        </h6>

        <div class="flex about-info-cont">
          <div class="about-info">
            &quot;מיקוד&quot; מרכז למידה הוא מרכז המציע שיעורים פרטיים וקבוצות למידה לתלמידים כיתות א עד יב, כמו כן גם
            לסטודנטים. במרכז זה
            יש מרכז ראשי בגבעת שמואל, שמוביל חוויות למידה מועילות ומתאימות לצרכי כל תלמיד. כמו כן, מיקוד מרכז למידה
            מקיים שיתופי פעולה עם
            בתי ספר וחוויות למידה מאופיינות להפעלה ולהשתתפות בלמידה המועילה ביותר. מורי המרכז מקצועיים ונדיבים, ומאמינים
            באינטראקציה מול
            התלמידים כדי להביא אותם לדרך לימוד המוצלחת. המרכז מכוון לעזור לתלמידים להשתפר בנושאים שמאופצים עליהם ולקבל
            ידע במיני ועמוק. אנו
            מאמינים בכל אחד ואחת.
          </div>
          <svgg />
        </div>
      </div>
    </div>

    <main class="learning-types main-layout">
      <div>
        <div class="learning-titles">
          <h1>צורות הלמידה אצלינו</h1>
          <h6 class="sub-title">כל המורים עוברים הסמכה אצלינו במרכז</h6>
        </div>

        <div class="learning-items">
          <div class="learning-item">
            <img src="../../src/styles/imgs/private-lesson.png" alt="" />

            <div class="learning-item-info">
              <h3>שיעורים פרטיים</h3>
              <div class="flex space-between">
                <h6>מספר תלמידים: 1</h6>
                <h6>ע"י: עדי</h6>
              </div>
              <p>
                {{ lorem }}
              </p>
            </div>
          </div>
          <div class="learning-item">
            <img src="../../src/styles/imgs/wwww.png" alt="" />

            <div class="learning-item-info">
              <h3>מרתונים</h3>

              <div class="flex space-between">
                <h6>מספר תלמידים: עד 5</h6>
                <h6>ע"י: עדי</h6>
              </div>
              <p>
                {{ lorem }}
              </p>
            </div>
          </div>
          <div class="learning-item">
            <img src="../../src/styles/imgs/zoom-call.png" alt="" />
            <div class="learning-item-info">
              <h3>למידה מרחוק</h3>

              <div class="flex space-between">
                <h6>מספר תלמידים: 1</h6>
                <h6>ע"י: עדי</h6>
              </div>
              <p>
                {{ lorem }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </main>

    <div class="main-layout flex review-container">
      <reviews />
    </div>
  </div>
</template>
<script>
import svgg from '../components/svg-aboutus.vue'
import open from '../components/home-open.vue'
import reviews from '../components/reviews.vue'
export default {
  components: { svgg, open, reviews },
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

<style>

</style>
