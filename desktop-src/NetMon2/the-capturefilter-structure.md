---
description: В сетевой монитор фильтр записи определяется структурой КАПТУРЕФИЛТЕР.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Структура КАПТУРЕФИЛТЕР
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991198"
---
# <a name="the-capturefilter-structure"></a><span data-ttu-id="4812a-103">Структура КАПТУРЕФИЛТЕР</span><span class="sxs-lookup"><span data-stu-id="4812a-103">The CAPTUREFILTER Structure</span></span>

<span data-ttu-id="4812a-104">В сетевой монитор [фильтр записи](capture-filters.md) определяется структурой [**каптурефилтер**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="4812a-104">In Network Monitor, the [capture filter](capture-filters.md) is defined by the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span> <span data-ttu-id="4812a-105">Отсутствие или сочетание флагов, значений и выражений определяет, какие кадры будут переданы или удалены драйвером сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="4812a-105">The absence or combination of flags, values, and expressions determines which frames will be passed on or dropped by the Network Monitor driver.</span></span> <span data-ttu-id="4812a-106">На следующем рисунке показаны три области анализа фильтра записи: ETYPE/SAP, Address и соответствие шаблону.</span><span class="sxs-lookup"><span data-stu-id="4812a-106">The following illustration shows the three areas of the capture filter analysis: Etype/SAP, address, and pattern match.</span></span>

![три области анализа фильтра записи](images/capfilter.png)

<span data-ttu-id="4812a-108">В следующей таблице перечислены функции каждого элемента фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="4812a-108">The following table lists the function of each capture filter element.</span></span>



| <span data-ttu-id="4812a-109">Filter, элемент</span><span class="sxs-lookup"><span data-stu-id="4812a-109">Filter element</span></span>                                       | <span data-ttu-id="4812a-110">Действие</span><span class="sxs-lookup"><span data-stu-id="4812a-110">Action</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4812a-111">ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="4812a-111">Etype/SAP</span></span>](writing-etypesap-filter-portion.md)     | <span data-ttu-id="4812a-112">Оценивает параметры ETYPE или SAP.</span><span class="sxs-lookup"><span data-stu-id="4812a-112">Evaluates Etype/SAP settings.</span></span> <span data-ttu-id="4812a-113">Сочетание флагов определяет, какие типы или значения параметров включаются или исключаются.</span><span class="sxs-lookup"><span data-stu-id="4812a-113">The combination of flags determines which setting types or values are included or excluded.</span></span>                                                                                    |
| [<span data-ttu-id="4812a-114">Адрес</span><span class="sxs-lookup"><span data-stu-id="4812a-114">Address</span></span>](writing-addresstable-filter-portion.md)   | <span data-ttu-id="4812a-115">Оценивает адреса источника и назначения и пары адресов.</span><span class="sxs-lookup"><span data-stu-id="4812a-115">Evaluates source and destination addresses and address pairs.</span></span> <span data-ttu-id="4812a-116">Различные сочетания флагов определяют, какие отдельные значения или сочетания пар адресов включаются или исключаются.</span><span class="sxs-lookup"><span data-stu-id="4812a-116">Different combinations of flags determine which individual values or combinations of address pairs are included or excluded.</span></span>                   |
| [<span data-ttu-id="4812a-117">Соответствие шаблону</span><span class="sxs-lookup"><span data-stu-id="4812a-117">Pattern Match</span></span>](writing-the-patternmatch-filter.md) | <span data-ttu-id="4812a-118">Определяет сложные соответствия шаблонов внутри фрейма.</span><span class="sxs-lookup"><span data-stu-id="4812a-118">Defines complex pattern matches within a frame.</span></span> <span data-ttu-id="4812a-119">Флаги предоставляются для различных типов и смещений.</span><span class="sxs-lookup"><span data-stu-id="4812a-119">Flags are provided for different types and offsets.</span></span> <span data-ttu-id="4812a-120">Совпадения шаблонов можно объединять с операторами логического оператора AND или OR.</span><span class="sxs-lookup"><span data-stu-id="4812a-120">You can combine pattern matches with logical AND or OR operator statements.</span></span>                              |
| [<span data-ttu-id="4812a-121">Вырезая</span><span class="sxs-lookup"><span data-stu-id="4812a-121">Clipping</span></span>](clipping-a-frame.md)                     | <span data-ttu-id="4812a-122">Обрезает фреймы способом, заданным различными байтовыми значениями.</span><span class="sxs-lookup"><span data-stu-id="4812a-122">Clips frames in a manner specified by various byte values.</span></span> <span data-ttu-id="4812a-123">Можно использовать только этот элемент, чтобы вырезать все кадры или использовать его с другими элементами фильтра записи. Например, чтобы найти и обрезать один кадр.</span><span class="sxs-lookup"><span data-stu-id="4812a-123">You can use only this element to clip all frames or use it with other capture filter elements; for example, to find and then clip a single frame.</span></span> |
| [<span data-ttu-id="4812a-124">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="4812a-124">**Trigger**</span></span>](trigger.md)                           | <span data-ttu-id="4812a-125">Этот элемент фильтра записи устарел.</span><span class="sxs-lookup"><span data-stu-id="4812a-125">This capture filter element is obsolete.</span></span> <span data-ttu-id="4812a-126">Триггеры больше не являются частью фильтра записи; Теперь они содержатся в собственных тегах больших двоичных объектов, которые задаются отдельно.</span><span class="sxs-lookup"><span data-stu-id="4812a-126">Triggers are no longer part of a capture filter; they are now contained in their own BLOB tags, which are specified separately.</span></span>                                     |



 

<span data-ttu-id="4812a-127">Кадр вычисляется по всем трем частям фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="4812a-127">A frame is evaluated against all three portions of the capture filter.</span></span> <span data-ttu-id="4812a-128">Поэтому успешно переданный кадр должен передавать каждый элемент.</span><span class="sxs-lookup"><span data-stu-id="4812a-128">Therefore, a successfully transmitted frame must pass each element.</span></span> <span data-ttu-id="4812a-129">Имейте в виду, что драйвер сетевой монитор оценивает отсутствие любого из трех элементов как **истинное**.</span><span class="sxs-lookup"><span data-stu-id="4812a-129">Be aware that the Network Monitor driver evaluates the absence of any of the three elements as **TRUE**.</span></span> <span data-ttu-id="4812a-130">Например, драйвер оценивает отсутствие раздела ETYPE/SAP, так как «все кадры с любым значением ETYPE/SAP являются допустимыми».</span><span class="sxs-lookup"><span data-stu-id="4812a-130">For example, the driver evaluates the absence of an Etype/SAP section as "ALL frames with the ANY Etype/SAP value are valid."</span></span>

 

 



