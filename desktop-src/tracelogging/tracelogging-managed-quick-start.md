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
# <a name="tracelogging-managed-quick-start"></a>Управляемый Быстрое начало Трацелоггинг

В следующем разделе описаны основные шаги, необходимые для добавления Трацелоггинг в управляемый код.

## <a name="prerequisites"></a>Предварительные условия

-   Windows 10

### <a name="simpletraceloggingexamplecs"></a>Симплетрацелоггинжексампле. CS

В этом примере показано, как вести журнал событий Трацелоггинг без необходимости вручную создавать отдельный XML-файл манифеста инструментирования.


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



### <a name="create-the-eventsource"></a>Создание EventSource

Прежде чем можно будет регистрировать события, необходимо создать экземпляр класса EventSource. Первый параметр конструктора определяет имя этого поставщика. Поставщик регистрируется автоматически, как показано в примере.


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



Экземпляр является статическим, поскольку за раз в приложении должен быть только один экземпляр конкретного поставщика.

### <a name="log-tracelogging-events"></a>Регистрация событий Трацелоггинг

После создания поставщика в следующем примере кода из приведенного выше журнала создается простое событие.


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a>Запись данных структурированных событий в журнал

Можно определить структурированные полезные данные, регистрируемые с помощью события. Предоставьте структурированные полезные данные либо как анонимный тип, либо как экземпляр класса, помеченный `[EventData]` атрибутом, как показано в следующем примере.


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



Необходимо добавить `[EventData]` атрибут в классы полезных данных события, которые вы определяете, как показано ниже.


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



Атрибут заменяет необходимость вручную создавать файл манифеста для описания данных события. Теперь все, что нужно сделать, — передать экземпляр класса в метод EventSource. Write (), чтобы зарегистрировать событие и соответствующие полезные данные.

## <a name="summary-and-next-steps"></a>Сводка и дальнейшие действия

Сведения о записи и просмотре данных Трацелоггинг с помощью последних внутренних версий средств обеспечения производительности Windows (WPT) см. в разделе [запись и отображение событий трацелоггинг](tracelogging-record-and-display-tracelogging-events.md) .

Дополнительные примеры для управляемых Трацелоггинг см. в разделе [примеры .NET трацелоггинг](tracelogging-net-examples.md) .

 

 




