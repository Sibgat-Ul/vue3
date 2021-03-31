<template>
    <div class="libmain">
        <Nav 
        :bg="style.bg"
        />
        <div class="body">
            
            <div class="secO">
                <div class="book" v-for="(book, index) in books" :key="index">

                    <Cards>
                        <template v-slot:bookimg>
                            <div class="title" v-if="book.cover_edition_key == null || book.cover_id == null">
                                {{ book.title }}
                            </div>
                            <img v-if=" book.cover_id != null"
                             :src="`http://covers.openlibrary.org/b/id/${book.cover_id}-M.jpg`" alt = "no image">
                        </template>
                    </Cards>
    
                </div>
            </div>
            
        </div>
    </div>
</template>

<script>
import Nav from '@/components/Navbar.vue'
import Cards from '@/components/Card.vue'
import { ref, reactive, computed, onMounted } from 'vue';

export default {
    components: {
        Nav,
        Cards
    },
    setup () {
        const login = false;
        let count = ref(0);

        let booksarr = reactive([]);

        let books = computed (() => {
            return booksarr[0]
        })

        const style = {
            bg : "0d001b",
            color : "42b9ac",
        }

        const incre = () => {
            count.value++
        }

        const fetcher = async () => {
            try {
                const res = await fetch (
                    "https://openlibrary.org/read.json"
                );
                let data = await res.json();
                booksarr.push(data.works);
                console.log(booksarr[0])
            } catch (err) {
                console.log (err)
            }
        }

    onMounted(fetcher())

    return {
      login,
      style,
      books,
      count,
      incre
    }
  },

}
</script>

<style scoped>
.book {
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.secO {
    display: grid;
    gap: 2rem;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
    margin: 30px
}

img {
    max-height: 250px;
    min-height: 250px;
    width: auto;
}

.libmain {
    background-color: #20063B;
}


@media screen and (max-width: 1650px) {
    .secO {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr;
    }

    #nav {
        max-width: 1650px
    }
}

@media screen and (max-width: 1440px) {
    .secO {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
    }

    #nav {
        max-width: 1650px
    }
}


@media screen and (max-width: 880px) {
    .secO {
        display: grid;
        grid-template-columns: 1fr 1fr;
    }
    #nav {
        max-width: 820px
    }
}

@media screen and (max-width: 640px) {
    .secO {
        display: grid;
        grid-template-columns: 1fr;
    }
}

button {
    cursor: pointer;
}
</style>