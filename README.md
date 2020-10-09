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

```bash
    git clone https://aur.archlinux.org/mongodb-bin.git
```

```bash
    cd mongodb-bin
```

```bash
    makepkg -si
```

```bash
    systemctl start mongodb
```

```bash
    systemctl enable mongodb
```

<h2 align="center">Listing Commands</h2>

```sql
    help
```

<h2 align="center">Create Database / Collection [states, persons]</h2>

```sql
    use db
```

```sql
    db.createCollection('states')
```

```sql
    db.createCollection('persons')
```

```sql
    show dbs
```

```sql
    show collections
```

<h2 align="center">Droping Databases / Collection [states, persons]</h2>

```sql
    db.states.drop()
```

```sql
    db.persons.drop()
```

<h2 align="center">Inserting Data</h2>

```sql
    db.persons.insert({ name: "John Doe", country: "United States of America" })

    db.persons.insert({ name: "Bia", country: "Brazil" })

    db.persons.insert({ name: "Bruna", country: "Brazil", age: 24 })

    db.persons.insert({ name: "Hannah", country: "UK" })

    db.states.insert({
        name: "Rio Grande do Sul",
        cities: [
            {
                _id: ObjectId(),
                name: "Novo Hamburgo"
            },
            {
                _id: ObjectId(),
                name: "Porto Alegre"
            },
            {
                _id: ObjectId(),
                name: "São Leopoldo"
            }
        ]
    })
```

<h2 align="center">Listing Data</h2>

```sql
    db.persons.find()

    db.persons.find().pretty()
```

<h2 align="center">Querys</h2>

```sql
    db.states.findOne({ name: "Rio Grande do Sul" })

    db.states.find({ name: "Rio Grande do Sul" }).pretty()
```

```sql
    db.persons.find({ $or: [{ name: "Bia" }, { name: "Hannah" }] }).pretty()
```

```sql
    db.persons.find({ $and: [{ country: "Brazil" }, { name: "Bruna" }] }).pretty()
```

```sql
    db.persons.find({ age: { $exists: true } })
```

<h4 align="center">Skip / Limit</h4>

```sql
    db.persons.find().skip(0).limit(1)
```

<h4 align="center">Count</h4>

```sql
    db.persons.count()
```

```sql
    db.persons.find({ country: "Brazil" }, { name: 1, country: 1, _id: 0 }).pretty()
```

```sql
    db.states.find({ name: "Rio Grande do Sul"  }, { "cities.name": 1, "_id": 0 }).pretty()
```