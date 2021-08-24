---
description: класс нтевентложевентконсумер записывает сообщение в журнал событий Windows, когда происходит указанное событие. Этот класс является стандартным потребителем событий, предоставляемым инструментарием WMI.
ms.assetid: ca998a91-d9f7-44ff-bb83-5ba92d68f31e
ms.tgt_platform: multiple
title: Ведение журнала событий NT на основе события
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c8c070b1a52fe41f32b8610ff0931d33be7feb33f9f5cd6f6067652e963f6824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050712"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a>Ведение журнала событий NT на основе события

класс [**нтевентложевентконсумер**](nteventlogeventconsumer.md) записывает сообщение в журнал событий Windows, когда происходит указанное событие. Этот класс является стандартным потребителем событий, предоставляемым инструментарием WMI.

> [!Note]  
> Пользователи, прошедшие проверку подлинности, по умолчанию не могут регистрировать события в журнале приложений на удаленном компьютере. В результате пример, описанный в этом разделе, завершится ошибкой, если вы используете свойство **унксервернаме** класса [**нтевентложевентконсумер**](nteventlogeventconsumer.md) и указали удаленный компьютер в качестве его значения. Чтобы узнать, как изменить безопасность журнала событий, ознакомьтесь с этой [статьей в базе знаний](https://support.microsoft.com/kb/323076).

 

Базовая процедура использования стандартного потребителя описана в разделе [мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md). Ниже приведены дополнительные шаги, которые выходят за пределы базовой процедуры, необходимые при использовании класса [**нтевентложевентконсумер**](nteventlogeventconsumer.md) . Шаги описывают создание объекта-получателя события, записывающего данные в журнал событий приложений.

В следующей процедуре описывается создание объекта-получателя события, записывающего данные в журнал событий NT.

**создание объекта-получателя события, записывающего данные в Windows журнал событий**

1.  В файле MOF-файл (MOF) создайте экземпляр [**нтевентложевентконсумер**](nteventlogeventconsumer.md) для получения событий, которые вы запрашиваете в запросе. Дополнительные сведения о написании MOF-кода см. в разделе [Разработка классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).
2.  Создайте и назовите экземпляр [**\_ \_ EventFilter**](--eventfilter.md), а затем создайте запрос для указания типа события, запускающего запись в журнал событий NT.

    Дополнительные сведения см. в разделе [запросы с помощью WQL](querying-with-wql.md).

3.  Создайте экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , чтобы связать фильтр с экземпляром [**нтевентложевентконсумер**](nteventlogeventconsumer.md).
4.  Скомпилируйте MOF-файл с помощью [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Пример

Пример в этом разделе находится в MOF-коде, но экземпляры можно создавать программно с помощью [API скриптов для WMI](scripting-api-for-wmi.md) или [COM API для WMI](com-api-for-wmi.md). В примере показано, как создать потребителя для записи в журнал событий приложения с помощью [**нтевентложевентконсумер**](nteventlogeventconsumer.md). MOF создает новый класс с именем «Нтлогконс \_ example», фильтр событий для запроса таких операций, как создание, на экземпляре этого нового класса и привязку между фильтром и потребителем. Поскольку последним действием в MOF является создание экземпляра Нтлогконс \_ , можно сразу же увидеть событие в журнале событий приложений, запустив Eventvwr.exe.

`EventID=0x0A for SourceName="WinMgmt"`Определяет сообщение со следующим текстом. "%1", "%2", "%3" — это местозаполнители для соответствующих строк, указанных в массиве Инсертионстрингтемплатес.

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

В следующей процедуре описывается использование примера.

**Использование примера**

1.  Скопируйте приведенный ниже список MOF в текстовый файл и сохраните его с расширением. mof.
2.  В командное окно Скомпилируйте MOF-файл с помощью следующей команды:

    **Mofcomp** *filename * * *. mof**

3.  Запустите Eventvwr.exe. Просмотрите журнал событий приложений. Должно отобразиться событие с ИДЕНТИФИКАТОРом 10 ( **EventID**), Source = "WMI" и Type = Error.
4.  Дважды щелкните сообщение **типа данных** из WMI с 10 в столбце **событий** . Для события будет отображаться следующее описание.

    ``` syntax
    Event filter with query "STRING2" could not be [re]activated in 
    namespace "STRING1" because of error STRING3. Events cannot be 
    delivered through this filter until the problem is corrected.
    ```

``` syntax
// Set the namespace as root\subscription.
// The NTEventLogEventConsumer is already
// compiled in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")
class NTLogCons_Example
{
 [key] string name;
 string InsertionString;
};

// Create an instance of the NT Event log consumer
// and give it the alias $CONSUMER

instance of NTEventLogEventConsumer as $CONSUMER
{
    // Unique instance name
    Name = "NTConsumerTest"; 
    // System component that generates the event
    SourceName = "WinMgmt";
    // Event message WBEM_MC_CANNOT_ACTIVATE_FILTER
    EventID = 0xC000000A;
    // EVENTLOG_ERROR_TYPE
    EventType = 1;
    // WMI event messages do not have multiple categories
    Category = 0;
    // Number of strings in InsertionStringTemplates property
    NumberOfInsertionStrings = 3;

    InsertionStringTemplates =
       {"%TargetInstance.Name%",
        "%TargetInstance.InsertionString%",
        "STRING3"};
};

// Create an instance of the event filter
// and give it the alias $FILTER
// The filter queries for any instance operation event
// for instances of the NTLogCons_Example class

instance of __EventFilter as $FILTER
{
    // Unique instance name
    Name = "NTLogConsFilter";
    Query = "SELECT * from __InstanceOperationEvent"
            " WHERE TargetInstance ISA \"NTLogCons_Example\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER;
    Filter = $FILTER;
};

// Create an instance of this class right now. 

instance of NTLogCons_Example
{
   Name = "STRING1";
   InsertionString = "STRING2";
};
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Мониторинг событий и реагирование на них с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



