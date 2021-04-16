---
description: Многие из средств отладки, описываемых в этом разделе, реализуются в библиотеке базовых классов DirectShow. Дополнительные сведения см. в разделе базовые классы DirectShow.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Отладка фильтров DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538069"
---
# <a name="debugging-directshow-filters"></a><span data-ttu-id="bc92f-104">Отладка фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="bc92f-104">Debugging DirectShow Filters</span></span>

<span data-ttu-id="bc92f-105">Многие из средств отладки, описываемых в этом разделе, реализуются в библиотеке базовых классов DirectShow.</span><span class="sxs-lookup"><span data-stu-id="bc92f-105">Many of the debugging facilities described in this topic are implemented in the DirectShow base class library.</span></span> <span data-ttu-id="bc92f-106">Дополнительные сведения см. в разделе [базовые классы DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="bc92f-106">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="assertion-checking"></a><span data-ttu-id="bc92f-107">Проверка утверждения</span><span class="sxs-lookup"><span data-stu-id="bc92f-107">Assertion Checking</span></span>

<span data-ttu-id="bc92f-108">Используйте проверку утверждения.</span><span class="sxs-lookup"><span data-stu-id="bc92f-108">Use assertion checking liberally.</span></span> <span data-ttu-id="bc92f-109">Утверждения могут проверять предположения, которые вы вносите в код в отношении предусловий и постусловий.</span><span class="sxs-lookup"><span data-stu-id="bc92f-109">Assertions can verify assumptions that you make in your code about preconditions and postconditions.</span></span> <span data-ttu-id="bc92f-110">DirectShow предоставляет несколько макросов утверждения.</span><span class="sxs-lookup"><span data-stu-id="bc92f-110">DirectShow provides several assertion macros.</span></span> <span data-ttu-id="bc92f-111">Дополнительные сведения см. в разделе [макросы Assert и точка останова](assert-and-breakpoint-macros.md).</span><span class="sxs-lookup"><span data-stu-id="bc92f-111">For more information, see [Assert and Breakpoint Macros](assert-and-breakpoint-macros.md).</span></span>

## <a name="object-names"></a><span data-ttu-id="bc92f-112">Имена объектов</span><span class="sxs-lookup"><span data-stu-id="bc92f-112">Object Names</span></span>

<span data-ttu-id="bc92f-113">В отладочных сборках имеется глобальный список объектов, производных от класса [**кбасеобжект**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="bc92f-113">In debug builds, there is a global list of objects that derive from the [**CBaseObject**](cbaseobject.md) class.</span></span> <span data-ttu-id="bc92f-114">По мере создания объектов они добавляются в список.</span><span class="sxs-lookup"><span data-stu-id="bc92f-114">As objects are created, they are added to the list.</span></span> <span data-ttu-id="bc92f-115">Когда они уничтожаются, они удаляются из списка.</span><span class="sxs-lookup"><span data-stu-id="bc92f-115">When they are destroyed, they are removed from the list.</span></span> <span data-ttu-id="bc92f-116">Чтобы отобразить список этих объектов, вызовите функцию [**дбгдумпобжектрегистер**](dbgdumpobjectregister.md) .</span><span class="sxs-lookup"><span data-stu-id="bc92f-116">To display a list of those objects, call the [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function.</span></span>

<span data-ttu-id="bc92f-117">Метод-конструктор для базового класса [**кбасеобжект**](cbaseobject.md) (и большинства производных от него классов) содержит параметр для имени объекта.</span><span class="sxs-lookup"><span data-stu-id="bc92f-117">The constructor method for the [**CBaseObject**](cbaseobject.md) base class—and most classes derived from it—includes a parameter for the name of the object.</span></span> <span data-ttu-id="bc92f-118">Присвойте объектам уникальные имена для их распознавания.</span><span class="sxs-lookup"><span data-stu-id="bc92f-118">Give your objects unique names to identify them.</span></span> <span data-ttu-id="bc92f-119">При объявлении имени используйте макрос [**Name**](name.md) , чтобы имя было выделено только в отладочных сборках.</span><span class="sxs-lookup"><span data-stu-id="bc92f-119">Use the [**NAME**](name.md) macro when you declare the name, so that the name is allocated only in debug builds.</span></span> <span data-ttu-id="bc92f-120">В розничных сборках имя принимает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bc92f-120">In retail builds, the name becomes **NULL**.</span></span>

## <a name="debug-logging"></a><span data-ttu-id="bc92f-121">Ведение журнала отладки</span><span class="sxs-lookup"><span data-stu-id="bc92f-121">Debug Logging</span></span>

<span data-ttu-id="bc92f-122">Функция [**дбглог**](dbglog.md) отображает сообщения отладки по мере выполнения программы.</span><span class="sxs-lookup"><span data-stu-id="bc92f-122">The [**DbgLog**](dbglog.md) function displays debugging messages as your program executes.</span></span> <span data-ttu-id="bc92f-123">Эта функция используется для трассировки выполнения приложения или фильтра.</span><span class="sxs-lookup"><span data-stu-id="bc92f-123">Use this function to trace the execution of your application or filter.</span></span> <span data-ttu-id="bc92f-124">Можно регистрировать коды возврата, значения переменных и любые другие важные сведения.</span><span class="sxs-lookup"><span data-stu-id="bc92f-124">You can log return codes, the values of variables, and any other relevant information.</span></span>

<span data-ttu-id="bc92f-125">Каждое сообщение отладки имеет тип, например \_ Трассировка журнала или ошибка журнала \_ , и уровень отладки, указывающий важность сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc92f-125">Every debug message has a type, such as LOG\_TRACE or LOG\_ERROR, and a debug level, which indicates the importance of the message.</span></span> <span data-ttu-id="bc92f-126">Сообщения с более низким уровнем отладки более важны, чем более высокие уровни.</span><span class="sxs-lookup"><span data-stu-id="bc92f-126">Messages with lower debug levels are more important than those with higher levels.</span></span>

<span data-ttu-id="bc92f-127">В следующем примере гипотетический фильтр отключает ПИН-код от массива закрепления.</span><span class="sxs-lookup"><span data-stu-id="bc92f-127">In the following example, a hypothetical filter disconnects a pin from an array of pins.</span></span> <span data-ttu-id="bc92f-128">Если попытки отключения завершились неуспешнее, фильтр отображает \_ сообщение трассировки журнала.</span><span class="sxs-lookup"><span data-stu-id="bc92f-128">If the disconnect attempt succeeds, the filter displays a LOG\_TRACE message.</span></span> <span data-ttu-id="bc92f-129">Если попытка не удалась, отображается \_ сообщение об ошибке журнала:</span><span class="sxs-lookup"><span data-stu-id="bc92f-129">If the attempt fails, it displays a LOG\_ERROR message:</span></span>


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



<span data-ttu-id="bc92f-130">При отладке можно задать уровень отладки для каждого типа сообщений.</span><span class="sxs-lookup"><span data-stu-id="bc92f-130">When you are debugging, you can set the debug level for each message type.</span></span> <span data-ttu-id="bc92f-131">Кроме того, каждый модуль (DLL или исполняемый файл) поддерживает собственные уровни отладки.</span><span class="sxs-lookup"><span data-stu-id="bc92f-131">Also, each module (DLL or executable) maintains its own debugging levels.</span></span> <span data-ttu-id="bc92f-132">При тестировании фильтра Повысьте уровень отладки для библиотеки DLL, содержащей фильтр.</span><span class="sxs-lookup"><span data-stu-id="bc92f-132">If you are testing a filter, raise the debug levels for the DLL that contains the filter.</span></span>

<span data-ttu-id="bc92f-133">Дополнительные сведения см. в разделе [отладочные функции вывода](debug-output-functions.md).</span><span class="sxs-lookup"><span data-stu-id="bc92f-133">For more information, see [Debug Output Functions](debug-output-functions.md).</span></span>

## <a name="critical-sections"></a><span data-ttu-id="bc92f-134">Критические разделы</span><span class="sxs-lookup"><span data-stu-id="bc92f-134">Critical Sections</span></span>

<span data-ttu-id="bc92f-135">Чтобы упростить отслеживание взаимоблокировок, включите утверждения, которые определяют, владеет ли вызывающий код заданный критический раздел.</span><span class="sxs-lookup"><span data-stu-id="bc92f-135">To make deadlocks easier to track, include assertions that determine whether the calling code owns a given critical section.</span></span> <span data-ttu-id="bc92f-136">Функции [**критчеккин**](critcheckin.md) и [**критчеккаут**](critcheckout.md) указывают, владеет ли вызывающий поток критическим разделом.</span><span class="sxs-lookup"><span data-stu-id="bc92f-136">The [**CritCheckIn**](critcheckin.md) and [**CritCheckOut**](critcheckout.md) functions indicate whether the calling thread owns a critical section.</span></span> <span data-ttu-id="bc92f-137">Как правило, эти функции вызываются внутри макроса Assert.</span><span class="sxs-lookup"><span data-stu-id="bc92f-137">Typically, you would call these functions from inside an assert macro.</span></span>

<span data-ttu-id="bc92f-138">Можно также использовать функцию [**дбглокктраце**](dbglocktrace.md) для трассировки при удержании или освобождении критических секций.</span><span class="sxs-lookup"><span data-stu-id="bc92f-138">You can also use the [**DbgLockTrace**](dbglocktrace.md) function to trace when critical sections are held or released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc92f-139">См. также</span><span class="sxs-lookup"><span data-stu-id="bc92f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc92f-140">Отладка в DirectShow</span><span class="sxs-lookup"><span data-stu-id="bc92f-140">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



