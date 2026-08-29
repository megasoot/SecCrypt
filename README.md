# SecCrypt

**SecCrypt** — плагин для [exteraGram](https://t.me/exteraReleases), предназначенный для защищённого шифрования и расшифровки текстовых сообщений и фотографий.

SecCrypt поддерживает несколько форматов шифрования и позволяет защищать как обычный текст, так и изображения с помощью парольной фразы.

## ✨ Возможности

- 🔐 Шифрование текстовых сообщений
- 🔓 Расшифровка защищённых сообщений
- 🖼️ Шифрование фотографий
- 🔓🖼️ Расшифровка зашифрованных фотографий
- 🛡️ Поддержка **SEC1 / SEC2 / SEC3**
- 🖼️ Поддержка **SECIMG3** для фотографий
- 🔎 Автоматическое определение формата защищённых данных
- 🔑 Защита с помощью парольной фразы
- 📦 Отправка зашифрованных фотографий в формате `.secimg`
- 📥 Загрузка зашифрованных файлов, полученных от других пользователей
- 💬 Отправка зашифрованных данных непосредственно из Telegram
- 📋 Копирование результата расшифровки
- 🌐 Русский и английский языки
- 🎨 Интерфейс в стиле **Material 3 Expressive**
- 📱 Оптимизация для мобильных устройств

---

# 🔒 Форматы шифрования

## SEC1

Режим совместимости со старыми сообщениями SecCrypt.

Предназначен для работы с сообщениями, созданными предыдущими версиями плагина.

## SEC2

Расширенный формат с проверкой целостности данных.

Позволяет обнаруживать изменение зашифрованного сообщения или повреждение его содержимого.

## SEC3

Современный формат SecCrypt с аутентифицированным шифрованием.

SEC3 использует **AES-256-GCM** для защиты данных и производный от парольной фразы ключ.

> Для новых текстовых сообщений рекомендуется использовать **SEC3**.

## SECIMG3

Формат SecCrypt для защищённых фотографий.

SECIMG3 используется для шифрования изображений перед их отправкой другому пользователю.

Зашифрованная фотография отправляется как файл `.secimg`. Получатель может загрузить файл и расшифровать его с помощью правильной парольной фразы.

SECIMG3 использует аутентифицированное шифрование **AES-GCM**.

---

# 📦 Установка

1. Установите [exteraGram](https://t.me/exteraReleases).
2. Перейдите в раздел **Releases** этого репозитория.
3. Скачайте последнюю версию SecCrypt.
4. Откройте файл `.plugin` через exteraGram.
5. Установите плагин.
6. Откройте настройки плагинов и убедитесь, что **SecCrypt** включён.

---

# 🚀 Использование

## 🔐 Шифрование текста

1. Откройте интерфейс SecCrypt с помощью команды:

   `.sec`

2. Выберите режим **Текст**.
3. Выберите формат:
   - `SEC1`
   - `SEC2`
   - `SEC3`
4. Укажите получателя.
5. Введите парольную фразу.
6. Введите сообщение.
7. Нажмите кнопку шифрования и отправки.

Получатель сможет расшифровать сообщение только при наличии правильной парольной фразы.

---

## 🖼️ Шифрование фотографии

1. Откройте SecCrypt с помощью:

   `.sec`

2. Выберите режим **Фото**.
3. Выберите фотографию.
4. Укажите получателя.
5. Введите парольную фразу.
6. Нажмите кнопку шифрования и отправки.

SecCrypt создаст зашифрованный файл **SECIMG3** с расширением `.secimg` и отправит его в чат.

---

## 🔓 Расшифровка текста

1. Ответьте на защищённое сообщение командой:

   `.unlock`

2. Введите парольную фразу.
3. Нажмите **«Расшифровать»**.
4. После успешной расшифровки содержимое сообщения будет отображено в интерфейсе.

Формат защищённого сообщения определяется автоматически, когда это возможно.

---

## 🖼️ Расшифровка фотографии

1. Получите зашифрованный файл `.secimg`.
2. Ответьте на сообщение командой:

   `.unlock`

3. Введите парольную фразу.
4. SecCrypt при необходимости загрузит зашифрованный файл.
5. После успешной расшифровки исходная фотография будет восстановлена и открыта.

Это работает и с фотографиями, зашифрованными **другими пользователями SecCrypt**.

---

# 🌐 Языки

SecCrypt поддерживает два языка интерфейса:

- 🇷🇺 **Русский**
- 🇬🇧 **English**

Язык можно изменить в настройках плагина.

---

# 🛡️ Безопасность

SecCrypt предназначен для защиты содержимого сообщений и фотографий от прочтения без соответствующей парольной фразы.

SEC3 и SECIMG3 используют аутентифицированное шифрование, позволяющее обнаруживать изменение или повреждение зашифрованных данных.

**Важно:** безопасность защищённых данных напрямую зависит от качества используемой парольной фразы.

Не рекомендуется использовать простые пароли:

- `123456`
- `password`
- `qwerty`
- имя пользователя
- дату рождения
- другие легко угадываемые значения

Для важных данных используйте длинные и уникальные парольные фразы.

**Не отправляйте парольную фразу вместе с зашифрованным сообщением или фотографией.**

---

# 📱 Совместимость

| Возможность | Поддержка |
|---|---|
| exteraGram | ✅ |
| Android | ✅ |
| SEC1 | ✅ |
| SEC2 | ✅ |
| SEC3 | ✅ |
| SECIMG3 | ✅ |
| Текст | ✅ |
| Фотографии | ✅ |
| Русский | ✅ |
| English | ✅ |

---

# 📥 Скачать

## Последняя стабильная версия

**SecCrypt v2.9.0**

Скачать `.plugin` можно в разделе **Releases → Assets**.

[Перейти к последнему релизу](../../releases/latest)

---

# 🐛 Ошибки и предложения

Если вы нашли ошибку или хотите предложить улучшение, создайте **Issue** в этом репозитории.

При сообщении об ошибке желательно указать:

- версию SecCrypt;
- версию exteraGram;
- используемый формат (`SEC1 / SEC2 / SEC3 / SECIMG3`);
- тип данных (текст или фотография);
- описание проблемы;
- шаги для воспроизведения.

**Не публикуйте пароли, личные данные или содержимое приватных зашифрованных сообщений и фотографий.**

---

# 🔄 Changelog

## v2.9.0

### ✨ Новое

- Добавлено шифрование фотографий.
- Добавлен формат **SECIMG3**.
- Добавлена отправка фотографий в формате `.secimg`.
- Добавлена расшифровка зашифрованных фотографий.
- Добавлена поддержка расшифровки фотографий, полученных от других пользователей.
- Добавлена автоматическая загрузка удалённых `.secimg` перед расшифровкой.
- Добавлен английский язык.
- Улучшен интерфейс выбора фотографий.
- Обновлён интерфейс Material 3 Expressive.

### 🔧 Исправления

- Исправлена работа с длинными парольными фразами.
- Исправлена загрузка зашифрованных фотографий от других пользователей.
- Улучшена обработка удалённых `.secimg`.
- Исправлено появление клавиатуры после успешной расшифровки.
- Улучшена обработка неправильных паролей.
- Улучшена обработка повреждённых зашифрованных данных.
- Исправлены различные проблемы локализации.

## v2.8.1

- Обновлён интерфейс SecCrypt.
- Улучшена работа с SEC1, SEC2 и SEC3.
- Улучшена обработка расшифровки.
- Улучшено отображение результата расшифровки.
- Улучшена автоматическая обработка форматов защищённых сообщений.
- Обновлён Material 3 Expressive интерфейс.

---

# 👤 Автор

**megasoot**

SecCrypt разработан как плагин для exteraGram.

---

# 📄 Лицензия

Распространяется в соответствии с лицензией, указанной в файле [`LICENSE`](LICENSE).

---

# 🇬🇧 English

**SecCrypt** is a plugin for [exteraGram](https://t.me/exteraReleases) designed for secure encryption and decryption of text messages and photos.

SecCrypt supports multiple encryption formats and allows users to protect both text and images using a password phrase.

## ✨ Features

- 🔐 Text message encryption
- 🔓 Encrypted message decryption
- 🖼️ Photo encryption
- 🔓🖼️ Encrypted photo decryption
- 🛡️ **SEC1 / SEC2 / SEC3** support
- 🖼️ **SECIMG3** support for photos
- 🔎 Automatic encrypted format detection
- 🔑 Password phrase protection
- 📦 Encrypted photo sharing using `.secimg`
- 📥 Automatic downloading of encrypted files received from other users
- 💬 Direct encrypted message sending through Telegram
- 📋 Copy decrypted content
- 🌐 Russian and English interfaces
- 🎨 **Material 3 Expressive** interface
- 📱 Optimized for mobile devices

---

# 🔒 Encryption Formats

## SEC1

Compatibility mode for older SecCrypt messages.

It is intended for working with messages created by previous versions of the plugin.

## SEC2

An extended format with integrity verification.

It can detect modified or corrupted encrypted messages.

## SEC3

SecCrypt's modern authenticated-encryption format.

SEC3 uses **AES-256-GCM** to protect data and derives the encryption key from the password phrase.

> **SEC3 is recommended for new text messages.**

## SECIMG3

SecCrypt's format for encrypted photos.

SECIMG3 is used to encrypt images before sending them to another user.

Encrypted photos are sent as `.secimg` files. The recipient can download and decrypt the file using the correct password phrase.

SECIMG3 uses authenticated **AES-GCM** encryption.

---

# 📦 Installation

1. Install [exteraGram](https://t.me/exteraReleases).
2. Open the **Releases** section of this repository.
3. Download the latest SecCrypt version.
4. Open the `.plugin` file using exteraGram.
5. Install the plugin.
6. Open the plugin settings and make sure **SecCrypt** is enabled.

---

# 🚀 Usage

## 🔐 Encrypting text

1. Open SecCrypt using:

   `.sec`

2. Select **Text** mode.
3. Select an encryption format:
   - `SEC1`
   - `SEC2`
   - `SEC3`
4. Specify the recipient.
5. Enter a password phrase.
6. Enter your message.
7. Press the encryption and send button.

The recipient will only be able to decrypt the message with the correct password phrase.

---

## 🖼️ Encrypting a photo

1. Open SecCrypt using:

   `.sec`

2. Select **Photo** mode.
3. Select a photo.
4. Specify the recipient.
5. Enter a password phrase.
6. Press the encryption and send button.

SecCrypt will create an encrypted **SECIMG3** file with the `.secimg` extension and send it to the chat.

---

## 🔓 Decrypting text

1. Reply to an encrypted message using:

   `.unlock`

2. Enter the password phrase.
3. Press **Decrypt**.
4. After successful decryption, the message content will be displayed.

The encrypted format is detected automatically whenever possible.

---

## 🖼️ Decrypting a photo

1. Receive an encrypted `.secimg` file.
2. Reply to the message using:

   `.unlock`

3. Enter the password phrase.
4. SecCrypt will download the encrypted file if necessary.
5. After successful decryption, the original photo will be restored and opened.

This also works with photos encrypted by **other SecCrypt users**.

---

# 🌐 Languages

SecCrypt supports two interface languages:

- 🇷🇺 **Russian**
- 🇬🇧 **English**

The interface language can be changed in the plugin settings.

---

# 🛡️ Security

SecCrypt is designed to protect message and photo contents from being read without the corresponding password phrase.

SEC3 and SECIMG3 use authenticated encryption, allowing modified or corrupted encrypted data to be detected.

**Important:** the security of encrypted data depends directly on the quality of the password phrase.

Avoid simple passwords such as:

- `123456`
- `password`
- `qwerty`
- usernames
- birth dates
- other easily guessable values

For important data, use long and unique password phrases.

**Do not send the password phrase together with the encrypted message or photo.**

---

# 📱 Compatibility

| Feature | Support |
|---|---|
| exteraGram | ✅ |
| Android | ✅ |
| SEC1 | ✅ |
| SEC2 | ✅ |
| SEC3 | ✅ |
| SECIMG3 | ✅ |
| Text | ✅ |
| Photos | ✅ |
| Russian | ✅ |
| English | ✅ |

---

# 📥 Download

## Latest stable version

**SecCrypt v2.9.0**

The `.plugin` file is available under **Releases → Assets**.

[Go to the latest release](../../releases/latest)

---

# 🐛 Issues and Suggestions

If you find a bug or have an improvement suggestion, create an **Issue** in this repository.

When reporting a bug, please include:

- SecCrypt version;
- exteraGram version;
- encryption format (`SEC1 / SEC2 / SEC3 / SECIMG3`);
- data type (text or photo);
- description of the problem;
- reproduction steps.

**Do not publish passwords, personal information, or private encrypted messages and photos.**

---

# 🔄 Changelog

## v2.9.0

### ✨ Added

- Added photo encryption.
- Added **SECIMG3** format.
- Added encrypted photo sharing using `.secimg`.
- Added encrypted photo decryption.
- Added support for decrypting photos received from other users.
- Added automatic downloading of remote `.secimg` files before decryption.
- Added English language support.
- Improved the photo selection interface.
- Updated the Material 3 Expressive interface.

### 🔧 Fixed

- Fixed long password phrase handling.
- Fixed downloading encrypted photos received from other users.
- Improved handling of remote `.secimg` files.
- Fixed the keyboard appearing after successful decryption.
- Improved incorrect-password handling.
- Improved handling of corrupted encrypted data.
- Fixed various localization issues.

## v2.8.1

- Updated the SecCrypt interface.
- Improved SEC1, SEC2 and SEC3 support.
- Improved decryption handling.
- Improved decrypted content display.
- Improved automatic encrypted-format handling.
- Updated the Material 3 Expressive interface.

---

# 👤 Author

**megasoot**

SecCrypt is developed as a plugin for exteraGram.

---

# 📄 License

Distributed under the license specified in the [`LICENSE`](LICENSE) file.