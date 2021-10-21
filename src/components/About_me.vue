<template>
    <div id="about_me">
        <div class="left clearfix">
            <img src="../assets/personal_pic.jpg" alt="Foto prsonale">
        </div>
        <div class="right">
            <h2>Full name:</h2>
            <p>Paul Denis-Ionut</p>
            <h2>Where are you from?</h2>
            <p>I was born in Romania but i live in Italy now.</p>
            <h2>Passions:</h2>
            <p>I love to play video games, but I was always interested in coding. I created a few games, but soon I discovered that was not as interesting as playing them. That's why I learned how to be a <span>Web Developer</span>, and now I'm here. I also like to create youtube content and try to make people interested in programming, since it's such an amazing world and the world need programmers.</p>
            <h2>Where did you learn to code?</h2>
            <p>I first started at school, with some basic C++. Then at first year of university, again with C++ and some Java. When I gave up university I bought a course in Udemy to learn how to code games on Unity using C#. In the end I found this course named <a href="https://www.boolean.careers/" target="_blank" rel="noopener noreferrer" class="boolean">Boolean Careers</a> that teached me how to be a professional Web-Developer, and they did an amazing job! </p>
            <h2>How would you describe yourself as a worker?</h2>
            <p>I am very dedicated to my job and I do it with passion. More importnat, I always put my 100% in everything I do, even when I don't like what I am doing. I can also put pride aside and tell that I am not skilled enough for the job, because I don't want someone to come to me for a web-page and to go away with a bad product and having to do it all over again. I care about my costumers and I want them to be happy about their page.</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AboutMe'
}
</script>

<style lang="scss" scoped>

    #about_me {
        // height: calc(100vh - 75px);
        width: 100%;
        height: 100vh;
        border-bottom: 2px solid cyan;
    }

    .left {
        float: left;
        margin-top: 100px;
        margin-left: 150px;
    }
    .left img {
        height: calc(100vh - 300px);
        border: 1px solid #ff6500;
        border-radius: 50%;
    }
    .right {
        padding-right: 20px;
        width: 48%;
        float: right;
        // margin-top: 50px;
    }
    .boolean {
        text-decoration: none;
        font-size: 20px;
        color: #0cd977;
    }
    .boolean:hover {
        color: #006cfa;
    }
    .right h2 {
        margin-top: 15px;
        font-size: 40px;
        color: #ff6500;
    }
    .right p {
        font-size: 18px;
    }
</style>