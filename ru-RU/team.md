---
layout: ru-RU/default
title: Команада Rust &middot; Язык Программирования Rust

# соответствие имени пользователя в GitHub с именем и irc ником (irc ник может быть пропущен, если
# соответсвует GitHub).
состав:
  aatch:
    имя: James Miller
  arielb1:
    имя: Ariel Ben-Yehuda
  alexcrichton:
    имя: Alex Crichton
    irc: acrichto
  aturon:
    имя: Aaron Turon
  bkoropoff:
    имя: Brian Koropoff
  brson:
    имя: Brian Anderson
  bstrie:
    имя: Ben Striegel
  BurntSushi:
    имя: Andrew Gallant
    irc: burntsushi
  carols10cents:
    имя: Carol Nichols
  dotdash:
    имя: Björn Steinbrink
    irc: doener
  eddyb:
    имя: Eduard Burtescu
  edunham:
    имя: Emily Dunham
  erickt:
    имя: Erick Tryzelaar
  Gankro:
    имя: Alexis Beingessner
    прошлые команды:: ["libs"]
  huonw:
    имя: Huon Wilson
    irc: huon
    прошлые команды:: ["core", "lang", "libs"]
  GuillaumeGomez:
    имя: Guillaume Gomez
    irc: imperio
  jonathandturner:
    имя: Jonathan Turner
    irc: jntrnr
  jseyfried:
    имя: Jeffrey Seyfried
    irc: jseyfried
  Kimundi:
    имя: Marvin Löbel
    irc: kimundi
  manishearth:
    имя: Manish Goregaokar
    irc: Manishearth
  mbrubeck:
    имя: Matt Brubeck
  michaelwoerister:
    имя: Michael Woerister
    irc: mw
  niconii:
    имя: Nicolette Verlinden
    irc: niconii
  nikomatsakis:
    имя: Niko Matsakis
    irc: nmatsakis
  nrc:
    имя: Nick Cameron
  pcwalton:
    имя: Patrick Walton
  peschkaj:
    имя: Jeremiah Peschka
    irc: peschkaj
  pnkfelix:
    имя: Felix Klock
  sfackler:
    имя: Steven Fackler
  skade:
    имя: Florian Gilcher
  steveklabnik:
    имя: Steve Klabnik
  vadimcn:
    имя: Vadim Chugunov
  wycats:
    имя: Yehuda Katz
  jonathandturner:
    имя: Jonathan Turner
  badboy:
    имя: Jan-Erik Rediger
  johannhof:
    имя: Johann Hofmann
  booyaa:
    имя: Mark Sta Ana

# Информация о командах. Пропускается `лидер` для команд без лидера.
команды:
  - название: Core team
    ответственность: "overall direction of the project, subteam leadership, cross-cutting concerns"
    члены: [brson, alexcrichton, wycats, steveklabnik, nikomatsakis, aturon, pcwalton, erickt]
  - название: Language design team
    ответственность: "designing new language features"
    члены: [eddyb, nrc, pnkfelix, nikomatsakis, aturon]
    lead: nikomatsakis
  - название: Library team
    ответственность: "the Rust standard library, rust-lang crates, conventions"
    члены: [brson, alexcrichton, sfackler, BurntSushi, Kimundi, aturon]
    lead: aturon
  - название: Compiler team
    ответственность: "compiler internals, optimizations"
    члены: [arielb1, eddyb, nrc, pnkfelix, bkoropoff, nikomatsakis, aatch, dotdash, michaelwoerister, jseyfried]
    lead: nikomatsakis
  - название: Tooling and infrastructure
    ответственность: "tool support (e.g. Cargo, rustup), CI infrastructure, etc."
    члены: [brson, nrc, alexcrichton, vadimcn, wycats, michaelwoerister]
    lead: alexcrichton
  - название: Community team
    ответственность: "coordinating events, outreach, commercial users, teaching materials, and exposure"
    lead: erickt
    члены: [brson, skade, manishearth, johannhof, steveklabnik, carols10cents, badboy, booyaa, bstrie, erickt, jonathandturner, edunham]
    email: community-team@rust-lang.org
  - название: Documentation team
    ответственность: "ensuring Rust has fantastic documentation"
    члены: [steveklabnik, GuillaumeGomez, jonathandturner, peschkaj]
  - название: Модераторы
    ответственность: "helping uphold the <a href='https://www.rust-lang.org/conduct.html'>code of conduct</a>"
    члены: [mbrubeck, BurntSushi, manishearth, pnkfelix, niconii]
    email: rust-mods@rust-lang.org
  - название: Rust team alumni
    ответственность: "enjoying a leisurely retirement"
    члены: [Gankro, huonw]

# Information on sites to get profile information from
sites:
  github:
    url: https://github.com/%nick
    avatar: https://avatars.githubusercontent.com/%nick
  twitter:
    url: https://twitter.com/%nick
    avatar: https://avatars.io/twitter/%nick?size=large
---

<style type="text/css">
.headshot {
  border: 1px solid #888;
  width: 140px;
}

.person {
  display: inline-block;
  position: relative;
  margin-bottom: 20px;
}
.lead { font-weight: bold; }
.lead .name::after { content: " (lead)"; }
.details {
  display: none;
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: rgba(0, 0, 0, 0.5);
  color: white;
  font-weight: normal;
}
.person:hover .details {
   display: block;
}

.headshots {
  text-align: center;
  margin: 0px auto;
  padding: 0;
  width: 700px;
  max-width: 100%;
  list-style: none;
}
</style>

# The Rust Team

The Rust project is
[governed](https://github.com/rust-lang/rfcs/blob/master/text/1068-rust-governance.md)
by a number of teams, each focused on a specific area of concern. Below are
the rosters, in alphabetical order.

To contact a team, post your question or comment to [the Internals
forum](https://internals.rust-lang.org/) and tag your post with the category
corresponding to the team name. Note that security disclosures should follow
the [Rust security disclosure process](security.html). 

{% for team in page.teams %}
<section id="{{ team.name | replace:' ','-' }}">
<h2> {{ team.name }} </h2>

<strong>Responsibility</strong>: <em>{{ team.responsibility }}</em>

<br />

{% if team.email %}
  <strong>Contact</strong>:
  <a href="mailto:{{ team.email | uri_escape }}">{{ team.email }}</a>
{% endif %}

<ul class="headshots">
{% for nick in team.members %}
  {% assign person = page.people[nick] %}
  {% if person.site %}
    {% assign sitename = person.site %}
  {% else %}
    {% assign sitename = "github" %}
  {% endif %}
  {% assign site = page.sites[sitename] %}
  <li class="person {% if team.lead and team.lead == nick %}lead{% endif %}">
  <a href="{{ site.url | replace:'%nick',nick }}">
    <div class="name">{{ person.name }}</div>
    <div class="details">
      <div>irc: {% if person.irc %}{{ person.irc }}{% else %}{{ nick }}{% endif %}</div>
      {% if person.ex-teams %}
      <div>teams: {{ person.ex-teams | join: ", " }}</div>
      {% endif %}
    </div>
    <img class="headshot" src="{{ site.avatar | replace:'%nick',nick }}" alt="{{ person.name }}">
  </a>
</li>
{% endfor %}
</ul>
</section>
{% endfor %}

