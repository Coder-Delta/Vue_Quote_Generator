<script setup>
import { ref } from "vue";
import Quote from "inspirational-quotes";
const quote = Quote.getQuote();
const quoteText = ref(quote.text);
const quoteAuthor = ref(quote.author);
const href = ref("https://www.google.com/search?q=" + quoteAuthor.value.replace(" ", "+"));

</script>

<template>
    <main>
        <section>
            <p>{{ quoteText }}</p>
            <a v-bind:href="href" target="_blank"><span>{{ quoteAuthor }}</span></a>
        </section>
        <div>
            <button>Another! </button>
            <button>Share</button>
        </div>
    </main>
</template>

<style scoped>
/* MAIN CSS */
main {
    background: #CCD6D9;
    max-width: 90%;
    border-radius: 0 15px 0 15px;
    padding: 35px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
}

main section {
    display: flex;
    width: 100%;
    flex-direction: column;
    gap: 10px;
    margin-bottom: 25px;
}

main p ::before {
    content: '"';

}


main p::after {
    content: '"';

}

a {
    text-decoration: none;
}

span {
    align-self: end;
    color: #406473;

}


span::before {
    content: "- "

}

div {
    display: flex;
    gap: 45px;
}

button {
    background: #406473;
    color: white;
    padding: 10px;
    border: 0;
    font-size: 1.2rem;
    border-radius: 0 5px 0 5px;
    font-weight: bold;
    margin-top: 20px;
    cursor: pointer;
    transition: transform 0.2s;
    
}

button:hover {
    transform: scale(1.05);
}
</style>