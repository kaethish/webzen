<script>
    let first = '<font color="#FCFF5C">&lt;body&gt; <br> &emsp;&lt;h1&gt; </font><br> &emsp;&ensp;Do you find free Youtube courses <br> &emsp;&ensp;overwhelming? <br> <font color="#FCFF5C">&emsp;&lt;/h1&gt; <br> &emsp;&lt;h2&gt; </font> <br> &emsp;&ensp;I will help you become a pro web dev <br> &emsp;&ensp;in just 30 days <br> <font color="#FCFF5C"> &emsp;&lt;/h2&gt; <br> &emsp;&lt;div&gt; </font> <br> &emsp;&ensp;For $29.99 only <br> <font color="#FCFF5C"> &emsp;&lt;/div&gt; <br> &lt;/body&gt;</font>'
    let second = '<font color="#FCFF5C">&lt;p&gt; </font> <br> &ensp;Although everything is available on <br> the internet for free, it is cluttered <br> and unorganised. Beginners waste so much <br> time learning concepts they do not need. <br> A structured course will save a lot of <br> your precious time and help you achieve <br> your dream of becoming a professional <br> web developer in a short period. <br> <font color="#FCFF5C"> &lt;/p&gt; </font>'
    let third = '<font color="#FCFF5C">&lt;p&gt; </font> <br> &ensp; Do you feel alone in your webdev <br> journey? Get access to my private <br> Discord server, where you can meet <br> fellow members who share the same goals <br> and are ready to help you whenever you <br> are stuck. <br> <font color="#FCFF5C">&lt;b&gt; </font> <br> No more learning concepts that you <br> don’t need. No more tutorial hell. No <br> more being confused about what to do <br> next. <br> <font color="#FCFF5C"> &lt;/b&gt; <br> &lt;/p&gt; </font>'
    let logo = '<font color="#ffffff">web</font>'
    let nxt1 = 'WHY BUY THIS COURSE?'
    let nxt2 = 'COMMUNITY'
    let nxt3 = 'CLICK TO JOIN'

    let state = 1;
    let nxt = 1;
    let dispState = first;
    let dispNxt = nxt1;

    function handleClick () {
        state++;
        nxt++;
        console.log(state);
        if (state === 2) {
        dispState = second;
        dispNxt = nxt2;
        }

        if (state === 3) {
        dispState = third;
        dispNxt = nxt3;
        }
        if (state > 3) {
            state = 1;
            dispState = first;
            dispNxt = nxt1;
        }
    }
    
</script>

<h1 class = "logo"> {@html logo}zen </h1>

<div class = "container">
    <p class = "content"> 
        {@html dispState}
    </p>
</div>

<div class = "next" on:click={handleClick}> {dispNxt} </div>

<style>
    :global(body) {
        background: #067ED5;
        
    }

    .logo {
        position: absolute;
        width: 359px;
        height: 75px;
        left: 30rem;
        top: 13px;

        font-family: 'Intrepid';
        font-style: bold;
        font-size: 70px;
        line-height: 75px;
        text-align: center;
        color: #FCFF5C;
    }

    .container {
        position: absolute;
        width: 58.438rem;
        height: 40.25rem;
        left: 13rem;
        top: 194px;
        background: #171717;
        border-radius: 49px;
        display: grid;
        place-items: center;

    }

    .content {
        position: relative;
        width: 712px;
        height: 553px;
        /* left: 100px;
        top: 50px; */
        top: 50%;
        bottom: 50%;
        transform: translate(0, -55%);
        font-family: 'Consolas';
        font-style: normal;
        font-weight: 400;
        font-size: 31.7202px;
        line-height: 37px;
        color: #FFFFFF;
    }
    .next {
        position: absolute;
        /* width: 290px; */
        /* height: 56px; */
        left: 50%;
        transform: translate(-50%);
        display: grid;
        place-items: center;
        /* align-items: center; */
        top: 55.313rem;
        padding-bottom: 5rem;
        font-family: 'Intrepid';
        font-style: bold;
        font-weight: 600;
        font-size: 2rem;
        cursor: pointer;
        color: #FCFF5C;
    }
</style>