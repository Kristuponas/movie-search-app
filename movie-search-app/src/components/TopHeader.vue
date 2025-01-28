<template>
    <nav>
        <a href="/" class="logo">OMDb</a>
        <div class="searchtype">
            <h4>All</h4>
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
    props: {
        msg: String
    }
}
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
    height: 3.5rem;
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
    padding: 0.5rem 1rem;
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
    padding: 0.5rem 1rem;
    margin: 0;
    font-weight: bold;
    border-radius: 5px 0 0 5px;
    display: flex;
    align-items: center;
}
.searchtype h4 {
    margin: 0;
    padding: 0;
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
    width: 100%; /* Make the input take the full width of the container */
    border: none; /* Remove the default border */
    outline: none; /* Remove the default outline on focus */
    font-size: 1rem; /* Ensure readable font size */
    background: transparent; /* Match background with the parent */
    color: var(--emerald-glow); /* Use your theme color for text */
    margin: 0;
    padding: 0;

}
.searchbox input::placeholder {
    color: var(--misty-meadow); /* Style the placeholder text */
}

</style>