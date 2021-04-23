---
description: Шаг 4.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Шаг 4. Задание свойств распределителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32d5e3affba32b96dc93cb97e1886322bc6f2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684132"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="b4055-104">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="b4055-104">Step 4.</span></span> <span data-ttu-id="b4055-105">Задание свойств распределителя</span><span class="sxs-lookup"><span data-stu-id="b4055-105">Set Allocator Properties</span></span>

<span data-ttu-id="b4055-106">Это шаг 4 учебника [Создание фильтров преобразования](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b4055-106">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="b4055-107">Этот шаг не является обязательным для фильтров, производных от **ктрансинплацефилтер**.</span><span class="sxs-lookup"><span data-stu-id="b4055-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="b4055-108">После того как два контакта договариваются по типу носителя, они выбирают распределителя для соединения и согласовывают свойства распределителя, такие как размер буфера и количество буферов.</span><span class="sxs-lookup"><span data-stu-id="b4055-108">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="b4055-109">В классе **ктрансформфилтер** есть два распределителя, один для вышестоящего соединения, а другой — для соединения с нижестоящим ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="b4055-109">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="b4055-110">Вышестоящий фильтр выбирает вышестоящий распределитель, а также выбирает свойства распределителя.</span><span class="sxs-lookup"><span data-stu-id="b4055-110">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="b4055-111">Входной ПИН-код принимает любой способ, который принимается в качестве вышестоящего фильтра.</span><span class="sxs-lookup"><span data-stu-id="b4055-111">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="b4055-112">Если необходимо изменить это поведение, переопределите метод [**кбасеинпутпин:: нотифяллокатор**](cbaseinputpin-notifyallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b4055-112">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="b4055-113">Закрепление вывода фильтра преобразования выбирает нисходящий распределитель.</span><span class="sxs-lookup"><span data-stu-id="b4055-113">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="b4055-114">Он выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b4055-114">It performs the following steps:</span></span>

1.  <span data-ttu-id="b4055-115">Если подчиненный фильтр может предоставить распределитель, то он будет использоваться выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="b4055-115">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="b4055-116">В противном случае выходной ПИН-код создает новый распределитель.</span><span class="sxs-lookup"><span data-stu-id="b4055-116">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="b4055-117">Закрепление вывода получает требования к распределительу подчиненного фильтра (если таковые имеются) путем вызова [**имеминпутпин:: жеталлокаторрекуирементс**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span><span class="sxs-lookup"><span data-stu-id="b4055-117">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="b4055-118">Закрепление вывода вызывает метод [**ктрансформфилтер::D еЦидебуфферсизе**](ctransformfilter-decidebuffersize.md) фильтра преобразования, который является чистым виртуальным.</span><span class="sxs-lookup"><span data-stu-id="b4055-118">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="b4055-119">Параметры этого метода являются указателем на структуру распределителя и структурой [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) с требованиями подчиненного фильтра.</span><span class="sxs-lookup"><span data-stu-id="b4055-119">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="b4055-120">Если в подчиненном фильтре нет требований к распределительу, то структура будет обнулена.</span><span class="sxs-lookup"><span data-stu-id="b4055-120">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="b4055-121">В методе **деЦидебуфферсизе** производный класс задает свойства распределителя путем вызова [**Имемаллокатор:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span><span class="sxs-lookup"><span data-stu-id="b4055-121">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="b4055-122">Как правило, производный класс выберет свойства распределителя на основе выходного формата, требований подчиненного фильтра и собственных требований фильтра.</span><span class="sxs-lookup"><span data-stu-id="b4055-122">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="b4055-123">Попробуйте выбрать свойства, совместимые с запросом подчиненного фильтра.</span><span class="sxs-lookup"><span data-stu-id="b4055-123">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="b4055-124">В противном случае подчиненный фильтр может отклонить соединение.</span><span class="sxs-lookup"><span data-stu-id="b4055-124">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="b4055-125">В следующем примере кодировщик RLE устанавливает минимальные значения для размера буфера, выравнивания буфера и количества буферов.</span><span class="sxs-lookup"><span data-stu-id="b4055-125">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="b4055-126">Для префикса используется любое значение, запрошенное нисходящим фильтром.</span><span class="sxs-lookup"><span data-stu-id="b4055-126">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="b4055-127">Префикс обычно равен нулю байт, но для некоторых фильтров это требуется.</span><span class="sxs-lookup"><span data-stu-id="b4055-127">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="b4055-128">Например, фильтр [мультиплексора](avi-mux-filter.md) в формате AVI использует префикс для записи заголовков Metallica.</span><span class="sxs-lookup"><span data-stu-id="b4055-128">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


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



<span data-ttu-id="b4055-129">Распределитель не сможет точно сопоставить ваш запрос.</span><span class="sxs-lookup"><span data-stu-id="b4055-129">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="b4055-130">Поэтому метод **SetProperties** возвращает фактический результат в отдельной структуре **\_ свойств распределителя** ( *фактический* параметр в предыдущем примере).</span><span class="sxs-lookup"><span data-stu-id="b4055-130">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="b4055-131">Даже если **SetProperties** , следует проверить результат, чтобы убедиться, что они соответствуют минимальным требованиям фильтра.</span><span class="sxs-lookup"><span data-stu-id="b4055-131">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="b4055-132">**Пользовательские распределителя**</span><span class="sxs-lookup"><span data-stu-id="b4055-132">**Custom Allocators**</span></span>

<span data-ttu-id="b4055-133">По умолчанию все классы фильтров используют класс [**кмемаллокатор**](cmemallocator.md) для своих распределительов.</span><span class="sxs-lookup"><span data-stu-id="b4055-133">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="b4055-134">Этот класс выделяет память из виртуального адресного пространства клиентского процесса (с помощью **VirtualAlloc**).</span><span class="sxs-lookup"><span data-stu-id="b4055-134">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="b4055-135">Если фильтр должен использовать некоторый другой тип памяти, например поверхности DirectDraw, можно реализовать пользовательский распределитель.</span><span class="sxs-lookup"><span data-stu-id="b4055-135">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="b4055-136">Можно использовать класс [**кбасеаллокатор**](cbaseallocator.md) или написать совершенно новый класс распределителя.</span><span class="sxs-lookup"><span data-stu-id="b4055-136">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="b4055-137">Если фильтр имеет пользовательский распределитель, переопределите следующие методы в зависимости от того, какой ПИН-код использует распределитель:</span><span class="sxs-lookup"><span data-stu-id="b4055-137">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="b4055-138">Входной ПИН-код: [**кбасеинпутпин::-распределителя**](cbaseinputpin-getallocator.md) и [**Кбасеинпутпин:: нотифяллокатор**](cbaseinputpin-notifyallocator.md).</span><span class="sxs-lookup"><span data-stu-id="b4055-138">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="b4055-139">Выходной ПИН-код: [**кбасеаутпутпин::D еЦидеаллокатор**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="b4055-139">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="b4055-140">Если другой фильтр отказывается подключиться с помощью пользовательского распределителя, то фильтр может либо завершить подключение, либо подключиться к распределителю другого фильтра.</span><span class="sxs-lookup"><span data-stu-id="b4055-140">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="b4055-141">В последнем случае может потребоваться установить внутренний флаг, указывающий тип распределителя.</span><span class="sxs-lookup"><span data-stu-id="b4055-141">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="b4055-142">Пример такого подхода см. в разделе [**класс кдравимаже**](cdrawimage.md).</span><span class="sxs-lookup"><span data-stu-id="b4055-142">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="b4055-143">Далее. [Шаг 5. Преобразование изображения](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="b4055-143">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4055-144">См. также</span><span class="sxs-lookup"><span data-stu-id="b4055-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4055-145">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="b4055-145">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



