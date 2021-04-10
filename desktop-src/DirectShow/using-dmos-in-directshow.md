---
description: Использование дмос в DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Использование дмос в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c90513649756a49067e523390292d4b44e1eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156731"
---
# <a name="using-dmos-in-directshow"></a><span data-ttu-id="877d0-103">Использование дмос в DirectShow</span><span class="sxs-lookup"><span data-stu-id="877d0-103">Using DMOs in DirectShow</span></span>

<span data-ttu-id="877d0-104">Приложения, основанные на DirectShow, могут использовать дмос в графе фильтров с помощью фильтра [оболочки DMO](dmo-wrapper-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="877d0-104">Applications based on DirectShow can use DMOs in a filter graph, through the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="877d0-105">Этот фильтр объединяет DMO и обрабатывает все детали использования DMO, такие как передача данных в DMO, выделение объектов [**имедиабуффер**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) и т. д.</span><span class="sxs-lookup"><span data-stu-id="877d0-105">This filter aggregates a DMO and handles all the details of using the DMO, such as passing data to and from the DMO, allocating [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) objects, and so forth.</span></span>

<span data-ttu-id="877d0-106">Поскольку объекты DMO объединяются фильтром, приложение может запросить фильтр для любых COM-интерфейсов, предоставляемых DMO.</span><span class="sxs-lookup"><span data-stu-id="877d0-106">Because the DMO is aggregated by the filter, the application can query the filter for any COM interfaces that the DMO exposes.</span></span> <span data-ttu-id="877d0-107">Однако приложение должно позволить фильтру выполнять все операции потоковой передачи на DMO.</span><span class="sxs-lookup"><span data-stu-id="877d0-107">However, the application should let the filter handle all streaming operations on the DMO.</span></span> <span data-ttu-id="877d0-108">Например, не следует задавать типы носителей, обрабатывать любые буферы, сбрасывать объекты DMO, блокировать объекты DMO, включать или отключать контроль качества, а также устанавливать оптимизации видео.</span><span class="sxs-lookup"><span data-stu-id="877d0-108">For example, do not set media types, process any buffers, flush the DMO, lock the DMO, enable or disable quality control, or set video optimizations.</span></span>

<span data-ttu-id="877d0-109">Если вы знакомы с идентификатором класса (CLSID) конкретного DMO, который вы хотите использовать, можно инициализировать фильтр оболочки DMO с этим DMO следующим образом:</span><span class="sxs-lookup"><span data-stu-id="877d0-109">If you know the class identifier (CLSID) of a specific DMO that you want to use, you can initialize the DMO Wrapper filter with that DMO, as follows:</span></span>

1.  <span data-ttu-id="877d0-110">Вызовите **CoCreateInstance** , чтобы создать фильтр оболочки DMO.</span><span class="sxs-lookup"><span data-stu-id="877d0-110">Call **CoCreateInstance** to create the DMO Wrapper filter.</span></span>
2.  <span data-ttu-id="877d0-111">Запросите фильтр оболочки DMO для интерфейса [**идмоврапперфилтер**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .</span><span class="sxs-lookup"><span data-stu-id="877d0-111">Query the DMO Wrapper filter for the [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="877d0-112">Вызовите метод [**идмоврапперфилтер:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) .</span><span class="sxs-lookup"><span data-stu-id="877d0-112">Call the [**IDMOWrapperFilter::Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) method.</span></span> <span data-ttu-id="877d0-113">Укажите идентификатор CLSID DMO и идентификатор GUID категории DMO.</span><span class="sxs-lookup"><span data-stu-id="877d0-113">Specify the CLSID of the DMO and the GUID of the DMO's category.</span></span> <span data-ttu-id="877d0-114">Список категорий DMO см. в разделе [идентификаторы GUID DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="877d0-114">For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="877d0-115">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="877d0-115">The following code shows these steps:</span></span>


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



<span data-ttu-id="877d0-116">Функция [**дмоенум**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) перечисляет дмос в реестре.</span><span class="sxs-lookup"><span data-stu-id="877d0-116">The [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function enumerates DMOs in the registry.</span></span> <span data-ttu-id="877d0-117">Эта функция использует другой набор идентификаторов GUID категорий из тех, которые используются для фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="877d0-117">This function uses a different set of category GUIDs from the ones used for DirectShow filters.</span></span>

<span data-ttu-id="877d0-118">**Использование перечислителя системных устройств с дмос**</span><span class="sxs-lookup"><span data-stu-id="877d0-118">**Using the System Device Enumerator with DMOs**</span></span>

<span data-ttu-id="877d0-119">Вместо непосредственного создания DMO можно использовать [перечислитель системных устройств](system-device-enumerator.md), который позволяет перечислить любую категорию DMO, поддерживаемую методом **дмоенум** .</span><span class="sxs-lookup"><span data-stu-id="877d0-119">Instead of creating a DMO directly, you can use the [System Device Enumerator](system-device-enumerator.md), which can enumerate any DMO category that is supported by the **DMOEnum** method.</span></span> <span data-ttu-id="877d0-120">Перечислитель системных устройств также включает дмос, когда он перечисляет определенные категории фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="877d0-120">The System Device Enumerator also includes DMOs when it enumerates certain DirectShow filter categories.</span></span> <span data-ttu-id="877d0-121">В следующей таблице показано сопоставление между категориями DMO и категориями DirectShow.</span><span class="sxs-lookup"><span data-stu-id="877d0-121">The following table shows the mapping between DMO categories and DirectShow categories.</span></span>



|                             |                                |
|-----------------------------|--------------------------------|
| <span data-ttu-id="877d0-122">Категория DMO</span><span class="sxs-lookup"><span data-stu-id="877d0-122">DMO Category</span></span>                | <span data-ttu-id="877d0-123">Эквивалент DirectShow</span><span class="sxs-lookup"><span data-stu-id="877d0-123">DirectShow Equivalent</span></span>          |
| <span data-ttu-id="877d0-124">\_КОДИРОВЩИК дмокатегори Audio \_</span><span class="sxs-lookup"><span data-stu-id="877d0-124">DMOCATEGORY\_AUDIO\_ENCODER</span></span> | <span data-ttu-id="877d0-125">\_АУДИОКОМПРЕССОРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="877d0-125">CLSID\_AudioCompressorCategory</span></span> |
| <span data-ttu-id="877d0-126">\_декодер дмокатегори Audio \_</span><span class="sxs-lookup"><span data-stu-id="877d0-126">DMOCATEGORY\_AUDIO\_DECODER</span></span> | <span data-ttu-id="877d0-127">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="877d0-127">CLSID\_LegacyAmFilterCategory</span></span>  |
| <span data-ttu-id="877d0-128">\_кодировщик видео \_ дмокатегори</span><span class="sxs-lookup"><span data-stu-id="877d0-128">DMOCATEGORY\_VIDEO\_ENCODER</span></span> | <span data-ttu-id="877d0-129">\_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="877d0-129">CLSID\_VideoCompressorCategory</span></span> |
| <span data-ttu-id="877d0-130">\_декодер видео \_ дмокатегори</span><span class="sxs-lookup"><span data-stu-id="877d0-130">DMOCATEGORY\_VIDEO\_DECODER</span></span> | <span data-ttu-id="877d0-131">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="877d0-131">CLSID\_LegacyAmFilterCategory</span></span>  |



 

<span data-ttu-id="877d0-132">Перечислитель системных устройств возвращает список объектов моникера.</span><span class="sxs-lookup"><span data-stu-id="877d0-132">The System Device Enumerator returns a list of moniker objects.</span></span> <span data-ttu-id="877d0-133">Если моникер представляет DMO, метод **IMoniker:: биндтубжект** автоматически создает фильтр оболочки DMO и инициализирует его с этим DMO.</span><span class="sxs-lookup"><span data-stu-id="877d0-133">If the moniker represents a DMO, the **IMoniker::BindToObject** method automatically creates the DMO Wrapper filter and initializes it with that DMO.</span></span> <span data-ttu-id="877d0-134">Таким же, тот факт, что задействован DMO, прозрачен для приложения.</span><span class="sxs-lookup"><span data-stu-id="877d0-134">Thus, the fact that a DMO is involved is transparent to the application.</span></span> <span data-ttu-id="877d0-135">Дополнительные сведения об использовании перечислителя системных устройств см. в разделе [Использование перечислителя системных устройств](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="877d0-135">For more information on using the System Device Enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="877d0-136">**Ограничения**</span><span class="sxs-lookup"><span data-stu-id="877d0-136">**Limitations**</span></span>

<span data-ttu-id="877d0-137">При использовании дмос в DirectShow существуют некоторые ограничения:</span><span class="sxs-lookup"><span data-stu-id="877d0-137">There are some limitations when using DMOs in DirectShow:</span></span>

-   <span data-ttu-id="877d0-138">Фильтр оболочки DMO не поддерживает дмос с нулевым числом входов, несколькими входами или нулевыми выходами.</span><span class="sxs-lookup"><span data-stu-id="877d0-138">The DMO Wrapper filter does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span>
-   <span data-ttu-id="877d0-139">Все соединения ПИН-кода в фильтре оболочки DMO используют интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="877d0-139">All pin connections on the DMO Wrapper Filter use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="877d0-140">Службы редактирования DirectShow не поддерживают эффекты и переходы на основе DMO.</span><span class="sxs-lookup"><span data-stu-id="877d0-140">DirectShow Editing Services does not support DMO-based effects or transitions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="877d0-141">См. также</span><span class="sxs-lookup"><span data-stu-id="877d0-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="877d0-142">Использование дмос</span><span class="sxs-lookup"><span data-stu-id="877d0-142">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



