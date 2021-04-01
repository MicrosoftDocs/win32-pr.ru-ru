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
# <a name="writing-to-a-log-file-based-on-an-event"></a><span data-ttu-id="0e051-104">Запись в файл журнала на основе события</span><span class="sxs-lookup"><span data-stu-id="0e051-104">Writing to a Log File Based on an Event</span></span>

<span data-ttu-id="0e051-105">Класс [**логфиливентконсумер**](logfileeventconsumer.md) может записывать предопределенный текст в файл журнала при наступлении указанного события.</span><span class="sxs-lookup"><span data-stu-id="0e051-105">The [**LogFileEventConsumer**](logfileeventconsumer.md) class can write predefined text to a log file when a specified event occurs.</span></span> <span data-ttu-id="0e051-106">Этот класс является стандартным потребителем событий, предоставляемым инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0e051-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="0e051-107">Базовая процедура использования стандартных потребителей всегда одинакова и находится в [мониторинге и реагировании на события со стандартными потребителями](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="0e051-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="0e051-108">Следующая процедура добавляет в основную процедуру, относящуюся к классу [**логфиливентконсумер**](logfileeventconsumer.md) , и описывает создание объекта-получателя события, запускающего программу.</span><span class="sxs-lookup"><span data-stu-id="0e051-108">The following procedure adds to the basic procedure, is specific to the [**LogFileEventConsumer**](logfileeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

<span data-ttu-id="0e051-109">**Создание объекта-получателя события, записывающего данные в файл журнала**</span><span class="sxs-lookup"><span data-stu-id="0e051-109">**To create an event consumer that writes to a log file**</span></span>

1.  <span data-ttu-id="0e051-110">В файле MOF-файл (MOF) создайте экземпляр [**логфиливентконсумер**](logfileeventconsumer.md) для получения событий, которые вы запрашиваете в запросе, присвойте имя экземпляру в свойстве **Name** , а затем поместите путь к файлу журнала в свойстве **filename** .</span><span class="sxs-lookup"><span data-stu-id="0e051-110">In the Managed Object Format (MOF) file, create an instance of [**LogFileEventConsumer**](logfileeventconsumer.md) to receive the events you request in the query, name the instance in the **Name** property, and then place the path to the log file in the **Filename** property.</span></span>

    <span data-ttu-id="0e051-111">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="0e051-111">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="0e051-112">Укажите текстовый шаблон для записи в файл журнала в свойстве Text.</span><span class="sxs-lookup"><span data-stu-id="0e051-112">Provide the text template to write to the log file in the Text property.</span></span>

    <span data-ttu-id="0e051-113">Дополнительные сведения см. [в разделе Использование стандартных строковых шаблонов](using-standard-string-templates.md).</span><span class="sxs-lookup"><span data-stu-id="0e051-113">For more information, see [Using Standard String Templates](using-standard-string-templates.md).</span></span>

3.  <span data-ttu-id="0e051-114">Создайте экземпляр [**\_ \_ EventFilter**](--eventfilter.md) и определите запрос для указания событий, которые будут активировать потребитель.</span><span class="sxs-lookup"><span data-stu-id="0e051-114">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query to specify the events that will activate the consumer.</span></span>

    <span data-ttu-id="0e051-115">Дополнительные сведения см. [в разделе запросы с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="0e051-115">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="0e051-116">Создайте экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , чтобы связать фильтр с экземпляром [**логфиливентконсумер**](logfileeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="0e051-116">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**LogFileEventConsumer**](logfileeventconsumer.md).</span></span>
5.  <span data-ttu-id="0e051-117">Чтобы контролировать, кто читает файл журнала или выполняет запись в него, задайте уровень безопасности для каталога, в котором находится журнал, на требуемом уровне.</span><span class="sxs-lookup"><span data-stu-id="0e051-117">To control who reads or writes to your log file, set the security on the directory where the log is located to the required level.</span></span>
6.  <span data-ttu-id="0e051-118">Скомпилируйте MOF-файл с помощью [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="0e051-118">Compile your MOF file using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="0e051-119">Пример</span><span class="sxs-lookup"><span data-stu-id="0e051-119">Example</span></span>

<span data-ttu-id="0e051-120">Пример в этом разделе находится в MOF-коде, но экземпляры можно создавать программно с помощью [API скриптов для WMI](scripting-api-for-wmi.md) или [COM API для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0e051-120">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="0e051-121">В примере используется стандартный Логфиливентконсумер для создания класса-получателя с именем Логфиливент, который записывает строку в файл c: \\ файл_журнала. log при создании экземпляра класса логфиливент.</span><span class="sxs-lookup"><span data-stu-id="0e051-121">The example uses the standard LogFileEventConsumer to create a consumer class named LogFileEvent that writes a line to the file c:\\Logfile.log when an instance of the class LogFileEvent is created.</span></span>

<span data-ttu-id="0e051-122">В следующей процедуре описывается использование примера.</span><span class="sxs-lookup"><span data-stu-id="0e051-122">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="0e051-123">**Использование примера**</span><span class="sxs-lookup"><span data-stu-id="0e051-123">**To use the example**</span></span>

1.  <span data-ttu-id="0e051-124">Скопируйте приведенный ниже список MOF в текстовый файл и сохраните его с расширением. mof.</span><span class="sxs-lookup"><span data-stu-id="0e051-124">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="0e051-125">В окне командной строки Скомпилируйте MOF-файл с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="0e051-125">In a command window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="0e051-126">**Mofcomp** *filename \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="0e051-126">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="0e051-127">Откройте файл файл_журнала. log, чтобы увидеть строку, указанную параметром LogFileEvent.Name: "событие файла-получателя события.</span><span class="sxs-lookup"><span data-stu-id="0e051-127">Open Logfile.log to see the line specified by LogFileEvent.Name: "Logfile Event Consumer event".</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0e051-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0e051-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e051-129">Мониторинг событий и реагирование на них с помощью стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="0e051-129">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



