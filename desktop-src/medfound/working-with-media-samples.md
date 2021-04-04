---
description: Работа с примерами мультимедиа
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: Работа с примерами мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999864"
---
# <a name="working-with-media-samples"></a><span data-ttu-id="482c7-103">Работа с примерами мультимедиа</span><span class="sxs-lookup"><span data-stu-id="482c7-103">Working with Media Samples</span></span>

<span data-ttu-id="482c7-104">В этом разделе описывается использование интерфейса [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) для управления примерами объектов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="482c7-104">This topic describes how to use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to manipulate media sample objects.</span></span> <span data-ttu-id="482c7-105">Общие сведения о примерах мультимедиа см. в статье [примеры носителей](media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="482c7-105">For a general overview of media samples, see [Media Samples](media-samples.md).</span></span>

<span data-ttu-id="482c7-106">Чтобы создать пример носителя, вызовите функцию [**мфкреатесампле**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) .</span><span class="sxs-lookup"><span data-stu-id="482c7-106">To create a new media sample, call the [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) function.</span></span> <span data-ttu-id="482c7-107">Изначально список буферов примера пуст.</span><span class="sxs-lookup"><span data-stu-id="482c7-107">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="482c7-108">Чтобы добавить буфер в конец списка, вызовите метод [**имфсампле:: аддбуффер**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span><span class="sxs-lookup"><span data-stu-id="482c7-108">To add a buffer to the end of the list, call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="482c7-109">В следующем коде показано, как создать пример и добавить в него буфер.</span><span class="sxs-lookup"><span data-stu-id="482c7-109">The following code shows how to create a sample and add a buffer to it.</span></span>


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="482c7-110">Чтобы получить буферы из образца, рекомендуется вызвать метод [**имфсампле:: конверттоконтигуаусбуффер**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span><span class="sxs-lookup"><span data-stu-id="482c7-110">The recommended way to get the buffers from the sample is to call [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span></span> <span data-ttu-id="482c7-111">Этот метод возвращает один буфер контингуаус.</span><span class="sxs-lookup"><span data-stu-id="482c7-111">This method returns a single continguous buffer.</span></span>

<span data-ttu-id="482c7-112">Чтобы выполнить итерацию по буферам в списке, начните с вызова [**имфсампле:: жетбуфферкаунт**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span><span class="sxs-lookup"><span data-stu-id="482c7-112">To iterate through the buffers in the list, start by calling [**IMFSample::GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span></span> <span data-ttu-id="482c7-113">Этот метод возвращает количество буферов.</span><span class="sxs-lookup"><span data-stu-id="482c7-113">This method returns the number of buffers.</span></span> <span data-ttu-id="482c7-114">Затем вызовите [**имфсампле:: жетбуффербиндекс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) и укажите индекс буфера для извлечения.</span><span class="sxs-lookup"><span data-stu-id="482c7-114">Then call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) and specify the index of the buffer to retrieve.</span></span> <span data-ttu-id="482c7-115">Буферы индексируются с нуля.</span><span class="sxs-lookup"><span data-stu-id="482c7-115">Buffers are indexed from zero.</span></span>

<span data-ttu-id="482c7-116">В следующем коде показано, как выполнить итерацию по буферам в примере.</span><span class="sxs-lookup"><span data-stu-id="482c7-116">The following code shows how to iterate through the buffers in a sample.</span></span>


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



<span data-ttu-id="482c7-117">Примеры имеют отметку времени и длительность.</span><span class="sxs-lookup"><span data-stu-id="482c7-117">Samples have a time stamp and a duration.</span></span> <span data-ttu-id="482c7-118">Метка времени показывает, когда данные в образце должны быть визуализированы относительно часов представления.</span><span class="sxs-lookup"><span data-stu-id="482c7-118">The time stamp indicates when the data in the sample should be rendered, relative to the presentation clock.</span></span> <span data-ttu-id="482c7-119">Длительность — это период времени, в течение которого данные должны быть визуализированы.</span><span class="sxs-lookup"><span data-stu-id="482c7-119">The duration is the length of time for which the data should be rendered.</span></span> <span data-ttu-id="482c7-120">Обычно компонент, создающий данные, задает начальную отметку времени и длительность.</span><span class="sxs-lookup"><span data-stu-id="482c7-120">Typically the component that generates the data sets the initial time stamp and duration.</span></span> <span data-ttu-id="482c7-121">Эти значения могут быть изменены сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="482c7-121">These values might get modified by the Media Session.</span></span> <span data-ttu-id="482c7-122">Чтобы задать метку времени, вызовите [**имфсампле:: сетсамплетиме**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span><span class="sxs-lookup"><span data-stu-id="482c7-122">To set the time stamp, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="482c7-123">Чтобы задать длительность, вызовите [**имфсампле:: сетсампледуратион**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span><span class="sxs-lookup"><span data-stu-id="482c7-123">To set the duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="482c7-124">Примеры также могут иметь атрибуты, которые содержат дополнительные сведения о примере.</span><span class="sxs-lookup"><span data-stu-id="482c7-124">Samples can also have attributes, which contain additional information about the sample.</span></span> <span data-ttu-id="482c7-125">Список образцов атрибутов см. в разделе [Sample Attributes](sample-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="482c7-125">For a list of sample attributes, see [Sample Attributes](sample-attributes.md).</span></span> <span data-ttu-id="482c7-126">Чтобы задать и получить атрибуты, используйте [**интерфейс имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), который [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) наследует.</span><span class="sxs-lookup"><span data-stu-id="482c7-126">To set and retrieve attributes, use the [**IMFAttributes Interface**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) inherits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="482c7-127">См. также</span><span class="sxs-lookup"><span data-stu-id="482c7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="482c7-128">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="482c7-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="482c7-129">Буферы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="482c7-129">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



