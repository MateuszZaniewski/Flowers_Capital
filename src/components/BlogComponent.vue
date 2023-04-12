<script setup>

</script>

<template>
    <div id="blog" class="blogWrapper">
        <div class="blogSection">
            <h2>Blog</h2> 
            <div class="blogInfos">
                <p>We want to share with you our love and passion for flowers, as well as provide you with helpful tips and inspiration for incorporating blooms into your daily life. Here you will find the articles on flower care, design ideas for special occasions, and the latest floral trends.</p>
                <p>Whether you're an avid gardener, a DIY enthusiast, or just looking for new ways to bring the beauty of nature into your home, our blog has something for everyone. </p>
                <p>Enjoy exploring the world of flowers with us. </p>
                <button>Go to blog posts</button>
            </div>
        </div>
        <div class="imageSection">
            <div class="image">
                <div></div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">

@import '@/assets/_variables.scss';


.blogSection {
    position: relative;
    display: flex;
    max-width: 1400px;
    margin: 0 auto;
    padding-bottom: 84px;

    h2 {
        transform: rotate(180deg);
        white-space: nowrap;
        color: $gold600;
        margin: 0;
        width: fit-content;
        position: absolute;
        z-index: 1;
        top: 0%;
        left: 4%;
        writing-mode: vertical-lr;
        font-size: $mobileH2;
        
      }


    .blogInfos {
        width: 80%;
        margin-right: 16px;
        margin-left: clamp(10px, 20vw, 130px);
        padding-bottom: $spc36;

        h3 {
            font-size: $mobileH3;
            line-height: 34px;
            color: $black900;
            margin: 0;
            padding-bottom: 40px;

        }

        p {
            font-size: $mobileBody;
            line-height: 27px;
            color: $black900;
            margin: 0;
            padding-bottom: 36px;
        }

        button {
            padding: 15px 40px 15px 40px;
            background: $gold600;
            font-size: $mobileBody;
            border-radius: 40px;
            color: $white100;
            border: none;
            line-height: 27.6px;
            margin-top: 20px;
        }

        button:hover {
            background: $gold700;
          }
    }
    
}

@media screen and (min-width: 1024px) {
    .blogWrapper {
        display: flex;
        flex-flow: row nowrap;
        padding-bottom: 72px;
        max-width: 2000px;
        margin: 0 auto;

        .blogSection {
            position: relative;
            display: flex;
            max-width: 1400px;
            margin: 0 auto;

            h2 {
                font-size: $desktopH4;
                left: 6%;
            }


            .blogInfos {
                margin-left: clamp(10px, 20vw, 130px);
                width: 70%;

                p {
                    font-size: $desktopH6;
                }

                button {
                    font-size: 25px;
                }
            }
            
        }

        .imageSection {
            width: 50%;
            


            .image {
                margin-right: 10vw;

                div {
                    width: 25.833vw;
                    height: 35.625vw;
                    background-image: url('../assets/blogImage.png');
                    background-size: cover;
                    background-repeat: no-repeat;
                    margin: 0 auto;
                    position: relative;

                    &:before {
                        content: '';
                        position: absolute;
                        z-index: 1;
                        transform: translateY(-35%);
                        top: 25%;
                        left: 103%;
                        width: 5%;
                        height: 105%;
                        border-right: 2px solid $gold600;
                    }
            
                    &:after{
                        content: '';
                        position: absolute;
                        z-index: 1;
                        transform: translateY(-50%);
                        top: -7%;
                        left: -10%;
                        width: 130%;
                        height: 5%;
                        border-bottom: 2px solid $gold600;
                  
                      }
                }
            }
        }

    }
}

</style>