---
description: Класс Нтевентложевентконсумер записывает сообщение в журнал событий Windows при наступлении указанного события. Этот класс является стандартным потребителем событий, предоставляемым инструментарием WMI.
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
ms.openlocfilehash: 69bf24c0d64c95a012b8681b88bde34dc28fa179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911491"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a><span data-ttu-id="21393-104">Ведение журнала событий NT на основе события</span><span class="sxs-lookup"><span data-stu-id="21393-104">Logging to NT Event Log Based on an Event</span></span>

<span data-ttu-id="21393-105">Класс [**нтевентложевентконсумер**](nteventlogeventconsumer.md) записывает сообщение в журнал событий Windows при наступлении указанного события.</span><span class="sxs-lookup"><span data-stu-id="21393-105">The [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class writes a message to the Windows Event log when a specified event occurs.</span></span> <span data-ttu-id="21393-106">Этот класс является стандартным потребителем событий, предоставляемым инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="21393-106">This class is a standard event consumer that WMI provides.</span></span>

> [!Note]  
> <span data-ttu-id="21393-107">Пользователи, прошедшие проверку подлинности, по умолчанию не могут регистрировать события в журнале приложений на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="21393-107">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="21393-108">В результате пример, описанный в этом разделе, завершится ошибкой, если вы используете свойство **унксервернаме** класса [**нтевентложевентконсумер**](nteventlogeventconsumer.md) и указали удаленный компьютер в качестве его значения.</span><span class="sxs-lookup"><span data-stu-id="21393-108">As a result, the example described in this topic will fail if you use the **UNCServerName** property of the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class and specify a remote computer as its value.</span></span> <span data-ttu-id="21393-109">Чтобы узнать, как изменить безопасность журнала событий, ознакомьтесь с этой [статьей в базе знаний](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="21393-109">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

 

<span data-ttu-id="21393-110">Базовая процедура использования стандартного потребителя описана в разделе [мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="21393-110">The basic procedure for using a standard consumer is described in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="21393-111">Ниже приведены дополнительные шаги, которые выходят за пределы базовой процедуры, необходимые при использовании класса [**нтевентложевентконсумер**](nteventlogeventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="21393-111">The following are additional steps beyond the basic procedure, required when using the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class.</span></span> <span data-ttu-id="21393-112">Шаги описывают создание объекта-получателя события, записывающего данные в журнал событий приложений.</span><span class="sxs-lookup"><span data-stu-id="21393-112">The steps describe how to create an event consumer that writes to the Application event log.</span></span>

<span data-ttu-id="21393-113">В следующей процедуре описывается создание объекта-получателя события, записывающего данные в журнал событий NT.</span><span class="sxs-lookup"><span data-stu-id="21393-113">The following procedure describes how to create an event consumer that writes to the NT Event Log.</span></span>

<span data-ttu-id="21393-114">**Создание объекта-получателя события, записывающего данные в журнал событий Windows**</span><span class="sxs-lookup"><span data-stu-id="21393-114">**To create an event consumer that writes to the Windows Event Log**</span></span>

1.  <span data-ttu-id="21393-115">В файле MOF-файл (MOF) создайте экземпляр [**нтевентложевентконсумер**](nteventlogeventconsumer.md) для получения событий, которые вы запрашиваете в запросе.</span><span class="sxs-lookup"><span data-stu-id="21393-115">In a Managed Object Format (MOF) file, create an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="21393-116">Дополнительные сведения о написании MOF-кода см. в разделе [Разработка классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="21393-116">For more information about writing MOF code, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="21393-117">Создайте и назовите экземпляр [**\_ \_ EventFilter**](--eventfilter.md), а затем создайте запрос для указания типа события, запускающего запись в журнал событий NT.</span><span class="sxs-lookup"><span data-stu-id="21393-117">Create, and name, an instance of [**\_\_EventFilter**](--eventfilter.md), and then create a query to specify the type of event which triggers writing to the NT Event Log.</span></span>

    <span data-ttu-id="21393-118">Дополнительные сведения см. в разделе [запросы с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="21393-118">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

3.  <span data-ttu-id="21393-119">Создайте экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , чтобы связать фильтр с экземпляром [**нтевентложевентконсумер**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="21393-119">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span>
4.  <span data-ttu-id="21393-120">Скомпилируйте MOF-файл с помощью [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="21393-120">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="21393-121">Пример</span><span class="sxs-lookup"><span data-stu-id="21393-121">Example</span></span>

<span data-ttu-id="21393-122">Пример в этом разделе находится в MOF-коде, но экземпляры можно создавать программно с помощью [API скриптов для WMI](scripting-api-for-wmi.md) или [COM API для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="21393-122">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="21393-123">В примере показано, как создать потребителя для записи в журнал событий приложения с помощью [**нтевентложевентконсумер**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="21393-123">The example shows how to create a consumer to write to the Application event log by using [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="21393-124">MOF создает новый класс с именем «Нтлогконс \_ example», фильтр событий для запроса таких операций, как создание, на экземпляре этого нового класса и привязку между фильтром и потребителем.</span><span class="sxs-lookup"><span data-stu-id="21393-124">The MOF creates a new class named "NTLogCons\_Example", an event filter to query for operations, such as creation, on an instance of this new class, and a binding between filter and consumer.</span></span> <span data-ttu-id="21393-125">Поскольку последним действием в MOF является создание экземпляра Нтлогконс \_ , можно сразу же увидеть событие в журнале событий приложений, запустив Eventvwr.exe.</span><span class="sxs-lookup"><span data-stu-id="21393-125">Because the last action in the MOF is to create an instance of NTLogCons\_Example, you can immediately see the event in the Application event log by running Eventvwr.exe.</span></span>

<span data-ttu-id="21393-126">`EventID=0x0A for SourceName="WinMgmt"`Определяет сообщение со следующим текстом.</span><span class="sxs-lookup"><span data-stu-id="21393-126">The `EventID=0x0A for SourceName="WinMgmt"` identifies a message with the following text.</span></span> <span data-ttu-id="21393-127">"%1", "%2", "%3" — это местозаполнители для соответствующих строк, указанных в массиве Инсертионстрингтемплатес.</span><span class="sxs-lookup"><span data-stu-id="21393-127">The "%1", "%2", "%3" are placeholders for corresponding strings specified in InsertionStringTemplates array.</span></span>

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

<span data-ttu-id="21393-128">В следующей процедуре описывается использование примера.</span><span class="sxs-lookup"><span data-stu-id="21393-128">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="21393-129">**Использование примера**</span><span class="sxs-lookup"><span data-stu-id="21393-129">**To use the example**</span></span>

1.  <span data-ttu-id="21393-130">Скопируйте приведенный ниже список MOF в текстовый файл и сохраните его с расширением. mof.</span><span class="sxs-lookup"><span data-stu-id="21393-130">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="21393-131">В командное окно Скомпилируйте MOF-файл с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="21393-131">In a Command window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="21393-132">**Mofcomp** *filename \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="21393-132">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="21393-133">Запустите Eventvwr.exe.</span><span class="sxs-lookup"><span data-stu-id="21393-133">Run Eventvwr.exe.</span></span> <span data-ttu-id="21393-134">Просмотрите журнал событий приложений.</span><span class="sxs-lookup"><span data-stu-id="21393-134">Look at the Application event log.</span></span> <span data-ttu-id="21393-135">Должно отобразиться событие с ИДЕНТИФИКАТОРом 10 ( **EventID**), Source = "WMI" и Type = Error.</span><span class="sxs-lookup"><span data-stu-id="21393-135">You should see an event with ID = 10 (the **EventID**), Source = "WMI", and Type = Error.</span></span>
4.  <span data-ttu-id="21393-136">Дважды щелкните сообщение **типа данных** из WMI с 10 в столбце **событий** .</span><span class="sxs-lookup"><span data-stu-id="21393-136">Double-click the **Information type** message from WMI with 10 in the **Event** column.</span></span> <span data-ttu-id="21393-137">Для события будет отображаться следующее описание.</span><span class="sxs-lookup"><span data-stu-id="21393-137">The following description will be displayed for the event.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="21393-138">См. также</span><span class="sxs-lookup"><span data-stu-id="21393-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21393-139">Мониторинг событий и реагирование на них с помощью стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="21393-139">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



