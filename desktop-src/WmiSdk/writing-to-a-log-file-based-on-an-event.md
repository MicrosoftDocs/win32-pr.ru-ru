---
description: Класс Логфиливентконсумер может записывать предопределенный текст в файл журнала при наступлении указанного события. Этот класс является стандартным потребителем событий, предоставляемым инструментарием WMI.
ms.assetid: c337e9f7-f40c-4d7d-a180-c053e24c882b
ms.tgt_platform: multiple
title: Запись в файл журнала на основе события
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33cc82925b6afc1690f2cd87607f21e9ea02fdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263916"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a>Запись в файл журнала на основе события

Класс [**логфиливентконсумер**](logfileeventconsumer.md) может записывать предопределенный текст в файл журнала при наступлении указанного события. Этот класс является стандартным потребителем событий, предоставляемым инструментарием WMI.

Базовая процедура использования стандартных потребителей всегда одинакова и находится в [мониторинге и реагировании на события со стандартными потребителями](monitoring-and-responding-to-events-with-standard-consumers.md).

Следующая процедура добавляет в основную процедуру, относящуюся к классу [**логфиливентконсумер**](logfileeventconsumer.md) , и описывает создание объекта-получателя события, запускающего программу.

**Создание объекта-получателя события, записывающего данные в файл журнала**

1.  В файле MOF-файл (MOF) создайте экземпляр [**логфиливентконсумер**](logfileeventconsumer.md) для получения событий, которые вы запрашиваете в запросе, присвойте имя экземпляру в свойстве **Name** , а затем поместите путь к файлу журнала в свойстве **filename** .

    Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).

2.  Укажите текстовый шаблон для записи в файл журнала в свойстве Text.

    Дополнительные сведения см. [в разделе Использование стандартных строковых шаблонов](using-standard-string-templates.md).

3.  Создайте экземпляр [**\_ \_ EventFilter**](--eventfilter.md) и определите запрос для указания событий, которые будут активировать потребитель.

    Дополнительные сведения см. [в разделе запросы с помощью WQL](querying-with-wql.md).

4.  Создайте экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , чтобы связать фильтр с экземпляром [**логфиливентконсумер**](logfileeventconsumer.md).
5.  Чтобы контролировать, кто читает файл журнала или выполняет запись в него, задайте уровень безопасности для каталога, в котором находится журнал, на требуемом уровне.
6.  Скомпилируйте MOF-файл с помощью [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Пример

Пример в этом разделе находится в MOF-коде, но экземпляры можно создавать программно с помощью [API скриптов для WMI](scripting-api-for-wmi.md) или [COM API для WMI](com-api-for-wmi.md). В примере используется стандартный Логфиливентконсумер для создания класса-получателя с именем Логфиливент, который записывает строку в файл c: \\ файл_журнала. log при создании экземпляра класса логфиливент.

В следующей процедуре описывается использование примера.

**Использование примера**

1.  Скопируйте приведенный ниже список MOF в текстовый файл и сохраните его с расширением. mof.
2.  В окне командной строки Скомпилируйте MOF-файл с помощью следующей команды.

    **Mofcomp** *filename * * *. mof**

3.  Откройте файл файл_журнала. log, чтобы увидеть строку, указанную параметром LogFileEvent.Name: "событие файла-получателя события.

``` syntax
// Set the namespace as root\subscription.
// The LogFileEventConsumer is already compiled 
//     in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")

class LogFileEvent
{
    [key]string Name;
};

// Create an instance of the standard log
// file consumer and give it the alias $CONSUMER

instance of LogFileEventConsumer as $CONSUMER
{
    // If the file does not already exist, it is created.
    Filename = "c:\\Logfile.log";  
    IsUnicode = FALSE;
    // Name of this instance of LogFileEventConsumer
    Name = "LogfileEventConsumer_Example";  
    // See "Using Standard String Templates"; 
    Text = "%TargetInstance.Name%"; 
    // TargetInstance is the instance of LogFileEvent 
    //    requested in the filter        
                                         
};

// Create an instance of the event filter 
// and give it the alias $FILTER
// Query for any instance operation type,
// such as instance creation, for LogFileEvent class

instance of __EventFilter as $FILTER
{
    Name = "LogFileFilter";
    Query = "SELECT * FROM __InstanceOperationEvent "
        "WHERE TargetInstance.__class = \"LogFileEvent\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding.

instance of __FilterToConsumerBinding
{
    Consumer=$CONSUMER;
    Filter=$FILTER;
 DeliverSynchronously=FALSE;
};

// Create an instance of this class right now
// Look at the file c:\Logfile.log to see
// that a line has been written.

instance of LogFileEvent
{
 Name = "Logfile Event Consumer event";  
};
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Мониторинг событий и реагирование на них с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



