<template>
    <section class="links-footer">
        <div class="my-container links-wrap">
            <div class="links">
                <div class="link">
                    <span class="title">dc comics</span>
                    <ul>
                        <li v-for="(link, i) in linksComics"><a href="link.url">{{link.text}}</a></li>
                    </ul>
                    <span class="title">shop</span>
                    <ul>
                        <li v-for="(link, i) in linksShop"><a href="link.url">{{link.text}}</a></li>
                    </ul>
                </div>
                <div class="link">
                    <span class="title">dc</span>
                    <ul>
                        <li v-for="(link, i) in linksDc"><a href="link.url">{{link.text}}</a></li>
                    </ul>
                </div>
                <div class="link">
                    <span class="title">sites</span>
                    <ul>
                        <li v-for="(link, i) in linksSites"><a href="link.url">{{link.text}}</a></li>
                    </ul>
                </div>
            </div>
            <div class="img-box"><img src="/img/dc-logo-bg.png" alt=""></div>
        </div>
    </section>
</template>

<script>
    export default {
        data(){
            return{
                linksComics: [
                    {
                        text: "Characters",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Comics",
                        url: "#",
                        active: true,
                    },
                    {
                        text: "Movies",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "TV",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Games",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Collectibles",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Videos",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Fans",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "News",
                        url: "#",
                        active: false,
                    },
                ],
                linksShop: [
                    {
                        text: "Shop DC",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Shop DC Collectibles",
                        url: "#",
                        active: false,
                    },
                ],
                linksDc: [
                    {
                        text: "Terms Of Use",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Privacy Policy (New)",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Add Choices",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Advertising",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Jobs",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Subscriptions",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Talent Workshops",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "CPSC Certificates",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Ratings",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Shop Help",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "Contacts Us",
                        url: "#",
                        active: false,
                    }
                ],
                linksSites: [
                    {
                        text: "DC",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "MAD Magazine",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "DC Kids",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "DC Universe",
                        url: "#",
                        active: false,
                    },
                    {
                        text: "DC Power Visa",
                        url: "#",
                        active: false,
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;
@use '../../assets/styles/partials/mixins' as *;
    .links-footer{
        background-image: url('/img/footer-bg.jpg');
        background-size: cover;
        background-position: center;
        color: $white;
        
        .links-wrap{
            @include dflex('between');
            height: 400px;
            overflow: hidden;
                .links{
                display: flex;
                .link{
                    padding: 1rem 1rem 1rem 0;
                    .title{
                        font-size: 1.5rem;
                        text-transform: uppercase;
                        font-weight: bold;
                        display: inline-block;
                        padding: 0.8rem 0;
                    }
                    li{
                        padding: 0.1rem 0;
                    }
                    a{
                        color: grey;

                        &:hover{
                            color: $white;
                        }
                    }
                }
            }
        }
    }
</style>