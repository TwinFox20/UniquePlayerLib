# EN:

**UniquePlayerLib** is a helper library mod for [tModLoader](https://github.com/tModLoader/tModLoader) that assigns each player a unique, persistent `GUID` (Globally Unique Identifier), synced between client and server. It allows mod developers to reliably identify players across sessions, regardless of their `whoAmI` value.

## ✨ Features
- Assigns a unique `GUID` to each player
- Automatically saves/loads the `GUID` on the client
- Syncs the `GUID` with the server when the player joins
- Prevents clients from faking `GUID`s
- Removes the `GUID` when a player leaves
- Easy-to-use `API` for getting and checking `GUID`s

## 📦 Installation

### From Mod Browser
1. Open the Mod Browser in tModLoader
2. Search for **UniquePlayerLib**
3. Install the mod

### As a dependency
Add to your `build.txt`:
```txt
ModReferences = UniquePlayerLib
```

## 🧠 Why use this?
In Terraria, the player's `whoAmI` can change between sessions. If your mod needs to store persistent data tied to a player — such as chest access, quests, zones, housing, or any other per-player logic — you need a reliable identifier. And **UniquePlayerLib** gives you that.

## 📁 Structure
- **UniqueSystem** — server-side static `API`
- **UniquePlayer** — handles save, load and create `GUID`
- **PlayerIDLib** — `IL` code patching & packet handling

---

# RU:

**UniquePlayerLib** — это вспомогательный мод-библиотека для [tModLoader](https://github.com/tModLoader/tModLoader), которая позволяет каждому игроку иметь постоянный уникальный `GUID`, синхронизируемый между клиентом и сервером. Она предназначена для модов, которым нужно сохранять и привязывать данные к конкретным игрокам — независимо от их сетевого идентификатора (`whoAmI`).

## ✨ Возможности
- Назначает каждому игроку уникальный `GUID`
- Сохраняет и загружает `GUID`
- Синхронизирует `GUID` с сервером при входе
- Обеспечивает защиту от подделки `GUID` со стороны клиента
- Удаляет `GUID`, когда игрок выходит с сервера
- Простой `API` для получения и проверки `GUID`

## 📦 Установка

### Через tModLoader
1. Откройте браузер модов в игре
2. Найдите **UniquePlayerLib**
3. Установите мод

### Для использования в других модах
В `build.txt` добавьте:
```txt
ModReferences = UniquePlayerLib
```

## 🧠 Зачем это нужно?
В Terraria значение `whoAmI` может меняться от сессии к сессии. Если моду нужно хранить персональные данные игрока (доступ к сундукам, квесты, зоны и т.д.), важно использовать постоянный идентификатор. **UniquePlayerLib** решает эту задачу, предоставляя безопасный и стабильный способ идентификации игроков.

## 📁 Структура
- **UniqueSystem** — статичный `API` на стороне сервера
- **UniquePlayer** — обеспечивает сохранение, загрузку и создаине `GUID`
- **PlayerIDLib** — изменение `IL` кода и обработка пакетов
