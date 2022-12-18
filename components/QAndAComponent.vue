<template>
    <v-container>
    <v-row justify="center" align="center">
        <h1 :class="{'heading': $vuetify.breakpoint. smAndDown, 
      'display-3': $vuetify.breakpoint. mdAndUp}">Questions? Answers.</h1>
    </v-row>
    <v-list class="white black--text mt-15">
      <v-list-group
        v-for="item in items"
        :key="item.title"
      >
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title class="black--text">
                <h2>{{ item.title }}</h2>
                <v-divider class="mt-5"></v-divider>
            </v-list-item-title>
          </v-list-item-content>
        </template>
        

        <v-list-item>
          <v-list-item-content class="black--text">
           {{ item.des }}
           <a style="font-weight:bold;" class="mt-5" v-if="item.loadMore">{{item.loadMoreValue}}<v-icon small color="blue">mdi-chevron-right</v-icon></a>
          </v-list-item-content>
        </v-list-item>
      </v-list-group>
    </v-list>
    </v-container>
</template>

<script>
export default {
    setup() {
        const items = [
            {
                title: "What is Apple TV+?",
                des: "Apple TV+ is a streaming service featuring Apple Originals — award-winning series, compelling dramas,  groundbreaking documentaries, kids’ entertainment, comedies, and more — with new Apple Originals added every month.",
                loadMore: false,
                loadMoreValue: "",
            },
            {
                title: "How can I watch it?",
                des: "Watch Apple TV+ on the Apple TV app, which is already on your favorite Apple devices. Just open the app, click or tap Apple TV+, and enjoy the shows and movies. You can also watch Apple TV+ on streaming platforms, popular smart TVs, and AirPlay-enabled TVs with the Apple TV app — or watch online at tv.apple.com.",
                loadMore: true,
                loadMoreValue: "Learn more",
            },
            {
                title: "What does it cost?",
                des: "That all depends on which offer you choose. (1) If you buy an Apple device, Apple TV+ is included free for 3 months.1 (2) A monthly subscription is just $6.99 per month after a free seven-day trial.2(3) Apple TV+ is included in Apple One, which bundles up to five other Apple services into a single monthly subscription. Apple One plans start at $16.95 per month. (4) The Apple Music Student Plan comes with a free subscription to Apple TV+.4",
                loadMore: false,
                loadMoreValue: "",
            },
            {
                title: "Can I shre with my family?",
                des: "Of course. Apple TV+ lets you share your subscription with up to five family members.",
                loadMore: false,
                loadMoreValue: "",
            },
            {
                title: "What is Apple TV+?",
                des: "Apple TV+ is a streaming service featuring Apple Originals — award-winning series, compelling dramas, groundbreaking documentaries, kids’ entertainment, comedies, and more — with new Apple Originals added every month.",
                loadMore: false,
                loadMoreValue: "",
            },
            {
                title: "Are there commercials? And can I watch on demand?",
                des: "Apple Originals are always commercial-free. Some shows release all episodes at once. Other shows add new episodes every Friday. You can then watch them on demand anytime, anywhere.",
                loadMore: false,
                loadMoreValue: "",
            },
            {
                title: "Do I need an Apple TV 4K?",
                des: "No, you don’t. While Apple TV 4K — with 4K HDR and Dolby Atmos sound — is the ultimate way to experience Apple TV+, the original shows and movies on Apple TV+ are always available on the Apple TV app on your favorite devices.",
                loadMore: true,
                loadMoreValue: "See all supported devices",
            },
            {
                title: "Can I download to watch offline?",
                des: "Absolutely. Download your favorite Apple Originals to your Apple device and watch them anywhere, anytime without a Wi-Fi connection.",
                loadMore: false,
                loadMoreValue: "",
            },
        ]
        return { items }
    }
}
</script>

<style>

</style>