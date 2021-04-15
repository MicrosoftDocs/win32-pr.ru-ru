---
description: Задание свойств сжатия видео
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Задание свойств сжатия видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d29ed7e42745ffd51fca14b7da5f72c749281e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422941"
---
# <a name="setting-video-compression-properties"></a><span data-ttu-id="419ff-103">Задание свойств сжатия видео</span><span class="sxs-lookup"><span data-stu-id="419ff-103">Setting Video Compression Properties</span></span>

<span data-ttu-id="419ff-104">Фильтры сжатия видео могут поддерживать интерфейс [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) на выходных контактах.</span><span class="sxs-lookup"><span data-stu-id="419ff-104">Video compression filters can support the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface on their output pins.</span></span> <span data-ttu-id="419ff-105">Этот интерфейс используется для задания свойств сжатия, таких как частота ключевых кадров, число прогнозируемых кадров (P) на опорный кадр и относительное качество сжатия.</span><span class="sxs-lookup"><span data-stu-id="419ff-105">Use this interface to set compression properties, such as the key frame rate, the number of predicted (P) frames per key frame, and the relative compression quality.</span></span>

<span data-ttu-id="419ff-106">Сначала вызовите метод [**ибасефилтер:: енумпинс**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , чтобы найти ПИН-код вывода фильтра, и запросите ПИН-код для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="419ff-106">First, call the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the filter's output pin, and query the pin for the interface.</span></span> <span data-ttu-id="419ff-107">Некоторые фильтры могут вообще не поддерживать интерфейс.</span><span class="sxs-lookup"><span data-stu-id="419ff-107">Some filters may not support the interface at all.</span></span> <span data-ttu-id="419ff-108">Другие могут предоставлять интерфейс, но не поддерживают все свойства сжатия.</span><span class="sxs-lookup"><span data-stu-id="419ff-108">Others may expose the interface but not support every compression property.</span></span> <span data-ttu-id="419ff-109">Чтобы определить, какие свойства поддерживаются, вызовите [**иамвидеокомпрессион:: info**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span><span class="sxs-lookup"><span data-stu-id="419ff-109">To determine which properties are supported, call [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="419ff-110">Этот метод возвращает несколько фрагментов информации:</span><span class="sxs-lookup"><span data-stu-id="419ff-110">This method returns several pieces of information:</span></span>

-   <span data-ttu-id="419ff-111">Набор флагов возможностей</span><span class="sxs-lookup"><span data-stu-id="419ff-111">A set of capabilities flags</span></span>
-   <span data-ttu-id="419ff-112">Строка описательной строки и номера версии</span><span class="sxs-lookup"><span data-stu-id="419ff-112">A descriptive string and version-number string</span></span>
-   <span data-ttu-id="419ff-113">Значения по умолчанию для частоты ключевых кадров, P-частоты кадров и качества (если поддерживается)</span><span class="sxs-lookup"><span data-stu-id="419ff-113">Default values for key frame rate, P frame rate, and quality (when supported)</span></span>

<span data-ttu-id="419ff-114">Метод имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="419ff-114">The method has the following syntax:</span></span>


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



<span data-ttu-id="419ff-115">Параметры *псзверсион* и *псздеск* — это буферы расширенных символов, которые получают строку версии и строку описания.</span><span class="sxs-lookup"><span data-stu-id="419ff-115">The *pszVersion* and *pszDesc* parameters are wide-character buffers that receive the version string and description string.</span></span> <span data-ttu-id="419ff-116">Параметры *кбверсион* и *кбдеск* получают требуемые размеры буфера в байтах (не в символах).</span><span class="sxs-lookup"><span data-stu-id="419ff-116">The *cbVersion* and *cbDesc* parameters receive the required buffer sizes in bytes (not characters).</span></span> <span data-ttu-id="419ff-117">Параметры *лкэйфраме*, *лпфраме* и *дблкуалити* получают значения по умолчанию для частоты ключевых кадров, P частоты кадров и качества.</span><span class="sxs-lookup"><span data-stu-id="419ff-117">The *lKeyFrame*, *lPFrame*, and *dblQuality* parameters receive the default values for the key frame rate, P frame rate, and quality.</span></span> <span data-ttu-id="419ff-118">Качество выражается в виде числа с плавающей запятой от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="419ff-118">Quality is expressed as a floating-point number from 0.0 to 1.0.</span></span> <span data-ttu-id="419ff-119">Параметр *лкап* получает битовую операцию **или** для флагов возможностей, которые определяются перечисляемым типом [**компрессионкапс**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) .</span><span class="sxs-lookup"><span data-stu-id="419ff-119">The *lCap* parameter receives a bitwise **OR** of the capabilities flags, which are defined by the [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) enumerated type.</span></span>

<span data-ttu-id="419ff-120">Любой из этих параметров может иметь **значение NULL**, в этом случае метод игнорирует этот параметр.</span><span class="sxs-lookup"><span data-stu-id="419ff-120">Any of these parameters can be **NULL**, in which case the method ignores that parameter.</span></span> <span data-ttu-id="419ff-121">Например, чтобы выделить буферы для строк версии и описания, сначала вызовите метод со **значением NULL** в первом и третьем параметрах.</span><span class="sxs-lookup"><span data-stu-id="419ff-121">For example, to allocate buffers for the version and description strings, first call the method with **NULL** in the first and third parameters.</span></span> <span data-ttu-id="419ff-122">Используйте возвращаемые значения для *кбверсион* и *кбдеск* , чтобы выделить буферы, а затем снова вызовите метод:</span><span class="sxs-lookup"><span data-stu-id="419ff-122">Use the returned values for *cbVersion* and *cbDesc* to allocate the buffers and then call the method again:</span></span>


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



<span data-ttu-id="419ff-123">Значение *лкап* указывает, какие из других методов **иамвидеокомпрессион** поддерживаются фильтром.</span><span class="sxs-lookup"><span data-stu-id="419ff-123">The value of *lCap* indicates which of the other **IAMVideoCompression** methods the filter supports.</span></span> <span data-ttu-id="419ff-124">Например, если *лкап* содержит \_ флаг компрессионкапс канкэйфраме, можно вызвать [**иамвидеокомпрессион:: Get \_ кэйфрамерате**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) , чтобы получить частоту ключевых кадров и [**иамвидеокомпрессион::p UT \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) , чтобы установить частоту ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="419ff-124">For example, if *lCap* contains the CompressionCaps\_CanKeyFrame flag, you can call [**IAMVideoCompression::get\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) to get the key frame rate and [**IAMVideoCompression::put\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) to set the key frame rate.</span></span> <span data-ttu-id="419ff-125">Отрицательное значение указывает, что фильтр будет использовать значение по умолчанию, полученное из [**иамвидеокомпрессион::-info**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span><span class="sxs-lookup"><span data-stu-id="419ff-125">A negative value indicates that the filter will use the default value, as obtained from [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="419ff-126">Пример:</span><span class="sxs-lookup"><span data-stu-id="419ff-126">For example:</span></span>


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



<span data-ttu-id="419ff-127">В следующем примере кода предпринимается попытка найти интерфейс **иамвидеокомпрессион** на выходном ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="419ff-127">The following code example tries to find the **IAMVideoCompression** interface on the output pin.</span></span> <span data-ttu-id="419ff-128">Если он будет выполнен, он извлекает значения по умолчанию и фактические данные для свойств сжатия:</span><span class="sxs-lookup"><span data-stu-id="419ff-128">If it succeeds, it retrieves the default and actual values for the compression properties:</span></span>


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="419ff-129">Если для построения графа используется интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , можно получить интерфейс **иамвидеокомпрессион** , вызвав [**ICaptureGraphBuilder2:: Финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)вместо **ибасефилтер:: енумпинс**.</span><span class="sxs-lookup"><span data-stu-id="419ff-129">If you are using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface to build your graph, you can obtain the **IAMVideoCompression** interface by calling [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), instead of using **IBaseFilter::EnumPins**.</span></span> <span data-ttu-id="419ff-130">Метод **финдинтерфаце** — это вспомогательный метод, который ищет в графе фильтры и ПИН-коды для указанного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="419ff-130">The **FindInterface** method is a helper method that searches filters and pins in the graph for a specified interface.</span></span>

 

 

 



