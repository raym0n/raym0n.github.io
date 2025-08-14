---
layout: page
title: Музыка
permalink: /music
---

<section class="neuro-section">
  <h2 class="glitch-title">Дискография</h2>

  <div class="track-list">
    {% for album in site.data.discography %}
    <div class="track">
      <h3>{{ album.title }}</h3>
      <p>{{ album.year }} | {{ album.label }}</p>

      <div class="neuro-player">
        <audio controls>
          <source src="{{ album.preview }}" type="audio/mpeg">
        </audio>
      </div>

      <ul>
        {% for track in album.tracks %}
        <li>{{ track.title }} <span class="neuro-duration">{{ track.duration }}</span></li>
        {% endfor %}
      </ul>
    </div>
    {% endfor %}
  </div>
</section>

<section class="neuro-section">
  <h2 class="glitch-title">Видео</h2>

  <div class="video-grid">
    <div class="video-item glitch-video">
      <iframe src="https://www.youtube.com/embed/..." frameborder="0" allowfullscreen></iframe>
    </div>
  </div>
</section>
