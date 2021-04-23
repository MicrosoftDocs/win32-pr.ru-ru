---
description: Перечисления обычно используют значительный объем системных ресурсов.
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: Повышение производительности перечисления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265602"
---
# <a name="improving-enumeration-performance"></a><span data-ttu-id="37e26-103">Повышение производительности перечисления</span><span class="sxs-lookup"><span data-stu-id="37e26-103">Improving Enumeration Performance</span></span>

<span data-ttu-id="37e26-104">Перечисления обычно используют значительный объем системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37e26-104">Enumerations tend to use a significant amount of system resources.</span></span> <span data-ttu-id="37e26-105">Поэтому следует попытаться оптимизировать процесс перечисления WMI, если планируется выполнять перечисления для большой группы.</span><span class="sxs-lookup"><span data-stu-id="37e26-105">Therefore, you should try to optimize the WMI enumeration process if you plan on performing enumerations on a large group.</span></span> <span data-ttu-id="37e26-106">Скрипты также могут использовать запрос, чтобы избежать снижения производительности в операциях "For Each.... Next" с большим набором.</span><span class="sxs-lookup"><span data-stu-id="37e26-106">Scripts can also use a query to avoid performance degradation in "For each….Next" operations with a large set.</span></span> <span data-ttu-id="37e26-107">Дополнительные сведения см. в разделе [запрос WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="37e26-107">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="37e26-108">Следующая процедура описывает, как повысить производительность перечисления.</span><span class="sxs-lookup"><span data-stu-id="37e26-108">The following procedure describes how to improve enumeration performance.</span></span>

<span data-ttu-id="37e26-109">**Повышение производительности перечисления**</span><span class="sxs-lookup"><span data-stu-id="37e26-109">**To improve enumeration performance**</span></span>

1.  <span data-ttu-id="37e26-110">Установите параметр *лфлагс* , чтобы разрешить семисинчронаус возвращать данные с помощью перечислителя, который удаляет каждый элемент из WMI по мере его доставки.</span><span class="sxs-lookup"><span data-stu-id="37e26-110">Set the *lFlags* parameter to allow semisynchronous return of the data with an enumerator that discards each item from WMI as it is delivered.</span></span> <span data-ttu-id="37e26-111">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="37e26-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="37e26-112">В следующем примере кода C++ показано, как использовать **флаг WBEM \_ , \_ возвращающий \_** флаги Immediate и **WBEM, \_ \_ \_ только** флаги forward.</span><span class="sxs-lookup"><span data-stu-id="37e26-112">The following C++ code example shows how to use the **WBEM\_FLAG\_RETURN\_IMMEDIATE** and **WBEM\_FLAG\_FORWARD\_ONLY** flags.</span></span>

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    <span data-ttu-id="37e26-113">В VBScript или Visual Basic используйте флаги скрипта **вбемфлагретурниммедиатели** и **вбемфлагфорвардонли** из [вбемфлаженум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="37e26-113">In VBScript or Visual Basic, use the scripting flags **WbemFlagReturnImmediately** and **WbemFlagForwardOnly** from [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span> <span data-ttu-id="37e26-114">Объединенное значение этих флагов — десятичное число 48.</span><span class="sxs-lookup"><span data-stu-id="37e26-114">The combined value of these flags is decimal 48.</span></span>

    <span data-ttu-id="37e26-115">Флаги скрипта и параметров вызывают следующее поведение:</span><span class="sxs-lookup"><span data-stu-id="37e26-115">The scripting and parameter flags cause the following behavior:</span></span>

    -   <span data-ttu-id="37e26-116">**Флаг WBEM \_ \_ возвращает \_ немедленные** или **вбемфлагретурниммедиатели** запросы флагов, семисинчронаус поведение.</span><span class="sxs-lookup"><span data-stu-id="37e26-116">The **WBEM\_FLAG\_RETURN\_IMMEDIATE** or **wbemFlagReturnImmediately** flag requests semisynchronous behavior.</span></span> <span data-ttu-id="37e26-117">Вызов для создания перечислителя немедленно возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="37e26-117">The call to create the enumerator returns immediately.</span></span> <span data-ttu-id="37e26-118">Затем можно начать проход по полученному набору объектов.</span><span class="sxs-lookup"><span data-stu-id="37e26-118">You can then begin to traverse the object set that you receive.</span></span>
    -   <span data-ttu-id="37e26-119">Флаг **WBEM \_ \_ \_ только флаг Forward** или **вбемфлагфорвардонли** запрашивает перечислитель, который нельзя перемотать назад.</span><span class="sxs-lookup"><span data-stu-id="37e26-119">The **WBEM\_FLAG\_FORWARD\_ONLY** flag or **wbemFlagForwardOnly** flag requests an enumerator that you cannot rewind.</span></span> <span data-ttu-id="37e26-120">Это значит, что инструментарий WMI может освободить объект после просмотра объекта.</span><span class="sxs-lookup"><span data-stu-id="37e26-120">That is, WMI can release an object after you view the object.</span></span>

    <span data-ttu-id="37e26-121">В ситуациях, когда перечисление велико, и приложение выполняется очень быстро, использование перечислителей с семисинчронаус позволяет инструментарию WMI разместить на гораздо меньшем количестве объектов, тем самым повышая время отклика и производительность памяти.</span><span class="sxs-lookup"><span data-stu-id="37e26-121">In situations where the enumeration is large and the application is very fast, using forward-only enumerators with semisynchronous processing allows WMI to hold on to far fewer objects, thereby increasing response time and memory performance significantly.</span></span>

    <span data-ttu-id="37e26-122">В следующем примере кода VBScript показано, как выполнить вызов с использованием комбинированных флагов **вбемфлагретурниммедиатели** и **вбемфлагфорвардонли** для получения коллекции событий из журнала событий.</span><span class="sxs-lookup"><span data-stu-id="37e26-122">The following VBScript code example shows how to make a call using the combined **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** flags to obtain a collection of events from an event log.</span></span>

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  <span data-ttu-id="37e26-123">По возможности избегайте использования [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) в C++ или [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md)и вместо этого используйте **ExecQuery**.</span><span class="sxs-lookup"><span data-stu-id="37e26-123">Whenever possible, avoid using [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) in C++ or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), and instead use **ExecQuery**.</span></span>

    <span data-ttu-id="37e26-124">Метод **ExecQuery** запрашивает WMI с помощью технологий баз данных, в то время как [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) или [**SWBEMSERVICES. инстанцесоф**](swbemservices-instancesof.md) перечисляет объекты WMI.</span><span class="sxs-lookup"><span data-stu-id="37e26-124">The **ExecQuery** method queries WMI using database technologies, while [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) enumerates WMI objects.</span></span> <span data-ttu-id="37e26-125">В частности, **ExecQuery** может запрашивать определенные подмножества данных, которые не могут перечислять методы.</span><span class="sxs-lookup"><span data-stu-id="37e26-125">Specifically, **ExecQuery** can request specific subsets of data that the enumerating methods cannot.</span></span>

    <span data-ttu-id="37e26-126">Поскольку некоторые поставщики не имеют возможностей запросов, Инструментарий WMI предоставляет функцию "POST Filter", позволяющую инструментарию WMI удалять экземпляры, не выполняющие спецификаций запроса.</span><span class="sxs-lookup"><span data-stu-id="37e26-126">Because some providers do not have querying capabilities, WMI provides a "post filter" feature that allows WMI to discard instances that do not fulfill a query's specifications.</span></span> <span data-ttu-id="37e26-127">Использует ли конкретный поставщик преимущества этой функции, разработчик поставщика.</span><span class="sxs-lookup"><span data-stu-id="37e26-127">Whether a particular provider takes advantage of this feature is up to the provider author.</span></span>

3.  <span data-ttu-id="37e26-128">Экспериментируйте с различными запросами, чтобы определить, что обеспечивает наилучшую производительность.</span><span class="sxs-lookup"><span data-stu-id="37e26-128">Experiment with different queries to determine what gives you the best performance.</span></span>

    <span data-ttu-id="37e26-129">Например, Инструментарий WMI редко эффективно обрабатывает запросы с предложениями **WHERE** формы Prop1 < "x".</span><span class="sxs-lookup"><span data-stu-id="37e26-129">For example, WMI seldom efficiently processes queries with **WHERE** clauses of the form Prop1 < "x".</span></span> <span data-ttu-id="37e26-130">В отличие от этого, WMI обычно обрабатывает запросы формы KeyProp1 = "x" эффективно.</span><span class="sxs-lookup"><span data-stu-id="37e26-130">In contrast, WMI normally processes queries of the form KeyProp1 = "x" efficiently.</span></span>

<span data-ttu-id="37e26-131">Дополнительные сведения см. в разделе [перечисление WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="37e26-131">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

 

 



