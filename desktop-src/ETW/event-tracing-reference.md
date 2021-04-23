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
# <a name="event-tracing-reference"></a><span data-ttu-id="deca8-103">Справочник по трассировке событий</span><span class="sxs-lookup"><span data-stu-id="deca8-103">Event Tracing Reference</span></span>

<span data-ttu-id="deca8-104">Для написания приложений, включающих трассировку событий, используются следующие элементы программирования:</span><span class="sxs-lookup"><span data-stu-id="deca8-104">You use the following programming elements to write applications that incorporate event tracing:</span></span>

-   [<span data-ttu-id="deca8-105">Перечисления трассировки событий</span><span class="sxs-lookup"><span data-stu-id="deca8-105">Event Tracing Enumerations</span></span>](/windows/desktop/api/_etw/#enumerations)
-   [<span data-ttu-id="deca8-106">Функции трассировки событий</span><span class="sxs-lookup"><span data-stu-id="deca8-106">Event Tracing Functions</span></span>](/windows/desktop/api/_etw/#functions)
-   [<span data-ttu-id="deca8-107">Интерфейсы трассировки событий</span><span class="sxs-lookup"><span data-stu-id="deca8-107">Event Tracing Interfaces</span></span>](/windows/desktop/api/_etw/#interfaces)
-   [<span data-ttu-id="deca8-108">Структуры трассировки событий</span><span class="sxs-lookup"><span data-stu-id="deca8-108">Event Tracing Structures</span></span>](/windows/desktop/api/_etw/#structures)
-   [<span data-ttu-id="deca8-109">Константы трассировки событий</span><span class="sxs-lookup"><span data-stu-id="deca8-109">Event Tracing Constants</span></span>](event-tracing-constants.md)

<span data-ttu-id="deca8-110">Дополнительные сведения о примерах, использующих эти элементы программирования, см. в разделе [примеры трассировки событий](event-tracing-samples.md).</span><span class="sxs-lookup"><span data-stu-id="deca8-110">For details on samples that use these programming elements, see [Event Tracing Samples](event-tracing-samples.md).</span></span>

<span data-ttu-id="deca8-111">В этом разделе также содержатся сведения о:</span><span class="sxs-lookup"><span data-stu-id="deca8-111">This section also contains information on:</span></span>

-   <span data-ttu-id="deca8-112">[Средства](event-tracing-tools.md) , ПРЕДОСТАВЛЯЕМые ETW</span><span class="sxs-lookup"><span data-stu-id="deca8-112">[Tools](event-tracing-tools.md) that ETW provides</span></span>
-   <span data-ttu-id="deca8-113">[Определения классов MOF](event-tracing-mof-classes.md) для событий ядра</span><span class="sxs-lookup"><span data-stu-id="deca8-113">[MOF class definitions](event-tracing-mof-classes.md) for kernel events</span></span>
-   <span data-ttu-id="deca8-114">[Квалификаторы классов MOF](event-tracing-mof-qualifiers.md) , используемые при определении классов событий</span><span class="sxs-lookup"><span data-stu-id="deca8-114">[MOF class qualifiers](event-tracing-mof-qualifiers.md) used when defining your event classes</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="deca8-115">Обработка трассировок трассировки событий Windows в коде .NET</span><span class="sxs-lookup"><span data-stu-id="deca8-115">Process ETW traces in .NET code</span></span>

<span data-ttu-id="deca8-116">Вы также можете использовать [API .NET трацепроцессинг](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) для анализа трассировок трассировки событий Windows для приложений и других программных компонентов.</span><span class="sxs-lookup"><span data-stu-id="deca8-116">You can also use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="deca8-117">Этот API внутренне используется в корпорации Майкрософт для анализа данных ETW, созданных в системе разработки Windows, а также для включения нескольких таблиц в [анализаторе производительности Windows](/windows-hardware/test/wpt/windows-performance-analyzer).</span><span class="sxs-lookup"><span data-stu-id="deca8-117">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="deca8-118">Этот API доступен в виде пакета NuGet.</span><span class="sxs-lookup"><span data-stu-id="deca8-118">This API is available as a NuGet package.</span></span>

<span data-ttu-id="deca8-119">Дополнительные сведения см. в [этой статье](/windows/apps/trace-processing/overview).</span><span class="sxs-lookup"><span data-stu-id="deca8-119">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>
