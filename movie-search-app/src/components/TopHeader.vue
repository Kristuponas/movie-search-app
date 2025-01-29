<template>
    <nav>
        <a href="/" class="logo">OMDb</a>

        <div class="searchtype" @click="toggleDropdown">
            <h4>{{ selectedType }}</h4>
            <div v-if="dropdownVisible" class="search-options">
                <div v-for="type in searchTypes" :key="type" @click="selectType(type)">
                    {{ type }}
                </div>
            </div>
        </div>

        <div class="searchbox">
            <input type="text" placeholder="Search OMDb..."/>
        </div>

        <div class="searchbutton">
            <button>

            </button>
        </div>
        
    </nav>
</template>

<script>
export default {
    name: 'TopHeader',
    data() {
        return {
            selectedType: "All",
            dropdownVisible: false,
            searchTypes: ["All", "Titles", "Actors", "Writer"]
        };
    },
    methods: {
        toggleDropdown() {
            this.dropdownVisible = !this.dropdownVisible;
        },
        selectType(type) {
            this.selectedType = type;
            this.dropdownVisible = false;
        }
    }
};
</script>

<style>
:root {
    --emerald-glow: #BBDB9B;
    --misty-meadow: #ABC4A1;
    --silver-screen: #9DB4AB;
    --foggy-forest: #8D9D90;
    --foggy-forest2: #9cac9f;
    --vintage-reel: #878E76;
}
html, body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}
nav {
    width: 100%;
    height: 3.53rem;
    color: var(--emerald-glow);
    background-color: var(--vintage-reel);
    display: flex;
    align-items: center;
    padding: 0 1rem;
}
.logo {
    text-decoration: none;
    color: var(--emerald-glow);
    background-color: var(--foggy-forest);
    padding: 0.53rem 1rem;
    margin: 0 2rem 0 8rem;
    font-weight: bold;
    transition: background-color 0.3s ease;
    border-radius: 5px;
}
.logo:hover {
    background-color: var(--foggy-forest2);
}
.searchtype {
    color: var(--emerald-glow);
    background-color: var(--foggy-forest);
    padding: 0.53rem 1rem;
    margin: 0;
    font-weight: bold;
    border-radius: 5px 0 0 5px;
    display: flex;
    align-items: center;
    position: relative;
    cursor: pointer;
    min-width: 60px;
}
.searchtype h4 {
    margin: 0;
    padding: 0;
}
.searchtype button {
    margin: 0 0 0 1rem;

}
.search-options {
    position: absolute;
    top: 100%;
    left: 0;
    background: var(--foggy-forest);
    color: var(--emerald-glow);
    width: 100px;
    max-height: 120px;
    overflow-y: auto;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.2);
    scrollbar-width: none;
    -ms-overflow-style: none;
}
.search-options::-webkit-scrollbar {
    display: none;
}
.search-options div {
    padding: 8px;
    cursor: pointer;
    text-align: left;
    padding-left: 10px;
}
.search-options div:hover {
    background: var(--foggy-forest2);
}
.searchbox {
    background-color: var(--foggy-forest);
    padding: 0.5rem 1rem;
    margin: 0;
    display: flex;
    align-items: center;
    flex-grow: 1;
}
.searchbox input {
    width: 100%;
    height: 100%;
    border: none;
    outline: none;
    font-size: 1rem;
    background: transparent;
    color: var(--emerald-glow);
    margin: 0;
    padding: 0;
    line-height: 1;
}
.searchbox input::placeholder {
    color: var(--misty-meadow);
}
</style>