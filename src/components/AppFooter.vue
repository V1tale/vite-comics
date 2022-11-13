<script>
export default {
    name: "AppFooter",
    data() {
        return {
            map: [
                {
                    name: "DC COMICS",
                    items: ["Characters", "Movies", "Comics", "Tv", "Games", "Videos", "News"]
                },
                {
                    name: "SHOP",
                    items: ["Shop DC", "Shop DC Collectibles"]
                },
                {
                    name: "DC",
                    items: ["Terms of use", "Privacy Policy(New)", "AD Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact us"]
                },
                {
                    name: "Sites",
                    items: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"]
                }
            ],
            social: ["footer-facebook.png", "footer-periscope.png", "footer-pinterest.png", "footer-youtube.png"]
        }
    }
}
</script>

<template>
    <footer>
        <div class="footerbg-top">
            <div class="container">
                <div class="footer-top">
                    <div class="list-contents">                   
                        <div v-for="(list) in map" class="list">
                            <h2>{{list.name}}</h2>
                            <ul>
                                <li v-for="(items) in list.items"><a href="">{{items}}</a></li>
                            </ul>
                        </div>
                    </div>
                    <div class="footer-logo">
                        <img src="img/dc-logo-bg.png" alt="">
                    </div>

                </div>
            </div>
            <div class="bg-footer-bottom">
                    <div class="container">

                    <div class="footer-bottom">
                        <div class="button">
                            <button>Sign-Up Now</button>
                        </div>
                        <div class="social">
                            <h3>Follow Us</h3>
                            <img v-for="(social) in social" :src="`img/${social}`" alt="">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>    
</template>

<style lang="scss">
    .footerbg-top {
        background-image: url("img/footer-bg.jpg");
        object-fit: contain;
        h2 {
            color: white;
            font-size: 1rem;
        }
        li {
            color:gray;
            font-size: .8rem;
        }
    }
    .list-contents {
        height: 270px;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        padding: 2rem 0;
        a {
            color:inherit
        }
    }
    .footer-top {
        display: flex;
        justify-content: space-between;
        height: 250px;
        align-items: center;
        overflow: hidden;
        h2 {
            margin: .5rem 0;
        }
        li {
            margin-right: 20px;
        }
    }
    .footer-logo {
        img {
            width:300px;
            opacity: 100%;

        }
    }
    .footer-bottom {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1rem 0;
        button {
            background-color: rgba($color: #000000, $alpha: 0.0);
            border: 2px solid #0f7eed;
            color: white;
            padding: 5px 10px;
            cursor:pointer;
        }
    }
    .bg-footer-bottom {
        background-color: #303030;
    }
    .social {
        font-size: 1rem;
        display: flex;
        font-size: .8rem;
        align-items: center;
        color:#0f7eed;
        img {
            width: 25px;
        }
        * {
            margin:5px;
        }
    }

</style>