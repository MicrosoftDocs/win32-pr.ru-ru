---
description: Формат потока
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Формат потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684117"
---
# <a name="stream-format"></a><span data-ttu-id="34d5d-103">Формат потока</span><span class="sxs-lookup"><span data-stu-id="34d5d-103">Stream Format</span></span>

<span data-ttu-id="34d5d-104">Драйвер МСДВ и УВК может выводить два формата DV: чередование аудио-видео или видео.</span><span class="sxs-lookup"><span data-stu-id="34d5d-104">Both the MSDV and the UVC driver can output two DV formats: interleaved audio-video, or video only.</span></span> <span data-ttu-id="34d5d-105">Чередование аудио-видео — это исходный формат с устройства.</span><span class="sxs-lookup"><span data-stu-id="34d5d-105">Interleaved audio-video is the original format from the device.</span></span> <span data-ttu-id="34d5d-106">Формат видео содержит те же данные, но образцы помечены как не имеющие звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="34d5d-106">The video-only format contains the same data, but the samples are marked as having no audio data.</span></span> <span data-ttu-id="34d5d-107">Формат видео хранится в основном для обеспечения совместимости с приложениями, которые используют видео для Windows.</span><span class="sxs-lookup"><span data-stu-id="34d5d-107">The video-only format exists mainly for compatibility with applications that use Video for Windows.</span></span> <span data-ttu-id="34d5d-108">Дополнительные сведения см. в разделе [видео AVI типа "тип 1" и "тип-2](type-1-vs--type-2-dv-avi-files.md)".</span><span class="sxs-lookup"><span data-stu-id="34d5d-108">For more information, see [Type-1 vs. Type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md).</span></span>

<span data-ttu-id="34d5d-109">**Драйвер МСДВ**</span><span class="sxs-lookup"><span data-stu-id="34d5d-109">**MSDV Driver**</span></span>

<span data-ttu-id="34d5d-110">Драйвер МСДВ имеет два выходных контакта.</span><span class="sxs-lookup"><span data-stu-id="34d5d-110">The MSDV driver has two output pins.</span></span> <span data-ttu-id="34d5d-111">Первый выходной ПИН-код отправляет данные с чередованием, а второй выходной закрепление отправляет данные только для видео.</span><span class="sxs-lookup"><span data-stu-id="34d5d-111">The first output pin sends interleaved data, and the second output pin sends video-only data.</span></span> <span data-ttu-id="34d5d-112">В каждый момент времени может быть подключен только один выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="34d5d-112">Only one output pin can be connected at a time.</span></span> <span data-ttu-id="34d5d-113">Чтобы выбрать формат, подключите соответствующий выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="34d5d-113">To select a format, connect the appropriate output pin.</span></span> <span data-ttu-id="34d5d-114">Для поиска формата можно использовать интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) на выходном ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="34d5d-114">You can use the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on the output pin to find the format.</span></span>

<span data-ttu-id="34d5d-115">**Драйвер УВК**</span><span class="sxs-lookup"><span data-stu-id="34d5d-115">**UVC Driver**</span></span>

<span data-ttu-id="34d5d-116">В отличие от драйвера МСДВ драйвер УВК доставляет оба формата из одного и того же ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="34d5d-116">Unlike the MSDV driver, the UVC driver delivers both formats from the same pin.</span></span> <span data-ttu-id="34d5d-117">Форматом по умолчанию является "только видео".</span><span class="sxs-lookup"><span data-stu-id="34d5d-117">The default format is video-only.</span></span> <span data-ttu-id="34d5d-118">Чтобы выбрать формат, используйте интерфейс **иамстреамконфиг** на выходном ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="34d5d-118">To select the format, use the **IAMStreamConfig** interface on the output pin.</span></span> <span data-ttu-id="34d5d-119">Вызовите метод **жетстреамкапс** , чтобы перечислить типы мультимедиа для выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="34d5d-119">Call the **GetStreamCaps** method to enumerate the media types on the output pin.</span></span> <span data-ttu-id="34d5d-120">Если основной тип соответствует требуемому формату, то для каждого типа носителя вызовите **сетформат** и передайте этот тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="34d5d-120">For each media type, if the major type matches the desired format, call **SetFormat** and pass in that media type.</span></span>



| <span data-ttu-id="34d5d-121">Формат</span><span class="sxs-lookup"><span data-stu-id="34d5d-121">Format</span></span>                      | <span data-ttu-id="34d5d-122">Основной тип</span><span class="sxs-lookup"><span data-stu-id="34d5d-122">Major type</span></span>             |
|-----------------------------|------------------------|
| <span data-ttu-id="34d5d-123">Аудио и видео с чередованием</span><span class="sxs-lookup"><span data-stu-id="34d5d-123">Interleaved audio and video</span></span> | <span data-ttu-id="34d5d-124">\_Чередующийся MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="34d5d-124">MEDIATYPE\_Interleaved</span></span> |
| <span data-ttu-id="34d5d-125">Только видео</span><span class="sxs-lookup"><span data-stu-id="34d5d-125">Video only</span></span>                  | <span data-ttu-id="34d5d-126">\_Видео MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="34d5d-126">MEDIATYPE\_Video</span></span>       |



 

<span data-ttu-id="34d5d-127">Следующая функция задает формат, основанный на идентификаторе GUID основного типа.</span><span class="sxs-lookup"><span data-stu-id="34d5d-127">The following function sets the format based on the major type GUID.</span></span>


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



<span data-ttu-id="34d5d-128">Драйвер МСДВ также поддерживает **иамстреамконфиг**, поэтому можно написать код, который работает для обоих типов устройств.</span><span class="sxs-lookup"><span data-stu-id="34d5d-128">The MSDV driver also supports **IAMStreamConfig**, so you can write code that works for both device types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34d5d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="34d5d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34d5d-130">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="34d5d-130">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



