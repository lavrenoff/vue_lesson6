<template>
    <main class="mainproject">
        <div class="mainblog__photo">
                <img src="@/assets/img/photoproject.png" alt="photo">
                <div class="mainblog__txt">
                    <h1 class="mainblog__h1">Our Project</h1>

                    <p>Home / Project</p>
                </div>
            </div>

        <div class="mainproject__categorybuttons center">
            <button class="mainproject__btns">
                <button :class="['mainproject_button',button.id===CurrentCategory ? 'mainproject_button_active' : false]" v-for="button in CategoryButtons" :key="button.id"
                    @click="CurrentCategory = button.id">
                    {{ button.title }}
                </button>
            </button>
        </div>
        <div class="mainproject__items center">
            <div v-for="item in ChangeCategory" :key="item.id" class="mainproject__item">
                <img class="mainproject__img" :src="item.src" :alt="item.alt">
                <div class="mainproject__content">
                    <div class="mainproject__box">
                        <p class="mainproject__title">{{ item.p1 }}</p>
                        <p class="mainproject__subtitle">{{ item.p2 }}</p>
                    </div>
                    <a href="#" class="mainproject__a">
                        <svg width="9" height="16" viewBox="0 0 9 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M1.27101 14.9525L7.21387 8.26683L1.27101 1.58112" stroke="#292F36" stroke-width="2"
                                stroke-linecap="round" stroke-linejoin="round" />
                        </svg>
                    </a>
                </div>
            </div>
        </div>
        <div class="mainblog__nav">
                <button class="btn btn1">01</button>
                <button class="btn btn2">02</button>
                <button class="btn btn3">03</button>
                <button class="btn btn4">></button>
            </div>
    </main>
</template>

<script>
export default {
    name: 'ProjectComponent',
    components: {
    },

    data() {
        return {
            CategoryList: [
                { id: '1', tag: 'kitchen', src: require('@/assets/img/kitchen1.png'), alt: 'kitchen1', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '2', tag: 'kitchen', src: require('@/assets/img/kitchen2.png'), alt: 'kitchen2', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '3', tag: 'kitchen', src: require('@/assets/img/kitchen3.png'), alt: 'kitchen3', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '4', tag: 'kitchen', src: require('@/assets/img/kitchen4.png'), alt: 'kitchen4', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '5', tag: 'kitchen', src: require('@/assets/img/kitchen5.png'), alt: 'kitchen5', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '6', tag: 'kitchen', src: require('@/assets/img/kitchen6.png'), alt: 'kitchen6', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                
                


                { id: '9', tag: 'bedroom', src: require('@/assets/img/kitchen2.png'), alt: 'kitchen1', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '10', tag: 'bedroom', src: require('@/assets/img/kitchen1.png'), alt: 'kitchen2', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '11', tag: 'bedroom', src: require('@/assets/img/kitchen3.png'), alt: 'kitchen3', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '12', tag: 'bedroom', src: require('@/assets/img/kitchen4.png'), alt: 'kitchen4', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '13', tag: 'bedroom', src: require('@/assets/img/kitchen5.png'), alt: 'kitchen5', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },


                { id: '14', tag: 'bathroom', src: require('@/assets/img/kitchen6.png'), alt: 'kitchen6', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '15', tag: 'bathroom', src: require('@/assets/img/kitchen7.png'), alt: 'kitchen7', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '16', tag: 'bathroom', src: require('@/assets/img/kitchen8.png'), alt: 'kitchen8', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '17', tag: 'bathroom', src: require('@/assets/img/kitchen1.png'), alt: 'kitchen1', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '18', tag: 'bathroom', src: require('@/assets/img/kitchen2.png'), alt: 'kitchen2', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '19', tag: 'bathroom', src: require('@/assets/img/kitchen3.png'), alt: 'kitchen3', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                
                
                { id: '22', tag: 'livingarea', src: require('@/assets/img/kitchen6.png'), alt: 'kitchen6', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '23', tag: 'livingarea', src: require('@/assets/img/kitchen7.png'), alt: 'kitchen7', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '24', tag: 'livingarea', src: require('@/assets/img/kitchen8.png'), alt: 'kitchen8', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '25', tag: 'livingarea', src: require('@/assets/img/kitchen8.png'), alt: 'kitchen8', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '26', tag: 'livingarea', src: require('@/assets/img/kitchen8.png'), alt: 'kitchen8', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' },
                { id: '27', tag: 'livingarea', src: require('@/assets/img/kitchen8.png'), alt: 'kitchen8', p1: 'Modern Kitchen', p2: 'Decor / Artchitecture' }, ],    
            CategoryButtons:
                [
                    { id: 'bathroom', title: 'Bathroom' },
                    { id: 'bedroom', title: 'Bed room' },
                    { id: 'kitchen', title: 'Kitchan' },
                    { id: 'livingarea', title: 'Living Area' }
                ],
            CurrentCategory: 'bathroom',
        }

    },

    computed: {
        ChangeCategory() {
            return this.CategoryList.filter((flt) => flt.tag === this.CurrentCategory)
        }

    },


    methods: {

    },
};
</script>

<style lang="scss" scoped></style>