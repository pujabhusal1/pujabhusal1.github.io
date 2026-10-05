---
layout: default
title: Puja Bhusal | Portfolio
---

<!-- Navigation -->
<header class="site-header">
  <nav class="navbar navbar-expand-lg">
    <div class="container">

      <a href="{{ '/' | relative_url }}" class="navbar-brand logo">
        Puja<span>.</span>
      </a>

      <!-- Mobile three-line menu -->
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#mainNavigation"
        aria-controls="mainNavigation"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="mainNavigation">
        <div class="navbar-nav ms-auto nav-links">
          <a class="nav-link" href="#about">About</a>
          <a class="nav-link" href="#projects">Projects</a>
          <a class="nav-link" href="#education">Education</a>
          <a class="nav-link" href="#skills">Skills</a>
          <a class="nav-link" href="#traineeship">Traineeship</a>
          <a class="nav-link" href="#contact">Contact</a>
        </div>
      </div>

    </div>
  </nav>
</header>


<!-- Hero Section -->
<section class="hero" id="about">
  <div class="container">
    <div class="hero-content">

      <div class="hero-text">
        <p class="welcome">WELCOME TO MY PORTFOLIO</p>

        <h1>
          Hi, I'm <span>Puja Bhusal</span>
        </h1>

        <h2>BCA Graduate & Aspiring IT Student</h2>

        <p>
          I am from Nepal and have completed my Bachelor's degree in
          Computer Applications (BCA). I am currently learning Python
          programming and continuously improving my technical skills.
        </p>

        <p>
          I am interested in technology, Quality Assurance, programming,
          and continuous learning. My goal is to build a successful career
          in the IT field through practical experience and real-world projects.
        </p>

        <div class="hero-buttons">
          <a href="#projects" class="btn primary-btn">
            View My Projects
          </a>

          <a href="#contact" class="btn secondary-btn">
            Contact Me
          </a>
        </div>
      </div>

      <div class="hero-image">
        <div class="image-circle">
          <img
            src="{{ '/assets/images/photo_of_puja.jpg' | relative_url }}"
            alt="Portrait of Puja Bhusal"
          />
        </div>
      </div>

    </div>
  </div>
</section>


<!-- About Section -->
<section class="section about-section">
  <div class="container">

    <div class="section-heading">
      <p class="section-label">ABOUT ME</p>
      <h2>Turning Knowledge Into Practice</h2>
    </div>

    <div class="about-content">

      <div class="about-card">
        <div class="icon">🎓</div>
        <h3>BCA Graduate</h3>
        <p>
          I have completed my Bachelor's degree in Computer Applications
          and developed a foundation in computer science and information
          technology.
        </p>
      </div>

      <div class="about-card">
        <div class="icon">💻</div>
        <h3>Learning Python</h3>
        <p>
          I am currently strengthening my programming skills with Python
          through practice, exercises, and practical projects.
        </p>
      </div>

      <div class="about-card">
        <div class="icon">🎨</div>
        <h3>UI/UX Interest</h3>
        <p>
          I am interested in creating simple, user-friendly and visually
          appealing digital experiences.
        </p>
      </div>

    </div>
  </div>
</section>


<!-- Projects Section -->
<section class="section projects-section" id="projects">
  <div class="container">

    <div class="section-heading">
      <p class="section-label">MY WORK</p>
      <h2>Projects</h2>
      <p>
        Here are some of the projects and practical work I have worked on.
      </p>
    </div>

    <div class="card-grid">

      {% for project in site.data.projects %}
      <article class="portfolio-card">

        <div class="card-number">
          {{ forloop.index | prepend: '0' }}
        </div>

        <div class="card-content">
          <h3>{{ project.name }}</h3>

          <p>
            {{ project.description }}
          </p>

          {% if project.url %}
          <a
            href="{{ project.url }}"
            target="_blank"
            rel="noopener"
            class="card-link"
          >
            View Project →
          </a>
          {% endif %}
        </div>

      </article>
      {% endfor %}

    </div>
  </div>
</section>


<!-- Education Section -->
<section class="section education-section" id="education">
  <div class="container">

    <div class="section-heading">
      <p class="section-label">MY JOURNEY</p>
      <h2>Education</h2>
    </div>

    <div class="timeline">

      {% for education_info in site.data.education %}
      <article class="timeline-item">

        <div class="timeline-dot"></div>

        <div class="timeline-content">

          <span class="timeline-number">
            0{{ forloop.index }}
          </span>

          <h3>{{ education_info.name }}</h3>

          <p>
            {{ education_info.description }}
          </p>

          {% if education_info.url %}
          <a
            href="{{ education_info.url }}"
            target="_blank"
            rel="noopener"
            class="card-link"
          >
            View Details →
          </a>
          {% endif %}

        </div>
      </article>
      {% endfor %}

    </div>
  </div>
</section>


<!-- Skills Section -->
<section class="section skills-section" id="skills">
  <div class="container">

    <div class="section-heading">
      <p class="section-label">WHAT I KNOW</p>
      <h2>Skills</h2>
      <p>
        I am continuously developing my technical and creative skills.
      </p>
    </div>

    <div class="skills-grid">

      {% for skills_info in site.data.skills %}
      <article class="skill-card">

        <div class="skill-icon">
          ✦
        </div>

        <h3>{{ skills_info.name }}</h3>

        <p>
          {{ skills_info.description }}
        </p>

        {% if skills_info.url %}
        <a
          href="{{ skills_info.url }}"
          target="_blank"
          rel="noopener"
          class="card-link"
        >
          Learn More →
        </a>
        {% endif %}

      </article>
      {% endfor %}

    </div>

  </div>
</section>


<!-- Traineeship Section -->
<section class="section traineeship-section" id="traineeship">
  <div class="container">

    <div class="section-heading">
      <p class="section-label">EXPERIENCE</p>
      <h2>Traineeship</h2>
    </div>

    <div class="traineeship-list">

      {% for traineeship_info in site.data.traineeship %}
      <article class="traineeship-card">

        <div class="traineeship-icon">
          💼
        </div>

        <div class="traineeship-content">

          <h3>{{ traineeship_info.name }}</h3>

          <p>
            {{ traineeship_info.description }}
          </p>

          {% if traineeship_info.url %}
          <a
            href="{{ traineeship_info.url }}"
            target="_blank"
            rel="noopener"
            class="card-link"
          >
            View Traineeship →
          </a>
          {% endif %}

        </div>
      </article>
      {% endfor %}

    </div>

  </div>
</section>


<!-- Contact Section -->
<section class="contact-section" id="contact">
  <div class="container">

    <div class="contact-content">

      <p class="section-label">GET IN TOUCH</p>

      <h2>Let's Connect</h2>

      <p>
        I am always interested in learning, collaborating, and exploring
        opportunities in the IT field.
      </p>

      <form
        action="https://formspree.io/f/xoevbkdd"
        method="POST"
        class="contact-form"
      >

        <div class="form-group">
          <label for="name">Name</label>

          <input
            type="text"
            id="name"
            name="name"
            placeholder="Your name"
            required
          />
        </div>

        <div class="form-group">
          <label for="email">Email</label>

          <input
            type="email"
            id="email"
            name="email"
            placeholder="your@email.com"
            required
          />
        </div>

        <div class="form-group">
          <label for="message">Message</label>

          <textarea
            id="message"
            name="message"
            rows="6"
            placeholder="Write your message..."
            required
          ></textarea>
        </div>

        <button type="submit" class="btn primary-btn">
          Send Message
        </button>

      </form>

      <p class="contact-email">
        Or email me directly:
        <a href="mailto:pujabhusal1234@gmail.com">
          pujabhusal1234@gmail.com
        </a>
      </p>

    </div>
  </div>
</section>


<!-- Footer -->
<footer class="site-footer">
  <div class="container footer-content">

    <div>
      <a href="{{ '/' | relative_url }}" class="logo">
        Puja<span>.</span>
      </a>

      <p>BCA Graduate</p>
    </div>

    <p class="copyright">
      {{ 'now' | date: "%Y" }} Puja Bhusal.
    </p>

  </div>
</footer>


<!-- Bootstrap JavaScript -->
<script
  src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js">
</script>
