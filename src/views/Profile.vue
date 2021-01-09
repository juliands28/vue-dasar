<template>
  <div class="profile">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-6">
          <div class="media text-left">
            <img
              src="../assets/starbucks-logo-BFBFE6C3A3-seeklogo.com.png"
              class="mr-3 user-pic"
              alt="user-pic"
            />
            <div class="media-body">
              <h5 class="mt-0">{{ firstName }} {{ lastName }}</h5>
              <p>
                {{ bio }}
              </p>
            </div>
          </div>
        </div>
      </div>
      <section id="app">
        <div class="row mt-5 justify-content-center">
          <div class="col-lg-6 text-left">
            <h2>What I do to day?</h2>
          </div>
          <div class="col-lg-8">
            <div class="pekerjaan-rumah">
              <div
                v-for="tugasSaya in tugas"
                v-bind:key="tugasSaya.id"
                class="tugas mb-3 text-left"
              >
                <item-tugas v-bind:tugasSaya="tugasSaya" />
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import "bootstrap/dist/css/bootstrap.css";
import ItemTugas from "@/components/ItemTugas.vue";

export default {
  name: "profile",
  data: function() {
    return {
      firstName: "Dini",
      lastName: "Julian",
      bio:
        "Cras sit amet nibh libero, in gravida nulla. Nulla vel metus scelerisque ante sollicitudin.",
      tugas: [
        {
          id: 1,
          namaTugas: "belajar Buildwith Angga",
          isDone: false,
        },
        {
          id: 2,
          namaTugas: "coding website",
          isDone: false,
        },
        {
          id: 3,
          namaTugas: "Nonton Netflix",
          isDone: false,
        },
        {
          id: 3,
          namaTugas: "Cari Kerja",
          isDone: false,
        },
      ],
    };
  },
  components: {
    // HelloWorld
    ItemTugas,
  },
};
</script>

<style scoped>
.user-pic {
  width: 80px;
  height: 80px;
  border-radius: 100%;
}
.tugas {
  margin-left: 100px;
}
.tugas .item {
  font-size: 18px;
}
.item-complate {
  color: #1abc9c;
}
</style>
