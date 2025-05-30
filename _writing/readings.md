---
title: 阅读
---

# 序

这周在晨昕家里我结识了一位新的伙伴，盛辙易。
辙易为人乐观洒脱，涉猎繁广。
别瞧他年仅二十又二，思想的广度和深度却实在令我由衷赞叹。
勤于实践固然居功汗马，博览群书、笔耕不辍更乃于春之计。

读过辙易的《书单回忆录》我颇受启发，想来自己也应当梳理一下三十年来自己的各种阅读心得，于是开设此番“阅读”栏目。
一来回顾自己的阅读历史，结合当时的人生阶段，体悟个体的修习规律。
再者于回顾中鞭策，三省吾身：阅而思乎？读而习乎？其致博乎？
其三以书会友，与博学者交流，择善而从，不善而改。
待到栏目初成之日，期待与辙易的书单互相碰撞，绽放智慧的花火。

书单分类所列皆为使我受益匪浅之作。
有些益在思想，有些利在执笔，还有些裨于习惯养成。
所有点评时时回顾，时时修补，为保心迹，皆留时间。

<p align="right">2024.12.20于零号湾</p>

<ul>
  {% assign sorted = site.writing_readings | sort: 'num' %}
  {% for post in sorted %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    </li>
  {% endfor %}
</ul>