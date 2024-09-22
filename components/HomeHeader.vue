<template>
    <div class="home_header">
        <div class="name_style"></div>
        <h1 class="first_name" v-html="formattedName"></h1>
    </div>
</template>

<script>
import gsap from 'gsap';

export default {
    name: 'HomeHeader',
    data() {
        return {
            originalName: 'Rony Peter',
            formattedName: ''
        };
    },
    mounted() {
        this.splitAndAnimateName();
    },
    methods: {
        splitAndAnimateName() {
            const letters = this.originalName.split('').map(char => `<span class="letter">${char}</span>`).join('');
            this.formattedName = letters;

            this.$nextTick(() => {
                gsap.from('.letter', {
                    duration: 1,
                    y: 50,
                    opacity: 0,
                    stagger: 0.1,
                    ease: 'power4.out'
                });
            });
        },
    }
}
</script>

<style scoped>
.home_header {
    position: relative;
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.name_style {
    position: absolute;
    width: 98%;
    height: 95%;
    border: 1px solid #ccc;
    border-radius: 10px;
}

.name_style::after {
    position: absolute;
    content: "9847646190 ||| /// |||";
    background: #000;
    bottom: -10px;
    left: 20px;
}

.first_name {
    font-size: calc(4vw + 40px);
    display: inline-block;
}
</style>
