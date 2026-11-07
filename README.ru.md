<p><img src="https://raw.githubusercontent.com/lenar2/luch/main/website/assets/luch-ray.svg" width="36"></p>

# LUCH для Gemini CLI
### Терминал остаётся знакомым. Работа выходит за его пределы.

В Gemini CLI вы формулируете задачу. **LUCH при разрешённом аккаунте может дать ограниченный доступ к браузеру, файлам, устройствам и выбранным серверам** — без безусловного права выполнять любые действия.

[**Настоящий случай LUCH**](https://github.com/lenar2/luch/blob/design/hea-evidence-first-20261107/docs/REAL_WORK.ru.md) · [**Начать подключение**](#подключение-в-gemini-cli) · [English](README.md) · [Главный LUCH](https://github.com/lenar2/luch)

> **Ранний доступ:** исходники расширения доступны, но самостоятельная регистрация нового пользователя, полный путь OAuth в Gemini CLI и работа со всеми устройствами **не подтверждены**. Установка не открывает аккаунт.

## Проверяемая работа

Основатель попросил переделать слишком технический сайт LUCH, не затрагивая Mac. ИИ через разрешённые инструменты исследовал живой сайт и GitHub, подготовил редакцию, исправил мобильный дефект и с разрешения выпустил новую версию. [Точный коммит](https://github.com/lenar2/luch/commit/06daa8d6b89a3dfd65e74628b895879e79a0c931) · [запись выпуска](https://github.com/lenar2/ai-factory-evidence/issues/4009#issuecomment-6692683064).

**Этот случай не является проверкой выполнения именно в Gemini CLI.** [Полные факты и ограничения](https://github.com/lenar2/luch/blob/design/hea-evidence-first-20261107/docs/REAL_WORK.ru.md).

## Подключение в Gemini CLI

**1 · Проверьте аккаунт.** [Доступность LUCH](https://luch.lenarsalimov.ru/ru/status/). Если доступ не включён, установка расширения сама его не создаст.

**2 · Установите расширение:**

```bash
gemini extensions install https://github.com/lenar2/luch-gemini
```

Перезапустите Gemini CLI и проверьте:

```text
/extensions list
/mcp auth luch
/mcp list
```

Для OAuth может потребоваться локальный браузер с callback. Пользуйтесь только своим разрешённым аккаунтом.

**3 · Сначала задача без записи:** «Открой эту публичную страницу и перескажи её со ссылкой». Сверьте доступные инструменты и результат до запросов на изменение.

## Что внутри

| Часть | Назначение |
| --- | --- |
| [`gemini-extension.json`](gemini-extension.json) | Защищённый HTTPS MCP |
| [`skills/`](skills/) | 12 навыков с учётом разрешений |
| [`GEMINI.md`](GEMINI.md) | Правила безопасности без скрытых автоматических команд |

MCP: `https://api.lenarsalimov.ru/luch/core/mcp`. Ключи, чужие устройства и закрытый сервер не входят в пакет.

<details><summary>Проверки для разработчиков</summary>

Установка расширения — не проверка реального OAuth, доступа к ресурсам, отказа при отсутствии разрешения или отзыва доступа. Независимый новый пользовательский E2E пока не имеет PASS. Текстовый значок расширения остаётся черновиком до утверждения бренда.

[Безопасность](SECURITY.md) · [Условия](https://luch.lenarsalimov.ru/terms/) · [Конфиденциальность](https://luch.lenarsalimov.ru/privacy/) · [Поддержка](https://luch.lenarsalimov.ru/support/)

</details>
