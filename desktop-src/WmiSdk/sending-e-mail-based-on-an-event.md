---
description: С помощью класса Смтпевентконсумер можно отправить сообщение электронной почты назначенному пользователю при наступлении указанного события. Этот класс является стандартным потребителем событий, предоставляемым инструментарием WMI.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Отправка сообщения электронной почты на основе события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4929b7c8c29d514d73a6e4c9d14049a19f306233
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702366"
---
# <a name="sending-email-based-on-an-event"></a><span data-ttu-id="902ed-104">Отправка сообщения электронной почты на основе события</span><span class="sxs-lookup"><span data-stu-id="902ed-104">Sending Email Based on an Event</span></span>

<span data-ttu-id="902ed-105">С помощью класса [смтпевентконсумер](smtpeventconsumer.md) можно отправить сообщение электронной почты назначенному пользователю при наступлении указанного события.</span><span class="sxs-lookup"><span data-stu-id="902ed-105">By using the [SMTPEventConsumer](smtpeventconsumer.md) class, you can send email to a designated user when a specified event occurs.</span></span> <span data-ttu-id="902ed-106">Этот класс является [стандартным потребителем событий](standard-consumer-classes.md) , ПРЕДОСТАВЛЯЕМым инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="902ed-106">This class is a [standard event consumer](standard-consumer-classes.md) that WMI provides.</span></span>

<span data-ttu-id="902ed-107">Класс [смтпевентконсумер](smtpeventconsumer.md) требует следующих условий для отправки сообщения электронной почты в ответ на событие:</span><span class="sxs-lookup"><span data-stu-id="902ed-107">The [SMTPEventConsumer](smtpeventconsumer.md) class requires the following conditions to send an email message in response to an event:</span></span>

-   <span data-ttu-id="902ed-108">Класс [смтпевентконсумер](smtpeventconsumer.md) должен быть скомпилирован в правильное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="902ed-108">The [SMTPEventConsumer](smtpeventconsumer.md) class must be compiled into the correct namespace.</span></span> <span data-ttu-id="902ed-109">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="902ed-109">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>
-   <span data-ttu-id="902ed-110">SMTP-сервер должен существовать в сети.</span><span class="sxs-lookup"><span data-stu-id="902ed-110">An SMTP server must exist on the network.</span></span>
-   <span data-ttu-id="902ed-111">Сообщение электронной почты не может иметь вложение.</span><span class="sxs-lookup"><span data-stu-id="902ed-111">The email message cannot have an attachment.</span></span>
-   <span data-ttu-id="902ed-112">Сообщение электронной почты должно быть закодировано в US-ASCII.</span><span class="sxs-lookup"><span data-stu-id="902ed-112">The email message must be encoded in US-ASCII.</span></span>

<span data-ttu-id="902ed-113">Базовая процедура использования стандартных потребителей всегда одинакова и находится в [мониторинге и реагировании на события со стандартными потребителями](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="902ed-113">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="902ed-114">Следующая процедура добавляет к основной процедуре. относится только к классу [смтпевентконсумер](smtpeventconsumer.md) ; и описывает создание объекта-получателя события, отправляющего электронную почту.</span><span class="sxs-lookup"><span data-stu-id="902ed-114">The following procedure adds to the basic procedure; is specific to the [SMTPEventConsumer](smtpeventconsumer.md) class; and describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="902ed-115">В следующей процедуре описывается создание объекта-получателя события, отправляющего электронную почту.</span><span class="sxs-lookup"><span data-stu-id="902ed-115">The following procedure describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="902ed-116">**Создание потребителя событий, отправляющего электронную почту**</span><span class="sxs-lookup"><span data-stu-id="902ed-116">**To create an event consumer that sends email**</span></span>

1.  <span data-ttu-id="902ed-117">При необходимости установите и зарегистрируйте класс [смтпевентконсумер](smtpeventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="902ed-117">Install and register the [SMTPEventConsumer](smtpeventconsumer.md) class, if necessary.</span></span>

    <span data-ttu-id="902ed-118">Класс [смтпевентконсумер](smtpeventconsumer.md) компилируется в \\ пространство имен корневой подписки программой установки WMI.</span><span class="sxs-lookup"><span data-stu-id="902ed-118">The [SMTPEventConsumer](smtpeventconsumer.md) class is compiled into the root\\subscription namespace by the WMI setup program.</span></span>

2.  <span data-ttu-id="902ed-119">Найдите событие, которое необходимо отслеживать, и создайте запрос события.</span><span class="sxs-lookup"><span data-stu-id="902ed-119">Identify the event that you want to monitor and create the event query.</span></span>

    <span data-ttu-id="902ed-120">Возможно, имеется встроенное событие, которое используется для отслеживания события.</span><span class="sxs-lookup"><span data-stu-id="902ed-120">There might be an existing intrinsic event that use to monitor your event.</span></span> <span data-ttu-id="902ed-121">Большинство внутренних событий связаны с изменениями экземпляров класса в \\ пространстве имен root cimv2.</span><span class="sxs-lookup"><span data-stu-id="902ed-121">Most intrinsic events are associated with changes to class instances in the "root\\cimv2" namespace.</span></span> <span data-ttu-id="902ed-122">Анализируя классы в справочнике по [классам WMI](wmi-classes.md) , можно, вероятно, найти класс, определяющий событие, которое необходимо отслеживать.</span><span class="sxs-lookup"><span data-stu-id="902ed-122">By analyzing the classes in the [WMI Classes](wmi-classes.md) reference, you can probably find a class that identifies the event you want to monitor.</span></span> <span data-ttu-id="902ed-123">Например, используйте класс [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) для отслеживания изменений на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="902ed-123">For example, use the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class to monitor changes to a hard disk drive.</span></span>

    <span data-ttu-id="902ed-124">Если нет существующих внутренних событий, которые используют, может существовать внешний поставщик событий, который может работать.</span><span class="sxs-lookup"><span data-stu-id="902ed-124">If there are no existing intrinsic events that use, there might be an extrinsic event provider that can work.</span></span> <span data-ttu-id="902ed-125">Например, используйте класс [**регистритричанжеевент**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) поставщика реестра для отслеживания изменений в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="902ed-125">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="902ed-126">Если класс, определяющий событие, которое необходимо отслеживать, не существует, необходимо создать собственный поставщик событий и определить новые классы внешних событий.</span><span class="sxs-lookup"><span data-stu-id="902ed-126">If a class does not exist that identifies the event you want to monitor, you must create your own event provider and define new extrinsic event classes.</span></span> <span data-ttu-id="902ed-127">Дополнительные сведения см. в разделе [запись поставщика событий](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="902ed-127">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

3.  <span data-ttu-id="902ed-128">В файле MOF-файл (MOF) создайте экземпляр [смтпевентконсумер](smtpeventconsumer.md) для получения событий.</span><span class="sxs-lookup"><span data-stu-id="902ed-128">In the Managed Object Format (MOF) file, create an instance of the [SMTPEventConsumer](smtpeventconsumer.md) to receive events.</span></span>

    <span data-ttu-id="902ed-129">Используйте свойства экземпляра, чтобы определить сообщение электронной почты, которое будет отправлено при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="902ed-129">Use the properties of the instance to define the email message to send when an event occurs.</span></span> <span data-ttu-id="902ed-130">Например, свойство **поле ToLine** определяет адрес электронной почты, а свойство **Message** определяет текст сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="902ed-130">For example, the **ToLine** property defines the email address, and the **Message** property defines the text of the email message.</span></span> <span data-ttu-id="902ed-131">Необходимо определить адрес электронной почты, тему и текст сообщения, но сообщение электронной почты не может содержать вложение.</span><span class="sxs-lookup"><span data-stu-id="902ed-131">You must define the email address, subject, and text of a message, but an email message cannot have an attachment.</span></span> <span data-ttu-id="902ed-132">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="902ed-132">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

4.  <span data-ttu-id="902ed-133">Создайте запрос события, указывающий события, которые необходимо отслеживать.</span><span class="sxs-lookup"><span data-stu-id="902ed-133">Create an event query that specifies the events you want to monitor.</span></span>

    <span data-ttu-id="902ed-134">Дополнительные сведения см. [в разделе запросы с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="902ed-134">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

5.  <span data-ttu-id="902ed-135">Создайте экземпляр [**\_ \_ EventFilter**](--eventfilter.md) и сохраните запрос в свойстве **Query** .</span><span class="sxs-lookup"><span data-stu-id="902ed-135">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and store your query in the **Query** property.</span></span>

    <span data-ttu-id="902ed-136">Дополнительные сведения см. в разделе [запросы с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="902ed-136">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

6.  <span data-ttu-id="902ed-137">Создайте экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , чтобы связать фильтр и потребитель.</span><span class="sxs-lookup"><span data-stu-id="902ed-137">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer.</span></span>
7.  <span data-ttu-id="902ed-138">Скомпилируйте MOF-файл с помощью [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="902ed-138">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>


## <a name="example"></a><span data-ttu-id="902ed-139">Пример</span><span class="sxs-lookup"><span data-stu-id="902ed-139">Example</span></span>

<span data-ttu-id="902ed-140">Пример в этом разделе находится в MOF-коде, но экземпляры можно создавать программно с помощью [API скриптов для WMI](scripting-api-for-wmi.md) или [COM API для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="902ed-140">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="902ed-141">В следующей процедуре описывается использование примера.</span><span class="sxs-lookup"><span data-stu-id="902ed-141">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="902ed-142">**Использование примера**</span><span class="sxs-lookup"><span data-stu-id="902ed-142">**To use the example**</span></span>

1.  <span data-ttu-id="902ed-143">Скопируйте следующий MOF в текстовый файл и сохраните его с расширением. mof.</span><span class="sxs-lookup"><span data-stu-id="902ed-143">Copy the following MOF to a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="902ed-144">В окне командной строки Скомпилируйте MOF-файл с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="902ed-144">In a command prompt window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="902ed-145">**Mofcomp** *filename \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="902ed-145">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

> [!Note]  
> <span data-ttu-id="902ed-146">Когда MOF-код компилируется в \\ пространство имен корневой подписки, [смтпевентконсумер](smtpeventconsumer.md) компилируется в то же пространство имен.</span><span class="sxs-lookup"><span data-stu-id="902ed-146">When MOF code is compiled into the root\\subscription namespace, the [SMTPEventConsumer](smtpeventconsumer.md) is compiled into the same namespace.</span></span>

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a><span data-ttu-id="902ed-147">См. также</span><span class="sxs-lookup"><span data-stu-id="902ed-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="902ed-148">Мониторинг событий и реагирование на них с помощью стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="902ed-148">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
