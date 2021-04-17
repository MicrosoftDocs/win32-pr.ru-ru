---
title: Написание манифеста инструментирования
description: Приложения и библиотеки DLL используют манифест инструментирования для обнаружения поставщиков инструментирования и событий, записываемых поставщиками.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104412999"
---
# <a name="writing-an-instrumentation-manifest"></a><span data-ttu-id="a878f-103">Написание манифеста инструментирования</span><span class="sxs-lookup"><span data-stu-id="a878f-103">Writing an Instrumentation Manifest</span></span>

<span data-ttu-id="a878f-104">Приложения и библиотеки DLL используют манифест инструментирования для обнаружения поставщиков инструментирования и событий, записываемых поставщиками.</span><span class="sxs-lookup"><span data-stu-id="a878f-104">Applications and DLLs use an instrumentation manifest to identify their instrumentation providers and the events that the providers write.</span></span> <span data-ttu-id="a878f-105">Манифест — это XML-файл, содержащий элементы, которые указывают поставщика.</span><span class="sxs-lookup"><span data-stu-id="a878f-105">A manifest is an XML file that contains the elements that identify your provider.</span></span> <span data-ttu-id="a878f-106">Соглашение заключается в использовании. Man в качестве расширения для манифеста.</span><span class="sxs-lookup"><span data-stu-id="a878f-106">The convention is to use .man as the extension for your manifest.</span></span> <span data-ttu-id="a878f-107">Манифест должен соответствовать XSD-манифесту события.</span><span class="sxs-lookup"><span data-stu-id="a878f-107">The manifest must conform to the event manifest XSD.</span></span> <span data-ttu-id="a878f-108">Дополнительные сведения о схеме см. в разделе [Евентманифест Schema](eventmanifestschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="a878f-108">For details on the schema, see [EventManifest Schema](eventmanifestschema-schema.md).</span></span>

<span data-ttu-id="a878f-109">Поставщик инструментирования — это любое приложение или библиотека DLL, которые вызывают функции [**евентвритикс**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)или [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) для записи событий в сеанс трассировки трассировки [событий](/windows/desktop/ETW/event-tracing-portal) (ETW) или канал журнала событий.</span><span class="sxs-lookup"><span data-stu-id="a878f-109">An instrumentation provider is any application or DLL that calls the [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring), or [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) functions to write events to an [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) tracing session or an Event Log channel.</span></span> <span data-ttu-id="a878f-110">Приложение может определить одного поставщика инструментирования, охватывающего все события, которые он записывает, или определить поставщика для приложения и поставщика для каждой из его библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="a878f-110">An application can define a single instrumentation provider that covers all events that it writes or it can define a provider for the application and a provider for each of its DLLs.</span></span> <span data-ttu-id="a878f-111">Число поставщиков, определяемых приложением в манифесте, зависит только от того, как приложение хочет упорядочить записываемые события.</span><span class="sxs-lookup"><span data-stu-id="a878f-111">The number of providers that the application defines in the manifest depends solely on how the application wants to organize the events that it writes.</span></span>

<span data-ttu-id="a878f-112">Преимущество указания поставщика для каждой библиотеки DLL заключается в том, что после этого можно включить и отключить отдельные поставщики и, таким же, события, которые они создают.</span><span class="sxs-lookup"><span data-stu-id="a878f-112">The advantage of specifying a provider for each DLL is that you can then enable and disable the individual providers and thus the events that they generate.</span></span> <span data-ttu-id="a878f-113">Это преимущество применимо только в том случае, если поставщик включен в сеансе трассировки ETW.</span><span class="sxs-lookup"><span data-stu-id="a878f-113">This advantage applies only if the provider is enabled by an ETW tracing session.</span></span> <span data-ttu-id="a878f-114">Все события, указывающие канал журнала событий, всегда записываются в этот канал.</span><span class="sxs-lookup"><span data-stu-id="a878f-114">Any events that specify an event log channel are always written to that channel.</span></span>

<span data-ttu-id="a878f-115">Манифест должен выявлять поставщика и события, которые он записывает, но другие метаданные, такие как каналы, уровни и ключевые слова, являются необязательными. определение необязательных метаданных зависит от того, кто будет потреблять события.</span><span class="sxs-lookup"><span data-stu-id="a878f-115">The manifest must identify the provider and the events that it writes but the other metadata such as channels, levels, and keywords are optional; whether you define the optional metadata depends on who will be consuming the events.</span></span> <span data-ttu-id="a878f-116">Например, если администраторы или персонал службы поддержки используют события с помощью такого средства, как Просмотр событий Windows, считывающее события из каналов журнала событий, необходимо определить каналы, на которые записываются эти события.</span><span class="sxs-lookup"><span data-stu-id="a878f-116">For example, if administrators or support personnel consume the events using a tool like the Windows Event Viewer that reads events from event log channels, then you must define the channels to which the events are written.</span></span> <span data-ttu-id="a878f-117">Однако если поставщик будет включен только сеансом трассировки событий Windows, то не нужно определять каналы.</span><span class="sxs-lookup"><span data-stu-id="a878f-117">However, if the provider will only be enabled by an ETW tracing session, then you do not need to define channels.</span></span>

<span data-ttu-id="a878f-118">Несмотря на то, что уровни, задачи, коды операций и метаданные ключевых слов необязательны, их следует использовать для логической группировки или сегментирования событий.</span><span class="sxs-lookup"><span data-stu-id="a878f-118">Although the levels, tasks, opcodes, and keywords metadata are optional, you should use them to logically group or bucket the events.</span></span> <span data-ttu-id="a878f-119">Группирование событий помогает потребителям использовать только те события, которые представляют интерес.</span><span class="sxs-lookup"><span data-stu-id="a878f-119">Grouping the events helps the consumers consume only those events that are of interest.</span></span> <span data-ttu-id="a878f-120">Например, потребитель может запрашивать все события, уровень "критический" и ключевое слово "Write", или запрашивать все события, записанные определенной задачей.</span><span class="sxs-lookup"><span data-stu-id="a878f-120">For example, the consumer could query for all events where level is "critical" and keyword is "write", or query for all events written by a specific task.</span></span>

<span data-ttu-id="a878f-121">Помимо потребителей, использующих уровни и ключевые слова для использования конкретных типов событий, сеанс трассировки ETW может использовать метаданные уровня и ключевого слова, чтобы сообщения ETW могли ограничивать события, записываемые в журнал трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="a878f-121">In addition to consumers using level and keywords to consume specific types of events, an ETW tracing session can use the level and keyword metadata to tell ETW to limit the events that are written to the event tracing log.</span></span> <span data-ttu-id="a878f-122">Например, сеанс может ограничить события только событиями, для которых уровень — "ошибка" или "критическая", а ключевое слово "Read".</span><span class="sxs-lookup"><span data-stu-id="a878f-122">For example, the session could limit the events to only events where level is "error" or "critical" and keyword is "read".</span></span>

<span data-ttu-id="a878f-123">Поставщик может определять фильтры, которые сеанс использует для фильтрации событий на основе данных событий.</span><span class="sxs-lookup"><span data-stu-id="a878f-123">A provider can define filters that a session uses to filter the events based on event data.</span></span> <span data-ttu-id="a878f-124">С помощью уровня и ключевых слов ETW определяет, записывается ли событие в журнал, но с фильтрами поставщик использует критерии фильтрации данных, чтобы определить, записывает ли событие в этот сеанс.</span><span class="sxs-lookup"><span data-stu-id="a878f-124">With level and keywords, ETW determines whether the event is written to the log but with filters, the provider uses the filter data criteria to determine whether it writes the event to that session.</span></span> <span data-ttu-id="a878f-125">Фильтры применяются только в том случае, если сеанс трассировки ETW включает ваш поставщик.</span><span class="sxs-lookup"><span data-stu-id="a878f-125">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="a878f-126">В следующих разделах показано, как определить компоненты манифеста.</span><span class="sxs-lookup"><span data-stu-id="a878f-126">The following sections show how to define the components of the manifest:</span></span>

-   [<span data-ttu-id="a878f-127">Определение поставщика</span><span class="sxs-lookup"><span data-stu-id="a878f-127">Identifying the provider</span></span>](identifying-the-provider.md)
-   [<span data-ttu-id="a878f-128">Определение каналов, на которых записываются события</span><span class="sxs-lookup"><span data-stu-id="a878f-128">Defining the channels to where the events are written</span></span>](defining-channels.md)
-   [<span data-ttu-id="a878f-129">Определение уровней серьезности событий, записываемых поставщиком</span><span class="sxs-lookup"><span data-stu-id="a878f-129">Defining the severity levels of events that the provider writes</span></span>](defining-severity-levels.md)
-   [<span data-ttu-id="a878f-130">Определение задач и операций, выполняемых поставщиком</span><span class="sxs-lookup"><span data-stu-id="a878f-130">Defining the tasks and operations that your provider performs</span></span>](defining-tasks-and-opcodes.md)
-   [<span data-ttu-id="a878f-131">Определение ключевых слов, которые классифицируют события, записываемые поставщиком</span><span class="sxs-lookup"><span data-stu-id="a878f-131">Defining the keywords that classify the events that the provider writes</span></span>](defining-keywords-used-to-classify-types-of-events.md)
-   [<span data-ttu-id="a878f-132">Определение фильтров, используемых поставщиком для фильтрации записываемых событий</span><span class="sxs-lookup"><span data-stu-id="a878f-132">Defining the filters that the provider uses to filter the events that it writes</span></span>](defining-filters.md)
-   [<span data-ttu-id="a878f-133">Определение сопоставлений имен и значений, на которые ссылаются данные шаблона</span><span class="sxs-lookup"><span data-stu-id="a878f-133">Defining the name/value maps that your template data references</span></span>](defining-name-value-mappings.md)
-   [<span data-ttu-id="a878f-134">Определение шаблонов, определяющих данные, относящиеся к событиям</span><span class="sxs-lookup"><span data-stu-id="a878f-134">Defining the templates that define the event-specific data</span></span>](defining-event-data-templates.md)
-   [<span data-ttu-id="a878f-135">Определение событий, записываемых поставщиком</span><span class="sxs-lookup"><span data-stu-id="a878f-135">Defining the events that the provider writes</span></span>](defining-events.md)

<span data-ttu-id="a878f-136">Хотя манифест инструментирования можно создать вручную, следует использовать средство ECManGen.exe, которое входит в \\ папку Bin Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a878f-136">Although you can author an instrumentation manifest manually, you should consider using the ECManGen.exe tool that is included in the \\Bin folder of the Windows SDK.</span></span> <span data-ttu-id="a878f-137">Средство ECManGen.exe использует графический интерфейс пользователя, который помогает создать манифест с нуля без использования XML-тегов.</span><span class="sxs-lookup"><span data-stu-id="a878f-137">The ECManGen.exe tool uses a GUI that guides you through creating a manifest from scratch without ever having to use XML tags.</span></span> <span data-ttu-id="a878f-138">Знание сведений в этом разделе и в разделе [схемы евентманифест](eventmanifestschema-schema.md) поможет при использовании этого средства.</span><span class="sxs-lookup"><span data-stu-id="a878f-138">Having knowledge of the information in this section and in the [EventManifest Schema](eventmanifestschema-schema.md) section will help when using the tool.</span></span>

<span data-ttu-id="a878f-139">Если вы используете Visual Studio в качестве редактора XML, вы можете добавить в проект схему [евентманифест](eventmanifestschema-schema.md) (см. меню XML), чтобы воспользоваться преимуществами IntelliSense, встроенной проверкой схемы и другими функциями для упрощения и точной записи манифеста.</span><span class="sxs-lookup"><span data-stu-id="a878f-139">If you use Visual Studio as your XML editor, you can add the [EventManifest](eventmanifestschema-schema.md) schema to the project (see the XML menu) to take advantage of Intellisense, inline schema validation, and other features to make writing the manifest easy and accurate.</span></span>

<span data-ttu-id="a878f-140">После записи манифеста используйте компилятор сообщений для проверки манифеста и создания файлов ресурсов и заголовков, включаемых в поставщик.</span><span class="sxs-lookup"><span data-stu-id="a878f-140">After writing your manifest, use the message compiler to validate the manifest and generate the resource and header files that you include in your provider.</span></span> <span data-ttu-id="a878f-141">Дополнительные сведения см. в разделе [Компиляция манифеста инструментирования](compiling-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="a878f-141">For more information, see [Compiling an Instrumentation Manifest](compiling-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="a878f-142">В следующем примере показана скелет полностью определенного манифеста события.</span><span class="sxs-lookup"><span data-stu-id="a878f-142">The following example shows the skeleton of a fully defined event manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 