# Devi Yolanda - Freelance Portfolio

> [[Freelance Portfolio](https://good-pastel.github.io/freelance-portfolio/)]

[![LinkedIn][linkedin-shield]][linkedin-url]

<br />
<div align="center">
  <a href="https://github.com/good-pastel/good-pastel.github.io">
    <img src="https://raw.githubusercontent.com/good-pastel/good-pastel.github.io/refs/heads/main/img/logo_trans.png" alt="Header">
  </a>

  <h3 align="center">Welcome to Good Pastel</h3>

  <p align="center">
   <blockquote><i>"Colors fade, but pastels hold their magic forever. Let the pastels be a reflection of the beauty within your soul."</i></blockquote>
   <br />
    <a href="https://github.com/good-pastel?tab=repositories"><strong>Explore the other Repo»</strong></a>
  </p>
</div>

---

## Description

Freelance Portfolio.
<br/>
<br/>
The form on this portfolio website is connected to <b><a href="https://docs.google.com/spreadsheets/">Google Sheet Apps Script</a></b> to automate the data submission process.
<br/>

```html
<form
  id="contact-form"
  action="https://script.google.com/macros/s/YOUR_ID/exec"
  method="POST"
>
  <input type="text" name="name" placeholder="Nama Anda" required />
  <input type="email" name="email" placeholder="Email Anda" required />
  <textarea
    name="message"
    rows="5"
    placeholder="Pesan Anda"
    required
  ></textarea>
  <button type="submit">Kirim Pesan</button>
</form>
```

```js
<script>
const form = document.getElementById('contact-form');
const status = document.getElementById('form-status');

form.addEventListener('submit', async (e) => {
  e.preventDefault();
  status.textContent = "Mengirim...";

  try {
    await fetch(form.action, {
      method: 'POST',
      body: new FormData(form),
      mode: "no-cors"
    });

    status.textContent = "Pesan berhasil terkirim!";
    form.reset();
  } catch (error) {
    status.textContent = "Terjadi kesalahan. Coba lagi.";
    console.error(error);
  }
});
</script>
```

&copy; Good Pastel. 2025

<!-- MARKDOWN LINKS & IMAGES -->

[linkedin-shield]: https://img.icons8.com/arcade/64/linkedin.png
[linkedin-url]: https://linkedin.com/in/deviyool
