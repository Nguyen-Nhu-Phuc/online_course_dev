<template>
  <div class="grid wide">
    <BannerIntro />
    <BannerSkill />

    <h4 style="margin-bottom: 1rem;">GIỚI THIỆU KHÓA HỌC TẠI IVY ACADEMIA</h4>
    <div class="row row-video-intro">
      <div class="col lg-4 md-6 col-8">
        <vue-plyr ref="plyr">
          <div class="plyr__video-embed">
            <iframe class="player" src="https://www.youtube.com/embed/qpdVd710rC8?si=MB1mPkau8MVUYGps" allowfullscreen
              allowtransparency></iframe>
          </div>
        </vue-plyr>
      </div>
      <div class="col lg-4 md-6 col-8">
        <vue-plyr ref="plyr">
          <div class="plyr__video-embed">
            <iframe class="player" src="https://www.youtube.com/embed/DpvYHLUiZpc?si=Tnzfsrn_HYbXZqiD" allowfullscreen
              allowtransparency></iframe>
          </div>
        </vue-plyr>
      </div>
      <div class="col lg-4 md-6 col-8">
        <vue-plyr ref="plyr">
          <div class="plyr__video-embed">
            <iframe class="player" src="https://www.youtube.com/embed/YH-E4Y3EaT4?si=M4m2aUGXMNWGU9Si" allowfullscreen
              allowtransparency></iframe>
          </div>
        </vue-plyr>
      </div>
    </div>
  </div>
</template>

<script>
import BannerIntro from './BannerIntro.vue';
import BannerSkill from './BannerSkill.vue';
import { useUserStore } from '../../stores/user.js';

export default {
  components: { BannerIntro, BannerSkill },
  setup() {
    const userStore = useUserStore();
    return {
      userStore
    }
  },
  async created() {
    if (this.userStore.account.role == 'Admin') {
      this.$router.push('/admin');
    }
  }
}
</script>
<style lang="scss" scoped>
.row-video-intro {
  margin-bottom: 1.5rem;
  overflow: auto;
  flex-wrap: nowrap;
}
</style>