# BluePill_Blink — проверенный базовый проект

[← Лабораторная работа №1](../README.md) | [↑ Карта курса](../../README.md) | [Главная](../../../README.md)

---

Этот каталог содержит **проверенный базовый проект Части А** лабораторной работы №1.

Конфигурация проекта:

```text
Board: Blue Pill
MCU: STM32F103C8T6
STM32CubeMX: 6.18.1
STM32CubeIDE: 2.2.0
STM32CubeF1: 1.8.0
Library: HAL
Programmer: ST-LINK V2
Interface: SWD
```

Проект проверен на реальном оборудовании.

## Что реализовано

```text
5 миганий
ON 300 мс
OFF 300 мс
↓
пауза 2000 мс
↓
повтор
```

Используется:

```c
HAL_GPIO_WritePin()
HAL_Delay()
for
while (1)
```

## Основные файлы

```text
BluePill_Blink.ioc
Core/
Drivers/
Startup/
STM32F103C8TX_FLASH.ld
```

Главный пользовательский файл:

```text
Core/Src/main.c
```

Конфигурация STM32CubeMX:

```text
BluePill_Blink.ioc
```

## Проверенные настройки

```text
SYS → Debug → Serial Wire
PA13 → SWDIO
PA14 → SWCLK
PC13 → GPIO_Output
User Label → LED
GPIO output level → High
```

Для генерации проекта используется локальный пакет:

```text
STM32Cube FW_F1 V1.8.0
```

## Проверенный результат

```text
Build: 0 errors, 0 warnings
Flash: Download verified successfully
Hardware test: PASS
```

## Как использовать этот каталог

Порядок выполнения лабораторной работы задаётся в:

➡️ **[course/01-blink/README.md](../README.md)**

Сначала требуется создать проект самостоятельно по инструкции. После этого данный каталог используется для сравнения конфигурации и исходного кода.

Индивидуальная часть лабораторной работы в готовом проекте **не реализована**. Она должна быть выполнена студентом самостоятельно с использованием `HAL_GPIO_TogglePin()` и назначенного варианта.


## Восстановление проекта из GitHub

GitHub-версия хранит конфигурацию `.ioc`, исходный код и необходимые драйверы. Служебные скрытые файлы Eclipse могут отсутствовать.

Если STM32CubeIDE не распознаёт каталог как готовый IDE-проект, выполните:

```text
BluePill_Blink.ioc
→ открыть в STM32CubeMX
→ проверить STM32Cube FW_F1 V1.8.0
→ GENERATE CODE
→ Open Project
```

После генерации CubeMX создаст необходимые служебные файлы IDE локально.

## Не добавлять в репозиторий

Результаты локальной сборки и служебные файлы рабочей области не должны версионироваться:

```text
Debug/
Release/
.metadata/
```

Они исключены правилами `.gitignore`.
