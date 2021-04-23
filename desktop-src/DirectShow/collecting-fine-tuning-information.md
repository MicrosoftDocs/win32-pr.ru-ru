---
description: Сбор сведений о Fine-Tuning
ms.assetid: 0d9ea896-e0a9-411b-9a10-e366e3686a34
title: Сбор сведений о Fine-Tuning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d191f677acc9306202bce141ef8f6683b43c61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662015"
---
# <a name="collecting-fine-tuning-information"></a><span data-ttu-id="aa448-103">Сбор сведений о Fine-Tuning</span><span class="sxs-lookup"><span data-stu-id="aa448-103">Collecting Fine-Tuning Information</span></span>

<span data-ttu-id="aa448-104">Несмотря на то, что частоты кабелей обычно должны быть точными, частота широковещательной передачи может быть увеличена или снижена на несколько кГц на станции вещания, чтобы снизить потенциальные помехи с соседними каналами.</span><span class="sxs-lookup"><span data-stu-id="aa448-104">Although cable frequencies are generally expected to be exact, broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span>

<span data-ttu-id="aa448-105">Когда фильтр ТВ-тюнера подстраивается к каналу, он сканирует наиболее точный сигнал.</span><span class="sxs-lookup"><span data-stu-id="aa448-105">When the TV Tuner filter tunes to a channel, it scans for the most precise signal.</span></span> <span data-ttu-id="aa448-106">Чтобы сохранить эти сведения в реестре для последующих операций настройки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="aa448-106">To save this information in the registry for subsequent tuning operations, do the following:</span></span>

1.  <span data-ttu-id="aa448-107">Вызовите [**иамтунер:: чаннелминмакс**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) , чтобы определить диапазон частотных записей в текущей таблице частоты.</span><span class="sxs-lookup"><span data-stu-id="aa448-107">Call [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) to determine the range of frequency entries in the current frequency table.</span></span>
2.  <span data-ttu-id="aa448-108">Вызовите метод [**иамтунер::p \_ UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) один раз для каждого индекса частоты в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="aa448-108">Call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method once for each frequency index in the range.</span></span>
3.  <span data-ttu-id="aa448-109">Вызовите метод [**иамтвтунер:: стореаутотуне**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) , чтобы сохранить сведения о точной настройке в реестре.</span><span class="sxs-lookup"><span data-stu-id="aa448-109">Call [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) to save the fine-tuning information in the registry.</span></span> <span data-ttu-id="aa448-110">Сведения хранятся в разделе реестра для текущего пространства настройки.</span><span class="sxs-lookup"><span data-stu-id="aa448-110">The information is stored under the registry key for the current tuning space.</span></span>

<span data-ttu-id="aa448-111">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="aa448-111">The following code shows these steps:</span></span>


```C++
long lMin = 0, lMax = 0;
hr = pTuner->ChannelMinMax(&lMin, &lMax);
if (SUCCEEDED(hr))
{
    for (long i = lMin; i <= lMax; i++)
    {
        pTuner->put_Channel(i, AMTUNER_SUBCHAN_DEFAULT,
            AMTUNER_SUBCHAN_DEFAULT)
    }
    pTuner->StoreAutoTune();
}
```



<span data-ttu-id="aa448-112">В более ранних версиях фильтра ТВ-тюнера для точной настройки рекомендуется метод [**иамтвтунер:: автонастройка**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) .</span><span class="sxs-lookup"><span data-stu-id="aa448-112">With earlier versions of the TV Tuner filter, the [**IAMTVTuner::AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method was recommended for fine-tuning.</span></span> <span data-ttu-id="aa448-113">Однако этот метод игнорирует любые переопределения частоты, поэтому его использование больше не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="aa448-113">However, this method ignores any frequency overrides, so its use is no longer recommended.</span></span> <span data-ttu-id="aa448-114">Следующий код эквивалентен методу **автонастройки** , но правильно работает с переопределениями частоты:</span><span class="sxs-lookup"><span data-stu-id="aa448-114">The following code is equivalent to the **AutoTune** method, but works correctly with frequency overrides:</span></span>


```C++
HRESULT MyAutoTune(IAMTVTuner *pTuner, long lIndex, long *plFoundSignal)
{
    long SignalStrength = AMTUNER_NOSIGNAL;
    HRESULT hr;
    hr = pTuner->put_Channel(lIndex, AMTUNER_SUBCHAN_DEFAULT, AMTUNER_SUBCHAN_DEFAULT);
    if (NOERROR == hr)
        pTuner->SignalPresent(&SignalStrength);
    *plFoundSignal = (SignalStrength != AMTUNER_NOSIGNAL);
        return hr;
}
```



<span data-ttu-id="aa448-115">При получении широковещательной рассылки не всегда можно получить горизонтальную блокировку, хотя изображение отображается.</span><span class="sxs-lookup"><span data-stu-id="aa448-115">With broadcast reception, it is not always possible to get a horizontal lock, although the picture is viewable.</span></span> <span data-ttu-id="aa448-116">В этих случаях оборудование тюнера будет иметь частотную блокировку, но декодер не будет иметь горизонтальную блокировку.</span><span class="sxs-lookup"><span data-stu-id="aa448-116">In these cases, the tuner hardware will have a frequency lock, but the decoder will not have horizontal lock.</span></span> <span data-ttu-id="aa448-117">Это условие может быть обнаружено при использовании метода [**размещения \_ канала**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) или [**автонастройки**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) с помощью проверки кода возврата.</span><span class="sxs-lookup"><span data-stu-id="aa448-117">This condition can be detected when using [**put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) or [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) by examining the return code.</span></span>



| <span data-ttu-id="aa448-118">Значение</span><span class="sxs-lookup"><span data-stu-id="aa448-118">Value</span></span>    | <span data-ttu-id="aa448-119">Описание</span><span class="sxs-lookup"><span data-stu-id="aa448-119">Description</span></span>                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa448-120">\_ОК</span><span class="sxs-lookup"><span data-stu-id="aa448-120">S\_OK</span></span>    | <span data-ttu-id="aa448-121">Операция настройки прошла удачно, и тюнер получил блокировку частоты.</span><span class="sxs-lookup"><span data-stu-id="aa448-121">The tune operation succeeded and the tuner got a frequency lock.</span></span>                                                                                                                          |
| <span data-ttu-id="aa448-122">S \_ false</span><span class="sxs-lookup"><span data-stu-id="aa448-122">S\_FALSE</span></span> | <span data-ttu-id="aa448-123">Во время операции настройки ошибки не возникали, но тюнеру не удалось получить частоту блокировки.</span><span class="sxs-lookup"><span data-stu-id="aa448-123">There were no errors during the tune operation, but the tuner was not able to get a frequency lock.</span></span> <span data-ttu-id="aa448-124">Очень маловероятно, что в результате выполнения этой операции отображается отображаемый канал.</span><span class="sxs-lookup"><span data-stu-id="aa448-124">It is highly unlikely that there is a viewable channel resulting from this operation.</span></span> |



 

<span data-ttu-id="aa448-125">Любой другой код возврата указывает на то, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="aa448-125">Any other return code indicates that some error occurred.</span></span>

<span data-ttu-id="aa448-126">Возвращаемое значение \_ ОК не гарантирует, что декодер будет горизонтальной блокировкой.</span><span class="sxs-lookup"><span data-stu-id="aa448-126">A return value of S\_OK does not guarantee that the decoder has a horizontal lock.</span></span> <span data-ttu-id="aa448-127">Метод [**автонастройки**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) обновляет параметр *фаундсигнал* , чтобы указать, была ли достигнута горизонтальная блокировка.</span><span class="sxs-lookup"><span data-stu-id="aa448-127">The [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method updates the *FoundSignal* parameter to indicate whether or not horizontal lock was achieved.</span></span> <span data-ttu-id="aa448-128">Метод [**иамтунер:: сигналпресент**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) возвращает одну и ту же информацию.</span><span class="sxs-lookup"><span data-stu-id="aa448-128">The [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) method returns the same information.</span></span>

<span data-ttu-id="aa448-129">Однако если возвращаемое значение — S \_ (ОК), приложение может пропустить параметр *фаундсигнал* , так как этот тюнер сообщает о частоте блокировки.</span><span class="sxs-lookup"><span data-stu-id="aa448-129">When the return value is S\_OK, however, the application has the option of ignoring the *FoundSignal* parameter, because the tuner is reporting a frequency lock.</span></span> <span data-ttu-id="aa448-130">Существует вероятность того, что на помехах будет блокироваться частота, но эту возможность следует взвесить на возможность пропуска просматриваемых каналов.</span><span class="sxs-lookup"><span data-stu-id="aa448-130">There is the possibility of a frequency lock on noise, but this possibility should be weighed against the possibility of skipping viewable channels.</span></span>

## <a name="registry-conversion"></a><span data-ttu-id="aa448-131">Преобразование реестра</span><span class="sxs-lookup"><span data-stu-id="aa448-131">Registry Conversion</span></span>

<span data-ttu-id="aa448-132">Для поддержки переопределений частоты внутренний формат раздела реестра, содержащего сведения о тонкой настройке, изменился.</span><span class="sxs-lookup"><span data-stu-id="aa448-132">To support frequency overrides, the internal format of the registry key that holds fine-tuning information has changed.</span></span> <span data-ttu-id="aa448-133">Исходный формат по-прежнему поддерживается для обратной совместимости, но не поддерживает переопределения частоты.</span><span class="sxs-lookup"><span data-stu-id="aa448-133">The original format is still supported for backward compatibility, but it does not support frequency overrides.</span></span>

<span data-ttu-id="aa448-134">Старый формат реестра преобразуется в новый формат всякий раз, когда вызывается метод [**иамтвтунер:: стореаутотуне**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) .</span><span class="sxs-lookup"><span data-stu-id="aa448-134">The old registry format is converted to the new format whenever the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method is called.</span></span> <span data-ttu-id="aa448-135">Если приложение добавляет переопределения частоты, оно должно вызывать метод **стореаутотуне** для преобразования в новый формат реестра.</span><span class="sxs-lookup"><span data-stu-id="aa448-135">If your application adds frequency overrides, it should call the **StoreAutoTune** method to convert to the new registry format.</span></span> <span data-ttu-id="aa448-136">Перед вызовом **стореаутотуне** не нужно сохранять сведения о точной настройке.</span><span class="sxs-lookup"><span data-stu-id="aa448-136">It is not necessary to collect any fine-tuning information before calling **StoreAutoTune**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa448-137">См. также</span><span class="sxs-lookup"><span data-stu-id="aa448-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa448-138">Международная Настройка аналогового ТВ</span><span class="sxs-lookup"><span data-stu-id="aa448-138">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



