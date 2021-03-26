---
description: Список элементов, используемых для трассировки событий.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Справочник по трассировке событий
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 7e0ee4576b9b9d64a5766c6ab096ea34abc2b176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985948"
---
# <a name="event-tracing-reference"></a>Справочник по трассировке событий

Для написания приложений, включающих трассировку событий, используются следующие элементы программирования:

-   [Перечисления трассировки событий](/windows/desktop/api/_etw/#enumerations)
-   [Функции трассировки событий](/windows/desktop/api/_etw/#functions)
-   [Интерфейсы трассировки событий](/windows/desktop/api/_etw/#interfaces)
-   [Структуры трассировки событий](/windows/desktop/api/_etw/#structures)
-   [Константы трассировки событий](event-tracing-constants.md)

Дополнительные сведения о примерах, использующих эти элементы программирования, см. в разделе [примеры трассировки событий](event-tracing-samples.md).

В этом разделе также содержатся сведения о:

-   [Средства](event-tracing-tools.md) , ПРЕДОСТАВЛЯЕМые ETW
-   [Определения классов MOF](event-tracing-mof-classes.md) для событий ядра
-   [Квалификаторы классов MOF](event-tracing-mof-qualifiers.md) , используемые при определении классов событий

## <a name="process-etw-traces-in-net-code"></a>Обработка трассировок трассировки событий Windows в коде .NET

Вы также можете использовать [API .NET трацепроцессинг](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) для анализа трассировок трассировки событий Windows для приложений и других программных компонентов. Этот API внутренне используется в корпорации Майкрософт для анализа данных ETW, созданных в системе разработки Windows, а также для включения нескольких таблиц в [анализаторе производительности Windows](/windows-hardware/test/wpt/windows-performance-analyzer). Этот API доступен в виде пакета NuGet.

Дополнительные сведения см. в [этой статье](/windows/apps/trace-processing/overview).
