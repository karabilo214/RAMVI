<div align="center">

# RAMVI

**Персональная AI-платформа для Windows и macOS.**

Работает на вашем компьютере, без подписки и без телеметрии. Облако подключается, только если вы сами этого хотите.

[**⬇ Скачать последнюю версию**](https://github.com/karabilo214/RAMVI/releases/latest) · [Лицензии](LICENSES.md) · [Сообщить об ошибке](https://github.com/karabilo214/RAMVI/issues) · [English](#english)

</div>

---

## Экраны

| Чат | Агент |
|---|---|
| ![Чат](docs/screenshots/chat.png) | ![Агент](docs/screenshots/agent.png) |

| Мастер запуска | Голосовой ввод |
|---|---|
| ![Мастер запуска](docs/screenshots/first-run.png) | ![Голосовой ввод](docs/screenshots/voice.png) |

<sub>Мастер запуска и агент сняты в настоящих окнах Windows. Мастер — в чистой Windows Sandbox без сети и без установленных библиотек, агент — на ноутбуке с RTX 5060 и моделью qwen3-8b. Чат и голосовой ввод отрисованы автотестами оболочки, текст в них тестовый.</sub>

## Функции

- **Чат.** Движок поддерживает архитектуры Qwen3 (обычные модели) и Qwen3 MoE в формате GGUF, квантования Q4_K_M, Q6_K и F16 у обычных моделей и Q4_K_M у MoE. Размер модели ограничивает только память: что не помещается в видеопамять, работает из оперативной. Ответы ускоряет маленькая модель-предсказатель (speculative decoding). Есть ответ строго по JSON-схеме и вызов инструментов. Модели можно скачать из встроенного каталога Hugging Face и Ollama или подключить свой файл (одним куском: GGUF, разбитый на части, пока не открывается). Если файл модели перенесли или диск отключён, на экране «Модели» она помечена «Файл модели не найден»: можно указать, где файл теперь (чаты останутся), или убрать модель. При возврате в длинный чат локальная модель не перечитывает историю заново: прочитанное хранится в памяти и на диске (размер — в настройках). На Qwen3-14B после другого чата первое слово появилось через 1,4 с вместо 208 с, ответ тот же. В чате видно, как модель рассуждает. Llama, Gemma, Mistral и DeepSeek пока не поддерживаются, они в планах.
- **Голосовой ввод.** Речь распознаётся на вашем компьютере моделью Whisper. В настройках можно выбрать русский, английский или украинский язык или автоопределение: тогда распознаются и другие языки, которые знает Whisper. Микрофон включается только когда вы сами его включили.
- **Агент для файлов.** Читает, ищет и правит файлы только в папке, которую вы выбрали. Каждую правку сначала показывает как diff и применяет только после вашего подтверждения.
- **API для своих программ**, совместимый с OpenAI, Anthropic и Ollama. По умолчанию доступен только с этого компьютера. У каждого клиента свой ключ и свой счётчик токенов.
- **Без интернета.** Когда модель скачана, сеть больше не нужна.
- **Приватность.** Телеметрии нет. В сеть приложение выходит, только когда вы сами что-то делаете: открываете каталог моделей, скачиваете модель или проверяете обновления.
- **Без установки.** Запускается из любой папки, в том числе с флешки.
- **Горячие клавиши:** Ctrl+M — микрофон, Esc — остановить ответ или запись, Ctrl+N — новый чат. Горячие клавиши меняются в настройках.
- **Облачные модели по API.** Подключаются три вида API: OpenAI (в том числе Codex) и любые совместимые с ним сервисы, например OpenRouter, DeepSeek, Groq, а также LM Studio или vLLM на этом компьютере; Anthropic (Claude); Google Gemini. Адрес сервиса можно указать свой, ключ — ваш. Облачную модель можно выбрать в чате, у агента, у персонажа и в своём API. Ключ лежит в защищённом хранилище системы. Рядом с выбранной моделью написано, куда уходят запросы. Расходы считаются, можно поставить лимит на день и на месяц. Вместо ключа можно войти через ChatGPT: кнопка «Войти через ChatGPT» использует вашу подписку через официальный Codex CLI (он должен быть установлен). Так работают чат и персонаж, агент с инструментами — нет; ответ приходит целиком, реплика персонажа — около 11 с. Пока вы не подключили облако, всё работает локально, как раньше. На Mac без NVIDIA Claude и Codex ответили в чате за 2,2–2,6 с, агент с инструментами решил задачу.
- **Персонаж** (отдельный модуль). Собеседник со своим характером: дружелюбный, саркастичный, строгий и другие. Говорит текстом и голосом, помнит о вас (память можно посмотреть и удалить) и подстраивается под то, как вы реагируете в разговоре: смеётесь, подхватываете или раздражаетесь. Кнопок оценки нет. Многое зависит от модели. В опасной ситуации на облачных Claude и Codex персонаж отвечал всерьёз и называл номер экстренной службы в 4 ответах из 4, на локальной 8B — в 1 из 2.

## Системные требования для Windows

| | |
|---|---|
| Система | Windows 10 или 11, 64-бит |
| Видеокарта | **NVIDIA**, которую поддерживает CUDA 13 |
| Драйвер | **NVIDIA с поддержкой CUDA 13.2 или новее**: [скачать драйвер GeForce](https://www.nvidia.com/drivers) |
| Оперативная память | сколько нужно выбранной модели: мастер запуска посчитает и подскажет, какие модели подойдут |
| Место на диске (SSD, HDD, NVMe) | 3,3 ГБ под программу и место под модели |

Если драйвера нет или он устарел, RAMVI при запуске подскажет, что поставить.

Видеокарта NVIDIA и драйвер нужны только для локальных моделей. С облачными моделями RAMVI работает и без них.

## macOS (Apple Silicon)

С версии 0.9.0 есть сборка для Mac; в 0.9.1 — `RAMVI-0.9.1-macos-arm64.zip`, 153 МиБ. В ней облачные модели, агент, персонаж и голосовой ввод. Локальных моделей на Mac нет, потому что движку нужна видеокарта NVIDIA. Мастер запуска сразу предложит подключить облачную модель. Нужен Mac на Apple Silicon (M1 и новее) с macOS 12 или новее.

Программа пока не подписана Apple. Поэтому перед первым запуском снимите в Терминале метку «скачано из интернета»: `xattr -dr com.apple.quarantine /Applications/RAMVI.app` (укажите путь, где лежит программа). Можно и иначе: попробуйте запустить, затем откройте «Системные настройки» → «Конфиденциальность и безопасность» и нажмите «Открыть всё равно».

Проверяли на Mac M1 Pro. Архив распаковали в пустую папку, окно открылось, Claude ответил в чате за 1,9 с, агент с инструментами решил задачу, персонаж ответил в своём характере. torch и CUDA при этом не загружаются.

## Замеры

Ноутбук с RTX 5060 Laptop (8 ГБ видеопамяти), 16 ГБ оперативной памяти, Windows 11. RAMVI и Ollama 0.40.13 мерили в один день, 19.11.2026, на одном и том же наборе вопросов.

| Случай | RAMVI 0.8.0 | RAMVI 0.9.0 | Ollama 0.40.13 |
|---|---:|---:|---:|
| **Модель больше видеопамяти:** Qwen3-14B Q4_K_M (9,3 ГБ) с моделью-предсказателем Qwen3-0.6B, часть слоёв в видеопамяти, остальные в оперативной | **8,17** ток/с | **8,17** ток/с | 6,17 ток/с |
| **Модель целиком в видеопамяти:** Qwen3-8B Q4_K_M | 34,2 ток/с | 56,6 ток/с | **62,7** ток/с |
| Время до первого слова (медиана), 14B / 8B | 0,55 / 0,18 с | 0,55 / 0,18 с | **0,35 / 0,07** с |

- **14B.** RAMVI быстрее в 1,33 раза и обгоняет Ollama на 22 вопросах из 30.
- **8B.** В версии 0.9.0 RAMVI больше не включает предсказатель, если модель целиком помещается в видеопамять: в этом случае он только тормозил. Скорость выросла в 1,65 раза, ответы те же (совпали 30 из 30). Ollama на 8B пока быстрее примерно на 10%.
- **Первое слово** в обоих случаях быстрее выдаёт Ollama.

Как мерили: 30 вопросов разных типов (факты, код, математика, перевод, творческие задания и другие), до 200 токенов на ответ, температура 0, контекст 2048, размышления выключены. RAMVI и Ollama получали одинаковые запросы. RAMVI на 8B прогнали дважды: 56,61 и 56,65 ток/с, тексты совпали 30 из 30.

Выигрыш на 14B зависит от того, что за текст. На JSON RAMVI быстрее в 3,6 раза, на математике в 2,4, на коде в 2,0. А на творческих заданиях (0,80) и диалогах (0,89) медленнее Ollama: там предсказатель хуже угадывает следующие слова.

## Установка и первый запуск

1. Скачайте `RAMVI-<версия>-win-x64.zip` со страницы [Releases](https://github.com/karabilo214/RAMVI/releases/latest).
2. Распакуйте в любое место, на диск или на флешку. Устанавливать ничего не нужно, флешку можно переносить на другой компьютер.
3. Запустите **`RAMVI.exe`**.
4. Мастер проверит компьютер и предложит модель. **Моделей в архиве нет**: основную модель и маленькую модель-предсказатель, которая ускоряет ответы, приложение скачает само. Можно подключить и уже скачанный файл GGUF или модели Ollama.

Настройки и история лежат рядом с приложением, в папке `data`. Если в эту папку нельзя писать, RAMVI предложит выбрать другую.

## Обновления

Как перейти на новую версию (например, с 0.9.0 на 0.9.1):

1. Закройте RAMVI полностью: если персонаж работает в фоне — значок в трее → «Выйти».
2. Распакуйте новый архив в **новую** папку, не поверх старой.
3. Скопируйте из старой папки RAMVI в новую папку `data` (чаты, память персонажа), файл `settings.json` (если он есть) и папку `models` (скачанные модели). Если в настройках указаны свои папки данных или моделей, копировать их не нужно.
4. Запустите `RAMVI.exe` из новой папки, проверьте, что чаты на месте, и удалите старую папку.

Модели, подключённые из папки Ollama или из другого места на диске, остаются на месте. На Mac данные лежат внутри программы: перед заменой откройте старую `RAMVI.app` через «Показать содержимое пакета» и перенесите `Contents/Resources/data` и `settings.json` в новую.

Встроенная установка обновления из файла («Настройки» → «Общие» → «Обновления») проверяет подпись ключом выпуска (Ed25519) и при неудаче возвращает прежнюю версию, но пока не обновляет саму программу-оболочку, поэтому для 0.9.1 нужен способ выше.

## Исходный код

Код RAMVI открыт по лицензии MIT: [github.com/karabilo214/AI](https://github.com/karabilo214/AI), папка [ramvi](https://github.com/karabilo214/AI/tree/main/ramvi). Там сервис, движок, оболочка, тесты и отчёты проверок. В этом репозитории лежат готовые сборки, описание и лицензии.

## Состав и лицензии

Код RAMVI распространяется по лицензии [MIT](LICENSE). В архив входят сторонние компоненты, у каждого свои условия: Python, PyTorch с библиотеками NVIDIA CUDA и cuDNN, Triton, Transformers, whisper.cpp, .NET, Avalonia и другие. **Полный список со ссылками на все тексты лицензий — в [LICENSES.md](LICENSES.md)**, сами тексты — в папке [`licenses/`](licenses/) (такая же папка есть в архиве). Библиотеки NVIDIA и Microsoft можно использовать только в составе RAMVI, подробности в [THIRD_PARTY_TERMS.txt](licenses/THIRD_PARTY_TERMS.txt).

Целостность скачанного архива можно проверить по SHA-256, он указан в описании каждого релиза:

```powershell
Get-FileHash .\RAMVI-0.9.1-win-x64.zip -Algorithm SHA256
```

---

<a id="english"></a>

## English

**RAMVI is a personal AI platform for Windows and macOS.** It runs on your own computer, with no subscription and no telemetry. Cloud models are used only if you connect them yourself.

### Features

- **Chat.** The engine supports the Qwen3 (dense) and Qwen3 MoE architectures in GGUF format, with Q4_K_M, Q6_K and F16 quantization for dense models and Q4_K_M for MoE. Model size is limited only by memory: whatever doesn't fit in GPU memory runs from RAM. A small draft model speeds up replies (speculative decoding). JSON-schema output and tool calling are supported. Models can be downloaded from the built-in Hugging Face and Ollama catalog, or you can use your own file (a single file: split GGUF files are not supported yet). If a model file was moved or its drive is disconnected, the Models screen marks it "Model file not found": you can point to where the file is now (chats stay) or remove the model. When you return to a long chat, the local model does not re-read the history: what it has read is kept in RAM and on disk (size in the settings). On Qwen3-14B, after another chat, the first word came in 1.4 s instead of 208 s, with the same answer. Llama, Gemma, Mistral and DeepSeek are not supported yet; they are planned.
- **Voice input**, recognized on your computer by Whisper. In settings you can pick Russian, English or Ukrainian, or automatic detection, which also covers the other languages Whisper knows. The microphone is on only when you turn it on.
- **File agent** that works only inside a folder you choose. Every change is shown as a diff first and applied only after you approve it.
- **API for your own tools**, compatible with OpenAI, Anthropic and Ollama. Local-only by default, with a separate key per client.
- Works offline once a model is downloaded. No installation needed: runs from any folder or a USB stick.
- **Shortcuts:** Ctrl+M — microphone, Esc — stop the reply or recording, Ctrl+N — new chat. Shortcuts can be changed in the settings.
- **Cloud models via API.** Three kinds of API: OpenAI (including Codex) and any service compatible with it, such as OpenRouter, DeepSeek, Groq, or LM Studio and vLLM on this computer; Anthropic (Claude); Google Gemini. You can set your own service address; the key is yours. You can pick a cloud model in chat, for the agent, for the character and in the API. The key is kept in the system key store, the model picker shows where requests go, and costs are tracked with optional daily and monthly limits. Instead of a key you can sign in with ChatGPT: the “Sign in with ChatGPT” button uses your subscription through the official Codex CLI (it must be installed). Chat and the character work, the agent with tools does not; the reply arrives in one piece, a character line takes about 11 s. Until you connect a cloud model, everything stays local. On a Mac without NVIDIA, Claude and Codex answered in chat in 2.2–2.6 s and the agent solved a task with tools. Cloud models don't need an NVIDIA GPU.
- **Character** (a separate module): a companion with a personality, text and voice, and a memory you can view and delete. A lot depends on the model. In an emergency, on cloud Claude and Codex it answered seriously and gave an emergency number in 4 of 4 replies; on local 8B, in 1 of 2.

### macOS (Apple Silicon)

`RAMVI-0.9.1-macos-arm64.zip`, 153 MiB, for Apple Silicon Macs (M1 and newer) with macOS 12 or newer: cloud models, agent, character and voice input. There are no local models on Mac because the engine needs an NVIDIA GPU. The app isn't signed by Apple yet, so run `xattr -dr com.apple.quarantine /Applications/RAMVI.app` once, or try to open it and then go to System Settings → Privacy & Security → Open Anyway.

### System requirements for Windows

Windows 10 or 11, 64-bit; an **NVIDIA GPU** supported by CUDA 13, with a driver that supports **CUDA 13.2 or newer** ([GeForce drivers](https://www.nvidia.com/drivers)); as much RAM as the chosen model needs (the setup wizard works it out and shows which models fit); 3.3 GB of disk space for the app plus space for models.

### Getting started

Download the ZIP from [Releases](https://github.com/karabilo214/RAMVI/releases/latest), unzip it anywhere (a disk or a USB stick) and run `RAMVI.exe`. Models are not included: the app downloads the main model and the small draft model itself.

### Benchmarks

RTX 5060 Laptop (8 GB), 16 GB RAM, the same 30 mixed prompts, up to 200 tokens, temperature 0, measured on the same day as Ollama 0.40.13. Qwen3-14B Q4_K_M (larger than VRAM) with a Qwen3-0.6B draft model: RAMVI 8.17 tok/s, Ollama 6.17 tok/s (RAMVI was faster on 22 of 30 prompts). Qwen3-8B fully in VRAM: RAMVI 0.8.0 34.2, 0.9.0 56.6, Ollama 62.7 tok/s. Ollama gives the first token faster in both cases.

### Updating

Close RAMVI completely (tray → Exit), unzip the new version into a **new** folder, copy the `data` folder, `settings.json` (if present) and the `models` folder from the old RAMVI folder into the new one, start the new `RAMVI.exe` and delete the old folder once your chats are there. Models linked from the Ollama folder or elsewhere stay where they are. On Mac the data is inside the app: copy `Contents/Resources/data` and `settings.json` from the old `RAMVI.app` (Show Package Contents) into the new one. The built-in "install update from file" does not update the shell yet.

### Source code

Open under MIT at [github.com/karabilo214/AI](https://github.com/karabilo214/AI), in the `ramvi` folder. This repository holds release builds, docs and licenses.

### Licenses

RAMVI is [MIT](LICENSE)-licensed; third-party components keep their own terms. [LICENSES.md](LICENSES.md) links to every license text.
