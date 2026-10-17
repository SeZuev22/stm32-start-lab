# BluePill_Blink — проверенный базовый проект

[← Лабораторная работа №1](../README.md) | [↑ Карта курса](../../README.md) | [Главная](../../../README.md)

Каталог содержит проверенный проект, на котором подтверждён полный стартовый контур:

```text
STM32CubeMX
→ Build
→ ST-LINK
→ Flash
→ GPIO PC13
→ встроенный LED
```

Проект используется как **эталон конфигурации и диагностики стенда**, а не как готовое решение индивидуального задания.

## Конфигурация

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

## Реализованный проверочный алгоритм

В сохранённом `main.c` реализован базовый стендовый тест:

```text
5 миганий
ON 300 мс
OFF 300 мс
→ пауза 2000 мс
→ повтор
```

Используются:

```c
HAL_GPIO_WritePin()
HAL_Delay()
for
while (1)
```

Этот тест подтверждает корректность конфигурации GPIO, сборки, прошивки и аппаратного подключения.

## Что выполняется самостоятельно

В основной ЛР №1 студент отдельно выполняет:

- эксперимент с `HAL_GPIO_TogglePin()`;
- прикладной сигнал READY;
- индивидуальный диагностический сценарий;
- собственную проверку и защиту алгоритма.

Готовые решения индивидуальных сценариев в каталоге отсутствуют.

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

Исходники HAL GPIO:

```text
Drivers/STM32F1xx_HAL_Driver/Inc/stm32f1xx_hal_gpio.h
Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_gpio.c
```

## Проверенные настройки

```text
SYS → Debug → Serial Wire
PA13 → SWDIO
PA14 → SWCLK
PC13 → GPIO_Output
User Label → LED
GPIO output level → High
STM32Cube FW_F1 V1.8.0
```

## Проверенный результат

```text
Build: 0 errors, 0 warnings
Flash: Download verified successfully
Hardware test: PASS
```

## Как использовать проект

Сначала выполните **[ЛР №1](../README.md)** самостоятельно.

При неисправности проект можно использовать для сравнения:

- `.ioc`;
- `MX_GPIO_Init()`;
- структуры проекта;
- базового кода;
- HAL-драйверов.

Если STM32CubeIDE не распознаёт каталог как готовый проект:

```text
BluePill_Blink.ioc
→ открыть в STM32CubeMX
→ проверить STM32Cube FW_F1 V1.8.0
→ GENERATE CODE
→ Open Project
```

Локальные каталоги сборки и Workspace (`Debug/`, `Release/`, `.metadata/`) не должны добавляться в репозиторий.
