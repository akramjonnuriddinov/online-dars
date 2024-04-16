<script setup lang="ts">
const graduateLists = [
  {
    id: '1',
    text: 'Veb dizayn chizish'
  },
  {
    id: '2',
    text: 'Mobil dizayn chizish'
  },
  {
    id: '3',
    text: 'Chuqur UX analiz'
  },
  {
    id: '4',
    text: 'Veb dizayn chizish'
  },
  {
    id: '5',
    text: 'Mobil dizayn chizish'
  },
  {
    id: '6',
    text: 'Chuqur UX analiz'
  },
  {
    id: '7',
    text: 'Veb dizayn chizish'
  },
  {
    id: '8',
    text: 'Mobil dizayn chizish'
  },
  {
    id: '9',
    text: 'Chuqur UX analiz'
  }
]
</script>

<template>
  <section class="graduate">
    <div class="container graduate__container">
      <h2 class="graduate__title base-title">
        Siz kursni <span class="base-title-red">bitirganindan so’ng:</span>
      </h2>
      <div class="graduate__inner">
        <div class="graduate__inner-header">
          <div class="graduate__inner-header-left">
            <img
              class="graduate__user-img"
              src="/src/assets/images/graduate/student.png"
              alt="student_img"
            />
            <div class="graduate__user-info">
              <span class="graduate__inner-text-light uppercase">Mutaxassisligi</span>
              <span class="graduate__inner-text-bold uppercase">UX/UI DESIGNER</span>
            </div>
          </div>
          <div class="graduate__inner-header-right">
            <span class="graduate__inner-text-light uppercase">Oyligi</span>
            <span class="graduate__inner-text-bold">5 000 000 so’mdan</span>
          </div>
        </div>
        <div class="graduate__body">
          <h3 class="graduate__body-title">Nimalar qila oladi?</h3>
          <ul class="graduate__list">
            <li
              v-for="graduateList in graduateLists"
              :key="graduateList.id"
              class="graduate__list-item"
            >
              <span class="graduate__list-icon"></span>
              <p class="graduate__list-text">{{ graduateList.text }}</p>
            </li>
          </ul>
        </div>
        <div class="graduate__certificate">
          <div class="graduate__certificate-inner">
            <h3 class="graduate__certificate-title">Onlinedars sertifikati</h3>
            <p class="graduate__certificate-text">
              Bizni kursimizni yakunlaganingizni tasdiqlaydi va albatta ishga joylashishingizga
              yordam beradi
            </p>
          </div>
          <img src="@/assets/images/graduate/certificate.jpg" alt="certificate" />
        </div>
      </div>
    </div>
  </section>
</template>
