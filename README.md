<h1 align="center">MongoDB</h2>

<img src="Mongodb.png">

<p align="center">Repository containing the queries developed in MongoDB</p>

<h2>Website</h2>

<https://www.mongodb.com>

<h2>Installation on Manjaro</h2>

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

<h2>Listing Commands</h2>

```
    help
```

<h2>Create Database / Collections [states, persons]</h2>

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

<h2>Droping Databases / Collections [states, persons]</h2>

```
    db.states.drop()
```

```
    db.persons.drop()
```

<h2>Inserting</h2>

db.persons.insert({ name: "John Doe", country: "USA" })