<template>
    <nav class="tr">
            <div class="nav">
                <img src="@/assets/logo/logo-blue.png" alt="Krishna Apps Logo" />
                <span ref="spacer" class="spacer"></span>
                <menu-bar :name="key" :val="val" v-for="(val, key) in menu" :key="'menu' + key"/>
            </div>
        </nav>
</template>

<script>
import MenuBar from './MenuBar'
export default {
    name: 'NavBar',
    components: {
        MenuBar
    },
    data() {
        return {
            menu: {
                'Home': '#',
                'Services': {
                    'Software Development': 'https://www.upwork.com/signup/create-account/client_contact_freelancer?ciphertext=~0142999d8b15001517&BYOC',
                    'Business Training & Frenchise': 'https://www.badabusiness.com/dd/BIMK003866',
                    'Organic Marketing Training & Affiliate Program': 'https://leads-arc.web.app/'
                },
                'Our Apps': {
                    'All': 'https://play.google.com/store/apps/collection/cluster?clp=igM4ChkKEzUwMDkwNjA5NzAwNjg3NTk4ODIQCBgDEhkKEzUwMDkwNjA5NzAwNjg3NTk4ODIQCBgDGAA%3D:S:ANO1ljIhW_g&gsr=CjuKAzgKGQoTNTAwOTA2MDk3MDA2ODc1OTg4MhAIGAMSGQoTNTAwOTA2MDk3MDA2ODc1OTg4MhAIGAMYAA%3D%3D:S:ANO1ljJmSZ8',
                    'Featured': 'https://play.google.com/store/apps/dev?id=5009060970068759882',
                    'Srila Prabhupada Vani': 'https://play.google.com/store/apps/details?id=com.mayank.srilaprabhupadavani',
                    'ChatEasy - Easy Messaging': 'https://play.google.com/store/apps/details?id=c.kapps.easymessage.free'
                },
                'Blogs': 'https://mayank-1513.medium.com/',
                'Contact Us': 'https://mayank-chaudhari.web.app/',
            },
        }
    }
}
</script>
