---
title: Управляемый Быстрое начало Трацелоггинг
description: В следующем разделе описаны основные шаги, необходимые для добавления Трацелоггинг в управляемый код.
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7108dfc094f3183950dd94e5398263f4bf7cfd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329576"
---
# <a name="tracelogging-managed-quick-start"></a><span data-ttu-id="7f54a-103">Управляемый Быстрое начало Трацелоггинг</span><span class="sxs-lookup"><span data-stu-id="7f54a-103">TraceLogging Managed Quick Start</span></span>

<span data-ttu-id="7f54a-104">В следующем разделе описаны основные шаги, необходимые для добавления Трацелоггинг в управляемый код.</span><span class="sxs-lookup"><span data-stu-id="7f54a-104">The following section describes the basic steps required to add TraceLogging to managed code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7f54a-105">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7f54a-105">Prerequisites</span></span>

-   <span data-ttu-id="7f54a-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="7f54a-106">Windows 10</span></span>

### <a name="simpletraceloggingexamplecs"></a><span data-ttu-id="7f54a-107">Симплетрацелоггинжексампле. CS</span><span class="sxs-lookup"><span data-stu-id="7f54a-107">SimpleTraceLoggingExample.cs</span></span>

<span data-ttu-id="7f54a-108">В этом примере показано, как вести журнал событий Трацелоггинг без необходимости вручную создавать отдельный XML-файл манифеста инструментирования.</span><span class="sxs-lookup"><span data-stu-id="7f54a-108">This example demonstrates how to log Tracelogging events without the need to manually create a separate instrumentation manifest XML file.</span></span>


```CSharp
using System;
using System.Diagnostics.Tracing;

namespace SimpleTraceLoggingExample
{
    class Program
    {
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
        static void Main(string[] args)
        {
            log.Write("Event 1"); // write an event with no fields
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
        }
    }

    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
}
```



### <a name="create-the-eventsource"></a><span data-ttu-id="7f54a-109">Создание EventSource</span><span class="sxs-lookup"><span data-stu-id="7f54a-109">Create the EventSource</span></span>

<span data-ttu-id="7f54a-110">Прежде чем можно будет регистрировать события, необходимо создать экземпляр класса EventSource.</span><span class="sxs-lookup"><span data-stu-id="7f54a-110">Before you can log events you must create an instance of the EventSource class.</span></span> <span data-ttu-id="7f54a-111">Первый параметр конструктора определяет имя этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="7f54a-111">The first constructor parameter identifies the name of this provider.</span></span> <span data-ttu-id="7f54a-112">Поставщик регистрируется автоматически, как показано в примере.</span><span class="sxs-lookup"><span data-stu-id="7f54a-112">The provider is automatically registered for you as illustrated in the example.</span></span>


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



<span data-ttu-id="7f54a-113">Экземпляр является статическим, поскольку за раз в приложении должен быть только один экземпляр конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="7f54a-113">The instance is static because there should only be one instance of a specific provider in your application at a time.</span></span>

### <a name="log-tracelogging-events"></a><span data-ttu-id="7f54a-114">Регистрация событий Трацелоггинг</span><span class="sxs-lookup"><span data-stu-id="7f54a-114">Log Tracelogging events</span></span>

<span data-ttu-id="7f54a-115">После создания поставщика в следующем примере кода из приведенного выше журнала создается простое событие.</span><span class="sxs-lookup"><span data-stu-id="7f54a-115">After the provider is created, the following code from the example above logs a simple event.</span></span>


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a><span data-ttu-id="7f54a-116">Запись данных структурированных событий в журнал</span><span class="sxs-lookup"><span data-stu-id="7f54a-116">Log structured event payload data</span></span>

<span data-ttu-id="7f54a-117">Можно определить структурированные полезные данные, регистрируемые с помощью события.</span><span class="sxs-lookup"><span data-stu-id="7f54a-117">You can define structured payload data that is logged with the event.</span></span> <span data-ttu-id="7f54a-118">Предоставьте структурированные полезные данные либо как анонимный тип, либо как экземпляр класса, помеченный `[EventData]` атрибутом, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="7f54a-118">Provide structured payload data either as an anonymous type or as an instance of a class that has been annotated with the `[EventData]` attribute as shown in the following example.</span></span>


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



<span data-ttu-id="7f54a-119">Необходимо добавить `[EventData]` атрибут в классы полезных данных события, которые вы определяете, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7f54a-119">You must add the `[EventData]` attribute to event payload classes that you define as shown below.</span></span>


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



<span data-ttu-id="7f54a-120">Атрибут заменяет необходимость вручную создавать файл манифеста для описания данных события.</span><span class="sxs-lookup"><span data-stu-id="7f54a-120">The attribute replaces the need to manually create a manifest file to describe the event data.</span></span> <span data-ttu-id="7f54a-121">Теперь все, что нужно сделать, — передать экземпляр класса в метод EventSource. Write (), чтобы зарегистрировать событие и соответствующие полезные данные.</span><span class="sxs-lookup"><span data-stu-id="7f54a-121">Now all you have to do is pass an instance of the class to the EventSource.Write() method to log the event and corresponding payload data.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="7f54a-122">Сводка и дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="7f54a-122">Summary and next steps</span></span>

<span data-ttu-id="7f54a-123">Сведения о записи и просмотре данных Трацелоггинг с помощью последних внутренних версий средств обеспечения производительности Windows (WPT) см. в разделе [запись и отображение событий трацелоггинг](tracelogging-record-and-display-tracelogging-events.md) .</span><span class="sxs-lookup"><span data-stu-id="7f54a-123">See [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md) for information about how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT).</span></span>

<span data-ttu-id="7f54a-124">Дополнительные примеры для управляемых Трацелоггинг см. в разделе [примеры .NET трацелоггинг](tracelogging-net-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="7f54a-124">See [.NET Tracelogging Examples](tracelogging-net-examples.md) for more managed TraceLogging examples.</span></span>

 

 




