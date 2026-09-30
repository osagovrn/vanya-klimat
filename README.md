# Иван Климат — установка кондиционеров в Адлере и Сочи

Одностраничный сайт-визитка мастера по монтажу и обслуживанию кондиционеров
(Адлер, Сочи и радиус 200 км). Статический сайт без сборки, хостится на
**GitHub Pages**. Публикуется автоматически при пуше в `main`.

## Адреса

| Что | Где |
|---|---|
| Сайт (сейчас) | https://yvwvy.ru/vanya-klimat/ |
| Репозиторий | https://github.com/osagovrn/vanya-klimat |
| Ветка | `main` (публикуется автоматически) |

Домен пока не подключён. Когда домен `vanya-klimat.ru` будет куплен — добавить
файл `CNAME` в корень и заменить адреса на домен в `index.html`
(`canonical`, `og:url`, `og:image`, `twitter:image`, JSON-LD), `sitemap.xml`
и `robots.txt`.

## Структура

```
.
├── index.html               # Весь сайт (локально собранный Tailwind)
├── 404.html                 # Кастомная страница ошибки
├── privacy-policy.html      # Политика конфиденциальности
├── og-image.png             # Превью для соцсетей (1200×630)
├── robots.txt               # Разрешено всё + Sitemap
├── sitemap.xml              # Карта сайта
├── fonts/                   # Локальные шрифты (woff2 + fonts.css, без внешних CDN)
├── images/
│   └── hero.jpg             # Фоновое фото первого экрана
└── .github/workflows/
    └── pages.yml            # Публикация на GitHub Pages при push
```

## Локальные ресурсы

Внешние зависимости убраны: шрифты (`Manrope`, `Unbounded`) и hero-фото лежат
локально и подключены через `fonts/fonts.css` и `images/hero.jpg`. Единственное
внешнее встраивание — карта в блоке «Контакты» (Google Maps iframe).

## Как задеплоить изменения вручную

```bash
git add -A
git commit -m "Описание изменений"
git push origin main
```

Push в `main` автоматически публикует сайт через `pages.yml`.

## Что осталось заполнить

- Telegram: заменить во всех ссылках `t.me/+79182011940` на `@username` (без `+`).
- Коды подтверждения Яндекс.Вебмастер и Google Search Console (в `<head>` `index.html`).
