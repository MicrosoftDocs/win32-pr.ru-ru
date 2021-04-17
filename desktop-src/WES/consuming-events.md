---
title: Использование событий (журнал событий Windows)
description: События можно использовать из каналов или из файлов журнала.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb3fb1b36a0cd4ecf836a8893bc1abc14e46451
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691738"
---
# <a name="consuming-events-windows-event-log"></a><span data-ttu-id="dd1fc-103">Использование событий (журнал событий Windows)</span><span class="sxs-lookup"><span data-stu-id="dd1fc-103">Consuming Events (Windows Event Log)</span></span>

<span data-ttu-id="dd1fc-104">События можно использовать из каналов или из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-104">You can consume events from channels or from log files.</span></span> <span data-ttu-id="dd1fc-105">Для использования событий можно использовать все события или указать выражение XPath, определяющее события, которые требуется использовать.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-105">To consume events, you can consume all events or you can specify an XPath expression that identifies the events that you want to consume.</span></span> <span data-ttu-id="dd1fc-106">Сведения о том, как определить элементы и атрибуты события, которое можно использовать в выражении XPath, см. в разделе [схема событий](eventschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="dd1fc-106">To determine the elements and attributes of an event that you can use in your XPath expression, see [Event Schema](eventschema-schema.md).</span></span>

<span data-ttu-id="dd1fc-107">Журнал событий Windows поддерживает подмножество XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-107">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="dd1fc-108">Дополнительные сведения об ограничениях см. в разделе [ограничения XPath 1,0](#xpath-10-limitations).</span><span class="sxs-lookup"><span data-stu-id="dd1fc-108">For details on the limitations, see [XPath 1.0 limitations](#xpath-10-limitations).</span></span>

<span data-ttu-id="dd1fc-109">В следующих примерах показаны простые выражения XPath.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-109">The following examples show simple XPath expressions.</span></span>


```XML
// The following query selects all events from the channel or log file
XPath Query: *

// The following query selects all the LowOnMemory events from the channel or log file
XPath Query: *[UserData/LowOnMemory]

// The following query selects all events with a severity level of 1 (Critical) from the channel or log file
XPath Query: *[System/Level=1]

// The following query shows a compound expression that selects all events from the channel or log file
// where the printer's name is MyPrinter and severity level is 1.
XPath Query: *[UserData/*/PrinterName="MyPrinter" and System/Level=1]

// The following query selects all events from the channel or log file where the severity level is
// less than or equal to 3 and the event occurred in the last 24 hour period.
XPath Query: *[System[(Level <= 3) and TimeCreated[timediff(@SystemTime) <= 86400000]]]
```



<span data-ttu-id="dd1fc-110">Выражения XPath можно использовать непосредственно при вызове функций [**евткуери**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) или [**евтсубскрибе**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) , либо можно использовать структурированный XML-запрос, содержащий выражение XPath.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-110">You can use the XPath expressions directly when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions or you can use a structured XML query that contains the XPath expression.</span></span> <span data-ttu-id="dd1fc-111">Для простых запросов, которые запрашивают события из одного источника, использование выражения XPath является точным.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-111">For simple queries that query events from a single source, using an XPath expression is fine.</span></span> <span data-ttu-id="dd1fc-112">Если выражение XPath является составным выражением, содержащим более 20 выражений или выполняющих запросы к событиям из нескольких источников, необходимо использовать структурированный XML-запрос.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-112">If the XPath expression is a compound expression that contains more than 20 expressions or you are querying for events from multiple sources, then you must use a structured XML query.</span></span> <span data-ttu-id="dd1fc-113">Дополнительные сведения об элементах структурированного XML-запроса см. в разделе [Схема запроса](queryschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="dd1fc-113">For details on the elements of a structured XML query, see [Query Schema](queryschema-schema.md).</span></span>

<span data-ttu-id="dd1fc-114">Структурированный запрос определяет источник событий и один или несколько селекторов или подавления.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-114">A structured query identifies the source of the events and one or more selectors or suppressors.</span></span> <span data-ttu-id="dd1fc-115">Селектор содержит выражения XPath, выбирающие события из источника, а суппрессор содержит выражение XPath, которое предотвращает выбор событий.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-115">A selector contains an XPath expressions that selects events from the source and a suppressor contains an XPath expression that prevents events from being selected.</span></span> <span data-ttu-id="dd1fc-116">Можно выбрать события из нескольких источников.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-116">You can select events from more than one source.</span></span> <span data-ttu-id="dd1fc-117">Если селектор и суппрессор обозначают одно и то же событие, это событие не включается в результат.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-117">If a selector and suppressor identify the same event, the event is not included in the result.</span></span>

<span data-ttu-id="dd1fc-118">Ниже показан структурированный запрос XML, указывающий набор селекторов и подавления.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-118">The following shows a structured XML query that specifies a set of selectors and suppressors.</span></span>


```XML
<QueryList>
  <Query Id="0">
    <Select Path="Application">
        *[System[(Level <= 3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
  </Query>
</QueryList>
```



<span data-ttu-id="dd1fc-119">Результирующий набор запроса не содержит моментальный снимок событий во время запроса.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-119">The result set from the query does not contain a snapshot of the events at the time of the query.</span></span> <span data-ttu-id="dd1fc-120">Вместо этого результирующий набор включает события во время запроса и также содержит все новые события, которые вызываются в соответствии с критериями запроса во время перечисления результатов.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-120">Instead, the result set includes the events at the time of the query and will also contain all new events that are raised that match the query criteria while you are enumerating the results.</span></span>

> [!Note]  
> <span data-ttu-id="dd1fc-121">Порядок событий сохраняется для событий, записываемых тем же потоком.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-121">The order of the events is preserved for events that are written by the same thread.</span></span> <span data-ttu-id="dd1fc-122">Однако события, записываемые отдельными потоками на разных процессорах компьютера с несколькими процессорами, могут отображаться неупорядоченно.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-122">However, it is possible for events written by separate threads on different processors of a multiple processor computer to appear out of order.</span></span>

 

<span data-ttu-id="dd1fc-123">Дополнительные сведения о потреблении событий см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="dd1fc-123">For details on consuming events, see the following topics:</span></span>

-   [<span data-ttu-id="dd1fc-124">Запрос событий</span><span class="sxs-lookup"><span data-stu-id="dd1fc-124">Querying for Events</span></span>](querying-for-events.md)
-   [<span data-ttu-id="dd1fc-125">Подписка на события</span><span class="sxs-lookup"><span data-stu-id="dd1fc-125">Subscribing to Events</span></span>](subscribing-to-events.md)
-   [<span data-ttu-id="dd1fc-126">События отрисовки</span><span class="sxs-lookup"><span data-stu-id="dd1fc-126">Rendering Events</span></span>](rendering-events.md)
-   [<span data-ttu-id="dd1fc-127">Форматирование сообщений о событиях</span><span class="sxs-lookup"><span data-stu-id="dd1fc-127">Formatting Event Messages</span></span>](formatting-event-messages.md)
-   [<span data-ttu-id="dd1fc-128">События закладок</span><span class="sxs-lookup"><span data-stu-id="dd1fc-128">Bookmarking Events</span></span>](bookmarking-events.md)

<span data-ttu-id="dd1fc-129">Ниже перечислены стандартные средства для использования событий.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-129">The standard end user tools for consuming event are:</span></span>

-   <span data-ttu-id="dd1fc-130">[Просмотр событий](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="dd1fc-130">[Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span></span>
-   <span data-ttu-id="dd1fc-131">Командлет [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dd1fc-131">The Windows PowerShell [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) cmdlet</span></span>
-   [<span data-ttu-id="dd1fc-132">**Средств**</span><span class="sxs-lookup"><span data-stu-id="dd1fc-132">**WevtUtil**</span></span>](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a><span data-ttu-id="dd1fc-133">Ограничения XPath 1,0</span><span class="sxs-lookup"><span data-stu-id="dd1fc-133">XPath 1.0 limitations</span></span>

<span data-ttu-id="dd1fc-134">Журнал событий Windows поддерживает подмножество XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-134">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="dd1fc-135">Основное ограничение заключается в том, что селектором событий могут быть выбраны только элементы XML, представляющие события.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-135">The primary restriction is that only XML elements that represent events can be selected by an event selector.</span></span> <span data-ttu-id="dd1fc-136">Запрос XPath, который не выбирает событие, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-136">An XPath query that does not select an event is not valid.</span></span> <span data-ttu-id="dd1fc-137">Все допустимые пути селектора начинаются с \* или "Event".</span><span class="sxs-lookup"><span data-stu-id="dd1fc-137">All valid selector paths start with \* or "Event".</span></span> <span data-ttu-id="dd1fc-138">Все пути расположения работают на узлах событий и состоят из ряда шагов.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-138">All location paths operate on the event nodes and are composed of a series of steps.</span></span> <span data-ttu-id="dd1fc-139">Каждый шаг представляет собой структуру из трех частей: ось, тест узла и предикат.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-139">Each step is a structure of three parts: the axis, node test, and predicate.</span></span> <span data-ttu-id="dd1fc-140">Дополнительные сведения об этих частях и о XPath 1,0 см. в разделе [язык XML-путей (XPath)](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="dd1fc-140">For more information about these parts and about XPath 1.0, see [XML Path Language (XPath)](https://www.w3.org/TR/xpath).</span></span> <span data-ttu-id="dd1fc-141">В журнале событий Windows в выражение помещаются следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="dd1fc-141">Windows Event Log places the following restrictions on the expression:</span></span>

-   <span data-ttu-id="dd1fc-142">Axis: поддерживаются только дочерний элемент (по умолчанию) и атрибут (и его сокращенная ось "@").</span><span class="sxs-lookup"><span data-stu-id="dd1fc-142">Axis: Only the Child (default) and Attribute (and its shorthand "@") axis are supported.</span></span>
-   <span data-ttu-id="dd1fc-143">Проверки узлов. поддерживаются только имена узлов и тесты NCName.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-143">Node Tests: Only node names and NCName tests are supported.</span></span> <span data-ttu-id="dd1fc-144">\*Поддерживается символ "", который выбирает любой символ.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-144">The "\*" character, which selects any character, is supported.</span></span>
-   <span data-ttu-id="dd1fc-145">Предикаты. любое допустимое выражение XPath допустимо, если пути к расположению соответствуют следующим ограничениям.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-145">Predicates: Any valid XPath expression is acceptable if the location paths conform to the following restrictions:</span></span>
    -   <span data-ttu-id="dd1fc-146">Поддерживаются **стандартные операторы,** **и, and**, =,! =, <=, <, >=, > и круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-146">Standard operators **OR**, **AND**, =, !=, <=, <, >=, >, and parentheses are supported.</span></span>
    -   <span data-ttu-id="dd1fc-147">Создание строкового значения для имени узла не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-147">Generating a string value for a node name is not supported.</span></span>
    -   <span data-ttu-id="dd1fc-148">Вычисление в обратном порядке не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-148">Evaluation in reverse order is not supported.</span></span>
    -   <span data-ttu-id="dd1fc-149">Наборы узлов не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-149">Node sets are not supported.</span></span>
    -   <span data-ttu-id="dd1fc-150">Область видимости пространства имен не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-150">Namespace scoping is not supported.</span></span>
    -   <span data-ttu-id="dd1fc-151">Узлы пространства имен, обработки и комментариев не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-151">Namespace, processing, and comment nodes are not supported.</span></span>
    -   <span data-ttu-id="dd1fc-152">Размер контекста не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-152">Context size is not supported.</span></span>
    -   <span data-ttu-id="dd1fc-153">Привязки переменных не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-153">Variable bindings are not supported.</span></span>
    -   <span data-ttu-id="dd1fc-154">Функция позиционирования и ее сокращенная ссылка на массив поддерживаются (только на конечных узлах).</span><span class="sxs-lookup"><span data-stu-id="dd1fc-154">The position function, and its shorthand array reference, is supported (on leaf nodes only).</span></span>
    -   <span data-ttu-id="dd1fc-155">Поддерживается функция Band.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-155">The Band function is supported.</span></span> <span data-ttu-id="dd1fc-156">Функция выполняет побитовую операцию и для двух целочисленных аргументов числа.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-156">The function performs a bitwise AND for two integer number arguments.</span></span> <span data-ttu-id="dd1fc-157">Если результат побитового и не равен нулю, функция возвращает значение true; в противном случае функция возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-157">If the result of the bitwise AND is nonzero, the function evaluates to true; otherwise, the function evaluates to false.</span></span>
    -   <span data-ttu-id="dd1fc-158">Поддерживается функция тимедифф.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-158">The timediff function is supported.</span></span> <span data-ttu-id="dd1fc-159">Функция вычислит разницу между вторым аргументом и первым аргументом.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-159">The function computes the difference between the second argument and the first argument.</span></span> <span data-ttu-id="dd1fc-160">Один из аргументов должен быть литеральным числом.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-160">One of the arguments must be a literal number.</span></span> <span data-ttu-id="dd1fc-161">Аргументы должны использовать представление FILETIME.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-161">The arguments must use FILETIME representation.</span></span> <span data-ttu-id="dd1fc-162">Результатом является число миллисекунд между двумя значениями времени.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-162">The result is the number of milliseconds between the two times.</span></span> <span data-ttu-id="dd1fc-163">Результат является положительным, если второй аргумент представляет более позднее время; в противном случае это отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-163">The result is positive if the second argument represents a later time; otherwise, it is negative.</span></span> <span data-ttu-id="dd1fc-164">Если второй аргумент не указан, используется текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="dd1fc-164">When the second argument is not provided, the current system time is used.</span></span>

 

 
