---
description: Язык запросов WMI (WQL) — это подмножество стандартных Американский национальный институт стандартов (ANSI) язык SQL (ANSI SQL) с незначительными семантическими изменениями для поддержки инструментария WMI.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Запросы с помощью WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8e2d3f68f4d7384781110958070b33b67a78405f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692712"
---
# <a name="querying-with-wql"></a><span data-ttu-id="1e14a-103">Запросы с помощью WQL</span><span class="sxs-lookup"><span data-stu-id="1e14a-103">Querying with WQL</span></span>

<span data-ttu-id="1e14a-104">Язык запросов WMI (WQL) — это подмножество стандартных Американский национальный институт стандартов (ANSI) язык SQL (ANSI SQL) с незначительными семантическими изменениями для поддержки инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="1e14a-104">The WMI Query Language (WQL) is a subset of standard American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes to support WMI.</span></span>

<span data-ttu-id="1e14a-105">Полный список поддерживаемых ключевых слов WQL см. в разделе [WQL (SQL для WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="1e14a-105">For a complete list of supported WQL keywords, see [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span> <span data-ttu-id="1e14a-106">Использование ключевых слов SQL для имен объектов или свойств может привести к ограничению синтаксического анализа запроса.</span><span class="sxs-lookup"><span data-stu-id="1e14a-106">Using SQL keywords for object or property names may restrict a query from being parsed.</span></span> <span data-ttu-id="1e14a-107">Следующие ключевые слова SQL ограничены: **null**, **true** и **false**.</span><span class="sxs-lookup"><span data-stu-id="1e14a-107">The following SQL keywords are restricted: **NULL**, **TRUE**, and **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="1e14a-108">Существует ряд ограничений на количество ключевых слов AND и OR, которые могут использоваться в запросах WQL.</span><span class="sxs-lookup"><span data-stu-id="1e14a-108">There are limits to the number of AND and OR keywords that can be used in WQL queries.</span></span> <span data-ttu-id="1e14a-109">Большое количество ключевых слов WQL, используемых в сложном запросе, может привести к тому, что WMI вернет код ошибки **\_ \_ \_ нарушения квоты WBEM E** как значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e14a-109">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="1e14a-110">Ограничение ключевых слов WQL зависит от того, насколько сложным является запрос.</span><span class="sxs-lookup"><span data-stu-id="1e14a-110">The limit of WQL keywords depends on how complex the query is.</span></span>

 

<span data-ttu-id="1e14a-111">Запросы могут использовать предложение **WHERE** для расширения и настройки, хотя это необязательно.</span><span class="sxs-lookup"><span data-stu-id="1e14a-111">Queries can use the **WHERE** clause for extension and customization, although it is not required.</span></span> <span data-ttu-id="1e14a-112">Предложение **WHERE** состоит из свойства или ключевого слова, оператора и константы.</span><span class="sxs-lookup"><span data-stu-id="1e14a-112">The **WHERE** clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="1e14a-113">Все предложения **WHERE** должны указывать один из предопределенных операторов, которые включены в WQL.</span><span class="sxs-lookup"><span data-stu-id="1e14a-113">All **WHERE** clauses must specify one of the predefined operators that are included in WQL.</span></span> <span data-ttu-id="1e14a-114">Дополнительные сведения о синтаксисе см. в разделе [предложение WHERE](where-clause.md).</span><span class="sxs-lookup"><span data-stu-id="1e14a-114">For more information about syntax, see [WHERE Clause](where-clause.md).</span></span> <span data-ttu-id="1e14a-115">Дополнительные сведения о допустимых операторах WQL см. в разделе [Операторы WQL](wql-operators.md).</span><span class="sxs-lookup"><span data-stu-id="1e14a-115">For more information about valid WQL operators, see [WQL Operators](wql-operators.md).</span></span>

<span data-ttu-id="1e14a-116">Как и в случае с другими строками SQL-запросов, запросы можно экранировать.</span><span class="sxs-lookup"><span data-stu-id="1e14a-116">As with other SQL query strings, you can escape your queries.</span></span>

> [!Note]  
> <span data-ttu-id="1e14a-117">WQL не поддерживает запросы или связи между пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="1e14a-117">WQL does not support cross-namespace queries or associations.</span></span> <span data-ttu-id="1e14a-118">Нельзя выполнить запрос для всех экземпляров указанного класса, размещенных во всех пространствах имен на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="1e14a-118">You cannot query for all instances of a specified class residing in all of the namespaces on the target computer.</span></span>

 

<span data-ttu-id="1e14a-119">WQL поддерживает следующие типы запросов:</span><span class="sxs-lookup"><span data-stu-id="1e14a-119">WQL supports the following types of queries:</span></span>

-   <span data-ttu-id="1e14a-120">Запросы данных</span><span class="sxs-lookup"><span data-stu-id="1e14a-120">Data queries</span></span>

    <span data-ttu-id="1e14a-121">Запросы данных используются для получения экземпляров классов и ассоциаций данных.</span><span class="sxs-lookup"><span data-stu-id="1e14a-121">Data queries are used to retrieve class instances and data associations.</span></span> <span data-ttu-id="1e14a-122">Они являются наиболее часто используемым типом запроса в сценариях и приложениях WMI.</span><span class="sxs-lookup"><span data-stu-id="1e14a-122">They are the most commonly used type of query in WMI scripts and applications.</span></span> <span data-ttu-id="1e14a-123">Дополнительные сведения о синтаксисе запросов данных см. в разделе [запрос данных экземпляра класса](requesting-class-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="1e14a-123">For more information about the syntax of data queries, see [Requesting Class Instance Data](requesting-class-instance-data.md).</span></span> <span data-ttu-id="1e14a-124">Дополнительные сведения о связях см. [в разделе объявление класса ассоциации](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="1e14a-124">For more information about associations, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="1e14a-125">WQL не поддерживает запросы типов данных массива.</span><span class="sxs-lookup"><span data-stu-id="1e14a-125">WQL does not support queries of array datatypes.</span></span>

     

    <span data-ttu-id="1e14a-126">Следующий пример запроса данных запрашивает файл журнала событий с именем Application из всех экземпляров [**Win32 \_ нтложевент**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="1e14a-126">The following data query example requests the event log file named "Application" from all instances of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   <span data-ttu-id="1e14a-127">Запросы событий</span><span class="sxs-lookup"><span data-stu-id="1e14a-127">Event queries</span></span>

    <span data-ttu-id="1e14a-128">Потребители используют запросы событий для регистрации для получения уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="1e14a-128">Consumers use event queries to register to receive notification of events.</span></span> <span data-ttu-id="1e14a-129">Поставщики событий используют запросы событий для регистрации для поддержки одного или нескольких событий.</span><span class="sxs-lookup"><span data-stu-id="1e14a-129">Event providers use event queries to register to support one or more events.</span></span> <span data-ttu-id="1e14a-130">Дополнительные сведения о запросах событий см. в разделе [Получение уведомлений о событиях](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="1e14a-130">For more information about event queries, see [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

    <span data-ttu-id="1e14a-131">В следующем примере запрос события с помощью временного потребитель события запрашивает уведомление при создании нового экземпляра класса, производного от [**Win32 \_ нтложевент**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) .</span><span class="sxs-lookup"><span data-stu-id="1e14a-131">The following example event query by a temporary event consumer requests notification when a new instance of a class derived from [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) is created.</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   <span data-ttu-id="1e14a-132">Запросы схемы</span><span class="sxs-lookup"><span data-stu-id="1e14a-132">Schema queries</span></span>

    <span data-ttu-id="1e14a-133">Запросы схемы используются для получения определений классов (а не экземпляров классов) и связей схем.</span><span class="sxs-lookup"><span data-stu-id="1e14a-133">Schema queries are used to retrieve class definitions (rather than class instances) and schema associations.</span></span> <span data-ttu-id="1e14a-134">Поставщики классов используют запросы схемы для указания классов, которые они поддерживают при регистрации.</span><span class="sxs-lookup"><span data-stu-id="1e14a-134">Class providers use schema queries to specify the classes that they support when they register.</span></span> <span data-ttu-id="1e14a-135">Дополнительные сведения о запросах схемы см. в разделе [Получение определений классов](retrieving-class-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="1e14a-135">For more information about schema queries, see [Retrieving Class Definitions](retrieving-class-definitions.md).</span></span>

    <span data-ttu-id="1e14a-136">В следующем примере запроса схемы показан специальный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="1e14a-136">The following example schema query shows the special syntax.</span></span>

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="1e14a-137">См. также</span><span class="sxs-lookup"><span data-stu-id="1e14a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e14a-138">Формат даты и времени WMI</span><span class="sxs-lookup"><span data-stu-id="1e14a-138">WMI Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 
