---
description: Предварительный просмотр ТВ-звука
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Предварительный просмотр ТВ-звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cc63583c946d47ed744eacd51f0939ec852d53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494865"
---
# <a name="previewing-tv-audio"></a><span data-ttu-id="648e6-103">Предварительный просмотр ТВ-звука</span><span class="sxs-lookup"><span data-stu-id="648e6-103">Previewing TV Audio</span></span>

<span data-ttu-id="648e6-104">Для предварительного просмотра телевизионных передач направьте ПИН-код звукового декодера в фильтре микшера к ПИН-коду звукового тюнера.</span><span class="sxs-lookup"><span data-stu-id="648e6-104">To preview TV audio, route the Audio Decoder pin on the crossbar filter to the Audio Tuner pin.</span></span> <span data-ttu-id="648e6-105">Чтобы отключить звук, направьте ПИН-код звукового декодера в-1, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="648e6-105">To mute the audio, route the Audio Decoder pin to -1, as shown in the following diagram.</span></span> <span data-ttu-id="648e6-106">(Фильтры микшера описаны в разделе [Работа с микшерами](working-with-crossbars.md).)</span><span class="sxs-lookup"><span data-stu-id="648e6-106">(Crossbar filters are described in [Working with Crossbars](working-with-crossbars.md).)</span></span>

![Маршрутизация ПИН-кода звукового декодера](images/vidcap07.png)

<span data-ttu-id="648e6-108">Базовый подход выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="648e6-108">The basic approach is as follows:</span></span>

1.  <span data-ttu-id="648e6-109">Чтобы узнать Фильтр микшера, используйте метод [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) .</span><span class="sxs-lookup"><span data-stu-id="648e6-109">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the crossbar filter.</span></span>
2.  <span data-ttu-id="648e6-110">Используйте метод [**иамкроссбар:: Get \_ кроссбарпининфо**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) для перечисления входных и выходных закрепления фильтра микшера.</span><span class="sxs-lookup"><span data-stu-id="648e6-110">Use the [**IAMCrossbar::get\_CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) method to enumerate the crossbar filter's input and output pins.</span></span> <span data-ttu-id="648e6-111">Поиск выходного ПИН-кода декодера и входного контакта звукового тюнера.</span><span class="sxs-lookup"><span data-stu-id="648e6-111">Search for an audio decoder output pin and an audio tuner input pin.</span></span>
3.  <span data-ttu-id="648e6-112">Если вы нашли правильные ПИН-коды, вызовите [**иамкроссбар:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) , чтобы маршрутизировать контакты.</span><span class="sxs-lookup"><span data-stu-id="648e6-112">If you find the correct pins, call [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) to route the pins.</span></span> <span data-ttu-id="648e6-113">Если нет, воссмотрите поток для другого микшера и повторите этот процесс.</span><span class="sxs-lookup"><span data-stu-id="648e6-113">If not, look upstream for another crossbar and repeat the process.</span></span>
4.  <span data-ttu-id="648e6-114">Чтобы отключить звук, направьте ПИН-код звукового декодера в значение – 1.</span><span class="sxs-lookup"><span data-stu-id="648e6-114">To mute the audio, route the audio decoder pin to -1.</span></span>

<span data-ttu-id="648e6-115">Большинство ТВ-тюнеров используют один фильтр микшера, но некоторые используют два фильтра микшера.</span><span class="sxs-lookup"><span data-stu-id="648e6-115">Most TV tuners use a single crossbar filter, but some use two crossbar filters.</span></span> <span data-ttu-id="648e6-116">Поэтому, если первый из них завершается ошибкой, может потребоваться выполнить поиск второго микшера.</span><span class="sxs-lookup"><span data-stu-id="648e6-116">Therefore, you might have to search for a second crossbar if the first one fails.</span></span>

> [!Note]  
> <span data-ttu-id="648e6-117">В отличие от того, что вы можете ожидать, для предварительного просмотра звука не требуется фильтр записи звука или модуль подготовки звука, так как между платой тюнера и звуковой картой есть физическое подключение.</span><span class="sxs-lookup"><span data-stu-id="648e6-117">Contrary to what you might expect, no audio capture filter or audio renderer is required to preview the audio, because there is a physical connection between the tuner card and the sound card.</span></span>

 

<span data-ttu-id="648e6-118">В следующем коде эти действия показаны более подробно.</span><span class="sxs-lookup"><span data-stu-id="648e6-118">The following code shows these steps in more detail.</span></span> <span data-ttu-id="648e6-119">Во-первых, это вспомогательная функция, которая выполняет поиск фильтра микшера для указанного типа ПИН-кода:</span><span class="sxs-lookup"><span data-stu-id="648e6-119">First, here is a helper function that searches a crossbar filter for a specified pin type:</span></span>


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



<span data-ttu-id="648e6-120">Следующая функция пытается активировать или отключить звук, в зависимости от значения параметра *бактивате* .</span><span class="sxs-lookup"><span data-stu-id="648e6-120">The next function attempts to activate or mute the audio, depending on the value of the *bActivate* parameter.</span></span> <span data-ttu-id="648e6-121">Он выполняет поиск требуемых ПИН-кодов в указанном фильтре микшера.</span><span class="sxs-lookup"><span data-stu-id="648e6-121">It searches the specified crossbar filter for the required pins.</span></span> <span data-ttu-id="648e6-122">Если они не найдены, возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="648e6-122">If it cannot find them, it returns an error code.</span></span>


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



<span data-ttu-id="648e6-123">Следующая функция выполняет поиск фильтра микшера на графе фильтра.</span><span class="sxs-lookup"><span data-stu-id="648e6-123">The next function searches the filter graph for a crossbar filter.</span></span> <span data-ttu-id="648e6-124">Если он найден, он пытается активировать или отключить звук (с помощью функции Previous).</span><span class="sxs-lookup"><span data-stu-id="648e6-124">If it finds one, it attempts to activate or mute the audio (using the previous function).</span></span> <span data-ttu-id="648e6-125">Если эта операция завершается неудачно, метод выполняет поиск второго микшера и пытается повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="648e6-125">If that operation fails, the method searches upstream for a second crossbar and tries again.</span></span> <span data-ttu-id="648e6-126">Более обобщенный подход к управлению несколькими фильтрами микшера в графе см. в описании класса Ккроссбар в примере приложения Амкап.</span><span class="sxs-lookup"><span data-stu-id="648e6-126">For a more generalized approach to managing multiple crossbar filters in a graph, see the CCrossbar class in the AmCap sample application.</span></span>


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



<span data-ttu-id="648e6-127">В следующем коде показано, как вызывать эти функции:</span><span class="sxs-lookup"><span data-stu-id="648e6-127">The following code shows how to call these functions:</span></span>


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



<span data-ttu-id="648e6-128">Обратите внимание, что эти примеры функций повторяют многие из одних и тех же вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="648e6-128">Note that these example functions repeat many of the same function calls.</span></span> <span data-ttu-id="648e6-129">Например, они перечисляют контакты микшера каждый раз.</span><span class="sxs-lookup"><span data-stu-id="648e6-129">For example, they enumerate the crossbar pins each time.</span></span> <span data-ttu-id="648e6-130">В реальном приложении можно кэшировать некоторые из этих сведений.</span><span class="sxs-lookup"><span data-stu-id="648e6-130">In a real application, you might cache some of this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="648e6-131">См. также</span><span class="sxs-lookup"><span data-stu-id="648e6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="648e6-132">Аналоговый телевизор</span><span class="sxs-lookup"><span data-stu-id="648e6-132">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="648e6-133">Работа с микшерами</span><span class="sxs-lookup"><span data-stu-id="648e6-133">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



