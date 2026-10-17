# Учебные материалы и первоисточники

[← Ресурсы](../README.md) | [↑ Учебный курс](../../course/README.md) | [ЛР №1](../../course/01-blink/README.md)

## Принцип отбора

В этот список включаются материалы, которые на момент проверки доступны из открытого веба без платной подписки и полезны для обучения STM32, HAL или STM32CubeIDE.

Материалы из сомнительных файловых обменников и неофициальные копии коммерческих книг не используются.

Доступность внешнего сайта со временем может измениться, поэтому основной маршрут курса должен оставаться выполнимым непосредственно по STM32 Start Lab.

Последняя проверка списка: **17.10.2026**.

## Как пользоваться литературой

```text
STM32 Start Lab
↓
дополнительное объяснение
↓
университетское пособие / открытый tutorial
↓
официальная документация
↓
исходный код HAL
```

Для выполнения ЛР №1 не требуется заранее читать все источники.

## Русскоязычные материалы

### 1. Университет ИТМО — «Программирование STM32 на HAL. Часть 1»

Власов С. М., Жданов В. А., Маргун А. А. и др. Лабораторный практикум, 2025.

Официальный открытый PDF Университета ИТМО:

https://books.ifmo.ru/file/pdf/3382.pdf

Материал рекомендован в ИТМО для бакалаврских программ по направлениям «Мехатроника и робототехника» и «Управление в технических системах».

Использовать как дополнительный академический практикум по HAL. Аппаратная платформа и конкретные задания могут отличаться от STM32 Start Lab.

### 2. Университет ИТМО — «Программирование STM32 на HAL. Часть 2»

Власов С. М., Жданов В. А., Маргун А. А. и др. Лабораторный практикум, 2026.

Официальный открытый PDF Университета ИТМО:

https://books.ifmo.ru/file/pdf/3466.pdf

В пособии рассматривается программирование STM32 в STM32CubeIDE. Используется STM32F446RE, поэтому конкретные настройки выводов нельзя механически переносить на Blue Pill; полезны методика, структура работ и применение HAL.

### 3. MicroTechnics — быстрый старт с STM32CubeMX

https://microtechnics.ru/stm32cube-sozdanie-proekta/

Свободно доступная русскоязычная статья о создании проекта, структуре сгенерированного кода и работе STM32CubeMX/HAL.

Материал старше текущих версий STM32CubeMX, поэтому интерфейс может отличаться, но базовая логика остаётся полезной.

## Зарубежные открытые материалы

### 4. Discovering the STM32 Microcontroller — Geoffrey Brown

Открытый университетский учебник по STM32F1:

https://legacy.cs.indiana.edu/~geobrown/book.pdf

Лицензия книги:

```text
CC BY-NC-SA 3.0
```

Книга полезна для понимания архитектуры STM32F1, GPIO, таймеров, прерываний и периферии. Она предшествует современному STM32CubeIDE/HAL workflow, поэтому используется для фундаментального понимания, а не как пошаговая инструкция текущего курса.

### 5. DeepBlue Embedded — STM32 GPIO Output

https://deepbluembedded.com/stm32-gpio-write-pin-digital-output-lab/

Особенно полезно к ЛР №1:

- STM32F103C8T6 / Blue Pill;
- GPIO Output;
- STM32CubeMX;
- `HAL_GPIO_WritePin()`;
- `HAL_GPIO_TogglePin()`;
- `HAL_Delay()`.

Внешний пример использует собственную конфигурацию тактирования и другой вывод LED, поэтому настройки проекта STM32 Start Lab имеют приоритет.

### 6. ControllersTech — STM32 HAL Programming Tutorials

https://controllerstech.com/stm32-hal/

Открытая серия практических материалов по:

- GPIO;
- UART;
- таймерам;
- ADC;
- PWM;
- I2C;
- SPI;
- DMA;
- другим периферийным блокам.

Ресурс особенно полезен по мере развития курса после первой лабораторной работы.

### 7. DigiKey — Getting Started with STM32CubeIDE

https://www.digikey.com/en/maker/projects/getting-started-with-stm32-introduction-to-stm32cubeide/6a6c60a670c447abb90fd0fd78008697

Бесплатный материал по рабочему процессу STM32CubeIDE, сборке, прошивке и отладке. Используется другая плата, поэтому ресурс является дополнительным, а не заменой STM32 Start Lab.

### 8. STMicroelectronics — STM32CubeMX & CubeHAL basics MOOC

https://www.st.com/content/st_com/en/support/learning/stm32-moocs/stm32cubemx-and-cubeHhal-basics.html

Официальный бесплатный курс по STM32CubeMX и HAL. Полезен для углубления в конфигурацию периферии, HAL, callbacks, interrupts, DMA, GPIO, SPI, UART, timers и ADC.

### 9. STMicroelectronics — STM32CubeIDE basics MOOC

https://www.st.com/content/st_com/en/support/learning/stm32-moocs/STM32CubeIDE_basics_MOOC.html

Официальный курс по STM32CubeIDE с HAL/LL-примерами, GPIO, EXTI, PWM, ADC, DMA, USART и FreeRTOS.

## Официальные технические первоисточники

Оригинальные PDF ST не зеркалируются в этом репозитории. Они доступны бесплатно на официальном сайте ST и используются для проверки технических деталей.

Основная страница документации STM32F1:

https://www.st.com/en/microcontrollers-microprocessors/stm32f1-series/documentation.html

Для текущего трека особенно важны:

| Документ | Для чего используется |
|---|---|
| DS5319 | характеристики STM32F103x8/xB, выводы, память, электрические параметры |
| RM0008 | RCC, GPIO, EXTI, таймеры, ADC, интерфейсы и регистры STM32F1 |
| PM0056 | архитектура Cortex-M3, исключения, NVIC, модель памяти |
| UM1850 | HAL/LL API STM32F1 |
| AN2586 | аппаратная разработка на STM32F10xxx |
| UM1075 | ST-LINK/V2 и интерфейсы программирования/отладки |

Прямой официальный PDF UM1850:

https://www.st.com/resource/en/user_manual/dm00154093-description-of-stm32f1-hal-and-ll-drivers-stmicroelectronics.pdf

Прямой официальный PDF RM0008:

https://www.st.com/resource/en/reference_manual/cd00171190-stm32f101-103-105-107-stm32f100-series-armbased-32bit-mcus-stmicroelectronics.pdf

Прямой официальный PDF UM1075:

https://www.st.com/resource/en/user_manual/dm00026748-stlinkv2-incircuit-debuggerprogrammer-for-stm8-and-stm32-stmicroelectronics.pdf

## Локальный исходный код HAL

Для изучения HAL студенту не обязательно уходить во внешний источник: исходный код используемого драйвера входит в проверенный проект.

GPIO API:

**[`stm32f1xx_hal_gpio.h`](../../course/01-blink/project/Drivers/STM32F1xx_HAL_Driver/Inc/stm32f1xx_hal_gpio.h)**

Реализация функций:

**[`stm32f1xx_hal_gpio.c`](../../course/01-blink/project/Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_gpio.c)**

Для ЛР №1 полезно найти реализации:

```c
HAL_GPIO_Init()
HAL_GPIO_ReadPin()
HAL_GPIO_WritePin()
HAL_GPIO_TogglePin()
HAL_GPIO_LockPin()
```

Это прямой переход от использования API к пониманию того, что делает библиотека.

## Рекомендуемый маршрут после ЛР №1

```text
ЛР №1 STM32 Start Lab
↓
ИТМО: Программирование STM32 на HAL
↓
DeepBlue Embedded / ControllersTech
↓
Discovering the STM32 Microcontroller
↓
RM0008 + UM1850
↓
исходный код HAL
```

## Правило при расхождении материалов

Внешний источник может использовать другую плату, другую версию STM32CubeMX/IDE, другой вывод LED или другое семейство STM32.

Для выполнения конкретной лабораторной работы приоритет имеет проверенная конфигурация STM32 Start Lab. Внешние материалы используются для понимания принципов и расширения кругозора, а не для механического копирования настроек.
