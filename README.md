Гайд вставил на всякий случай мало ли будет полезен.

# Гайд по GitHub (Гайд сгенерирован искуственным интелектом)

## 3. Основные понятия

- **Репозиторий (repo)** — хранилище файлов и истории изменений.
- **Коммит (commit)** — сохранённое состояние проекта.
- **Ветка (branch)** — независимая линия разработки.
- **Pull Request (PR)** — предложение внести изменения в репозиторий.
- **Issue** — задача, баг или идея.
- **Fork** — копия чужого репозитория в вашем аккаунте.
- **Clone** — локальная копия репозитория.
- **Remote** — удалённый репозиторий (например, `origin`).

---

## 4. Создание репозитория

### Через веб-интерфейс
1. Нажмите **New repository**.
2. Введите имя, описание, выберите публичный или приватный.
3. При желании добавьте `README.md`, `.gitignore` и лицензию.

### Через командную строку
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin git@github.com:username/repo.git
git push -u origin main
```

---

## 5. Основные команды Git

```bash
git clone <url>          # клонировать репозиторий
git status               # статус изменений
git add <file>           # добавить файл в индекс
git add .                # добавить все изменения
git commit -m "message"  # закоммитить
git push                 # отправить на GitHub
git pull                 # получить изменения
git branch               # список веток
git checkout -b new      # создать и переключиться на ветку
git switch new           # переключиться на ветку (современный вариант)
git merge branch         # слить ветку в текущую
git log --oneline        # краткая история коммитов
```

---

## 6. Ветки и Pull Request

1. Создайте ветку:
   ```bash
   git checkout -b feature
   ```
2. Внесите изменения, закоммитьте и запушьте:
   ```bash
   git add .
   git commit -m "Add feature"
   git push -u origin feature
   ```
3. На GitHub нажмите **Compare & pull request**.
4. Опишите изменения, назначьте ревьюеров.
5. После одобрения нажмите **Merge pull request**.

---

## 7. Issues и Projects

- **Issues** — задачи, баги, идеи. Можно назначать исполнителей, метки, milestone.
- **Projects** — канбан-доски для управления задачами. Создаются во вкладке **Projects**.

---

## 8. GitHub Actions

Автоматизация тестов, сборки и деплоя. Пример `.github/workflows/ci.yml`:

```yaml
name: CI
on: [push, pull_request]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Setup Node
        uses: actions/setup-node@v4
        with:
          node-version: 20
      - run: npm ci
      - run: npm test
```

---

## 9. GitHub Pages

Хостинг статических сайтов бесплатно.

1. Создайте репозиторий `username.github.io`.
2. Добавьте `index.html`.
3. В **Settings → Pages** выберите ветку `main`.
4. Сайт будет доступен по `https://username.github.io`.

---

## 10. Совместная работа

- Сделайте **Fork** чужого репозитория.
- Клонируйте свой форк:
  ```bash
  git clone git@github.com:your-username/repo.git
  ```
- Создайте ветку, внесите изменения, запушьте.
- Создайте **Pull Request** в оригинальный репозиторий.
- Пройдите code review и дождитесь merge.

---

## 11. Полезные ссылки

- [Документация GitHub](https://docs.github.com)
- [Pro Git на русском](https://git-scm.com/book/ru/v2)
- [GitHub Skills](https://skills.github.com)
- [Шпаргалка по Git](https://education.github.com/git-cheat-sheet-education.pdf)

---

