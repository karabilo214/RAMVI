<div align="center">

# RAMVI

**RAMVI — ваша персональная AI-платформа для Windows.**

Без обязательного облака. Без подписки. Без телеметрии. Ваш ИИ — под вашим контролем.

[**⬇ Скачать последнюю версию**](https://github.com/karabilo214/RAMVI/releases/latest) · [Лицензии](LICENSES.md) · [Сообщить об ошибке](https://github.com/karabilo214/RAMVI/issues) · [English](#english)

</div>

---

## Как это выглядит

| Чат с моделью: видно, как она рассуждает | Агент ждёт вашего решения по правке (diff) |
|---|---|
| ![Чат](docs/screenshots/chat.png) | ![Агент](docs/screenshots/agent.png) |

| Первый запуск: мастер проверяет компьютер | Голосовой ввод: запись по кнопке или Ctrl+M |
|---|---|
| ![Первый запуск](docs/screenshots/first-run.png) | ![Голос](docs/screenshots/voice.png) |

<sub>Первый запуск и агент — снимки настоящих окон на Windows: первый запуск снят в чистой Windows Sandbox без сети и без установленных библиотек, агент — на ноутбуке с RTX 5060 (модель qwen3-8b). Чат и голос — тот же интерфейс, отрисованный автотестами оболочки с тестовым текстом.</sub>

## Что умеет

- 💬 **Чат с языковой моделью**: Qwen3 и другие поддерживаемые модели в формате GGUF. Видно, как модель рассуждает. Если модель больше видеопамяти, часть слоёв работает из оперативной памяти.
- 🎙 **Голосовой ввод**: русский, английский, украинский. Распознавание работает на этом компьютере, микрофон включается только по кнопке или Ctrl+M.
- 🛠 **Агент для файлов**: читает, ищет и правит файлы только в той папке, которую вы выбрали. Каждое изменение показывается как diff, и применяется только после вашего подтверждения.
- 🔌 **API для своих программ**: совместим с OpenAI, Anthropic и Ollama, по умолчанию доступен только на этом компьютере. Ключи для каждого клиента отдельные, счётчики токенов тоже.
- 📴 **Работает без интернета** после того, как модель скачана.
- 🔒 **Приватность**: телеметрии нет. В сеть приложение ходит только по вашему действию: каталог моделей, загрузка модели, проверка обновлений.
- 🧳 **Переносимое**: установка не нужна, запускается из любой папки и с флешки.

## Требования

| | |
|---|---|
| Система | Windows 10 или 11, 64-бит |
| Видеокарта | **NVIDIA** (GeForce RTX и подобные) |
| Драйвер | **NVIDIA с поддержкой CUDA 13.2 или новее**: [скачать драйвер GeForce](https://www.nvidia.com/drivers) |
| RAM | ≥ 16 ГБ |
| SSD / HDD / NVMe | ≥ 3,3 ГБ |

Если драйвера нет или он старый, RAMVI при запуске скажет, что установить.

## Скорость: замеры, а не обещание

Ноутбук с RTX 5060 Laptop (8 ГБ видеопамяти) и 16 ГБ RAM, Windows 11.

| Случай | RAMVI | Ollama | Кто быстрее |
|---|---:|---:|---|
| **Модель больше видеопамяти:** Qwen3-14B Q4_K_M (9,3 ГБ) с моделью-предсказателем Qwen3-0.6B. Часть слоёв в видеопамяти, остальное в RAM | **8,7–9,1** ток/с | 6,27 ток/с | RAMVI, ≈1,4× |
| **Модель целиком в видеопамяти:** Qwen3-8B Q4_K_M | 32,8 ток/с | **52,2** ток/с | Ollama, ≈1,6× |

Как мерили 14B: 30 вопросов разных типов (факты, код, математика, перевод, творчество и др.), до 200 токенов на ответ, температура 0, контекст 2048, размышления выключены, по два прогона; тексты ответов между прогонами совпали 30/30. Для Ollama взят более ранний замер на том же наборе и том же ноутбуке; на текущей версии Ollama его не повторяли.

Честно об ограничениях:
- Выигрыш зависит от типа текста: на коде, математике и JSON он больше, а на творческих запросах RAMVI с 14B даёт 3,5–5,3 ток/с — предсказатель хуже угадывает такой текст.
- Когда модель целиком помещается в видеопамять, Ollama сейчас быстрее. Причина известна: в этом случае предсказатель мешает (без него RAMVI даёт на 8B 39–42 ток/с).

## Установка и первый запуск

1. Скачайте `RAMVI-<версия>-win-x64.zip` со страницы [Releases](https://github.com/karabilo214/RAMVI/releases/latest).
2. Распакуйте в любое место: на диск или на флешку. RAMVI запускается прямо оттуда, установка не нужна, флешку можно подключать к другому компьютеру.
3. Запустите **`RAMVI.exe`**.
4. Мастер проверит компьютер и предложит модель. **Модели в архив не входят**: основную модель и маленькую модель-предсказатель (ускоряет ответы) приложение скачивает само из каталога. Можно и подключить уже скачанный файл GGUF или модели Ollama.

Настройки и история хранятся рядом с приложением, в папке `data`. Если папка открыта только на чтение, RAMVI предложит выбрать другую.

## Обновления

Обновления подписаны ключом выпуска (Ed25519). Неподписанный или изменённый пакет не установится. Если новая версия не запустится, RAMVI сам вернётся к прежней. Чаты, модели и настройки обновление не трогает.

## Исходный код

Исходный код RAMVI открыт по лицензии MIT: [github.com/karabilo214/AI](https://github.com/karabilo214/AI), папка [ramvi](https://github.com/karabilo214/AI/tree/main/ramvi) — сервис, движок, оболочка, тесты и отчёты проверок. В этом репозитории — готовые сборки, описание и лицензии.

## Состав и лицензии

Код RAMVI распространяется по лицензии [MIT](LICENSE). В архив входят сторонние компоненты: Python, PyTorch с библиотеками NVIDIA CUDA и cuDNN, Triton, Transformers, whisper.cpp, .NET и Avalonia и другие. У каждого свои условия. **Полный список со ссылками на все тексты — [LICENSES.md](LICENSES.md)**, сами тексты — в папке [`licenses/`](licenses/) (та же папка есть внутри архива). Библиотеки NVIDIA и Microsoft можно использовать только в составе RAMVI, подробнее — [THIRD_PARTY_TERMS.txt](licenses/THIRD_PARTY_TERMS.txt).

Проверить целостность скачанного архива можно по SHA-256, он указан в описании каждого релиза:

```powershell
Get-FileHash .\RAMVI-0.8.0-win-x64.zip -Algorithm SHA256
```

---

<a id="english"></a>

## English

**RAMVI is your personal AI platform for Windows.** No mandatory cloud. No subscription. No telemetry. Your AI, under your control.

- Chat with Qwen3 and other supported GGUF models, including models larger than your GPU memory (hybrid GPU+RAM).
- Local voice input (Russian, English, Ukrainian); the microphone turns on only when you press the button or Ctrl+M.
- File agent restricted to a folder you choose. Every change is shown as a diff and needs your approval.
- OpenAI-, Anthropic- and Ollama-compatible API for your own tools, local-only by default, with a separate key per client.
- Works offline once a model is downloaded. Portable: no installation, runs from any folder or a USB stick.

**Requirements:** Windows 10/11 x64, an **NVIDIA GPU** with a driver that supports **CUDA 13.2 or newer** ([GeForce drivers](https://www.nvidia.com/drivers)), RAM ≥ 16 GB, SSD/HDD/NVMe ≥ 3.3 GB.

**Getting started:** download the ZIP from [Releases](https://github.com/karabilo214/RAMVI/releases/latest), unzip it anywhere (a disk or a USB stick) and run `RAMVI.exe`. No models are included: the app downloads the model and the small draft model itself.

**Speed (measured, not promised):** on an RTX 5060 Laptop (8 GB) with 16 GB RAM, Qwen3-14B Q4_K_M (larger than VRAM) with a Qwen3-0.6B draft model runs at 8.7–9.1 tok/s in RAMVI vs 6.27 in Ollama (30 mixed prompts, ≤200 tokens, temperature 0). With Qwen3-8B fully in VRAM, Ollama is faster today: 52.2 vs 32.8 tok/s.

**Source code:** open under MIT at [github.com/karabilo214/AI](https://github.com/karabilo214/AI) (folder `ramvi`); this repository holds release builds, docs and licenses.

**Licenses:** RAMVI is [MIT](LICENSE)-licensed; third-party components keep their own terms. See [LICENSES.md](LICENSES.md) for links to every license text.
