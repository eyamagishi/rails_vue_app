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