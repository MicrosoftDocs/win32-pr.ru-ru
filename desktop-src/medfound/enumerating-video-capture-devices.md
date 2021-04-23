---
description: В этом разделе описывается, как перечислить устройства видеозаписи в системе пользователей и как создать экземпляр устройства.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Перечисление устройств видеозаписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccdbcf9df284cdccda09939d2d8a27174a2299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423538"
---
# <a name="enumerating-video-capture-devices"></a><span data-ttu-id="4e278-103">Перечисление устройств видеозаписи</span><span class="sxs-lookup"><span data-stu-id="4e278-103">Enumerating Video Capture Devices</span></span>

<span data-ttu-id="4e278-104">В этом разделе описывается, как перечислить устройства видеозаписи в системе пользователя и как создать экземпляр устройства.</span><span class="sxs-lookup"><span data-stu-id="4e278-104">This topic describes how to enumerate the video capture devices on the user's system, and how create an instance of a device.</span></span>

<span data-ttu-id="4e278-105">Чтобы перечислить устройства видеозаписи в системе, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4e278-105">To enumerate the video capture devices on the system, do the following:</span></span>

1.  <span data-ttu-id="4e278-106">Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="4e278-106">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span> <span data-ttu-id="4e278-107">Эта функция получает указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="4e278-107">This function receives an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="4e278-108">Вызовите метод [**имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) , чтобы задать атрибут [ \_ \_ \_ \_ типа источника атрибута MF девсаурце](mf-devsource-attribute-source-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4e278-108">Call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) to set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute.</span></span> <span data-ttu-id="4e278-109">Задайте для атрибута значение **MF \_ девсаурце \_ \_ тип источника атрибута \_ \_ видкап \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="4e278-109">Set the attribute value to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="4e278-110">Вызовите [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span><span class="sxs-lookup"><span data-stu-id="4e278-110">Call [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span></span> <span data-ttu-id="4e278-111">Эта функция получает массив [**имфактиватеных**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) указателей и размер массива.</span><span class="sxs-lookup"><span data-stu-id="4e278-111">This function receives an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and the array size.</span></span> <span data-ttu-id="4e278-112">Каждый указатель представляет отдельное устройство захвата видео.</span><span class="sxs-lookup"><span data-stu-id="4e278-112">Each pointer represents a distinct video capture device.</span></span>

<span data-ttu-id="4e278-113">Чтобы создать экземпляр устройства записи, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4e278-113">To create an instance of a capture device:</span></span>

-   <span data-ttu-id="4e278-114">Вызовите метод [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) , чтобы получить указатель на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="4e278-114">Call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>

<span data-ttu-id="4e278-115">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="4e278-115">The following code shows these steps:</span></span>


```C++
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="4e278-116">После создания источника мультимедиа Освободите указатели интерфейса и освободите память для массива:</span><span class="sxs-lookup"><span data-stu-id="4e278-116">After you create media source, release the interface pointers and free the memory for the array:</span></span>


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a><span data-ttu-id="4e278-117">См. также</span><span class="sxs-lookup"><span data-stu-id="4e278-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e278-118">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="4e278-118">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



