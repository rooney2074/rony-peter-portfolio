<template>
    <div class="nav_bar">
        <div class="nav_content">
            <div class="nav_links">
                <h1 style="color: #101010;">Port<span style="font-style: italic; font-weight: bolder;">folio..</span></h1>

                <!-- <div class="links">
                    <ul>
                        <li>Skills</li>
                        <li>Contact</li>
                    </ul>
                </div> -->
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'NavBar',
    methods: {
        showLinks() {
            console.log('hello')
        },
    },
}
</script>

<style scoped>
.nav_bar {
    width: 100%;
    position: fixed;
    padding: 40px 40px;
}

.nav_content {
    display: flex;
    justify-content: space-between;
}

.nav_links {
    display: flex;
    text-align: center;
    padding: 10px;
    border-radius: 10px;
    background: #FFFFFF;
}

.nav_links:hover {
    background: #000;
}

ul {
    padding: 10px !important;
    color: #101010;
    list-style: none;
    display: flex;
    margin: 0;
    padding: 0;
}

.nav_links li {
    margin-right: 20px;
}
</style>
