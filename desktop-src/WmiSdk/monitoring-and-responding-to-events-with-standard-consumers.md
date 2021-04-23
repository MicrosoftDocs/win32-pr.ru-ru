---
description: Установленные стандартные классы потребителей можно использовать для выполнения действий на основе событий в операционной системе.
ms.assetid: 1979dc55-a440-4c31-832b-36fa84def4c9
ms.tgt_platform: multiple
title: Мониторинг событий и реагирование на них с помощью стандартных потребителей
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5bd1d329cd861fa45c99851707177322d0b9d12f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "103914839"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a><span data-ttu-id="c1efc-103">Мониторинг событий и реагирование на них с помощью стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="c1efc-103">Monitoring and Responding to Events with Standard Consumers</span></span>

<span data-ttu-id="c1efc-104">Установленные [стандартные классы потребителей](standard-consumer-classes.md) можно использовать для выполнения действий на основе событий в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="c1efc-104">You can use the installed [standard consumer classes](standard-consumer-classes.md) to perform actions based on events in an operating system.</span></span> <span data-ttu-id="c1efc-105">Стандартные потребители — это простые классы, которые уже зарегистрированы и определяют постоянные классы потребителей.</span><span class="sxs-lookup"><span data-stu-id="c1efc-105">Standard consumers are simple classes that are already registered, and they define permanent consumer classes.</span></span> <span data-ttu-id="c1efc-106">Каждый стандартный потребитель выполняет определенное действие после получения уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="c1efc-106">Each standard consumer takes a specific action after it receives an event notification.</span></span> <span data-ttu-id="c1efc-107">Например, можно определить экземпляр [**активескриптевентконсумер**](activescripteventconsumer.md) для выполнения сценария, если свободное место на компьютере отличается от указанного размера.</span><span class="sxs-lookup"><span data-stu-id="c1efc-107">For example, you can define an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to execute a script when free disk space on a computer is different from a specified size.</span></span>

<span data-ttu-id="c1efc-108">Инструментарий WMI компилирует стандартных потребителей в пространства имен по умолчанию, зависящие от операционной системы, например:</span><span class="sxs-lookup"><span data-stu-id="c1efc-108">WMI compiles the standard consumers into default namespaces that depend on the operating system, for example:</span></span>

-   <span data-ttu-id="c1efc-109">В Windows Server 2003 все стандартные потребители компилируются по умолчанию в \\ пространство имен "Корневая подписка".</span><span class="sxs-lookup"><span data-stu-id="c1efc-109">In Windows Server 2003, all of the standard consumers are compiled by default into the "Root\\Subscription" namespace.</span></span>

> [!Note]  
> <span data-ttu-id="c1efc-110">Сведения о пространствах имен по умолчанию и операционных системах, которые относятся к каждому классу WMI, см. в разделах примечания и требования каждого класса.</span><span class="sxs-lookup"><span data-stu-id="c1efc-110">For the default namespaces and operating systems that are specific for each WMI class, see the Remarks and Requirements sections of each class topic.</span></span>

 

<span data-ttu-id="c1efc-111">В следующей таблице перечислены и описаны стандартные потребители WMI.</span><span class="sxs-lookup"><span data-stu-id="c1efc-111">The following table lists and describes the WMI standard consumers.</span></span>



| <span data-ttu-id="c1efc-112">Стандартный потребитель</span><span class="sxs-lookup"><span data-stu-id="c1efc-112">Standard consumer</span></span>                                              | <span data-ttu-id="c1efc-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c1efc-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1efc-114">**активескриптевентконсумер**</span><span class="sxs-lookup"><span data-stu-id="c1efc-114">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md) | <span data-ttu-id="c1efc-115">Выполняет скрипт при получении уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="c1efc-115">Executes a script when it receives an event notification.</span></span> <span data-ttu-id="c1efc-116">Дополнительные сведения см. в разделе [выполнение сценария на основе события](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="c1efc-116">For more information, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="c1efc-117">**логфиливентконсумер**</span><span class="sxs-lookup"><span data-stu-id="c1efc-117">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)           | <span data-ttu-id="c1efc-118">Записывает измененные строки в текстовый файл журнала при получении уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="c1efc-118">Writes customized strings to a text log file when it receives an event notification.</span></span> <span data-ttu-id="c1efc-119">Дополнительные сведения см. в разделе [запись в файл журнала на основе события](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="c1efc-119">For more information, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="c1efc-120">**нтевентложевентконсумер**</span><span class="sxs-lookup"><span data-stu-id="c1efc-120">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)     | <span data-ttu-id="c1efc-121">Записывает в журнал событий приложений определенное сообщение.</span><span class="sxs-lookup"><span data-stu-id="c1efc-121">Logs a specific message to the Application event log.</span></span> <span data-ttu-id="c1efc-122">Дополнительные сведения см. в разделе [ведение журнала событий NT на основе события](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="c1efc-122">For more information, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="c1efc-123">**смтпевентконсумер**</span><span class="sxs-lookup"><span data-stu-id="c1efc-123">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                 | <span data-ttu-id="c1efc-124">Отправляет сообщение электронной почты по протоколу SMTP каждый раз, когда в него доставляется событие.</span><span class="sxs-lookup"><span data-stu-id="c1efc-124">Sends an email message by using SMTP each time an event is delivered to it.</span></span> <span data-ttu-id="c1efc-125">Дополнительные сведения см. [в разделе Отправка сообщения электронной почты на основе события](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="c1efc-125">For more information, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="c1efc-126">**коммандлинивентконсумер**</span><span class="sxs-lookup"><span data-stu-id="c1efc-126">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)   | <span data-ttu-id="c1efc-127">Запускает процесс, когда событие доставляется в локальную систему.</span><span class="sxs-lookup"><span data-stu-id="c1efc-127">Launches a process when an event is delivered to a local system.</span></span> <span data-ttu-id="c1efc-128">Исполняемый файл должен находиться в безопасном месте или быть защищен с помощью строгого списка управления доступом (ACL), чтобы предотвратить несанкционированный пользователь заменить исполняемый объект другим исполняемым файлом.</span><span class="sxs-lookup"><span data-stu-id="c1efc-128">The executable file must be in a secure location, or secured with a strong access control list (ACL) to prevent an unauthorized user from replacing your executable with a different executable.</span></span> <span data-ttu-id="c1efc-129">Дополнительные сведения см. в разделе [Запуск программы из командной строки на основе события](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="c1efc-129">For more information, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span> |



 

<span data-ttu-id="c1efc-130">Следующая процедура описывает, как отслеживать события и реагировать на них с помощью стандартного потребителя.</span><span class="sxs-lookup"><span data-stu-id="c1efc-130">The following procedure describes how to monitor and respond to events by using a standard consumer.</span></span> <span data-ttu-id="c1efc-131">Обратите внимание, что процедура одинакова для файла MOF-файл (MOF), сценария или приложения.</span><span class="sxs-lookup"><span data-stu-id="c1efc-131">Note that the procedure is the same for a Managed Object Format (MOF) file, script, or application.</span></span>

<span data-ttu-id="c1efc-132">**Мониторинг событий и реагирование на них с помощью стандартного потребителя**</span><span class="sxs-lookup"><span data-stu-id="c1efc-132">**To monitor and respond to events with a standard consumer**</span></span>

1.  <span data-ttu-id="c1efc-133">Укажите пространство имен в MOF-файле, используя [ \# пространство имен pragma](pragma-namespace.md)команды препроцессора.</span><span class="sxs-lookup"><span data-stu-id="c1efc-133">Specify the namespace in a MOF file by using the MOF preprocessor command [\#pragma namespace](pragma-namespace.md).</span></span> <span data-ttu-id="c1efc-134">В скрипте или приложении укажите пространство имен в коде, который подключается к WMI.</span><span class="sxs-lookup"><span data-stu-id="c1efc-134">In a script or application, specify the namespace in the code that connects to WMI.</span></span>

    <span data-ttu-id="c1efc-135">В следующем примере кода MOF показано, как указать \\ пространство имен корневой подписки.</span><span class="sxs-lookup"><span data-stu-id="c1efc-135">The following MOF code example shows how to specify the root\\subscription namespace.</span></span>

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    <span data-ttu-id="c1efc-136">Большинство [*внутренних событий*](gloss-i.md) связаны с изменениями экземпляров класса в корневом \\ пространстве имен CIMV2.</span><span class="sxs-lookup"><span data-stu-id="c1efc-136">Most [*intrinsic events*](gloss-i.md) are associated with changes to class instances in the root\\cimv2 namespace.</span></span> <span data-ttu-id="c1efc-137">Однако события реестра, такие как [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) , срабатывают в корневом \\ пространстве имен по умолчанию [поставщиком системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider).</span><span class="sxs-lookup"><span data-stu-id="c1efc-137">However, registry events such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) are fired in the root\\default namespace by the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider).</span></span>

    <span data-ttu-id="c1efc-138">Потребитель может включать классы событий, расположенные в других пространствах имен, указывая пространство имен в свойстве **евентнамеспаце** в запросе [**\_ \_ EventFilter**](--eventfilter.md) для событий.</span><span class="sxs-lookup"><span data-stu-id="c1efc-138">A consumer can include event classes located in other namespaces by specifying the namespace in the **EventNamespace** property in the [**\_\_EventFilter**](--eventfilter.md) query for events.</span></span> <span data-ttu-id="c1efc-139">[*Внутренние классы событий*](gloss-i.md) , такие как [**\_ \_ инстанцеоператионевент**](--instanceoperationevent.md) , доступны в каждом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="c1efc-139">The [*intrinsic events*](gloss-i.md) classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

2.  <span data-ttu-id="c1efc-140">Создайте и заполните экземпляр класса стандартного потребителя.</span><span class="sxs-lookup"><span data-stu-id="c1efc-140">Create and populate an instance of a standard consumer class.</span></span>

    <span data-ttu-id="c1efc-141">Этот экземпляр может иметь уникальное значение в свойстве **Name** .</span><span class="sxs-lookup"><span data-stu-id="c1efc-141">This instance may have a unique value in the **Name** property.</span></span> <span data-ttu-id="c1efc-142">Существующий потребитель можно обновить, повторно используя то же имя.</span><span class="sxs-lookup"><span data-stu-id="c1efc-142">You can update an existing consumer by reusing the same name.</span></span>

    <span data-ttu-id="c1efc-143">**Инсертионстрингтемплатес** содержит текст для вставки в событие, указанное в **EventType**.</span><span class="sxs-lookup"><span data-stu-id="c1efc-143">**InsertionStringTemplates** contains the text to insert in an event that you specify in **EventType**.</span></span> <span data-ttu-id="c1efc-144">Можно использовать литеральные строки или напрямую обращаться к свойству.</span><span class="sxs-lookup"><span data-stu-id="c1efc-144">You can use literal strings or refer directly to a property.</span></span> <span data-ttu-id="c1efc-145">Дополнительные сведения см. в статьях [Использование стандартных строковых шаблонов](using-standard-string-templates.md) и [инструкция SELECT для запросов событий](select-statement-for-event-queries.md).</span><span class="sxs-lookup"><span data-stu-id="c1efc-145">For more information, see [Using Standard String Templates](using-standard-string-templates.md) and [SELECT Statement for Event Queries](select-statement-for-event-queries.md).</span></span>

    <span data-ttu-id="c1efc-146">Используйте существующий источник для журнала событий, который поддерживает строку вставки без связанного текста.</span><span class="sxs-lookup"><span data-stu-id="c1efc-146">Use an existing source for the event log that supports an insertion string without associated text.</span></span>

    <span data-ttu-id="c1efc-147">В следующем примере кода MOF показано, как использовать существующий источник сценариев WSH и значение **EventID** , равное 8.</span><span class="sxs-lookup"><span data-stu-id="c1efc-147">The following MOF code example shows how to use an existing source of WSH and an **EventID** value of 8.</span></span>

    ```syntax
    instance of NTEventLogEventConsumer as $Consumer
    {
        Name = "RunKeyEventlogConsumer";
        SourceName = "WSH";               
        EventID = 8;
        // Warning                              
        EventType = 2;
        // One string supplies the entire message          
        NumberOfInsertionStrings = 1;             
        // the %Hive% and %KeyPath% are properties of
        // the RegistryKeyChangeEvent instance 
        InsertionStringTemplates = 
            {"The key %Hive%\\%RootPath% has been modified."
            "Check if the change is intentional"};
    };
    ```

3.  <span data-ttu-id="c1efc-148">Создайте экземпляр [**\_ \_ EventFilter**](--eventfilter.md) и определите запрос для событий.</span><span class="sxs-lookup"><span data-stu-id="c1efc-148">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query for events.</span></span>

    <span data-ttu-id="c1efc-149">В следующем примере фильтр отслеживает раздел реестра, в котором зарегистрированы программы запуска.</span><span class="sxs-lookup"><span data-stu-id="c1efc-149">In the following example, the filter monitors the registry key where startup programs are registered.</span></span> <span data-ttu-id="c1efc-150">Наблюдение за этим ключом реестра может быть важным, так как несанкционированная программа может зарегистрироваться в ключе, что приводит к его запуску при загрузке компьютера.</span><span class="sxs-lookup"><span data-stu-id="c1efc-150">Monitoring this registry key may be important because an unauthorized program can register itself under the key, which causes it to be launched when the computer boots.</span></span>

    ```syntax
    instance of __EventFilter as $Filter
    {
    Name = "RunKeyFilter";
    QueryLanguage = "WQL"; 
    Query = "Select * from RegistryTreeChangeEvent"
        " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
        "RootPath = \"Software\\\\Microsoft\\\\Windows"
        "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire in root\default namespace
    EventNamespace = "root\\default";                       
    };
    ```

4.  <span data-ttu-id="c1efc-151">Определяет событие для отслеживания и создания запроса события.</span><span class="sxs-lookup"><span data-stu-id="c1efc-151">Identify an event to monitor and create an event query.</span></span>

    <span data-ttu-id="c1efc-152">Можно проверить, имеется ли внутреннее или внешнее событие, которое использует.</span><span class="sxs-lookup"><span data-stu-id="c1efc-152">You can check to see if there is an intrinsic or extrinsic event that use.</span></span> <span data-ttu-id="c1efc-153">Например, используйте класс [**регистритричанжеевент**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) поставщика реестра для отслеживания изменений в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="c1efc-153">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="c1efc-154">Если класс не существует, описывающий событие, которое необходимо отслеживать, необходимо создать собственный поставщик событий и определить новые классы внешних событий.</span><span class="sxs-lookup"><span data-stu-id="c1efc-154">If a class does not exist that describes an event you need to monitor, you must create your own event provider, and define new extrinsic event classes.</span></span> <span data-ttu-id="c1efc-155">Дополнительные сведения см. в разделе [запись поставщика событий](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c1efc-155">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

    <span data-ttu-id="c1efc-156">В MOF-файле можно определить [*псевдоним*](gloss-a.md) для фильтра и потребителя, который предоставляет простой способ описания путей к экземплярам.</span><span class="sxs-lookup"><span data-stu-id="c1efc-156">In a MOF file, you can define an [*alias*](gloss-a.md) for the filter and consumer, which provides an easy way to describe the instance paths.</span></span>

    <span data-ttu-id="c1efc-157">В следующем примере показано, как определить [*псевдоним*](gloss-a.md) для фильтра и потребителя.</span><span class="sxs-lookup"><span data-stu-id="c1efc-157">The following example shows how to define an [*alias*](gloss-a.md) for the filter and consumer.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  <span data-ttu-id="c1efc-158">Создайте экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , чтобы связать классы Filter и Consumer.</span><span class="sxs-lookup"><span data-stu-id="c1efc-158">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer classes.</span></span> <span data-ttu-id="c1efc-159">Этот экземпляр определяет, что при возникновении события, соответствующего указанному фильтру, должно произойти действие, указанное потребителем.</span><span class="sxs-lookup"><span data-stu-id="c1efc-159">This instance determines that when an event occurs that matches the specified filter, the action specified by the consumer must occur.</span></span> <span data-ttu-id="c1efc-160">[**\_ \_ EventFilter**](--eventfilter.md), [**\_ \_ евентконсумер**](--eventconsumer.md)и **\_ \_ филтертоконсумербиндинг** должны иметь один и тот же идентификатор безопасности (SID) в свойстве **креаторсид** .</span><span class="sxs-lookup"><span data-stu-id="c1efc-160">[**\_\_EventFilter**](--eventfilter.md), [**\_\_EventConsumer**](--eventconsumer.md), and **\_\_FilterToConsumerBinding** must have the same individual security identifier (SID) in the **CreatorSID** property.</span></span> <span data-ttu-id="c1efc-161">Дополнительные сведения см. в разделе [Привязка фильтра событий к логическому потребителю](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="c1efc-161">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

    <span data-ttu-id="c1efc-162">В следующем примере показано, как указать экземпляр по пути к объекту или использовать псевдоним в качестве краткого выражения для пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c1efc-162">The following example shows how to identify an instance by the object path, or use an alias as a shorthand expression for the object path.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    <span data-ttu-id="c1efc-163">В следующем примере фильтр привязывается к потребителю с помощью псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="c1efc-163">The following example binds the filter to the consumer by using aliases.</span></span>

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    <span data-ttu-id="c1efc-164">Можно привязать один фильтр к нескольким потребителям, что означает, что при возникновении событий сопоставления необходимо выполнить несколько действий. или можно привязать одного потребителя к нескольким фильтрам, что означает, что действие должно выполняться при возникновении событий, соответствующих одному из фильтров.</span><span class="sxs-lookup"><span data-stu-id="c1efc-164">You can bind one filter to several consumers, which indicates that when matching events occur, several actions must be taken; or you can bind one consumer to several filters, which indicates that the action must be taken when events that match one of the filters occur.</span></span>

    <span data-ttu-id="c1efc-165">В зависимости от состояния потребителей и событий выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c1efc-165">The following actions are taken based on the condition of consumers and events:</span></span>

    -   <span data-ttu-id="c1efc-166">Если один из постоянных потребителей завершается сбоем, другие потребители, запрашивающие получение уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="c1efc-166">If one of the permanent consumers fails, other consumers that request the event receive notification.</span></span>
    -   <span data-ttu-id="c1efc-167">Если событие удаляется, WMI запускает [**\_ \_ евентдроппедевент**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="c1efc-167">If an event is dropped, WMI fires [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>
    -   <span data-ttu-id="c1efc-168">Если вы подписались на это событие, он возвращает событие, которое удаляется, а ссылка на [**\_ \_ евентконсумер**](--eventconsumer.md) представляет неудачный потребитель.</span><span class="sxs-lookup"><span data-stu-id="c1efc-168">If you subscribe to this event, it returns the event that is dropped, and a reference to the [**\_\_EventConsumer**](--eventconsumer.md) represents the failed consumer.</span></span>
    -   <span data-ttu-id="c1efc-169">Если происходит сбой потребителя, Инструментарий WMI запускает [**\_ \_ консумерфаилуривент**](--consumerfailureevent.md), который может содержать дополнительные сведения в свойствах **ErrorCode**, **ErrorDescription** и **ерроробжект** .</span><span class="sxs-lookup"><span data-stu-id="c1efc-169">If a consumer fails, WMI fires [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md), which may contain more information in the **ErrorCode**, **ErrorDescription** and **ErrorObject** properties.</span></span>

    <span data-ttu-id="c1efc-170">Дополнительные сведения см. в разделе [Привязка фильтра событий к логическому потребителю](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="c1efc-170">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

## <a name="example"></a><span data-ttu-id="c1efc-171">Пример</span><span class="sxs-lookup"><span data-stu-id="c1efc-171">Example</span></span>

<span data-ttu-id="c1efc-172">В следующем примере показан MOF для экземпляра [**нтевентложевентконсумер**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="c1efc-172">The following example shows the MOF for an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="c1efc-173">После компиляции этого MOF-файла любая попытка создать, удалить или изменить значение в разделе реестра путь к файлу **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ выполнить** РЕГИСТРИРУЕТ запись в журнале событий приложения в исходном "WSH".</span><span class="sxs-lookup"><span data-stu-id="c1efc-173">After you compile this MOF, any attempt to create, delete, or modify a value in the Registry path **HKEY\_LOCAL\_MACHINE\\ Software\\Microsoft\\Windows\\CurrentVersion\\Run** logs an entry in the Application eventlog, under the source "WSH".</span></span>


```mof
#pragma namespace ("\\\\.\\root\\subscription")
 
instance of __EventFilter as $Filter
{
    Name = "RunKeyFilter";
    QueryLanguage = "WQL";
    Query = "Select * from RegistryTreeChangeEvent"
            " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
            "KeyPath = \"Software\\\\Microsoft\\\\Windows"
            "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire
    // in root\default namespace
    EventNamespace = "root\\default";   
};
 
instance of NTEventLogEventConsumer as $Consumer
{
    Name = "RunKeyEventlogConsumer";
    SourceName = "WSH";               
    EventID = 8;
    EventType = 2;                            // Warning
    Category = 0;
    NumberOfInsertionStrings = 1;

    // the %Hive% and %KeyPath% are properties
    // of the RegistryKeyChangeEvent instance 
    InsertionStringTemplates = {"The key %Hive%\\%RootPath% "
        "has been modified. Check if the change is intentional"};
};
 

// Bind the filter to the consumer
instance of __FilterToConsumerBinding
{
    Filter = $Filter;
    Consumer = $Consumer;
};
```



## <a name="related-topics"></a><span data-ttu-id="c1efc-174">См. также</span><span class="sxs-lookup"><span data-stu-id="c1efc-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1efc-175">Безопасное получение событий</span><span class="sxs-lookup"><span data-stu-id="c1efc-175">Receiving Events Securely</span></span>](receiving-events-securely.md)
</dt> </dl>

 

 
