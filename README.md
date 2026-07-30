# China Expo Hub

Агрегатор выставок Китая с базой компаний-участников, контактами и флагманскими товарами.

## Структура

```
china-expo-hub/
├── index.html          # текущий прототип (статика, данные встроены в JS)
├── docs/
│   ├── china_expo_hub_schema.sql     # DDL для Postgres/Supabase
│   └── china_expo_hub_structure.md   # классификация отраслей и freemium-модель
└── public/              # сюда позже — иконки, фавикон, статичные ассеты
```

## Как задеплоить (Vercel, 5 минут)

1. Зайти на [vercel.com](https://vercel.com), войти через GitHub-аккаунт.
2. New Project → выбрать этот репозиторий.
3. Framework Preset: **Other** (это статический HTML, билд не нужен).
4. Deploy — через ~30 секунд появится ссылка вида `china-expo-hub.vercel.app`.

Дальше при каждом `git push` в `main` Vercel пересобирает сайт автоматически.

## Следующие шаги

- [ ] Подключить Supabase (база данных вместо статичного JS-массива)
- [ ] Вынести данные компаний в `/data/companies.json`, подгружать через `fetch()`
- [ ] Настроить Telegram Mini App на этот же URL
