<template>
    <div>
        <h1>LIST CLASS</h1>
        <div class="row">
            <div class="col-sm-6" v-for="(item,i) in listClass" :key="i">
                <!-- <class-item :name="item.name" :desc="item.desc" /> -->
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title">{{ item.name }}</h5>
                        <p class="card-text">{{ item.desc }}</p>
                        <a href="#" class="btn btn-primary">{{ item.link }}</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default {
  asyncData() {
    return {
      listClass: [
        { name: "Data Science", desc: "Ini kelas DATA SCIENCE", link: "Lihat Kelas" },
        { name: "Data Analyst", desc: "Ini kelas DATA ANALYST", link: "Lihat Kelas" },
        { name: "Fullstack Developer", desc: "Ini kelas FULLSTACK DEVELOPER", link: "Lihat Kelas" },
        { name: "Digital Marketing", desc: "Ini kelas DIGITAL MARKETING", link: "Lihat Kelas" },
        ],
    };
  },
};
</script>