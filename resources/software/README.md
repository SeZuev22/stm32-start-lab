# Программное обеспечение STM32 Start Lab

[← Resources](../README.md) | [↑ На главную](../../README.md)

---

Текущий проверенный программный стек:

```text
Windows 10 x64
STM32CubeMX 6.18.1
STM32CubeIDE 2.2.0
STM32CubeF1 v1.8.0
```

Большие установочные файлы размещаются в GitHub Release:

➡️ **[STM32 Start Lab v0.2 — практико-ориентированный курс (Windows / Blue Pill)](https://github.com/SeZuev22/stm32-start-lab/releases/tag/v0.2)**

## Обязательные файлы

```text
SetupSTM32CubeMX-6.18.1-Win-x86_64.zip
stm32cubeide_2.2.0-Win-x86_64.exe.zip
stm32cubef1.zip
```

### STM32CubeMX 6.18.1

Используется для выбора MCU, настройки выводов и периферии, управления MCU Package и генерации проекта.

### STM32CubeIDE 2.2.0

Используется для редактирования кода, Build, прошивки через ST-LINK и отладки.

При установке оставляется включённым компонент `ST-LINK drivers`, поэтому отдельный пакет драйвера в текущий Release не входит.

### STM32CubeF1 v1.8.0

Локальный MCU Package для STM32F103C8T6. Устанавливается через:

```text
STM32CubeMX
→ INSTALL / REMOVE
→ From Local...
```

Архив `stm32cubef1.zip` перед установкой не распаковывается.

## Что не входит в текущий Release

```text
STM32CubeProgrammer
отдельный STSW-LINK009
STM32CubeF4
Black Pill
Linux-пакеты
```

Эти компоненты не требуются для текущего учебного маршрута и не должны отвлекать начинающего студента.

## Служебные файлы

- [VERSIONS.txt](VERSIONS.txt) — проверенные версии и статус проверки;
- [SHA256SUMS.txt](checksums/SHA256SUMS.txt) — контрольные суммы основных Release assets.

## Основная инструкция

➡️ **[00 — Подготовка рабочего места](../../course/00-getting-started/README.md)**
