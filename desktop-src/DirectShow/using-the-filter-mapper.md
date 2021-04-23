---
description: Использование средства сопоставления фильтров
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Использование средства сопоставления фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d7acf85a7b415fc161cd21e17d069b46c3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911071"
---
# <a name="using-the-filter-mapper"></a><span data-ttu-id="d1622-103">Использование средства сопоставления фильтров</span><span class="sxs-lookup"><span data-stu-id="d1622-103">Using the Filter Mapper</span></span>

<span data-ttu-id="d1622-104">Средство [сопоставления фильтров](filter-mapper.md) — это COM-объект, который перечисляет фильтры DirectShow на основе различных критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="d1622-104">The [Filter Mapper](filter-mapper.md) is a COM object that enumerates DirectShow filters based on various search criteria.</span></span> <span data-ttu-id="d1622-105">Средство сопоставления фильтров может быть менее эффективным, чем перечислитель системных устройств, поэтому если вам нужны фильтры из определенной категории, следует использовать перечислитель системных устройств.</span><span class="sxs-lookup"><span data-stu-id="d1622-105">The Filter Mapper can be less efficient than the System Device Enumerator, so if you need filters from a particular category, you should use the System Device Enumerator.</span></span> <span data-ttu-id="d1622-106">Но если необходимо выбрать фильтр, который поддерживает определенное сочетание типов мультимедиа, но не входит в категорию четких вырезания, может потребоваться использовать средство сопоставления фильтров.</span><span class="sxs-lookup"><span data-stu-id="d1622-106">But if you need to locate a filter that supports a certain combination of media types, but does not fall into a clear-cut category, you might need to use the Filter Mapper.</span></span> <span data-ttu-id="d1622-107">(Пример может быть фильтром визуализации или фильтром декодера.)</span><span class="sxs-lookup"><span data-stu-id="d1622-107">(An example would be a renderer filter or a decoder filter.)</span></span>

<span data-ttu-id="d1622-108">Средство сопоставления фильтров предоставляет интерфейс [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="d1622-108">The Filter Mapper exposes the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span> <span data-ttu-id="d1622-109">Чтобы найти фильтр, вызовите метод [**IFilterMapper2:: енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) .</span><span class="sxs-lookup"><span data-stu-id="d1622-109">To search for a filter, call the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method.</span></span> <span data-ttu-id="d1622-110">Этот метод принимает несколько параметров, определяющих условия поиска, и возвращает перечислитель для соответствующих фильтров.</span><span class="sxs-lookup"><span data-stu-id="d1622-110">This method takes several parameters that define the search criteria, and returns an enumerator for the matching filters.</span></span> <span data-ttu-id="d1622-111">Перечислитель поддерживает интерфейс [**иенуммоникер**](/windows/win32/api/objidl/nn-objidl-ienummoniker) и предоставляет уникальный моникер для каждого фильтра сопоставления.</span><span class="sxs-lookup"><span data-stu-id="d1622-111">The enumerator supports the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface, and supplies a unique moniker for each matching filter.</span></span>

<span data-ttu-id="d1622-112">В следующем примере перечисляются фильтры, которые принимают входные цифровые видео (DV) и имеют по крайней мере один выходной ПИН-код любого типа носителя.</span><span class="sxs-lookup"><span data-stu-id="d1622-112">The following example enumerates filters that accept digital video (DV) input and have at least one output pin, of any media type.</span></span> <span data-ttu-id="d1622-113">(Фильтр [видеодекодера DV](dv-video-decoder-filter.md) соответствует этим критериям.)</span><span class="sxs-lookup"><span data-stu-id="d1622-113">(The [DV Video Decoder](dv-video-decoder-filter.md) filter matches these criteria.)</span></span>


```C++
IFilterMapper2 *pMapper = NULL;
IEnumMoniker *pEnum = NULL;

hr = CoCreateInstance(CLSID_FilterMapper2, 
    NULL, CLSCTX_INPROC, IID_IFilterMapper2, 
    (void **) &pMapper);

if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = MEDIASUBTYPE_dvsd;

hr = pMapper->EnumMatchingFilters(
        &pEnum,
        0,                  // Reserved.
        TRUE,               // Use exact match?
        MERIT_DO_NOT_USE+1, // Minimum merit.
        TRUE,               // At least one input pin?
        1,                  // Number of major type/subtype pairs for input.
        arrayInTypes,       // Array of major type/subtype pairs for input.
        NULL,               // Input medium.
        NULL,               // Input pin category.
        FALSE,              // Must be a renderer?
        TRUE,               // At least one output pin?
        0,                  // Number of major type/subtype pairs for output.
        NULL,               // Array of major type/subtype pairs for output.
        NULL,               // Output medium.
        NULL);              // Output pin category.

// Enumerate the monikers.
IMoniker *pMoniker;
ULONG cFetched;
while (pEnum->Next(1, &pMoniker, &cFetched) == S_OK)
{
    IPropertyBag *pPropBag = NULL;
    hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
       (void **)&pPropBag);

    if (SUCCEEDED(hr))
    {
        // To retrieve the friendly name of the filter, do the following:
        VARIANT varName;
        VariantInit(&varName);
        hr = pPropBag->Read(L"FriendlyName", &varName, 0);
        if (SUCCEEDED(hr))
        {
            // Display the name in your UI somehow.
        }
        VariantClear(&varName);

        // To create an instance of the filter, do the following:
        IBaseFilter *pFilter;
        hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, (void**)&pFilter);
        // Now add the filter to the graph. Remember to release pFilter later.
    
        // Clean up.
        pPropBag->Release();
    }
    pMoniker->Release();
}

// Clean up.
pMapper->Release();
pEnum->Release();
```



<span data-ttu-id="d1622-114">Метод [**енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) имеет достаточно большое количество параметров, которые добавляются в комментарий в примере.</span><span class="sxs-lookup"><span data-stu-id="d1622-114">The [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method has a fairly large number of parameters, which are commented in the example.</span></span> <span data-ttu-id="d1622-115">К этим примерам относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="d1622-115">The significant ones for this example include:</span></span>

-   <span data-ttu-id="d1622-116">Минимальное количество недоступных: для фильтра должно быть задано значение неуспешное \_ \_ \_ использование.</span><span class="sxs-lookup"><span data-stu-id="d1622-116">Minimum merit value: The filter must have a merit value above MERIT\_DO\_NOT\_USE.</span></span>
-   <span data-ttu-id="d1622-117">Типы входных данных. вызывающий объект передает массив, содержащий пары основных типов и подтипов.</span><span class="sxs-lookup"><span data-stu-id="d1622-117">Input types: The caller passes an array containing pairs of major types and subtypes.</span></span> <span data-ttu-id="d1622-118">Будут соответствовать только те фильтры, которые поддерживают хотя бы одну из этих пар.</span><span class="sxs-lookup"><span data-stu-id="d1622-118">Only filters that support at least one of these pairs will match.</span></span>
-   <span data-ttu-id="d1622-119">Точное совпадение. фильтр может регистрировать значения **null** для основного типа, подтипа, категории закрепления или средних.</span><span class="sxs-lookup"><span data-stu-id="d1622-119">Exact match: A filter can register **NULL** values for major type, subtype, pin category, or medium.</span></span> <span data-ttu-id="d1622-120">Если не указано точное соответствие, значение **null** выступает в качестве подстановочного знака, совпадающего с любым указанным значением.</span><span class="sxs-lookup"><span data-stu-id="d1622-120">Unless you specify exact matching, a **NULL** value acts as a wildcard, matching any value that you specify.</span></span> <span data-ttu-id="d1622-121">С точным соответствием фильтр должен точно соответствовать вашим критериям.</span><span class="sxs-lookup"><span data-stu-id="d1622-121">With exact matching, the filter must exactly match your criteria.</span></span> <span data-ttu-id="d1622-122">Однако если в критериях поиска вы придаете параметр **null** , он всегда действует как подстановочный знак или значение "не важно", соответствующее любому фильтру.</span><span class="sxs-lookup"><span data-stu-id="d1622-122">However, if you give a **NULL** parameter in the search criteria, it always acts as a wildcard or "don't care" value, matching any filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1622-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d1622-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1622-124">Перечисление устройств и фильтров</span><span class="sxs-lookup"><span data-stu-id="d1622-124">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="d1622-125">Интеллектуальное подключение</span><span class="sxs-lookup"><span data-stu-id="d1622-125">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 
