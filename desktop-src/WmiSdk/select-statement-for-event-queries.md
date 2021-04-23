---
description: Описывает базовый синтаксис инструкции SELECT для запросов событий.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: Инструкция SELECT для запросов событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab840072269d04987bf42939f1f566ee6b99afab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272220"
---
# <a name="select-statement-for-event-queries"></a><span data-ttu-id="67387-103">Инструкция SELECT для запросов событий</span><span class="sxs-lookup"><span data-stu-id="67387-103">SELECT Statement for Event Queries</span></span>

<span data-ttu-id="67387-104">Для запроса сведений о событиях можно использовать разнообразные инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="67387-104">You can use a variety of SELECT statements to query for event information.</span></span> <span data-ttu-id="67387-105">Инструкции могут быть основными операторами, или они могут быть более ограничивающими, чтобы сократить результирующий набор, возвращаемый запросом.</span><span class="sxs-lookup"><span data-stu-id="67387-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="67387-106">В следующем примере показана базовая инструкция SELECT, которая используется для запроса сведений о событии.</span><span class="sxs-lookup"><span data-stu-id="67387-106">The following example is a basic SELECT statement that is used to query for event information.</span></span>


```sql
SELECT * FROM EventClass
```



<span data-ttu-id="67387-107">Когда потребитель отправляет запрос, это запрос на получение уведомления обо всех событиях события, представленного объектом **EventClass**.</span><span class="sxs-lookup"><span data-stu-id="67387-107">When a consumer submits a query, it is a request to be notified of all occurrences of the event represented by **EventClass**.</span></span> <span data-ttu-id="67387-108">Этот запрос содержит запрос на уведомление обо всех системных событиях и несистемных свойствах.</span><span class="sxs-lookup"><span data-stu-id="67387-108">This request includes a request for notification about all of the event system and nonsystem properties.</span></span> <span data-ttu-id="67387-109">Когда поставщик событий отправляет запрос, он регистрирует поддержку создания уведомлений при возникновении события, представленного методом **EventClass** .</span><span class="sxs-lookup"><span data-stu-id="67387-109">When an event provider submits a query, it registers support for generating notifications when an event represented by **EventClass** occurs.</span></span>

<span data-ttu-id="67387-110">Потребители могут задавать отдельные свойства вместо звездочки ( \* ) в инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="67387-110">Consumers can specify individual properties instead of the asterisk (\*) in the SELECT statement.</span></span>

<span data-ttu-id="67387-111">В следующем примере показано, как запросить определенные свойства.</span><span class="sxs-lookup"><span data-stu-id="67387-111">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



<span data-ttu-id="67387-112">Однако возвращаются все свойства внедренного объекта, даже если запрос задает свойства внедренного объекта.</span><span class="sxs-lookup"><span data-stu-id="67387-112">However, all of the properties of an embedded object are returned, even if the query specifies embedded object properties.</span></span>

<span data-ttu-id="67387-113">В следующем примере показаны два запроса, возвращающие одни и те же данные.</span><span class="sxs-lookup"><span data-stu-id="67387-113">The following example shows two queries that return the same data.</span></span>


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



<span data-ttu-id="67387-114">Если системное свойство не относится к конкретному запросу, оно содержит **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="67387-114">If a system property is not relevant for a specific query, it contains **NULL**.</span></span> <span data-ttu-id="67387-115">Например, значение системного свойства **\_ \_ релпас** равно **null** для всех запросов событий.</span><span class="sxs-lookup"><span data-stu-id="67387-115">For example, the value of the **\_\_RELPATH** system property is **NULL** for all event queries.</span></span>

<span data-ttu-id="67387-116">Следующие системные свойства содержат **значения NULL** для запросов событий:</span><span class="sxs-lookup"><span data-stu-id="67387-116">The following system properties contain **NULL** for event queries:</span></span>

<dl> <span data-ttu-id="67387-117">\_\_Имен</span><span class="sxs-lookup"><span data-stu-id="67387-117">\_\_Namespace</span></span>  
<span data-ttu-id="67387-118">\_\_Путь</span><span class="sxs-lookup"><span data-stu-id="67387-118">\_\_Path</span></span>  
<span data-ttu-id="67387-119">\_\_релпас</span><span class="sxs-lookup"><span data-stu-id="67387-119">\_\_RelPath</span></span>  
<span data-ttu-id="67387-120">\_\_Сервером</span><span class="sxs-lookup"><span data-stu-id="67387-120">\_\_Server</span></span>  
</dl>

<span data-ttu-id="67387-121">Дополнительные сведения см. в разделе [Справочник по системным свойствам WMI](wmi-system-properties.md).</span><span class="sxs-lookup"><span data-stu-id="67387-121">For more information, see [WMI System Property Reference](wmi-system-properties.md).</span></span>

<span data-ttu-id="67387-122">Все запросы событий могут включать необязательное [предложение WHERE](where-clause.md), но предложения WHERE в основном используются потребителями для указания дополнительной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="67387-122">All event queries can include an optional [WHERE clause](where-clause.md), but WHERE clauses are primarily used by consumers to specify additional filtering.</span></span> <span data-ttu-id="67387-123">Настоятельно рекомендуется, чтобы потребители всегда указали предложение WHERE.</span><span class="sxs-lookup"><span data-stu-id="67387-123">It is strongly recommended that consumers always specify a WHERE clause.</span></span> <span data-ttu-id="67387-124">Затраты на сложный запрос минимальны по сравнению с затратами на доставку и обработку ненужных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="67387-124">The cost of a complex query is minimal compared to the cost of delivering and processing unneeded notifications.</span></span>

<span data-ttu-id="67387-125">В следующем примере показан запрос, запрашивающий уведомления обо всех событиях изменения экземпляра, которые влияют на гипотетический класс **емаилевент**.</span><span class="sxs-lookup"><span data-stu-id="67387-125">The following example shows a query that requests notifications of all instance modification events that affect the hypothetical class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent
```



<span data-ttu-id="67387-126">Если события, связанные с **емаилевент** , происходят часто, потребитель передается с событиями.</span><span class="sxs-lookup"><span data-stu-id="67387-126">If events associated with **EmailEvent** occur frequently, the consumer is flooded with events.</span></span> <span data-ttu-id="67387-127">Более эффективный запрос запрашивает события только в том случае, если определенные условия используют свойства указанного класса, например, если уровень важности имеет значение High.</span><span class="sxs-lookup"><span data-stu-id="67387-127">A better query requests events only when specific conditions use properties of the class specified, such as when the importance level is high.</span></span>

<span data-ttu-id="67387-128">В следующем примере показан запрос, который можно использовать, если **емаилимпортанце** является свойством класса **емаилевент**.</span><span class="sxs-lookup"><span data-stu-id="67387-128">The following example shows the query you can use if **EmailImportance** is a property of the class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



<span data-ttu-id="67387-129">Обратите внимание, что инструментарий WMI может отклонять запрос по ряду причин.</span><span class="sxs-lookup"><span data-stu-id="67387-129">Note that WMI can reject a query for a number of reasons.</span></span> <span data-ttu-id="67387-130">Например, запрос может быть слишком сложным или ресурсоемким для оценки.</span><span class="sxs-lookup"><span data-stu-id="67387-130">For example, the query can be too complex or resource-intensive for evaluation.</span></span> <span data-ttu-id="67387-131">В этом случае Инструментарий WMI возвращает определенные коды ошибок, например **, \_ \_ Недопустимый \_ запрос WBEM E**.</span><span class="sxs-lookup"><span data-stu-id="67387-131">When this occurs, WMI returns specific error codes, such as **WBEM\_E\_INVALID\_QUERY**.</span></span>

<span data-ttu-id="67387-132">Свойства внедренных объектов можно использовать в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="67387-132">Properties of embedded objects can be used in the WHERE clause.</span></span>

<span data-ttu-id="67387-133">В следующем примере показано, как запросить объекты, где свойство **TargetInstance** класса System [**\_ \_ инстанцемодификатионевент**](--instancemodificationevent.md) является внедренным объектом [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , а **Freespace** — свойством **Win32 \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="67387-133">The following example shows how to query for objects where the **TargetInstance** property of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system class is an embedded [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) object and **FreeSpace** is a property of **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a><span data-ttu-id="67387-134">Примеры</span><span class="sxs-lookup"><span data-stu-id="67387-134">Examples</span></span>

<span data-ttu-id="67387-135">[Событие создания монитора для определенного имени процесса](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) в образце VBScript на сайте TechNet использует инструкцию SELECT для отслеживания событий создания экземпляра WMI для \_ процесса Win32, фильтрации по определенному имени процесса.</span><span class="sxs-lookup"><span data-stu-id="67387-135">The [Monitor creation event for specific process name](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) VBScript sample on TechNet uses the SELECT statement to monitor WMI instance creation events for Win32\_Process, filtering for a specific process name.</span></span>

 

 
