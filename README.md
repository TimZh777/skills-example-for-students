# Команда специалистов для вашего AI-агента

Пять скиллов для Claude Code и плагин Superpowers. Скилл — это инструкция для одного «специалиста»: Claude сам зовёт нужного, когда видит подходящую задачу.

| Роль | Скилл | Что делает |
|---|---|---|
| Разведчик | `competitor-research` | Тренды, дайджест новостей, анализ аудитории и конкурентов в вашей нише |
| Интервьюер | `discovery-interview` | Превращает размытую идею в подробное ТЗ через интервью с вариантами ответа |
| Писатель | `content-creator` | Посты, статьи, рассылки, описания продуктов |
| Разработчик | `fullstack-developer` | Код для сайтов, ботов, автоматизаций и прототипов |
| Дизайнер | `frontend-design` | Лендинги и интерфейсы, которые не выглядят «как сделано на ИИ» |
| Методолог | плагин Superpowers | Ведёт сложные задачи по этапам: обсуждение → план → выполнение с проверкой |

## Установка скиллов

1. Нажмите зелёную кнопку **Code** → **Download ZIP** и распакуйте архив.
2. Скопируйте папки из `skills/` в одно из мест:
   - **Для всех проектов (рекомендуется):** `C:\Users\<ваше имя>\.claude\skills\` на Windows или `~/.claude/skills/` на Mac.
   - **Только для одного проекта:** в папку `.claude/skills/` внутри проекта.
3. Перезапустите Claude Code (в VS Code: Ctrl+Shift+P → «Перезагрузить окно»).

Или просто напишите Claude Code:

```
Скачай скиллы из репозитория github.com/TimZh777/skills-example-for-students
и поставь их глобально в ~/.claude/skills
```

## Установка Superpowers

Superpowers — не скилл, а плагин (набор из многих скиллов). Он ставится командой, которую нужно ввести прямо в окно чата Claude Code:

```
/plugin install superpowers@claude-plugins-official
```

Плагин работает во всех проектах и включается сам: когда вы начинаете что-то строить, Claude сначала задаёт вопросы и уточняет задачу, потом показывает план, и только после вашего «да» делает работу, проверяя каждый шаг.

## Как пользоваться

Ничего запоминать не нужно — просто ставьте задачу обычными словами:

- «Сделай дайджест новостей по моей нише за неделю» → Разведчик
- «Хочу сделать онлайн-школу, помоги составить ТЗ» → Интервьюер
- «Напиши пост для Telegram про …» → Писатель
- «Сделай бота, который …» → Разработчик
- «Сделай лендинг для моего курса» → Дизайнер

Разведчик берёт вашу нишу и аудиторию из файлов агента (`USER.md`, `MEMORY.md`). Если их нет — один раз спросит сам.

## Источники и лицензии

| Скилл | Источник | Лицензия |
|---|---|---|
| `discovery-interview` | [parcadei/Continuous-Claude-v3](https://github.com/parcadei/Continuous-Claude-v3) | MIT — [licenses/MIT-Continuous-Claude-v3.txt](licenses/MIT-Continuous-Claude-v3.txt) |
| `content-creator`, `fullstack-developer` | [Shubhamsaboo/awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps) | Apache 2.0 — [licenses/Apache-2.0-awesome-llm-apps.txt](licenses/Apache-2.0-awesome-llm-apps.txt) |
| `frontend-design` | [anthropics/skills](https://github.com/anthropics/skills) | Apache 2.0 — [skills/frontend-design/LICENSE.txt](skills/frontend-design/LICENSE.txt) |
| `competitor-research` | переработанная универсальная версия | MIT |
| Superpowers | [obra/superpowers](https://github.com/obra/superpowers) | MIT (не входит в этот репозиторий) |

Изменения относительно оригиналов: в `discovery-interview` убрана привязка к устаревшей модели Claude; `competitor-research` переписан под любую нишу.
