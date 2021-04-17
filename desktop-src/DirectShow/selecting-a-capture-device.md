---
description: Выбор устройства записи
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Выбор устройства записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b599728c6bd2d98b89285b6008923aa4fb2a3aef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682230"
---
# <a name="selecting-a-capture-device"></a><span data-ttu-id="463d7-103">Выбор устройства записи</span><span class="sxs-lookup"><span data-stu-id="463d7-103">Selecting a Capture Device</span></span>

<span data-ttu-id="463d7-104">Чтобы выбрать устройство для захвата аудио или видео, используйте [перечислитель системных устройств](system-device-enumerator.md), описанный в разделе [Использование перечислителя системных устройств](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="463d7-104">To select an audio or video capture device, use the [System Device Enumerator](system-device-enumerator.md), described in the topic [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="463d7-105">Перечислитель системных устройств Возвращает коллекцию моникеров устройств, выбранную категорией устройств.</span><span class="sxs-lookup"><span data-stu-id="463d7-105">The System Device Enumerator returns a collection of device monikers, selected by device category.</span></span> <span data-ttu-id="463d7-106">*Моникер* — это COM-объект, который содержит сведения о другом объекте.</span><span class="sxs-lookup"><span data-stu-id="463d7-106">A *moniker* is a COM object that contains information about another object.</span></span> <span data-ttu-id="463d7-107">Моникеры позволяют приложению получать сведения об объекте без фактического создания объекта.</span><span class="sxs-lookup"><span data-stu-id="463d7-107">Monikers enable the application to get information about an object without actually creating the object.</span></span> <span data-ttu-id="463d7-108">Позже приложение может использовать моникер для создания объекта.</span><span class="sxs-lookup"><span data-stu-id="463d7-108">Later, the application can use the moniker to create the object.</span></span> <span data-ttu-id="463d7-109">Дополнительные сведения об моникерах см. в документации по [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span><span class="sxs-lookup"><span data-stu-id="463d7-109">For more information about monikers, see the documentation for [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span></span>

<span data-ttu-id="463d7-110">Чтобы использовать перечислитель системных устройств, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="463d7-110">To use the System Device Enumerator, perform the following steps.</span></span>

1.  <span data-ttu-id="463d7-111">Вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать экземпляр перечислителя системных устройств.</span><span class="sxs-lookup"><span data-stu-id="463d7-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create an instance of the System Device Enumerator.</span></span>
2.  <span data-ttu-id="463d7-112">Вызовите [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) и укажите категорию устройства в виде идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="463d7-112">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) and specify the device category as a GUID.</span></span> <span data-ttu-id="463d7-113">Для устройств записи важны следующие категории.</span><span class="sxs-lookup"><span data-stu-id="463d7-113">For capture devices, the following categories are relevant.</span></span> 

    | <span data-ttu-id="463d7-114">GUID категории</span><span class="sxs-lookup"><span data-stu-id="463d7-114">Category GUID</span></span>                       | <span data-ttu-id="463d7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="463d7-115">Description</span></span>           |
    |-------------------------------------|-----------------------|
    | <span data-ttu-id="463d7-116">**\_АУДИОИНПУТДЕВИЦЕКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="463d7-116">**CLSID\_AudioInputDeviceCategory**</span></span> | <span data-ttu-id="463d7-117">Устройства записи звука</span><span class="sxs-lookup"><span data-stu-id="463d7-117">Audio capture devices</span></span> |
    | <span data-ttu-id="463d7-118">**\_ВИДЕОИНПУТДЕВИЦЕКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="463d7-118">**CLSID\_VideoInputDeviceCategory**</span></span> | <span data-ttu-id="463d7-119">Устройства видеозаписи</span><span class="sxs-lookup"><span data-stu-id="463d7-119">Video capture devices</span></span> |

    

     

    <span data-ttu-id="463d7-120">Если видеокамера имеет встроенный микрофон, она отображается в обеих категориях.</span><span class="sxs-lookup"><span data-stu-id="463d7-120">If a video camera has an integrated microphone, it appears in both categories.</span></span> <span data-ttu-id="463d7-121">Однако Камера и микрофон обрабатываются системой как отдельные устройства для перечисления, создания устройств и потоковой передачи данных.</span><span class="sxs-lookup"><span data-stu-id="463d7-121">However, the camera and microphone are treated as separate devices by the system, for purposes of enumeration, device creation, and data streaming.</span></span>

3.  <span data-ttu-id="463d7-122">Метод [**креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) возвращает указатель на интерфейс [**иенуммоникер**](/windows/win32/api/objidl/nn-objidl-ienummoniker) .</span><span class="sxs-lookup"><span data-stu-id="463d7-122">The [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method returns a pointer to the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="463d7-123">Чтобы перечислить моникеры, вызовите метод [**иенуммоникер:: Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span><span class="sxs-lookup"><span data-stu-id="463d7-123">To enumerate the monikers, call [**IEnumMoniker::Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span></span>

<span data-ttu-id="463d7-124">Следующий код создает перечислитель для указанной категории устройств.</span><span class="sxs-lookup"><span data-stu-id="463d7-124">The following code creates an enumerator for a specified device category.</span></span>


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



<span data-ttu-id="463d7-125">Интерфейс [**иенуммоникер**](/windows/win32/api/objidl/nn-objidl-ienummoniker) перечисляет список интерфейсов [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) , каждый из которых представляет моникер устройства.</span><span class="sxs-lookup"><span data-stu-id="463d7-125">The [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface enumerates a list of [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interfaces, each of which represents a device moniker.</span></span> <span data-ttu-id="463d7-126">Приложение может считывать свойства из моникера или использовать моникер для создания фильтра записи DirectShow для устройства.</span><span class="sxs-lookup"><span data-stu-id="463d7-126">The application can read properties from the moniker, or use the moniker to create a DirectShow capture filter for the device.</span></span> <span data-ttu-id="463d7-127">Свойства моникера возвращаются в виде значений **типа Variant** .</span><span class="sxs-lookup"><span data-stu-id="463d7-127">Moniker properties are returned as **VARIANT** values.</span></span> <span data-ttu-id="463d7-128">Специальные имена устройств поддерживают следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="463d7-128">The following properties are supported by device monikers.</span></span>



| <span data-ttu-id="463d7-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="463d7-129">Property</span></span>       | <span data-ttu-id="463d7-130">Описание</span><span class="sxs-lookup"><span data-stu-id="463d7-130">Description</span></span>                                                               | <span data-ttu-id="463d7-131">Тип VARIANT</span><span class="sxs-lookup"><span data-stu-id="463d7-131">VARIANT Type</span></span> |
|----------------|---------------------------------------------------------------------------|--------------|
| <span data-ttu-id="463d7-132">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="463d7-132">"FriendlyName"</span></span> | <span data-ttu-id="463d7-133">Название устройства.</span><span class="sxs-lookup"><span data-stu-id="463d7-133">The name of the device.</span></span>                                                   | <span data-ttu-id="463d7-134">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="463d7-134">**VT\_BSTR**</span></span> |
| <span data-ttu-id="463d7-135">Nописание</span><span class="sxs-lookup"><span data-stu-id="463d7-135">"Description"</span></span>  | <span data-ttu-id="463d7-136">Описание устройства.</span><span class="sxs-lookup"><span data-stu-id="463d7-136">A description of the device.</span></span>                                              | <span data-ttu-id="463d7-137">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="463d7-137">**VT\_BSTR**</span></span> |
| <span data-ttu-id="463d7-138">Измените</span><span class="sxs-lookup"><span data-stu-id="463d7-138">"DevicePath"</span></span>   | <span data-ttu-id="463d7-139">Уникальная строка, идентифицирующая устройство.</span><span class="sxs-lookup"><span data-stu-id="463d7-139">A unique string that identifies the device.</span></span> <span data-ttu-id="463d7-140">(Только устройства записи видео.)</span><span class="sxs-lookup"><span data-stu-id="463d7-140">(Video capture devices only.)</span></span> | <span data-ttu-id="463d7-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="463d7-141">**VT\_BSTR**</span></span> |
| <span data-ttu-id="463d7-142">"Вавеинид"</span><span class="sxs-lookup"><span data-stu-id="463d7-142">"WaveInID"</span></span>     | <span data-ttu-id="463d7-143">Идентификатор устройства аудиозаписи.</span><span class="sxs-lookup"><span data-stu-id="463d7-143">The identifier for an audio capture device.</span></span> <span data-ttu-id="463d7-144">(Только для устройств записи звука.)</span><span class="sxs-lookup"><span data-stu-id="463d7-144">(Audio capture devices only.)</span></span> | <span data-ttu-id="463d7-145">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="463d7-145">**VT\_I4**</span></span>   |



 

<span data-ttu-id="463d7-146">Свойства "FriendlyName" и "Description" подходят для отображения в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="463d7-146">The "FriendlyName" and "Description" properties are suitable for displaying in a UI.</span></span>

-   <span data-ttu-id="463d7-147">Свойство "FriendlyName" доступно для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="463d7-147">The "FriendlyName" property is available for every device.</span></span> <span data-ttu-id="463d7-148">Он содержит удобное для чтения имя устройства.</span><span class="sxs-lookup"><span data-stu-id="463d7-148">It contains a human-readable name for the device.</span></span>
-   <span data-ttu-id="463d7-149">Свойство "Description" доступно только для устройств с видеокамерой DV и D-ВХС/MPEG.</span><span class="sxs-lookup"><span data-stu-id="463d7-149">The "Description" property is available only for DV and D-VHS/MPEG camcorder devices.</span></span> <span data-ttu-id="463d7-150">Дополнительные сведения см. в разделе [драйвер мсдв](msdv-driver.md) и [драйвер мстапе](mstape-driver.md).</span><span class="sxs-lookup"><span data-stu-id="463d7-150">For more information, see [MSDV Driver](msdv-driver.md) and [MSTape Driver](mstape-driver.md).</span></span> <span data-ttu-id="463d7-151">Если он доступен, он содержит описание устройства, более конкретное, чем свойство "FriendlyName".</span><span class="sxs-lookup"><span data-stu-id="463d7-151">If available, it contains a description of the device which is more specific than the "FriendlyName" property.</span></span> <span data-ttu-id="463d7-152">Обычно он включает имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="463d7-152">Typically it includes the vendor name.</span></span>
-   <span data-ttu-id="463d7-153">Свойство DevicePath не является удобной для чтения строкой, но гарантирует уникальность для каждого устройства видеозаписи в системе.</span><span class="sxs-lookup"><span data-stu-id="463d7-153">The "DevicePath" property is not a human-readable string, but is guaranteed to be unique for each video capture device on the system.</span></span> <span data-ttu-id="463d7-154">Это свойство можно использовать для различения двух или более экземпляров одной и той же модели устройства.</span><span class="sxs-lookup"><span data-stu-id="463d7-154">You can use this property to distinguish between two or more instances of the same model of device.</span></span>
-   <span data-ttu-id="463d7-155">Если свойство "Вавеинид" установлено, это означает, что фильтр записи DirectShow использует интерфейсы API [аудио Audio](../multimedia/waveform-audio.md) для взаимодействия с устройством.</span><span class="sxs-lookup"><span data-stu-id="463d7-155">If the "WaveInID" property is present, it means the DirectShow capture filter uses the [Waveform Audio](../multimedia/waveform-audio.md) APIs internally to communicate with the device.</span></span> <span data-ttu-id="463d7-156">Значение свойства "Вавеинид" соответствует идентификатору, используемому функциями \**Wave \** _, например, [_ *вавеинопен* \*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span><span class="sxs-lookup"><span data-stu-id="463d7-156">The value of the "WaveInID" property corresponds to the identifier used by the \**waveIn\** _ functions, such as [_ *waveInOpen*\*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span></span>

<span data-ttu-id="463d7-157">Чтобы прочитать свойства моникера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="463d7-157">To read properties from the moniker, perform the following steps.</span></span>

1.  <span data-ttu-id="463d7-158">Вызовите метод [**IMoniker:: биндтостораже**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) , чтобы получить указатель на интерфейс [**ипропертибаг**](../com/ipropertybag-and-ipersistpropertybag.md) .</span><span class="sxs-lookup"><span data-stu-id="463d7-158">Call [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) to get a pointer to the [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) interface.</span></span>
2.  <span data-ttu-id="463d7-159">Чтобы прочитать свойство, вызовите метод **ипропертибаг:: Read** .</span><span class="sxs-lookup"><span data-stu-id="463d7-159">Call **IPropertyBag::Read** to read the property.</span></span>

<span data-ttu-id="463d7-160">В следующем примере кода показано, как перечислить список моникеров устройств и получить свойства.</span><span class="sxs-lookup"><span data-stu-id="463d7-160">The following code example shows how to enumerate a list of device monikers and get the properties.</span></span>


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



<span data-ttu-id="463d7-161">Чтобы создать фильтр записи DirectShow для устройства, вызовите метод [**IMoniker:: биндтубжект**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) , чтобы получить указатель [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="463d7-161">To create a DirectShow capture filter for the device, call the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to get an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="463d7-162">Затем вызовите [**ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , чтобы добавить фильтр в граф фильтра:</span><span class="sxs-lookup"><span data-stu-id="463d7-162">Then call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph:</span></span>


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a><span data-ttu-id="463d7-163">См. также</span><span class="sxs-lookup"><span data-stu-id="463d7-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="463d7-164">Запись звука</span><span class="sxs-lookup"><span data-stu-id="463d7-164">Audio Capture</span></span>](audio-capture.md)
</dt> <dt>

[<span data-ttu-id="463d7-165">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="463d7-165">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
