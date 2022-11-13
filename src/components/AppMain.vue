<script>
export default {
    name: "AppMain",
    data() {
        return {
            menu: [
                {
                    img: "img/buy-comics-digital-comics.png",
                    name: "DIGITAL COMICS",
                },
                {
                    img: "img/buy-comics-merchandise.png",
                    name: "DC MERCHANDISE",
                },
                {
                    img: "img/buy-comics-subscriptions.png",
                    name: "SUBSCRIPTION",
                },
                {
                    img: "img/buy-comics-shop-locator.png",
                    name: "COMIC SHOP LOCATOR",
                },
                {
                    img: "img/buy-dc-power-visa.svg",
                    name: "DC POWER VISA",
                },
            ]
        }
    }
}
</script>
<template>
    <div class="main">
        <div class="container">
            <ul>
                <li v-for="(item) in menu"><img :src="item.img" alt=""> <span>{{item.name}}</span></li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss">
.main {
    background-color: #0f7eed;
}
.main ul {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 2rem 0;
    font-size: .8rem;
    li {
        list-style-type: none;
        color: white;
        img {
            vertical-align: middle;
            width:30px;
            margin-right:10px;
        }
    }
}
</style>