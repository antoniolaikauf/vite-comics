<script>

import card from './ComponentCard.vue'

export default {
    name: " ComMain",

    components: {
        card
    },

    data() {
        return {
            comics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ]
        }
    },


}
</script>

<template>
    <main>
        <section id="section-content">

            <span class="bg-img">
                <!-- immahine sfondo  -->
            </span>

            <!-- contenitore  -->
            <div>

                <a href="" class="current-series">
                    CURRENT SERIES
                </a>

                <div id="contenitore">
                    <card :cards="comics">
                        <!-- <card/> -->
                    </card>
                </div>

                <span>
                    <a href="" class="button-add">
                    LOAD MORE
                </a>
                </span>
            </div>
        </section>
        <section id="section-utility">
            <div>
                <ul><!--list acon dentro utility-->
                    <li>
                        <a href="#"><img src="../assets/img/buy-comics-digital-comics.png" alt="#"></a>
                        <span>DIGITAL COMICS</span>
                    </li>
                    <li>
                        <a href="#"><img src="../assets/img/buy-comics-merchandise.png" alt="#"></a>
                        <span>DC MERCHANDISE</span>
                    </li>
                    <li>
                        <a href="#"><img src="../assets/img/buy-comics-subscriptions.png" alt="#"></a>
                        <span>SUBSCRIPTION</span>
                    </li>
                    <li>
                        <a href="#"><img src="../assets/img/buy-comics-shop-locator.png" alt="#"></a>
                        <span>COMIC SHOP LOCATOR</span>
                    </li>
                    <li>
                        <a href="#"><img src="../assets/img/buy-dc-power-visa.svg" alt="#"></a>
                        <span>DC POWER VISA</span>
                    </li>
                </ul>
            </div>
        </section>
    </main>
</template>

<style scoped lang="scss">
@use '../style/general.scss' as *;
@use '../style/partials/variable' as *;

// sezione dove c'è il contenuto 
#section-content {
    background-color: black;
    color: white;
    padding-bottom: 40px;

    .bg-img {
        background-image: url(../assets/img/jumbotron.jpg);
        width: 100%;
        height: 200px;
        display: inline-block;
        background-size: cover;
    }

    div {
        width: $width_blocchi ;
        margin: $margin_blocchi;

        #contenitore {
            display: $display_flex ;
            flex-wrap: wrap;
            margin-top: 15px;
        }

        .button-add,
        .current-series {
            padding: 10px;
            background-color: $color-bg;
            color:$color_text ;
        }

        .current-series {
            position: relative;
            top: -10px;
        }

        span{
            display: block;
            text-align: center;
            margin-top: 10px;
        }
    }
}

// sezione condentro l'utility 
#section-utility {

    background-color: $color-bg;
    padding: 30px 0;


    div {
        width: $width_blocchi ;
        margin: $margin_blocchi;
        text-align: center;

        // caratteristiche di ul e tag al suo interno 
        ul {
            display: $display_flex;
            justify-content: center;

            li {
                display: $display_flex;
                align-items: $specific_align ;
                margin: 0 5px;
                color: $color_text;

                img {
                    width: 50px;
                    margin-right: 5px;
                }
            }
        }
    }
}
</style>