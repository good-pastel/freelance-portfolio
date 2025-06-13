# Devi Yolanda - Freelance Portfolio

> [[Freelance Portfolio](https://good-pastel.github.io/freelance-portfolio/)]

[![LinkedIn][linkedin-shield]][linkedin-url]

<br />
<div align="center">
  <a href="https://github.com/good-pastel/good-pastel.github.io">
    <img src="https://raw.githubusercontent.com/good-pastel/logos/main/20240210_203339_0000.png" alt="Header">
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
The form on this portfolio website is connected to <b><a href="https://zapier.com/">Zapier</a></b> to automate the data submission process.
<br/>
```html
<form id="contact-form" action="https://hooks.zapier.com/hooks/catch/23307115/uymv6gi/" method="POST">
      <input type="text" name="name" placeholder="Nama Anda" required />
      <input type="email" name="email" placeholder="Email Anda" required />
      <textarea name="message" rows="5" placeholder="Pesan Anda" required></textarea>
      <button type="submit">Kirim Pesan</button>
    </form>
```

```js
<script>
    const form = document.getElementById('contact-form');
    const status = document.getElementById('form-status');

    form.addEventListener('submit', async (e) => {
      e.preventDefault();
      const data = new FormData(form);
      const action = form.action;
      const response = await fetch(action, {
        method: 'POST',
        body: data,
        headers: { 'Accept': 'application/json' }
      });

      if (response.ok) {
        status.innerHTML = '<div class="alert alert-success">Pesan Anda berhasil dikirim!</div>';
        form.reset();
      } else {
        status.innerHTML = '<div class="alert alert-error">Terjadi kesalahan. Silakan coba lagi.</div>';
      }
    });
  </script>
```

&copy; Good Pastel. 2025

<!-- MARKDOWN LINKS & IMAGES -->

[linkedin-shield]: https://raw.githubusercontent.com/good-pastel/good-pastel.github.io/0081ddd54c76b5249abd15a39df972e47ad32547/img/icons8-linkedin.svg
[linkedin-url]: https://linkedin.com/in/deviyool
