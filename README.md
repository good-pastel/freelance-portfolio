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
        action="https://script.google.com/YOURID/exec"
        method="POST"
      >
        <input class="inp" name="name" required placeholder="Name" />
        <input
          class="inp"
          type="email"
          name="email"
          required
          placeholder="Email"
        />...
      </form>
```

```js
<script>
const f = document.getElementById("contact-form");
      const s = document.getElementById("form-status");

      f.addEventListener("submit", async (e) => {
        e.preventDefault();

        /* Ambil field */

        const service = document.getElementById("service");

        const project = document.getElementById("project");

        const message = document.getElementById("message");

        /* Gabungkan */

        message.value = `Service : ${service.value}

Project :

${project.value}`;

        s.innerHTML = "📨 Sending your request...";

        try {
          await fetch(
            f.action,

            {
              method: "POST",

              body: new FormData(f),

              mode: "no-cors",
            },
          );

          s.innerHTML = "✅ Thank you! I'll get back to you soon.";

          f.reset();
        } catch {
          s.innerHTML = "Failed to send";
        }
      });
</script>
```

&copy; Good Pastel. 2026

<!-- MARKDOWN LINKS & IMAGES -->

[linkedin-shield]: https://img.icons8.com/arcade/64/linkedin.png
[linkedin-url]: https://linkedin.com/in/deviyool
