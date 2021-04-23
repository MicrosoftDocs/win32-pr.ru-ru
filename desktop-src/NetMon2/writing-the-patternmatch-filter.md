---
description: Фильтр соответствия шаблону уведомляет драйвер о принятии кадров с конкретным шаблоном в указанном смещении.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Написание фильтра ПАТТЕРНМАТЧ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673572"
---
# <a name="writing-the-patternmatch-filter"></a><span data-ttu-id="60e88-103">Написание фильтра ПАТТЕРНМАТЧ</span><span class="sxs-lookup"><span data-stu-id="60e88-103">Writing the PATTERNMATCH Filter</span></span>

<span data-ttu-id="60e88-104">Фильтр соответствия шаблону уведомляет драйвер о принятии кадров с конкретным шаблоном в указанном смещении.</span><span class="sxs-lookup"><span data-stu-id="60e88-104">The pattern match filter notifies the driver to accept frames that have a specific pattern at a specific offset.</span></span> <span data-ttu-id="60e88-105">Можно указать не более четырех подробных совпадений шаблонов, которые можно объединить в логические операторы AND или OR для оценки драйвера сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="60e88-105">You can specify a maximum of four detailed pattern matches, which can be combined in logical AND or OR statements for Network Monitor driver evaluation.</span></span>

<span data-ttu-id="60e88-106">Для реализации совпадений шаблонов используйте следующие структуры сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="60e88-106">To implement pattern matches, use the following Network Monitor structures:</span></span>

-   [<span data-ttu-id="60e88-107">**ВЫРАЖЕНИЕ**</span><span class="sxs-lookup"><span data-stu-id="60e88-107">**EXPRESSION**</span></span>](expression.md)
-   [<span data-ttu-id="60e88-108">**андексп**</span><span class="sxs-lookup"><span data-stu-id="60e88-108">**ANDEXP**</span></span>](andexp.md)
-   [<span data-ttu-id="60e88-109">**паттернматч**</span><span class="sxs-lookup"><span data-stu-id="60e88-109">**PATTERNMATCH**</span></span>](patternmatch.md)

<span data-ttu-id="60e88-110">Чтобы вычислить оператор **или** , объедините два-четыре шаблона в структуру [**андексп**](andexp.md) (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3).</span><span class="sxs-lookup"><span data-stu-id="60e88-110">To evaluate an **OR** statement, combine two to four pattern matches an [**ANDEXP**](andexp.md) structure (PatternMatch1 \|\| PatternMatch2 \|\| PatternMatch3).</span></span> <span data-ttu-id="60e88-111">Чтобы вычислить оператор AND, объедините одну-четыре структуры **андексп** и структуру [**выражения**](expression.md) (AndExp1 && AndExp2).</span><span class="sxs-lookup"><span data-stu-id="60e88-111">To evaluate an AND statement, combine one to four **ANDEXP** structures and an [**EXPRESSION**](expression.md) structure (AndExp1 && AndExp2).</span></span>

## <a name="pattern-match-definitions"></a><span data-ttu-id="60e88-112">Определения соответствия шаблону</span><span class="sxs-lookup"><span data-stu-id="60e88-112">Pattern Match Definitions</span></span>

<span data-ttu-id="60e88-113">Одно соответствие шаблона определяется структурой [**паттернматч**](patternmatch.md) .</span><span class="sxs-lookup"><span data-stu-id="60e88-113">A single pattern match is defined by the [**PATTERNMATCH**](patternmatch.md) structure.</span></span> <span data-ttu-id="60e88-114">Отдельное соответствие может использоваться одним из двух способов.</span><span class="sxs-lookup"><span data-stu-id="60e88-114">An individual match can operate in one of two ways.</span></span>

<span data-ttu-id="60e88-115">Как правило, драйвер берет на себя смещение (которое может быть СМЕЩЕНо \_ \_ относительно \_ \_ кадра, смещение относительно \_ \_ \_ \_ эффективного \_ протокола, смещение относительно \_ \_ \_ \_ IPX или смещение \_ \_ относительно \_ \_ IP-адреса) и начать подсчет.</span><span class="sxs-lookup"><span data-stu-id="60e88-115">Normally, the driver will take the offset basis (which can be OFFSET\_BASIS\_RELATIVE\_TO\_FRAME, OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL, OFFSET\_BASIS\_RELATIVE\_TO\_IPX, or OFFSET\_BASIS\_RELATIVE\_TO\_IP) and start counting there.</span></span> <span data-ttu-id="60e88-116">Драйвер будет подсчитывать из него байты смещения, а затем сопоставлять найденные данные с первой длиной байтов в **паттернтоматч**.</span><span class="sxs-lookup"><span data-stu-id="60e88-116">The driver will count offset bytes from there and then match the data it finds with the first length bytes in **PatternToMatch**.</span></span> <span data-ttu-id="60e88-117">Если они совпадают и \_ флаг соответствия шаблону \_ \_ не установлен, то этот шаблон передается.</span><span class="sxs-lookup"><span data-stu-id="60e88-117">If they are the same, and the PATTERN\_MATCH\_FLAGS\_NOT flag is not set, then this pattern passes.</span></span> <span data-ttu-id="60e88-118">Если они отличаются и \_ \_ Флаги соответствия шаблону \_ не заданы, шаблон передается.</span><span class="sxs-lookup"><span data-stu-id="60e88-118">If they are different and the PATTERN\_MATCH\_FLAGS\_NOT has been set, the pattern passes.</span></span> <span data-ttu-id="60e88-119">В противном случае этот шаблон завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60e88-119">Otherwise this pattern fails.</span></span>

<span data-ttu-id="60e88-120">Или сделайте так:</span><span class="sxs-lookup"><span data-stu-id="60e88-120">Or:</span></span>

<span data-ttu-id="60e88-121">Если \_ установлен флаг соответствия шаблону \_ \_ порт \_ указан, а для базиса задано смещение \_ \_ относительно \_ \_ IPX или смещения \_ \_ относительно \_ \_ IP, сравнение является более сложным.</span><span class="sxs-lookup"><span data-stu-id="60e88-121">If the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag is set, and the basis is set to OFFSET\_BASIS\_RELATIVE\_TO\_IPX or OFFSET\_BASIS\_RELATIVE\_TO\_IP, the comparison is more complex.</span></span> <span data-ttu-id="60e88-122">Во-первых, драйвер гарантирует, что в нем используется протокол offset, а затем драйвер проверяет, соответствует ли указанный порт порту в кадре.</span><span class="sxs-lookup"><span data-stu-id="60e88-122">First, the driver ensures that the offset basis protocol is there, then the driver verifies that the specified port matches the port in the frame.</span></span> <span data-ttu-id="60e88-123">Наконец, драйвер гарантирует, что элемент **паттернтоматч** будет соответствовать, как и раньше, за исключением смещения от конца IP-адреса или IPX.</span><span class="sxs-lookup"><span data-stu-id="60e88-123">Finally the driver ensures that the **PatternToMatch** member matches as before, with the exception that the offset is from the end of IP or IPX.</span></span> <span data-ttu-id="60e88-124">Обратите внимание, что если базис не является одним из этих двух, то \_ флаг соответствия шаблону порта, указанный в параметре, \_ \_ \_ будет проигнорирован, и шаблон будет оцениваться так, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="60e88-124">Note that if the basis is not one of these two, then the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag will be ignored, and the pattern will be evaluated as above.</span></span>

<span data-ttu-id="60e88-125">Для вычисления одного соответствия шаблону структура [**выражения**](expression.md) должна иметь один элемент **андексп** , содержащий одно соответствие шаблона.</span><span class="sxs-lookup"><span data-stu-id="60e88-125">To evaluate a single pattern match, an [**EXPRESSION**](expression.md) structure must have one **AndExp** member containing a single pattern match.</span></span>

<span data-ttu-id="60e88-126">Создание фильтра соответствия шаблону включает создание структур [**паттернматч**](patternmatch.md) и логическое объединение их с структурами [**Expression**](expression.md) и [**андексп**](andexp.md) .</span><span class="sxs-lookup"><span data-stu-id="60e88-126">Building the pattern match filter involves creating [**PATTERNMATCH**](patternmatch.md) structures and logically combining them with [**EXPRESSION**](expression.md) and [**ANDEXP**](andexp.md) structures.</span></span>

<span data-ttu-id="60e88-127">**Написание фильтра ПАТТЕРНМАТЧ**</span><span class="sxs-lookup"><span data-stu-id="60e88-127">**To write a PATTERNMATCH filter**</span></span>

1.  <span data-ttu-id="60e88-128">В структуре [**андексп**](andexp.md) заполните массив совпадениями шаблона.</span><span class="sxs-lookup"><span data-stu-id="60e88-128">In the [**ANDEXP**](andexp.md) structure, populate the array with pattern matches.</span></span>
2.  <span data-ttu-id="60e88-129">Заполните структуру [**выражения**](expression.md) массивом элементов **андексп** .</span><span class="sxs-lookup"><span data-stu-id="60e88-129">Populate the [**EXPRESSION**](expression.md) structure with an array of **AndExp** members.</span></span>
3.  <span data-ttu-id="60e88-130">Не превышать всего четыре совпадения шаблона для фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="60e88-130">Do not exceed a total of four pattern matches for the capture filter.</span></span>
4.  <span data-ttu-id="60e88-131">В структуре [**паттернматч**](patternmatch.md) выберите тип флага.</span><span class="sxs-lookup"><span data-stu-id="60e88-131">In the [**PATTERNMATCH**](patternmatch.md) structure, select a flag type.</span></span>
5.  <span data-ttu-id="60e88-132">Выберите базис для смещения.</span><span class="sxs-lookup"><span data-stu-id="60e88-132">Select an offset basis.</span></span>
6.  <span data-ttu-id="60e88-133">Перечисление значения порта.</span><span class="sxs-lookup"><span data-stu-id="60e88-133">Enumerate a port value.</span></span>
7.  <span data-ttu-id="60e88-134">Определите значение смещения.</span><span class="sxs-lookup"><span data-stu-id="60e88-134">Define offset value.</span></span>
8.  <span data-ttu-id="60e88-135">Определите длину шаблона.</span><span class="sxs-lookup"><span data-stu-id="60e88-135">Define the pattern length.</span></span>
9.  <span data-ttu-id="60e88-136">Перечисление значения шаблона.</span><span class="sxs-lookup"><span data-stu-id="60e88-136">Enumerate the pattern value.</span></span>

## <a name="patternmatch-examples"></a><span data-ttu-id="60e88-137">Примеры ПАТТЕРНМАТЧ</span><span class="sxs-lookup"><span data-stu-id="60e88-137">PATTERNMATCH Examples</span></span>

<span data-ttu-id="60e88-138">Этот кадр представляет стандартное смещение.</span><span class="sxs-lookup"><span data-stu-id="60e88-138">This frame represents a standard offset.</span></span>

![Стандартный смещенный кадр](images/offs-pat.png)

<span data-ttu-id="60e88-140">Фрагмент кода реализуется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="60e88-140">The code fragment is implemented as:</span></span>

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

<span data-ttu-id="60e88-141">В этом кадре показано смещение, заданное портом (по протоколу IPX).</span><span class="sxs-lookup"><span data-stu-id="60e88-141">This frame depicts a port-specified offset (against IPX).</span></span>

![заданный портом кадр смещения](images/stan-pat.png)

<span data-ttu-id="60e88-143">Пример кода реализуется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="60e88-143">The example code is implemented as:</span></span>

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



