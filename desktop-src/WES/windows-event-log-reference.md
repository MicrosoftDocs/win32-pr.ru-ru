---
title: Справочник по журналам событий Windows
description: Ниже приведены элементы программирования, которые используются для создания манифеста инструментирования, создания ресурсов из манифеста, используемого поставщиком, получения метаданных инструментирования во время выполнения и запроса событий из каналов и файлов журналов.
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072381"
---
# <a name="windows-event-log-reference"></a>Справочник по журналам событий Windows

Ниже приведены элементы программирования, используемые для создания манифеста инструментирования, создания ресурсов из манифеста, используемого поставщиком, получения метаданных инструментирования во время выполнения и запроса событий из каналов и файлов журналов.

-   [Схема Евентманифест](eventmanifestschema-schema.md)
-   [Схема событий](eventschema-schema.md)
-   [Схема запроса](queryschema-schema.md)
-   [Константы журнала событий Windows](windows-event-log-constants.md)
-   [Типы данных журнала событий Windows](windows-event-log-data-types.md)
-   [Перечисления журнала событий Windows](windows-event-log-enumerations.md)
-   [Функции журнала событий Windows](windows-event-log-functions.md)
-   [Структуры журнала событий Windows](windows-event-log-structures.md)
-   [Средства журнала событий Windows](windows-event-log-tools.md)

Для приложений, написанных с использованием языка .NET, например C# или Visual Basic, см. следующие пространства имен:

-   Для записи событий используйте классы и методы, определенные в пространстве имен [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .
-   Чтобы использовать события из канала или журнала событий Windows, используйте классы и методы, определенные в пространстве имен [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .

В качестве альтернативы использованию пространства имен [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) для записи событий можно использовать аргумент **-CS** или **-CSS** , чтобы компилятор сообщений создавал код для записи событий. Дополнительные сведения см. в разделе [**компилятор сообщений**](message-compiler--mc-exe-.md).
