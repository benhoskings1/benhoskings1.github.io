---
title: "Emotion Recognition from a Sequence of 3D Facial Landmarks"
collection: academic_projects
permalink: /academic_projects/emotion_recognition
author_profile: true
overview: 
    "The project produced a novel facial emotion recognition framework that can be used to classify images. <br>
    The key contributions are ..."
git_link: https://github.com/benhoskings1/Emotion_Recognition.git
languages: "Matlab + Python"
cover_image: NoseTipDetection.png
dates: "2023"
---

{% include base_path %}

{% if post.id %}
  {% assign title = post.title | markdownify | remove: "<p>" | remove: "</p>" %}
{% else %}
  {% assign title = post.title %}
{% endif %}

<style>
/* Create two equal columns that floats next to each other */
.column {
  float: left;
  width: 50%;
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}
</style>

<div class="list__item">
  <article class="archive__item">
    <div class="row">
      <div class="column" style="float: left; width: 70%;">
        <!-- Left column - Product overview -->
        <h2 style="margin-left: auto; margin-right: auto;">
          {{ title }}
        </h2>
        {% if post.languages || if post.dates%}
          <table style="width:100%; border: none;">
            <tr style="padding-top: 50px;">
              {% if post.languages %}
                <td style="width:50%; border: none;font-style: italic;font-weight: normal; font-size: 18px; text-align: center;">
                  {{post.languages}}
                </td>
              {% endif %}
              {% if post.dates %}
                <td style="width:50%; border: none;
                font-style: italic;font-weight: normal; font-size: 18px; text-align: center;">
                  {{post.dates}}
                </td>
              {% endif %}
            </tr>
          </table>
        {% endif %}
        {% if post.overview %}
          <p style="padding-top: 0"> {{ post.overview }} </p>
        {% endif%}
        <div>
          <table style="width:100%;border:none;">
            <tr>
              {% if post.git_link %}
                <td style="width:50%; border: none; text-align:center;"><a>
                  Explore the project
                </a></td>
                <td style="width: 50%; border:none; text-align:center;"><a>
                  Explore the code
                </a></td>
              {% elsif post.permalink %}
                <td style="border:none; text-align:center;"><a>
                  Explore the project
                </a></td>
              {% endif %}
            </tr>
          </table>
        </div>
      </div>
      <!-- Right column - Image -->
      <div class="column" style="float: left; width: 30%">
        {% if post.cover_image %}
          <div>
            <img src="/assets/images/NoseTipDetection.png" alt="emotion-recognition-abstract" style="height: auto; max-height: 300px; display: block; margin-left: auto; margin-right: auto;"/>
          </div>
        {% endif %}
      </div>
    </div>
    <br>
  </article>
</div>