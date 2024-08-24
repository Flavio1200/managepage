<script setup>
 const emit = defineEmits(['verify'])
 function verify(text){
    if(text.target.value == null){
        console.log('no email')
    }
    emit('verify')
 }
// import ref from 'vue'
// const val = ref(email.target.value)
</script>

<template>
    <footer>
        <div class="footer-part">
            <img src="/images/logo.svg" alt="logo">
            <ul class="social-list">
                <li><a href="#" class="sl"><img src="/images/icon-facebook.svg" alt="social"></a></li>
                <li><a href="#" class="sl"><img src="/images/icon-youtube.svg" alt="social"></a></li>
                <li><a href="#" class="sl"><img src="/images/icon-twitter.svg" alt="social"></a></li>
                <li><a href="#" class="sl"><img src="/images/icon-pinterest.svg" alt="social"></a></li>
                <li><a href="#" class="sl"><img src="/images/icon-instagram.svg" alt="social"></a></li>
            </ul>
        </div>
        <div class="footer-part">
            <a href="#" class="info-foot">Home</a>
            <a href="#" class="info-foot">Pricing</a>
            <a href="#" class="info-foot">Products</a>
            <a href="#" class="info-foot">About Us</a>
        </div>
        <div class="footer-part">
            <a href="#" class="info-foot">Careers</a>
            <a href="#" class="info-foot">Community</a>
            <a href="#" class="info-foot">Privacy Policy</a>
        </div>
        <div class="footer-part">
            <div class="form">
                <input v-model="email" type="email" name="go" id="verify" placeholder="Updates in your inbox...">
                <!-- <span v-if="email"></span> -->
                <button class="go-btn" @click="verify">Go</button>
            </div>
            <p class="copy">Copyright 2020. All rights reserved</p>
        </div>
    </footer>
</template>

<style>
footer{
    padding: 2rem 5rem;
    background-color: var(--ultra-dark-blue);
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
}
.footer-part{
    flex: 1 1;
}
.footer-part a{
    color: #fff;
}

.social-list{
    margin-top: 2rem;
}
.social-list li{
    display: inline-block;
    margin-left: .5rem;
}
.info-foot{
    display: block;
    margin-block: 1rem;
}
.form{
    display: flex;
}
.go-btn{
    background-color: var(--red);
    border-radius: 20px;
    padding: .75rem 1rem;
    margin-left: .5rem;
    color: #fff;
    border: none;
    outline: none;
}
#verify{
    border-radius: 20px;
    padding: .75rem 1rem;
    border: none;
    outline: none;
}
.copy{
    margin-top: 2.5rem;
    text-align: center;
}
.info-foot:hover,.sl>img:hover{
    color: var(--red);
}
@media screen and (max-width: 375px){
    footer{
        flex-direction: column;
        text-align: center;
        padding: 1rem;
    }
    .social-list li:not(:first-child){
        margin-left: 1.5rem;
    }
}
</style>