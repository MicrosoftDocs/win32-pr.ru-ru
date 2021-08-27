---
description: Список элементов, используемых для трассировки событий.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Справочник по трассировке событий
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 20aaf59de3419b4015f03b38db69839b6f258ccd561b1e918694396e875ae5a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083284"
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

Вы также можете использовать [API .NET трацепроцессинг](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) для анализа трассировок трассировки событий Windows для приложений и других программных компонентов. этот API внутренне используется в корпорации майкрософт для анализа данных ETW, созданных Windows инженерной системе, а также для включения нескольких таблиц в [Windows анализаторе производительности](/windows-hardware/test/wpt/windows-performance-analyzer). этот API доступен в виде пакета NuGet.

Дополнительные сведения см. в [этой статье](/windows/apps/trace-processing/overview).
