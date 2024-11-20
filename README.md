# Задание 2

- Запросы для вставки данных о двух книгах в `books`:

```
db.books.insertOne({
	title: "Гиперион",
	description: "",
	authors: ""
})

db.books.insertOne({
	title: "Эндимион",
	description: "Книга вторая",
	authors: "Дэн Симмонс"
})
```

- Запрос для поиска полей документов в `books` по полю `title`:

```
db.books.find(
	{ title: /^Mongo/ },
	{ title: 1, description: 1, authors: 1}
)
```

- Запрос для редактирования полей `description` и `authors` в `books` по `_id` записи:

```
db.books.updateOne(
	{ _id: 1 }
	{ $set: { authors: "Майкл Маршалл Смит", description: "Книга о вкусной и здоровой пищи" } }
)
```
