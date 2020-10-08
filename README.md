<p align="center"><img src="Mongodb.png" width="400"></p>

<p align="center">Repository containing the queries developed in <a href="https://www.mongodb.com">👉 MongoDB 👈</a></p>

<p align="center">
    <a href="https://opensource.org/licenses/MIT">
        <img alt="License" src="https://img.shields.io/badge/License-MIT-yellow.svg">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/languages/count/MagicalStrangeQuark/MongoDB">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/last-commit/MagicalStrangeQuark/MongoDB">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/followers/MagicalStrangeQuark?style=social">
    </a>
</p>

<h2 align="center">Website</h2>

<h3 align="center">
    <a href="https://www.mongodb.com">https://www.mongodb.com</a>
</h3>

<h2 align="center">Installation on Manjaro</h2>

```
    git clone https://aur.archlinux.org/mongodb-bin.git
```

```
    cd mongodb-bin
```

```
    makepkg -si
```

```
    systemctl start mongodb
```

```
    systemctl enable mongodb
```

<h2 align="center">Listing Commands</h2>

```
    help
```

<h2 align="center">Create Database / Collections [states, persons]</h2>

```
    use db
```

```
    db.createCollection('states')
```

```
    db.createCollection('persons')
```

```
    show dbs
```

```
    show collections
```

<h2 align="center">Droping Databases / Collections [states, persons]</h2>

```
    db.states.drop()
```

```
    db.persons.drop()
```

<h2 align="center">Inserting</h2>

```
    db.persons.insert({ name: "John Doe", country: "United States of America" })

    db.persons.insert({ name: "Bia", country: "Brasil" })

    db.persons.insert({ name: "Hannah", country: "UK" })
```

<h2 align="center">Listing</h2>

```
    db.persons.find()

    db.persons.find().pretty()
```