---
description: Инструментарий WMI поддерживает различные модели потоков в зависимости от того, как размещается поставщик, и от типа функций поставщика, таких как класс или свойство.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Выбор правильной регистрации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712118"
---
# <a name="choosing-correct-registration"></a>Выбор правильной регистрации

Инструментарий WMI поддерживает различные модели потоков в зависимости от того, как размещается поставщик, и от типа функций поставщика, таких как [класс](writing-a-class-provider.md) или [свойство](writing-a-property-provider.md). Например, у [*несвязанных поставщиков*](gloss-d.md) не поддерживаются все типы функций поставщика. Дополнительные сведения о различных моделях размещения и их настройке см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).

## <a name="in-process-providers"></a>Поставщики In-Process

Внутрипроцессный поставщик выполняется в общем хост-процессе Wmiprvse.exe. Большинство типов внутрипроцессного поставщика используют модель многопотокового подразделения (MTA).

Модель MTA поддерживается для следующих типов функций поставщика:

-   [Поставщик класса](writing-a-class-provider.md)
-   [Поставщик экземпляров](writing-an-instance-provider.md)
-   [Поставщик метода](writing-a-method-provider.md)
-   [Поставщик свойств](writing-a-property-provider.md)
-   [Поставщик событий](writing-an-event-provider.md)
-   [Поставщик потребителей событий](writing-an-event-consumer-provider.md)

Модель с одним потоком подразделений (STA) поддерживается для некоторых типов функций поставщика:

-   [Поставщик экземпляров](writing-an-instance-provider.md)
-   [Поставщик метода](writing-a-method-provider.md)
-   [Поставщик событий](writing-an-event-provider.md)
-   [Поставщик потребителей событий](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a>Поставщики вне процесса

Поставщики, размещенные на разных узлах общих служб, поддерживают следующие функции поставщика:

-   [Поставщик класса](writing-a-class-provider.md)
-   [Поставщик экземпляров](writing-an-instance-provider.md)
-   [Поставщик метода](writing-a-method-provider.md)
-   [Поставщик свойств](writing-a-property-provider.md)
-   [Поставщик событий](writing-an-event-provider.md)
-   [Поставщик потребителей событий](writing-an-event-consumer-provider.md)

Дополнительные сведения об узлах общих служб см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).

## <a name="decoupled-providers"></a>Несвязанные поставщики

Отделенные поставщики размещаются в приложении. Дополнительные сведения см. [в разделе Включение поставщика в приложение](incorporating-a-provider-in-an-application.md). Поставщики, созданные с помощью WMI в платформа .NET Framework, отделены от. Несвязанные Поставщики поддерживают следующие функции поставщика:

-   [Поставщик экземпляров](writing-an-instance-provider.md)
-   [Поставщик метода](writing-a-method-provider.md)
-   [Поставщик событий](writing-an-event-provider.md)
-   [Поставщик потребителей событий](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Разработка поставщика WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Размещение и безопасность поставщика](provider-hosting-and-security.md)
</dt> </dl>

 

 



