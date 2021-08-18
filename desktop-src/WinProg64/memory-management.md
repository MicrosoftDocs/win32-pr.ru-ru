---
title: Управление памятью в эмуляторе WOW64
description: Управление памятью в эмуляторе WOW64 зависит от архитектуры процессора.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64-bit Windows программирование, управление памятью
- управление памятью 64-разрядное Windowsное программирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9908c8127f4fbe15b636d7d72fd19d2d8057c1d0a0c126393bc6c182e46925f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132837"
---
# <a name="memory-management-under-wow64"></a>Управление памятью в эмуляторе WOW64

Управление памятью в эмуляторе WOW64 зависит от архитектуры процессора.

## <a name="itanium-support"></a>Поддержка Itanium

WOW64 имитирует 4 КБ страниц поверх собственных 8 КБ страниц, используемых процессором Itanium. Это помогает процессору, обеспечивая отличное моделирование с низкими издержками. Код моделирования не может работать в следующих случаях:

-   Отслеживание записи. Функции [**жетвритеватч**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) и [**ресетвритеватч**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) реализуются в ядре с использованием собственной гранулярности размера страницы, что означает, что имитация страницы WOW64 4 КБ не может определить, какие из них будут записаны на странице размером 8 КБ.
-   [Расширения AWE](/windows/desktop/Memory/address-windowing-extensions). Функции AWE работают с номерами страниц, и не существует способа сопоставлять 64-разрядные номера страниц с номерами страниц 32-бит.
-   Выравнивание раздела. Для исполняемых образов с выравниванием разделов менее 8 КБ (значение по умолчанию — 4 КБ для образов x86), WOW64 должен быть грязным для всех страниц изображений. Это эффективно копирует каждую страницу в файл подкачки и предотвращает совместное применение страниц изображений только для чтения между процессами.
-   Функции [**реадфилескаттер**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) и [**вритефилегасер**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) не поддерживаются.

## <a name="x64-and-arm64-support"></a>Поддержка x64 и ARM64

Собственный размер страницы — 4 КБ. Таким образом, поддерживаются следующие действия.

-   Поддерживаются функции [**жетвритеватч**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) и [**ресетвритеватч**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) .
-   Поддерживаются функции [**реадфилескаттер**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) и [**вритефилегасер**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .
-   Использование больших адресов имеет свои преимущества, так как x64 WOW64 поддерживает виртуальное адресное пространство размером 4 ГБ.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[ограничения памяти для выпусков Windows](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[Настройка ОЗУ 4GT](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 