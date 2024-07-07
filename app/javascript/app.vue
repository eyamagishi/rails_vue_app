<template>
    <div id="app">
        <header>
            <h1>会社名</h1>
            <nav>
                <ul>
                    <li><a href="#home">ホーム</a></li>
                    <li><a href="#about">会社概要</a></li>
                    <li><a href="#services">サービス</a></li>
                    <li><a href="#contact">お問い合わせ</a></li>
                </ul>
            </nav>
        </header>

        <section id="home">
            <h2>ホーム</h2>
            <p>会社の紹介テキストをここに入れます。</p>
        </section>

        <section id="about">
            <h2>会社概要</h2>
            <p>会社の詳細情報をここに入れます。</p>
        </section>

        <section id="services">
            <h2>サービス</h2>
            <p>提供するサービスの説明をここに入れます。</p>
        </section>

        <section id="contact">
            <h2>お問い合わせ</h2>
            <form @submit.prevent="submitForm">
                <label for="name">名前:</label>
                <input type="text" id="name" v-model="name" required>
                <label for="email">メールアドレス:</label>
                <input type="email" id="email" v-model="email" required>
                <label for="message">メッセージ:</label>
                <textarea id="message" v-model="message" required></textarea>
                <button type="submit">送信</button>
            </form>
        </section>

        <footer>
            <p>&copy; 2024 会社名. All rights reserved.</p>
        </footer>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const name = ref('')
const email = ref('')
const message = ref('')

const submitForm = () => {
    alert(`名前: ${name.value}\nメールアドレス: ${email.value}\nメッセージ: ${message.value}`)
    name.value = ''
    email.value = ''
    message.value = ''
}
</script>
  
<style>
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
}

header {
    background: #333;
    color: #fff;
    padding: 1rem 0;
    text-align: center;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 1rem;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

section {
    padding: 2rem;
    text-align: center;
}

form {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    max-width: 600px;
    margin: 0 auto;
}

input,
textarea {
    padding: 0.5rem;
    width: 100%;
    box-sizing: border-box;
}

button {
    padding: 0.5rem;
    background: #333;
    color: #fff;
    border: none;
    cursor: pointer;
}

button:hover {
    background: #555;
}

footer {
    background: #333;
    color: #fff;
    text-align: center;
    padding: 1rem 0;
    position: fixed;
    bottom: 0;
    width: 100%;
}
</style>