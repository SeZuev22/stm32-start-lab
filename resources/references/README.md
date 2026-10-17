# Учебные материалы и первоисточники

[← Ресурсы](../README.md) | [↑ Карта курса](../../course/README.md) | [ЛР №1 — Blink](../../course/01-blink/README.md)

---

# 1. Как пользоваться этим разделом

Этот раздел содержит дополнительные материалы для самостоятельного изучения STM32.

Основной принцип курса:

> Для выполнения лабораторных работ студенту достаточно материалов STM32 Start Lab.  
> Внешние источники используются для углубления, проверки понимания и самостоятельного развития.

Студент не обязан читать все приведённые книги, статьи и руководства до выполнения лабораторной работы.

Для каждой лабораторной работы в курсе указывается:

- какой материал необходимо знать обязательно;
- какой материал изучается непосредственно в лабораторной работе;
- какие внешние источники полезны для углубления;
- какие темы относятся к следующим лабораторным работам.

Если внешний источник использует другую плату, другую версию STM32CubeIDE или другой микроконтроллер, настройки текущего учебного стенда выполняются по STM32 Start Lab.

---

# 2. Уровни материалов

## Уровень 1 — обязательно

Основной источник:

```text
STM32 Start Lab
```

Студент выполняет лабораторные работы по GitHub-курсу.

## Уровень 2 — рекомендуется

Дополнительные статьи и учебные материалы, которые помогают понять использованные функции HAL и периферию STM32.

## Уровень 3 — углублённое изучение

Книги, большие учебные курсы и официальная техническая документация.

---

# 3. Материалы к лабораторной работе №1

Тема ЛР №1:

```text
GPIO Output
+
Blue Pill STM32F103C8T6
+
HAL
+
управление встроенным светодиодом
```

В рамках ЛР №1 необходимо понять:

```text
GPIO
PC13
active-low
MX_GPIO_Init()
GPIO_InitTypeDef
GPIO_MODE_OUTPUT_PP
GPIO_NOPULL
GPIO_SPEED_FREQ_LOW
HAL_GPIO_Init()
HAL_GPIO_WritePin()
HAL_GPIO_TogglePin()
HAL_Delay()
```

Функции чтения входа, внешние прерывания и таймеры рассматриваются только обзорно и будут изучаться в следующих лабораторных работах.

---

# 4. DeepBlue Embedded — GPIO Output, WritePin и TogglePin

Ссылка:

https://deepbluembedded.com/stm32-gpio-write-pin-digital-output-lab/

Этот материал особенно близок к первой лабораторной работе STM32 Start Lab.

Рассматриваются:

- Blue Pill;
- STM32 GPIO Output;
- STM32CubeMX;
- STM32CubeIDE;
- мигание светодиодом;
- HAL_GPIO_WritePin();
- HAL_GPIO_TogglePin().

## Когда использовать

Рекомендуется после выполнения базового Blink.

Не копируйте настройки механически, если они отличаются от текущего проекта STM32 Start Lab.

---

# 5. ControllersTech — STM32 HAL

Основной раздел:

https://controllerstech.com/stm32-hal/

Курс для начинающих:

https://controllerstech.com/stm32-beginner-course-learn-stm32-from-scratch/

Материалы содержат практические примеры по:

- GPIO;
- UART;
- ADC;
- таймерам;
- PWM;
- I2C;
- SPI;
- DMA;
- другим периферийным устройствам STM32.

После ЛР №1 достаточно познакомиться с GPIO. Остальные темы рекомендуется открывать по мере прохождения соответствующих лабораторных работ.

---

# 6. Digi-Key — Getting Started with STM32CubeIDE

Ссылка:

https://www.digikey.com/en/maker/projects/getting-started-with-stm32-introduction-to-stm32cubeide/6a6c60a670c447abb90fd0fd78008697

Материал полезен для общего понимания:

- STM32CubeIDE;
- Workspace;
- создания проектов;
- Build;
- Debug;
- работы со средой разработки.

Плата и версии программного обеспечения могут отличаться от STM32 Start Lab, поэтому этот материал не заменяет пошаговую инструкцию курса.

---

# 7. Mastering STM32 — Carmine Noviello

Книга:

```text
Mastering STM32 — Second Edition
Carmine Noviello
```

Ссылка:

https://leanpub.com/mastering-stm32-2nd

Книга рассматривает:

- STM32CubeIDE;
- CubeHAL;
- GPIO;
- NVIC;
- UART;
- DMA;
- Clock Tree;
- таймеры;
- ADC;
- DAC;
- I2C;
- SPI;
- память;
- загрузку STM32;
- FreeRTOS;
- отладку;
- разработку собственных плат.

Рекомендуемый уровень:

```text
углублённое изучение
```

Для выполнения ЛР №1 книга не требуется.

---

# 8. Discovering the STM32 Microcontroller — Geoffrey Brown

Книга:

```text
Discovering the STM32 Microcontroller
Geoffrey Brown
```

Ссылка:

https://legacy.cs.indiana.edu/~geobrown/book.pdf

Книга полезна для понимания:

- архитектуры микроконтроллера;
- периферии STM32F1;
- GPIO;
- таймеров;
- прерываний;
- внутреннего устройства STM32.

Книга старше современного STM32CubeIDE/HAL workflow, поэтому используется для понимания микроконтроллера, а не как пошаговая инструкция STM32 Start Lab.

Книга распространяется автором по лицензии:

```text
CC BY-NC-SA 3.0
```

---

# 9. Бесплатные курсы STMicroelectronics

## STM32CubeMX & CubeHAL basics

https://www.st.com/content/st_com/en/support/learning/stm32-moocs/stm32cubemx-and-cubeHhal-basics.html

Темы:

- STM32CubeMX;
- Pinout;
- Clock Tree;
- периферия;
- генерация кода;
- HAL;
- callbacks;
- interrupts;
- DMA;
- GPIO;
- SPI;
- UART;
- timers;
- ADC.

Практика курса ST может выполняться на другой плате. Конфигурация Blue Pill выполняется по STM32 Start Lab.

## STM32CubeIDE basics

https://www.st.com/content/st_com/en/support/learning/stm32-moocs/STM32CubeIDE_basics_MOOC.html

Полезен для углубления знаний по:

- STM32CubeIDE;
- HAL;
- GPIO;
- EXTI;
- PWM;
- ADC;
- DMA;
- USART;
- FreeRTOS.

---

# 10. Официальные технические документы

Оригинальные PDF официальных документов ST в публичном репозитории STM32 Start Lab не размещаются.

Студенту не требуется открывать их для обычного выполнения ЛР №1.

## DS5319 — STM32F103x8/xB Datasheet

Первоисточник по:

- характеристикам STM32F103C8T6;
- корпусу;
- выводам;
- памяти;
- электрическим характеристикам;
- альтернативным функциям выводов.

Для ЛР №1 особенно важны:

```text
STM32F103C8T6
PC13
PA13
PA14
```

## RM0008 — STM32F1 Reference Manual

Основной документ по внутреннему устройству STM32F1.

Содержит:

- RCC;
- GPIO;
- EXTI;
- DMA;
- ADC;
- timers;
- USART;
- SPI;
- I2C;
- CAN;
- USB;
- Flash;
- регистры периферии.

Для ЛР №1 полезны прежде всего:

```text
RCC
GPIO
```

## PM0056 — Cortex-M3 Programming Manual

Используется для углублённого изучения:

- регистров процессора;
- модели памяти;
- исключений;
- NVIC;
- архитектуры Cortex-M3.

## UM1850 — STM32F1 HAL/LL Driver Manual

Связан с библиотеками:

```text
HAL
LL
```

Для GPIO доступны, в частности:

```c
HAL_GPIO_Init()
HAL_GPIO_DeInit()
HAL_GPIO_ReadPin()
HAL_GPIO_WritePin()
HAL_GPIO_TogglePin()
HAL_GPIO_LockPin()
```

В ЛР №1 обязательны:

```c
HAL_GPIO_WritePin()
HAL_GPIO_TogglePin()
```

## AN2586 — STM32F10xxx Hardware Development

Полезен для понимания:

- питания;
- Reset;
- Boot;
- тактирования;
- отладки;
- аппаратной части STM32F10xxx.

## UM1075 — ST-LINK/V2

Первоисточник по:

- ST-LINK/V2;
- SWD;
- SWDIO;
- SWCLK;
- программированию;
- отладке.

---

# 11. Что изучать после ЛР №1

## Минимальный уровень

Перейти к следующей лабораторной работе после её публикации.

## Средний уровень

Дополнительно изучить:

- DeepBlue Embedded;
- GPIO-материалы ControllersTech;
- MX_GPIO_Init();
- исходные функции HAL GPIO.

## Продвинутый уровень

Изучать:

- Mastering STM32;
- Discovering the STM32 Microcontroller;
- ST MOOCs;
- Reference Manual;
- исходный код HAL;
- работу GPIO через регистры.

---

# 12. Что важнее: HAL или регистры

STM32 Start Lab начинает обучение с HAL.

Последовательность:

```text
понять назначение периферии
↓
создать работающий проект
↓
понять логику HAL
↓
увидеть исходный код HAL
↓
изучить регистры
↓
понять работу аппаратной периферии
```

HAL не отменяет необходимость понимать внутреннее устройство микроконтроллера.

---

# 13. Правило использования внешних материалов

Если внешний источник отличается от текущего проекта, для выполнения лабораторной работы приоритет имеет STM32 Start Lab.

Причины различий:

- другая модель STM32;
- другая плата;
- другая версия STM32CubeMX;
- другая версия STM32CubeIDE;
- другая версия HAL;
- иная схема подключения LED;
- active-high вместо active-low.

Внешние материалы используются для понимания принципов, а не для механического копирования.

---

# 14. Рекомендуемый маршрут самостоятельного изучения

```text
STM32 Start Lab — ЛР №1
↓
DeepBlue Embedded — GPIO Output
↓
ControllersTech — STM32 HAL
↓
следующие лабораторные работы
↓
Mastering STM32
↓
Reference Manual + HAL source code
```

---

# 15. Итог

Основным учебным ресурсом является:

```text
STM32 Start Lab
```

Внешние материалы:

1. дают альтернативное объяснение;
2. позволяют изучить тему глубже;
3. формируют навык самостоятельной работы с технической литературой.

Правильная последовательность:

```text
задача
↓
практический пример
↓
понимание API
↓
дополнительный материал
↓
официальный первоисточник
↓
углублённое изучение
```

---

# Навигация

[← Ресурсы](../README.md)

[↑ Карта курса](../../course/README.md)

➡️ **[Лабораторная работа №1 — GPIO Output: Blink](../../course/01-blink/README.md)**
