---
description: Задайте свойства распределителя в процессе записи фильтра преобразования. Закрепление вывода фильтра преобразования выбирает нисходящий распределитель.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Шаг 4. Задание свойств распределителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ee7d9ecdc85b63ec6bd774a3a47e0e9399dcf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406827"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="c9810-105">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="c9810-105">Step 4.</span></span> <span data-ttu-id="c9810-106">Задание свойств распределителя</span><span class="sxs-lookup"><span data-stu-id="c9810-106">Set Allocator Properties</span></span>

<span data-ttu-id="c9810-107">Это шаг 4 учебника [Создание фильтров преобразования](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="c9810-107">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="c9810-108">Этот шаг не является обязательным для фильтров, производных от **ктрансинплацефилтер**.</span><span class="sxs-lookup"><span data-stu-id="c9810-108">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="c9810-109">После того как два контакта договариваются по типу носителя, они выбирают распределителя для соединения и согласовывают свойства распределителя, такие как размер буфера и количество буферов.</span><span class="sxs-lookup"><span data-stu-id="c9810-109">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="c9810-110">В классе **ктрансформфилтер** есть два распределителя, один для вышестоящего соединения, а другой — для соединения с нижестоящим ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="c9810-110">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="c9810-111">Вышестоящий фильтр выбирает вышестоящий распределитель, а также выбирает свойства распределителя.</span><span class="sxs-lookup"><span data-stu-id="c9810-111">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="c9810-112">Входной ПИН-код принимает любой способ, который принимается в качестве вышестоящего фильтра.</span><span class="sxs-lookup"><span data-stu-id="c9810-112">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="c9810-113">Если необходимо изменить это поведение, переопределите метод [**кбасеинпутпин:: нотифяллокатор**](cbaseinputpin-notifyallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="c9810-113">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="c9810-114">Закрепление вывода фильтра преобразования выбирает нисходящий распределитель.</span><span class="sxs-lookup"><span data-stu-id="c9810-114">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="c9810-115">Он выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c9810-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="c9810-116">Если подчиненный фильтр может предоставить распределитель, то он будет использоваться выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="c9810-116">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="c9810-117">В противном случае выходной ПИН-код создает новый распределитель.</span><span class="sxs-lookup"><span data-stu-id="c9810-117">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="c9810-118">Закрепление вывода получает требования к распределительу подчиненного фильтра (если таковые имеются) путем вызова [**имеминпутпин:: жеталлокаторрекуирементс**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span><span class="sxs-lookup"><span data-stu-id="c9810-118">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="c9810-119">Закрепление вывода вызывает метод [**ктрансформфилтер::D еЦидебуфферсизе**](ctransformfilter-decidebuffersize.md) фильтра преобразования, который является чистым виртуальным.</span><span class="sxs-lookup"><span data-stu-id="c9810-119">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="c9810-120">Параметры этого метода являются указателем на структуру распределителя и структурой [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) с требованиями подчиненного фильтра.</span><span class="sxs-lookup"><span data-stu-id="c9810-120">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="c9810-121">Если в подчиненном фильтре нет требований к распределительу, то структура будет обнулена.</span><span class="sxs-lookup"><span data-stu-id="c9810-121">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="c9810-122">В методе **деЦидебуфферсизе** производный класс задает свойства распределителя путем вызова [**Имемаллокатор:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span><span class="sxs-lookup"><span data-stu-id="c9810-122">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="c9810-123">Как правило, производный класс выберет свойства распределителя на основе выходного формата, требований подчиненного фильтра и собственных требований фильтра.</span><span class="sxs-lookup"><span data-stu-id="c9810-123">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="c9810-124">Попробуйте выбрать свойства, совместимые с запросом подчиненного фильтра.</span><span class="sxs-lookup"><span data-stu-id="c9810-124">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="c9810-125">В противном случае подчиненный фильтр может отклонить соединение.</span><span class="sxs-lookup"><span data-stu-id="c9810-125">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="c9810-126">В следующем примере кодировщик RLE устанавливает минимальные значения для размера буфера, выравнивания буфера и количества буферов.</span><span class="sxs-lookup"><span data-stu-id="c9810-126">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="c9810-127">Для префикса используется любое значение, запрошенное нисходящим фильтром.</span><span class="sxs-lookup"><span data-stu-id="c9810-127">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="c9810-128">Префикс обычно равен нулю байт, но для некоторых фильтров это требуется.</span><span class="sxs-lookup"><span data-stu-id="c9810-128">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="c9810-129">Например, фильтр [мультиплексора](avi-mux-filter.md) в формате AVI использует префикс для записи заголовков Metallica.</span><span class="sxs-lookup"><span data-stu-id="c9810-129">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



<span data-ttu-id="c9810-130">Распределитель не сможет точно сопоставить ваш запрос.</span><span class="sxs-lookup"><span data-stu-id="c9810-130">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="c9810-131">Поэтому метод **SetProperties** возвращает фактический результат в отдельной структуре **\_ свойств распределителя** ( *фактический* параметр в предыдущем примере).</span><span class="sxs-lookup"><span data-stu-id="c9810-131">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="c9810-132">Даже если **SetProperties** , следует проверить результат, чтобы убедиться, что они соответствуют минимальным требованиям фильтра.</span><span class="sxs-lookup"><span data-stu-id="c9810-132">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="c9810-133">**Пользовательские распределителя**</span><span class="sxs-lookup"><span data-stu-id="c9810-133">**Custom Allocators**</span></span>

<span data-ttu-id="c9810-134">По умолчанию все классы фильтров используют класс [**кмемаллокатор**](cmemallocator.md) для своих распределительов.</span><span class="sxs-lookup"><span data-stu-id="c9810-134">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="c9810-135">Этот класс выделяет память из виртуального адресного пространства клиентского процесса (с помощью **VirtualAlloc**).</span><span class="sxs-lookup"><span data-stu-id="c9810-135">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="c9810-136">Если фильтр должен использовать некоторый другой тип памяти, например поверхности DirectDraw, можно реализовать пользовательский распределитель.</span><span class="sxs-lookup"><span data-stu-id="c9810-136">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="c9810-137">Можно использовать класс [**кбасеаллокатор**](cbaseallocator.md) или написать совершенно новый класс распределителя.</span><span class="sxs-lookup"><span data-stu-id="c9810-137">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="c9810-138">Если фильтр имеет пользовательский распределитель, переопределите следующие методы в зависимости от того, какой ПИН-код использует распределитель:</span><span class="sxs-lookup"><span data-stu-id="c9810-138">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="c9810-139">Входной ПИН-код: [**кбасеинпутпин::-распределителя**](cbaseinputpin-getallocator.md) и [**Кбасеинпутпин:: нотифяллокатор**](cbaseinputpin-notifyallocator.md).</span><span class="sxs-lookup"><span data-stu-id="c9810-139">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="c9810-140">Выходной ПИН-код: [**кбасеаутпутпин::D еЦидеаллокатор**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="c9810-140">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="c9810-141">Если другой фильтр отказывается подключиться с помощью пользовательского распределителя, то фильтр может либо завершить подключение, либо подключиться к распределителю другого фильтра.</span><span class="sxs-lookup"><span data-stu-id="c9810-141">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="c9810-142">В последнем случае может потребоваться установить внутренний флаг, указывающий тип распределителя.</span><span class="sxs-lookup"><span data-stu-id="c9810-142">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="c9810-143">Пример такого подхода см. в разделе [**класс кдравимаже**](cdrawimage.md).</span><span class="sxs-lookup"><span data-stu-id="c9810-143">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="c9810-144">Далее. [Шаг 5. Преобразование изображения](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="c9810-144">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9810-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c9810-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9810-146">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="c9810-146">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



