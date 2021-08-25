---
title: Windows Справочник по журналам событий
description: Ниже приведены элементы программирования, которые используются для создания манифеста инструментирования, создания ресурсов из манифеста, используемого поставщиком, получения метаданных инструментирования во время выполнения и запроса событий из каналов и файлов журналов.
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ce52f3756b8f33ac710e189677de053dc538339d0a0cdeb335410dd76a171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957794"
---
# <a name="windows-event-log-reference"></a>Windows Справочник по журналам событий

Ниже приведены элементы программирования, используемые для создания манифеста инструментирования, создания ресурсов из манифеста, используемого поставщиком, получения метаданных инструментирования во время выполнения и запроса событий из каналов и файлов журналов.

-   [Схема Евентманифест](eventmanifestschema-schema.md)
-   [Схема событий](eventschema-schema.md)
-   [Схема запроса](queryschema-schema.md)
-   [Windows Константы журнала событий](windows-event-log-constants.md)
-   [Windows Типы данных журнала событий](windows-event-log-data-types.md)
-   [Windows Перечисления журнала событий](windows-event-log-enumerations.md)
-   [Windows Функции журнала событий](windows-event-log-functions.md)
-   [Windows Структуры журнала событий](windows-event-log-structures.md)
-   [Windows Средства журнала событий](windows-event-log-tools.md)

для приложений, написанных с использованием языка .net, например C# или Visual Basic, см. следующие пространства имен:

-   Для записи событий используйте классы и методы, определенные в пространстве имен [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .
-   чтобы использовать события из Windows канала журнала событий или журнала, используйте классы и методы, определенные в пространстве имен [System. Diagnostics. eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .

В качестве альтернативы использованию пространства имен [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) для записи событий можно использовать аргумент **-CS** или **-CSS** , чтобы компилятор сообщений создавал код для записи событий. Дополнительные сведения см. в разделе [**компилятор сообщений**](message-compiler--mc-exe-.md).
