<template>
    <v-container class="black--text">
        <p>
        * MLS Season Pass requires a subscription.
        </p>
        <p>
        1.$6.99/month after free trial. Only one offer per Apple ID and only one offer per family if you’re part of a Family Sharing group, regardless of the number of devices you or your family purchases. This offer is not available if you or your Family have previously accepted an Apple TV+ one year free offer. Offer good for 3 months after eligible device activation. Plan automatically renews until cancelled. Restrictions and other terms apply.
        </p>
        <p>
        2.One subscription per Family Sharing group. Plan automatically renews until cancelled.
        </p>
        <p>
        3.The Apple One free trial includes only services that you are not currently using through a free trial or a subscription. Plan automatically renews after trial until cancelled. Restrictions and other terms apply.
        </p>
        <p>
        4.Limited-time offer; offer may end at any time. Free Apple TV+ access for students ends when you no longer qualify or do not renew your Apple Music Student subscription. Offer good for verified college students only and does not extend to a Family Sharing group.
        </p>

      <v-divider class="mb-5"></v-divider>

      <v-icon small class="mb-1">mdi-apple</v-icon>
      <v-icon>mdi-chevron-right</v-icon>  only on Apple
      <v-icon>mdi-chevron-right</v-icon> Apple TV+

      

      <v-row justify="center" align="center"> 
        <v-col cols="12" lg="2" md="3">
            <v-list-item two-line>
                <v-list-item-content>
                    <v-list-item-title>Shop and Learn</v-list-item-title>
                    <span  v-for="(item, i) in list1"
                    :key="i">
                        <v-list-item-subtitle>{{item}}</v-list-item-subtitle>
                    </span>
                </v-list-item-content>
            </v-list-item>
        </v-col>

        <v-col cols="12" lg="2" md="3">
            <v-list-item two-line>
                <v-list-item-content>
                    <v-list-item-title>Services</v-list-item-title>
                    <span  v-for="(item, i) in list2"
                    :key="i">
                        <v-list-item-subtitle>{{item}}</v-list-item-subtitle>
                    </span>
                </v-list-item-content>
            </v-list-item>
        </v-col>

        <v-col cols="12" lg="2" md="3">
            <v-list-item two-line>
                <v-list-item-content>
                    <v-list-item-title>Apple store</v-list-item-title>
                    <span  v-for="(item, i) in list3"
                    :key="i">
                        <v-list-item-subtitle>{{item}}</v-list-item-subtitle>
                    </span>
                </v-list-item-content>
            </v-list-item>
        </v-col>

        <v-col cols="12" lg="2" md="3">
            <v-list-item two-line>
                <v-list-item-content>
                    <v-list-item-title>For Business</v-list-item-title>
                    <span  v-for="(item, i) in list4"
                    :key="i">
                        <v-list-item-subtitle>{{item}}</v-list-item-subtitle>
                    </span>
                </v-list-item-content>
            </v-list-item>
        </v-col>

        <v-col cols="12" lg="2" md="3">
            <v-list-item two-line>
                <v-list-item-content>
                    <v-list-item-title>Apple Value</v-list-item-title>
                    <span  v-for="(item, i) in list5"
                    :key="i">
                        <v-list-item-subtitle>{{item}}</v-list-item-subtitle>
                    </span>
                </v-list-item-content>
            </v-list-item>
        </v-col>

      </v-row>

      </v-container>
</template>

<script>
export default {
    setup() {
        const list1 = [ 
            'Store',
            'Mac',
            'iPad',
            'iPhone',
            'Watch',
            'AirPods',
            'TV & Home',
            'AirTag',
            'Accessories',
            'Gift Cards',
            '.',
        ]

        const list2 = [
            'Apple Music',
            'Apple TV+',
            'Apple Fitness+',
            'Apple News+',
            'Apple Arcade',
            'iCloud',
            'Apple One',
            'Apple Card',
            'Apple Books',
            'Apple Podcasts',
            'App Store',
            'Manage Your Apple ID',
            'Apple Store Account',
            'iCloud.com',
        ]

        const list3 = [
            'Find a Store',
            'Genius Bar',
            'Today at Apple',
            'Apple Camp',
            'Apple Store App',
            'Refurbished and Clearance',
            'Financing',
            'Apple Trade In',
            'Order Status',
            'Shopping Help',
        ]

        const list4 = [
            'For Business',
            'Apple and Business',
            'Shop for Business',
            'For Education',
            'Apple and Education',
            'Shop for K-12',
            'Shop for College',
            'For Healthcare',
            'Apple in Healthcare',
            'Health on Apple Watch',
            'Health Records on iPhone',
            'For Government',
            'Shop for Government',
            'Shop for Veterans and Military',
        ]

        const list5 = [
            'Accessibility',
            'Education',
            'Environment',
            'Inclusion and Diversity',
            'Privacy',
            'Racial Equity and Justice',
            'Supplier Responsibility',
            'About Apple',
            'Newsroom',
            'Apple Leadership',
            'Career Opportunities',
            'Investors',
            'Ethics & Compliance',
            'Events',
            'Contact Apple',
    ]

    
        return {
            list1,
            list2,
            list3,
            list4,
            list5
        }
    }
}
</script>

<style>

</style>