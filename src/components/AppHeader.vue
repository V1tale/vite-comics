<script>
export default {
    name: "AppHeader",
    data() {
        return {
            menu: [
                {
                name: "Characters",
                link: "Alink",
            },
                {
                name: "Comics",
                link: "Alink",
            },               
                {
                name: "Movies",
                link: "Alink",
            },               
                {
                name: "Tv",
                link: "Alink",
            },               
                {
                name: "Games",
                link: "Alink",
            },               
                {
                name: "Collectibles",
                link: "Alink",
            },               
                {
                name: "Videos",
                link: "Alink",
            },               
                {
                name: "Fans",
                link: "Alink",
            },               
                {
                name: "News",
                link: "Alink",
            },               
                {
                name: "Shop",
                link: "Alink",
            },
        ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="top">
                <div class="logo">
                    <img src="/img/dc-logo.png" alt="">
                </div>
                <div class="list">
                    <ul>
                        <li v-for="(link) in menu"><a :href="link.link">{{link.name}}</a></li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="bottom">
            <div class="container">
                <h2>Content goes here</h2>
            </div>
        </div>
        
    </header>
</template>

<style lang="scss">
header {
    width: 100%;
    margin:auto;
}
.top {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding:.5rem;
    ul {
        display: flex;
        justify-content: space-around;
        align-items: center;
        li {
            margin: 10px;
            
            a {
                text-decoration: none;
                color: black;
                font-size: .8rem;
                position: relative;
                line-height: 70px;
                &:hover {
                    color: #0f7eed;
                }
                &:hover::after {
                    content:"";
                    position: absolute;
                    bottom:-40px;
                    left:0;
                    width:100%;
                    height:4px;
                    background-color: #0f7eed;
                }
            }
        }
    }
    img {
        width:50px;
    }
}
.bottom {
    background-color: black;
    color: white;
    padding: 2rem;
}
</style>