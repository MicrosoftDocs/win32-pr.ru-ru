---
description: Microsoft Media Foundation поддерживает запись аудио и видео.
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: Видеозапись Аудио/видео в Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506c14ee4ab94a27cfafbe18a97ffa8f05676f1f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693868"
---
# <a name="audiovideo-capture-in-media-foundation"></a><span data-ttu-id="f6067-103">Видеозапись Аудио/видео в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6067-103">Audio/Video Capture in Media Foundation</span></span>

<span data-ttu-id="f6067-104">Microsoft Media Foundation поддерживает запись аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="f6067-104">Microsoft Media Foundation supports audio and video capture.</span></span> <span data-ttu-id="f6067-105">Устройства видеозаписи поддерживаются драйвером класса УВК и должны быть совместимы с УВК 1,1.</span><span class="sxs-lookup"><span data-stu-id="f6067-105">Video capture devices are supported through the UVC class driver and must be compatible with UVC 1.1.</span></span> <span data-ttu-id="f6067-106">Устройства записи звука поддерживаются через API сеанса Windows Audio (ВАСАПИ).</span><span class="sxs-lookup"><span data-stu-id="f6067-106">Audio capture devices are supported through Windows Audio Session API (WASAPI).</span></span>

<span data-ttu-id="f6067-107">Устройство записи представляется в Media Foundation объектом источника мультимедиа, который предоставляет интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="f6067-107">A capture device is represented in Media Foundation by a media source object, which exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="f6067-108">В большинстве случаев приложение не будет использовать этот интерфейс напрямую, но будет использовать API более высокого уровня, например [средство чтения исходного кода](source-reader.md) для управления устройством записи.</span><span class="sxs-lookup"><span data-stu-id="f6067-108">In most cases, the application will not use this interface directly, but will use a higher-level API such as the [Source Reader](source-reader.md) to control the capture device.</span></span>

## <a name="enumerate-capture-devices"></a><span data-ttu-id="f6067-109">Перечисление устройств записи</span><span class="sxs-lookup"><span data-stu-id="f6067-109">Enumerate Capture Devices</span></span>

<span data-ttu-id="f6067-110">Чтобы перечислить устройства записи в системе, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f6067-110">To enumerate the capture devices on the system, perform the following steps:</span></span>

1.  <span data-ttu-id="f6067-111">Вызовите функцию [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f6067-111">Call the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function to create an attribute store.</span></span>
2.  <span data-ttu-id="f6067-112">Задайте для [атрибута \_ девсаурце \_ \_ \_ типа источника атрибута MF](mf-devsource-attribute-source-type.md) одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f6067-112">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to one of the following values:</span></span>

    | <span data-ttu-id="f6067-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f6067-113">Value</span></span>                                                    | <span data-ttu-id="f6067-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f6067-114">Description</span></span>                      |
    |----------------------------------------------------------|----------------------------------|
    | <span data-ttu-id="f6067-115">**\_ \_ тип источника атрибута MF девсаурце \_ \_ \_ аудкап \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="f6067-115">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</span></span> | <span data-ttu-id="f6067-116">Перечисление устройств записи звука.</span><span class="sxs-lookup"><span data-stu-id="f6067-116">Enumerate audio capture devices.</span></span> |
    | <span data-ttu-id="f6067-117">**\_ \_ тип источника атрибута MF девсаурце \_ \_ \_ видкап \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="f6067-117">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</span></span> | <span data-ttu-id="f6067-118">Перечисление устройств видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="f6067-118">Enumerate video capture devices.</span></span> |

    

     

3.  <span data-ttu-id="f6067-119">Вызовите функцию [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="f6067-119">Call the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="f6067-120">Эта функция выделяет массив указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="f6067-120">This function allocates an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers.</span></span> <span data-ttu-id="f6067-121">Каждый указатель представляет объект активации для одного устройства в системе.</span><span class="sxs-lookup"><span data-stu-id="f6067-121">Each pointer represents an activation object for one device on the system.</span></span>
4.  <span data-ttu-id="f6067-122">Вызовите метод [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) , чтобы создать экземпляр источника мультимедиа из одного из объектов активации.</span><span class="sxs-lookup"><span data-stu-id="f6067-122">Call the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method to create an instance of the media source from one of the activation objects.</span></span>

<span data-ttu-id="f6067-123">В следующем примере создается источник мультимедиа для первого устройства записи видео в списке перечисления:</span><span class="sxs-lookup"><span data-stu-id="f6067-123">The following example creates a media source for the first video capture device in the enumeration list:</span></span>


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



<span data-ttu-id="f6067-124">Вы можете запросить объекты активации для различных атрибутов, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="f6067-124">You can query the activation objects for various attributes, including the following:</span></span>

-   <span data-ttu-id="f6067-125">Атрибут [ \_ \_ \_ понятного \_ имени атрибута MF девсаурце](mf-devsource-attribute-friendly-name.md) содержит отображаемое имя устройства.</span><span class="sxs-lookup"><span data-stu-id="f6067-125">The [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute contains the display name of the device.</span></span> <span data-ttu-id="f6067-126">Отображаемое имя подходит для отображения пользователю, но оно может быть неуникальным.</span><span class="sxs-lookup"><span data-stu-id="f6067-126">The display name is suitable for showing to the user, but might not be unique.</span></span>
-   <span data-ttu-id="f6067-127">Для видеоустройств [ \_ \_ тип источника атрибута MF девсаурце \_ \_ \_ видкап \_ символьная \_ ссылка](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) содержит символическую ссылку на устройство.</span><span class="sxs-lookup"><span data-stu-id="f6067-127">For video devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute contains the symbolic link to the device.</span></span> <span data-ttu-id="f6067-128">Символьная ссылка уникальным образом идентифицирует устройство в системе, но не является строкой, доступной для чтения.</span><span class="sxs-lookup"><span data-stu-id="f6067-128">The symbolic link uniquely identifies the device on the system, but is not a readable string.</span></span>
-   <span data-ttu-id="f6067-129">Для звуковых устройств в атрибуте [ \_ девсаурце \_ \_ типа источника атрибут MF \_ \_ аудкап \_ \_ ](mf-devsource-attribute-source-type-audcap-endpoint-id.md) содержится идентификатор конечной точки аудио устройства.</span><span class="sxs-lookup"><span data-stu-id="f6067-129">For audio devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute contains the audio endpoint ID of the device.</span></span> <span data-ttu-id="f6067-130">Идентификатор конечной точки аудио похож на символическую ссылку.</span><span class="sxs-lookup"><span data-stu-id="f6067-130">The audio endpoint ID is similar to a symbolic link.</span></span> <span data-ttu-id="f6067-131">Он однозначно определяет устройство в системе, но не является строкой, доступной для чтения.</span><span class="sxs-lookup"><span data-stu-id="f6067-131">It uniquely identifies the device on the system, but is not a readable string.</span></span>

<span data-ttu-id="f6067-132">Следующий пример принимает массив [**имфактиватеных**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) указателей и выводит отображаемое имя каждого устройства в окне отладки:</span><span class="sxs-lookup"><span data-stu-id="f6067-132">The following example takes an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and prints the display name of each device to the debug window:</span></span>


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



<span data-ttu-id="f6067-133">Если вы уже знакомы с символической ссылкой для видеоустройства, существует другой способ создания источника мультимедиа для устройства:</span><span class="sxs-lookup"><span data-stu-id="f6067-133">If you already know the symbolic link for a video device, there is another way to create the media source for the device:</span></span>

1.  <span data-ttu-id="f6067-134">Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f6067-134">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="f6067-135">Задайте для [атрибута \_ MF \_ девсаурце \_ \_ тип источника](mf-devsource-attribute-source-type.md) атрибут **MF \_ девсаурце \_ \_ тип источника атрибута \_ \_ \_ GUID видкап**.</span><span class="sxs-lookup"><span data-stu-id="f6067-135">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="f6067-136">Задайте для [атрибута \_ MF \_ девсаурце \_ \_ тип источника \_ видкап \_ символьную \_ ссылку](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) на символьную ссылку.</span><span class="sxs-lookup"><span data-stu-id="f6067-136">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute to the symbolic link.</span></span>
4.  <span data-ttu-id="f6067-137">Вызовите функцию [**мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) или [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="f6067-137">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span> <span data-ttu-id="f6067-138">Первый возвращает указатель [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="f6067-138">The former returns an [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) pointer.</span></span> <span data-ttu-id="f6067-139">Последний возвращает указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) на объект активации.</span><span class="sxs-lookup"><span data-stu-id="f6067-139">The latter returns an [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer to an activation object.</span></span> <span data-ttu-id="f6067-140">Для создания источника можно использовать объект активации.</span><span class="sxs-lookup"><span data-stu-id="f6067-140">You can use the activation object to create the source.</span></span> <span data-ttu-id="f6067-141">(Объект активации можно маршалировать в другой процесс, поэтому он полезен, если необходимо создать источник в другом процессе.</span><span class="sxs-lookup"><span data-stu-id="f6067-141">(An activation object can be marshaled to another process, so it is useful if you want to create the source in another process.</span></span> <span data-ttu-id="f6067-142">Дополнительные сведения см. в разделе [объекты активации](activation-objects.md).)</span><span class="sxs-lookup"><span data-stu-id="f6067-142">For more information, see [Activation Objects](activation-objects.md).)</span></span>

<span data-ttu-id="f6067-143">В следующем примере используется символьная ссылка видеоустройства и создается источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f6067-143">The following example takes the symbolic link of a video device and creates a media source.</span></span>


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



<span data-ttu-id="f6067-144">Существует эквивалентный способ создания звукового устройства из идентификатора конечной точки аудио:</span><span class="sxs-lookup"><span data-stu-id="f6067-144">There is an equivalent way to create an audio device from the audio endpoint ID:</span></span>

1.  <span data-ttu-id="f6067-145">Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f6067-145">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="f6067-146">Задайте для [атрибута \_ MF \_ девсаурце \_ \_ тип источника](mf-devsource-attribute-source-type.md) атрибут **MF \_ девсаурце \_ \_ тип источника атрибута \_ \_ \_ GUID аудкап**.</span><span class="sxs-lookup"><span data-stu-id="f6067-146">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="f6067-147">Задайте для [атрибута \_ девсаурце \_ \_ типа источника атрибута MF \_ \_ аудкап \_ \_ ](mf-devsource-attribute-source-type-audcap-endpoint-id.md) идентификатор конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f6067-147">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute to the endpoint ID.</span></span>
4.  <span data-ttu-id="f6067-148">Вызовите функцию [**мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) или [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="f6067-148">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="f6067-149">В следующем примере используется идентификатор конечной точки аудио и создается источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f6067-149">The following example takes an audio endpoint ID and creates a media source.</span></span>


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a><span data-ttu-id="f6067-150">Использование устройства записи</span><span class="sxs-lookup"><span data-stu-id="f6067-150">Use a capture device</span></span>

<span data-ttu-id="f6067-151">После создания источника мультимедиа для устройства записи используйте [средство чтения исходного кода](source-reader.md) для получения данных с устройства.</span><span class="sxs-lookup"><span data-stu-id="f6067-151">After you create the media source for a capture device, use the [Source Reader](source-reader.md) to get data from the device.</span></span> <span data-ttu-id="f6067-152">Модуль чтения исходного кода предоставляет примеры носителей, содержащие звуковые данные и видеокадры записи.</span><span class="sxs-lookup"><span data-stu-id="f6067-152">The Source Reader delivers media samples that contain the capture audio data or video frames.</span></span> <span data-ttu-id="f6067-153">Следующий шаг зависит от сценария приложения:</span><span class="sxs-lookup"><span data-stu-id="f6067-153">The next step depends on your application scenario:</span></span>

-   <span data-ttu-id="f6067-154">Предварительный просмотр видео. Используйте Microsoft Direct3D или Direct2D для вывода видео.</span><span class="sxs-lookup"><span data-stu-id="f6067-154">Video preview: Use Microsoft Direct3D or Direct2D to display the video.</span></span>
-   <span data-ttu-id="f6067-155">Запись файла. для кодирования файла используйте [модуль записи приемника](sink-writer.md) .</span><span class="sxs-lookup"><span data-stu-id="f6067-155">File capture: Use the [Sink Writer](sink-writer.md) to encode the file.</span></span>
-   <span data-ttu-id="f6067-156">Предварительный просмотр аудио: используйте [васапи](/windows/desktop/CoreAudio/wasapi).</span><span class="sxs-lookup"><span data-stu-id="f6067-156">Audio preview: Use [WASAPI](/windows/desktop/CoreAudio/wasapi).</span></span>

<span data-ttu-id="f6067-157">Если вы хотите объединить запись звука с видеозаписью, используйте *Объединенный источник мультимедиа*.</span><span class="sxs-lookup"><span data-stu-id="f6067-157">If you want to combine audio capture with video capture, use the *aggregate media source*.</span></span> <span data-ttu-id="f6067-158">Объединенный источник мультимедиа содержит коллекцию источников мультимедиа и объединяет все свои потоки в один объект источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f6067-158">The aggregate media source contains a collection of media sources and combines all of their streams into a single media source object.</span></span> <span data-ttu-id="f6067-159">Чтобы создать экземпляр агрегатного источника мультимедиа, вызовите функцию [**мфкреатеаггрегатесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) .</span><span class="sxs-lookup"><span data-stu-id="f6067-159">To create an instance of the aggregate media source, call the [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) function.</span></span>

## <a name="shut-down-the-capture-device"></a><span data-ttu-id="f6067-160">Завершение работы устройства записи</span><span class="sxs-lookup"><span data-stu-id="f6067-160">Shut down the capture device</span></span>

<span data-ttu-id="f6067-161">Если устройство записи больше не требуется, необходимо завершить работу устройства, вызвав метод [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) для объекта [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , полученного путем вызова [**Мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) или [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="f6067-161">When the capture device is no longer needed, you must shut down the device by calling [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) object you obtained by calling [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="f6067-162">Сбой вызова функции **завершения работы** может привести к созданию ссылок на память, так как система может оставаться ссылкой на ресурсы **имфмедиасаурце** , пока не будет вызвано **Завершение работы** .</span><span class="sxs-lookup"><span data-stu-id="f6067-162">Failure to call **Shutdown** can result in memory links because the system may keep a reference to **IMFMediaSource** resources until **Shutdown** is called.</span></span>


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



<span data-ttu-id="f6067-163">Если вы выделили строку, содержащую символическую ссылку на устройство записи, также следует освободить этот объект.</span><span class="sxs-lookup"><span data-stu-id="f6067-163">If you allocated a string containing the symbolic link to a capture device, you should release this object as well.</span></span>


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a><span data-ttu-id="f6067-164">См. также</span><span class="sxs-lookup"><span data-stu-id="f6067-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6067-165">Захват аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="f6067-165">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 
