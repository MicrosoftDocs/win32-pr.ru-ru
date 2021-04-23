---
description: Выбор фильтра сжатия
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Выбор фильтра сжатия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140659"
---
# <a name="choosing-a-compression-filter"></a><span data-ttu-id="e0c35-103">Выбор фильтра сжатия</span><span class="sxs-lookup"><span data-stu-id="e0c35-103">Choosing a Compression Filter</span></span>

<span data-ttu-id="e0c35-104">Несколько типов программных компонентов могут выполнять видео или аудио сжатие, например:</span><span class="sxs-lookup"><span data-stu-id="e0c35-104">Several types of software components can perform video or audio compression, such as:</span></span>

-   <span data-ttu-id="e0c35-105">Собственные фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="e0c35-105">Native DirectShow filters</span></span>
-   <span data-ttu-id="e0c35-106">Кодеки для сжатия видео (ВКМ)</span><span class="sxs-lookup"><span data-stu-id="e0c35-106">Video Compression Manager (VCM) codecs</span></span>
-   <span data-ttu-id="e0c35-107">Кодеки диспетчера аудиосжатия (ACM)</span><span class="sxs-lookup"><span data-stu-id="e0c35-107">Audio Compression Manager (ACM) codecs</span></span>
-   <span data-ttu-id="e0c35-108">Объекты мультимедиа DirectX (дмос)</span><span class="sxs-lookup"><span data-stu-id="e0c35-108">DirectX Media Objects (DMOs)</span></span>

<span data-ttu-id="e0c35-109">В DirectShow кодеки ВКМ упаковываются с помощью [фильтра AVI компрессор](avi-compressor-filter.md), а ACM кодеки упаковываются [фильтром оболочки ACM](acm-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="e0c35-109">In DirectShow, VCM codecs are wrapped by the [AVI Compressor Filter](avi-compressor-filter.md), and ACM codecs are wrapped by the [ACM Wrapper Filter](acm-wrapper-filter.md).</span></span> <span data-ttu-id="e0c35-110">Дмос упаковывается [фильтром оболочки DMO](dmo-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="e0c35-110">DMOs are wrapped by the [DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="e0c35-111">Перечислитель системных устройств обеспечивает единообразный способ перечисления и создания любого из этих типов сжатия, не беспокоясь о базовой модели.</span><span class="sxs-lookup"><span data-stu-id="e0c35-111">The system device enumerator provides a consistent way to enumerate and create any of these compressor types, without worrying about the underlying model.</span></span>

<span data-ttu-id="e0c35-112">Дополнительные сведения о перечислителе системных устройств см. [в разделе Использование перечислителя системных устройств](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="e0c35-112">For details about the system device enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="e0c35-113">Вкратце, все фильтры DirectShow классифицируются по категориям, и каждая категория идентифицируется по идентификатору GUID.</span><span class="sxs-lookup"><span data-stu-id="e0c35-113">Briefly, all DirectShow filters are classified by category, and each category is identified by a GUID.</span></span> <span data-ttu-id="e0c35-114">Для видео-компрессоров Категория GUID имеет значение CLSID \_ видеокомпрессоркатегори.</span><span class="sxs-lookup"><span data-stu-id="e0c35-114">For video compressors, the category GUID is CLSID\_VideoCompressorCategory.</span></span> <span data-ttu-id="e0c35-115">Для звуковых компрессоров это CLSID \_ аудиокомпрессоркатегори.</span><span class="sxs-lookup"><span data-stu-id="e0c35-115">For audio compressors, it is CLSID\_AudioCompressorCategory.</span></span> <span data-ttu-id="e0c35-116">Чтобы перечислить определенную категорию, перечислитель системных устройств создает объект *перечислителя* , который поддерживает интерфейс [**иенуммоникер**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) .</span><span class="sxs-lookup"><span data-stu-id="e0c35-116">To enumerate a particular category, the system device enumerator creates an *enumerator* object that supports the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="e0c35-117">Приложение использует этот интерфейс для получения моникеров устройств, где каждый моникер устройства представляет экземпляр фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e0c35-117">The application uses this interface to retrieve device monikers, where each device moniker represents an instance of a DirectShow filter.</span></span> <span data-ttu-id="e0c35-118">Можно использовать моникер для создания фильтра или для получения понятного имени устройства без создания фильтра.</span><span class="sxs-lookup"><span data-stu-id="e0c35-118">You can use the moniker to create the filter, or to get the device's friendly name without creating the filter.</span></span>

<span data-ttu-id="e0c35-119">Для перечисления видео или звуковых компрессоров, доступных в системе пользователя, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0c35-119">To enumerate the video or audio compressors available on the user's system, do the following:</span></span>

1.  <span data-ttu-id="e0c35-120">Вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать перечислитель системных устройств с идентификатором класса CLSID \_ системдевицеенум.</span><span class="sxs-lookup"><span data-stu-id="e0c35-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the system device enumerator, which has a class ID of CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="e0c35-121">Вызовите [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) с идентификатором GUID категории фильтра.</span><span class="sxs-lookup"><span data-stu-id="e0c35-121">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the filter category GUID.</span></span> <span data-ttu-id="e0c35-122">Метод возвращает указатель интерфейса **иенуммоникер** .</span><span class="sxs-lookup"><span data-stu-id="e0c35-122">The method returns an **IEnumMoniker** interface pointer.</span></span>
3.  <span data-ttu-id="e0c35-123">Используйте метод Иенуммоникер:: Next для перечисления моникеров устройств.</span><span class="sxs-lookup"><span data-stu-id="e0c35-123">Use the IEnumMoniker::Next method to enumerate the device monikers.</span></span> <span data-ttu-id="e0c35-124">Этот метод возвращает интерфейс [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) , который представляет моникер.</span><span class="sxs-lookup"><span data-stu-id="e0c35-124">This method returns an [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) interface, which represents the moniker.</span></span>

<span data-ttu-id="e0c35-125">Чтобы получить понятное имя из моникера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0c35-125">To get the friendly name from a moniker, do the following:</span></span>

1.  <span data-ttu-id="e0c35-126">Вызовите метод **IMoniker:: биндтостораже** .</span><span class="sxs-lookup"><span data-stu-id="e0c35-126">Call the **IMoniker::BindToStorage** method.</span></span> <span data-ttu-id="e0c35-127">Этот метод возвращает указатель интерфейса **ипропертибаг** .</span><span class="sxs-lookup"><span data-stu-id="e0c35-127">This method returns an **IPropertyBag** interface pointer.</span></span>
2.  <span data-ttu-id="e0c35-128">Используйте метод **ипропертибаг:: Read** для чтения свойства **FriendlyName** .</span><span class="sxs-lookup"><span data-stu-id="e0c35-128">Use the **IPropertyBag::Read** method to read the **FriendlyName** property.</span></span>

<span data-ttu-id="e0c35-129">Как правило, в приложении отображается список компрессоров, чтобы пользователь мог выбрать один из них.</span><span class="sxs-lookup"><span data-stu-id="e0c35-129">Typically, an application would display a list of compressors, so that the user could choose one.</span></span> <span data-ttu-id="e0c35-130">Например, следующий код заполняет список именами доступных компрессоров видео.</span><span class="sxs-lookup"><span data-stu-id="e0c35-130">For example, the following code populates a list box with the names of the available video compressors.</span></span>


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



<span data-ttu-id="e0c35-131">Чтобы создать экземпляр фильтра из моникера, вызовите метод **IMoniker:: биндтубжект** .</span><span class="sxs-lookup"><span data-stu-id="e0c35-131">To create a filter instance from the moniker, call the **IMoniker::BindToObject** method.</span></span> <span data-ttu-id="e0c35-132">Метод возвращает указатель [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="e0c35-132">The method returns an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span>


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



<span data-ttu-id="e0c35-133">Для кодеков ВКМ каждый моникер представляет один конкретный кодек, хотя все кодеки упаковываются одним и тем же фильтром сжатия AVI.</span><span class="sxs-lookup"><span data-stu-id="e0c35-133">For VCM codecs, each moniker represents one particular codec, even though all of the codecs are wrapped by the same AVI Compression filter.</span></span> <span data-ttu-id="e0c35-134">При вызове **биндтубжект** создается экземпляр этого фильтра, инициализированный для этого кодека.</span><span class="sxs-lookup"><span data-stu-id="e0c35-134">Calling **BindToObject** creates an instance of this filter, initialized for that codec.</span></span> <span data-ttu-id="e0c35-135">По этой причине нельзя вызвать метод **CoCreateInstance** непосредственно в фильтре сжатия AVI.</span><span class="sxs-lookup"><span data-stu-id="e0c35-135">For this reason, you cannot call **CoCreateInstance** directly on the AVI Compression filter.</span></span> <span data-ttu-id="e0c35-136">Необходимо пройти перечислитель системных устройств.</span><span class="sxs-lookup"><span data-stu-id="e0c35-136">You must go through the system device enumerator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0c35-137">См. также</span><span class="sxs-lookup"><span data-stu-id="e0c35-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0c35-138">Повторное сжатие файла AVI</span><span class="sxs-lookup"><span data-stu-id="e0c35-138">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 
