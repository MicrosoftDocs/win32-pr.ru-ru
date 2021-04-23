---
description: Шаг 1.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Шаг 1. Выбор базового класса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4679873e78e75b350335b5294db63579fd41f36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911095"
---
# <a name="step-1-choose-a-base-class"></a><span data-ttu-id="56ef8-104">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="56ef8-104">Step 1.</span></span> <span data-ttu-id="56ef8-105">Выбор базового класса</span><span class="sxs-lookup"><span data-stu-id="56ef8-105">Choose a Base Class</span></span>

<span data-ttu-id="56ef8-106">Это шаг 1 учебника [Создание фильтров преобразования](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="56ef8-106">This is step 1 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="56ef8-107">Предполагая, что вы решили написать фильтр, а не DMO, первым шагом будет выбор базового класса для использования.</span><span class="sxs-lookup"><span data-stu-id="56ef8-107">Assuming that you decide to write a filter and not a DMO, the first step is choosing which base class to use.</span></span> <span data-ttu-id="56ef8-108">Для фильтров преобразования подходят следующие классы:</span><span class="sxs-lookup"><span data-stu-id="56ef8-108">The following classes are appropriate for transform filters:</span></span>

-   <span data-ttu-id="56ef8-109">[**Ктрансформфилтер**](ctransformfilter.md) предназначен для фильтров преобразования, использующих отдельные буферы ввода и вывода.</span><span class="sxs-lookup"><span data-stu-id="56ef8-109">[**CTransformFilter**](ctransformfilter.md) is designed for transform filters that use separate input and output buffers.</span></span> <span data-ttu-id="56ef8-110">Этот тип фильтра иногда называют фильтром преобразования копий.</span><span class="sxs-lookup"><span data-stu-id="56ef8-110">This kind of filter is sometimes called a copy-transform filter.</span></span> <span data-ttu-id="56ef8-111">Когда фильтр преобразования копирования получает образец входных данных, он записывает новые данные в образец вывода и доставляет образец Output к следующему фильтру.</span><span class="sxs-lookup"><span data-stu-id="56ef8-111">When a copy-transform filter receives an input sample, it writes new data to an output sample and delivers the output sample to the next filter.</span></span>
-   <span data-ttu-id="56ef8-112">[**Ктрансинплацефилтер**](ctransinplacefilter.md) предназначен для фильтров, изменяющих данные в исходном буфере, также называемые фильтрами переноса на месте.</span><span class="sxs-lookup"><span data-stu-id="56ef8-112">[**CTransInPlaceFilter**](ctransinplacefilter.md) is designed for filters that modify data in the original buffer, also called trans-in-place filters.</span></span> <span data-ttu-id="56ef8-113">Когда фильтр на месте получает образец, он изменяет данные внутри этого образца и доставляет тот же самый нисходящий пример.</span><span class="sxs-lookup"><span data-stu-id="56ef8-113">When a trans-in-place filter receives a sample, it changes the data inside that sample and delivers the same sample downstream.</span></span> <span data-ttu-id="56ef8-114">Входной и выходной ПИН-код фильтра всегда соединяются с соответствующими типами носителей.</span><span class="sxs-lookup"><span data-stu-id="56ef8-114">The filter's input pin and output pin always connect with matching media types.</span></span>
-   <span data-ttu-id="56ef8-115">[**Квидеотрансформфилтер**](cvideotransformfilter.md) предназначен в первую очередь для видеодекодеров.</span><span class="sxs-lookup"><span data-stu-id="56ef8-115">[**CVideoTransformFilter**](cvideotransformfilter.md) is designed primarily for video decoders.</span></span> <span data-ttu-id="56ef8-116">Он является производным от **ктрансформфилтер**, но включает функции для удаления кадров, если подчиненный модуль подготовки к работе находится позади.</span><span class="sxs-lookup"><span data-stu-id="56ef8-116">It derives from **CTransformFilter**, but includes functionality for dropping frames if the downstream renderer falls behind.</span></span>
-   <span data-ttu-id="56ef8-117">[**Кбасефилтер**](cbasefilter.md) — это универсальный класс фильтра.</span><span class="sxs-lookup"><span data-stu-id="56ef8-117">[**CBaseFilter**](cbasefilter.md) is a generic filter class.</span></span> <span data-ttu-id="56ef8-118">Другие классы в этом списке являются производными от **кбасефилтер**.</span><span class="sxs-lookup"><span data-stu-id="56ef8-118">The other classes in this list all derive from **CBaseFilter**.</span></span> <span data-ttu-id="56ef8-119">Если ни один из них не подходит, можно вернуться к этому классу.</span><span class="sxs-lookup"><span data-stu-id="56ef8-119">If none of them is suitable, you can fall back on this class.</span></span> <span data-ttu-id="56ef8-120">Однако для этого класса также требуется наибольшая часть работы.</span><span class="sxs-lookup"><span data-stu-id="56ef8-120">However, this class also requires the most work on your part.</span></span>
-   <span data-ttu-id="56ef8-121">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="56ef8-121">\[!Important\]</span></span>  
    > <span data-ttu-id="56ef8-122">Преобразования видео на месте могут серьезно повлиять на производительность отрисовки.</span><span class="sxs-lookup"><span data-stu-id="56ef8-122">In-place video transforms can have a serious impact on rendering performance.</span></span> <span data-ttu-id="56ef8-123">Для преобразования на месте требуются операции чтения-изменения и записи в буфер.</span><span class="sxs-lookup"><span data-stu-id="56ef8-123">In-place transforms require read-modify-write operations on the buffer.</span></span> <span data-ttu-id="56ef8-124">Если память находится на графической карте, операции чтения значительно снижаются.</span><span class="sxs-lookup"><span data-stu-id="56ef8-124">If the memory resides on a graphics card, read operations are significantly slower.</span></span> <span data-ttu-id="56ef8-125">Более того, даже преобразование копирования может привести к непредвиденным операциям чтения, если не реализовать ее тщательно.</span><span class="sxs-lookup"><span data-stu-id="56ef8-125">Moreover, even a copy transform can cause unintended read operations if you do not implement it carefully.</span></span> <span data-ttu-id="56ef8-126">Поэтому при написании преобразования видео всегда следует выполнять тестирование производительности.</span><span class="sxs-lookup"><span data-stu-id="56ef8-126">Therefore, you should always do performance testing if you write a video transform.</span></span>

     

<span data-ttu-id="56ef8-127">Для примера кодировщика RLE лучшим выбором является либо **ктрансформфилтер** , либо **квидеотрансформфилтер**.</span><span class="sxs-lookup"><span data-stu-id="56ef8-127">For the example RLE encoder, the best choice is either **CTransformFilter** or **CVideoTransformFilter**.</span></span> <span data-ttu-id="56ef8-128">Фактически различия между ними являются внутренними, поэтому их легко преобразовать из одного в другой.</span><span class="sxs-lookup"><span data-stu-id="56ef8-128">In fact, the differences between them are largely internal, so it is easy to convert from one to the other.</span></span> <span data-ttu-id="56ef8-129">Так как типы мультимедиа должны различаться на двух контактах, класс **ктрансинплацефилтер** не подходит для этого фильтра.</span><span class="sxs-lookup"><span data-stu-id="56ef8-129">Because the media types must be different on the two pins, the **CTransInPlaceFilter** class is not appropriate for this filter.</span></span> <span data-ttu-id="56ef8-130">В этом примере будет использоваться **ктрансформфилтер**.</span><span class="sxs-lookup"><span data-stu-id="56ef8-130">This example will use **CTransformFilter**.</span></span>

<span data-ttu-id="56ef8-131">Далее. [Шаг 2. Объявите класс фильтра](step-2--declare-the-filter-class.md).</span><span class="sxs-lookup"><span data-stu-id="56ef8-131">Next: [Step 2. Declare the Filter Class](step-2--declare-the-filter-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56ef8-132">См. также</span><span class="sxs-lookup"><span data-stu-id="56ef8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56ef8-133">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="56ef8-133">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



