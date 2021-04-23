---
description: Настройка аналогового телевидения
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: Настройка аналогового телевидения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b85d0826340b913df88cb20dc538bc85943949b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655605"
---
# <a name="analog-television-tuning"></a><span data-ttu-id="db149-103">Настройка аналогового телевидения</span><span class="sxs-lookup"><span data-stu-id="db149-103">Analog Television Tuning</span></span>

<span data-ttu-id="db149-104">Настройка осуществляется с помощью фильтра ТВ-тюнера через интерфейс [**иамтвтунер**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) .</span><span class="sxs-lookup"><span data-stu-id="db149-104">Tuning is controlled by the TV Tuner filter, through the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="db149-105">Интерфейс Иамтвтунер наследует Иамтунер.</span><span class="sxs-lookup"><span data-stu-id="db149-105">The IAMTVTuner interface inherits IAMTuner.</span></span> <span data-ttu-id="db149-106">Чтобы получить указатель на интерфейс, вызовите метод [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="db149-106">To obtain a pointer to the interface, call the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method as follows:</span></span>


```C++
IAMTVTuner *pTuner = NULL;
hr = pBuild->FindInterface(
    &LOOK_UPSTREAM_ONLY,  // Look upstream from pCap.
    NULL,                 // No particular media type.
    pCap,                 // Pointer to the capture filter.
    IID_IAMTVTuner, (void**)&pTuner);
if (SUCCEEDED(hr))
{
    // Use pTuner ...
    pTuner->Release();
}
```



<span data-ttu-id="db149-107">Первый параметр указывает, что следует искать в потоке из фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="db149-107">The first parameter indicates to search upstream from the capture filter.</span></span>

<span data-ttu-id="db149-108">Частоты таблиц</span><span class="sxs-lookup"><span data-stu-id="db149-108">Frequency Tables</span></span>

<span data-ttu-id="db149-109">На внутреннем уровне фильтр ТВ-тюнера хранит список таблиц с частотой.</span><span class="sxs-lookup"><span data-stu-id="db149-109">Internally, the TV Tuner filter keeps a list of frequency tables.</span></span> <span data-ttu-id="db149-110">Каждая таблица частоты соответствует частоте вещания или кабелей для определенной страны или региона.</span><span class="sxs-lookup"><span data-stu-id="db149-110">Each frequency table corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="db149-111">Также существует стандартная таблица частоты "Уникабле", которая используется, когда страна или регион не имеют стандартного набора назначений частоты.</span><span class="sxs-lookup"><span data-stu-id="db149-111">There is also a generic "Unicable" frequency table, which is used when a country/region does not have a standard set of frequency assignments.</span></span>

<span data-ttu-id="db149-112">Каждая таблица Frequency содержит список частот настройки.</span><span class="sxs-lookup"><span data-stu-id="db149-112">Each frequency table contains a list of tuning frequencies.</span></span> <span data-ttu-id="db149-113">Для некоторых стран и регионов индексы в таблице непосредственно соответствуют номерам каналов, иными словами, частота для канала n — это n-й элемент в таблице.</span><span class="sxs-lookup"><span data-stu-id="db149-113">For some countries/regions, the indexes in the table correspond directly to channel numbers — in other words, the frequency for channel n is the n th entry in the table.</span></span> <span data-ttu-id="db149-114">Однако в некоторых странах и регионах нет прямой корреспонденции между номерами каналов и частотой.</span><span class="sxs-lookup"><span data-stu-id="db149-114">For some countries/regions, however, there is no direct correspondence between channel numbers and frequencies.</span></span> <span data-ttu-id="db149-115">В этом случае приложение должно иметь список, который сопоставляет номера каналов (обычно выбранные пользователем) с частотой записей таблицы.</span><span class="sxs-lookup"><span data-stu-id="db149-115">In that case, the application must keep a list that maps channel numbers (typically chosen by the user) to frequency table entries.</span></span> <span data-ttu-id="db149-116">Например, пользователь видит "канал 5" в таблице Frequency (частота) номер 12.</span><span class="sxs-lookup"><span data-stu-id="db149-116">For example, what the user sees as "channel 5" might be entry number 12 in the frequency table.</span></span>

<span data-ttu-id="db149-117">Дополнительные сведения см. в разделе [Международная Настройка аналогового телевидения](international-analog-tv-tuning.md).</span><span class="sxs-lookup"><span data-stu-id="db149-117">For details, see [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span>

<span data-ttu-id="db149-118">Базовые операции настройки</span><span class="sxs-lookup"><span data-stu-id="db149-118">Basic Tuning Operations</span></span>

<span data-ttu-id="db149-119">Если тюнер поддерживает несколько режимов приема, таких как телевизоры и FM-Радио, вызовите [**иамтунер::p UT \_ , чтобы**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) выбрать режим.</span><span class="sxs-lookup"><span data-stu-id="db149-119">If the tuner supports multiple reception modes, such as television and FM radio, call [**IAMTuner::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) to select the mode.</span></span> <span data-ttu-id="db149-120">Метод [**иамтунер:: жетаваилаблемодес**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) возвращает все режимы, поддерживаемые тюнером.</span><span class="sxs-lookup"><span data-stu-id="db149-120">The [**IAMTuner::GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) method returns all of the modes that the tuner supports.</span></span> <span data-ttu-id="db149-121">Например, следующий код проверяет, поддерживает ли тюнер FM-Радио, и, если да, переключается в этот режим.</span><span class="sxs-lookup"><span data-stu-id="db149-121">For example, the following code checks whether the tuner supports FM radio, and if so, switches to that mode.</span></span>


```C++
// Check whether the mode is supported.
long lModes = 0;
hr = m_pTuner->GetAvailableModes(&lModes);
if (SUCCEEDED(hr) && (lModes & AMTUNER_MODE_FM_RADIO))
{
    // Set the mode.
    hr = pTuner->put_Mode(AMTUNER_MODE_FM_RADIO);
}
```



<span data-ttu-id="db149-122">Чтобы задать страну или регион, вызовите метод [**иамтунер::p UT \_ каунтрикоде**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) .</span><span class="sxs-lookup"><span data-stu-id="db149-122">To set the country/region, call the [**IAMTuner::put\_CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) method.</span></span> <span data-ttu-id="db149-123">Этот параметр используется программой настройки для выбора подходящей таблицы частоты.</span><span class="sxs-lookup"><span data-stu-id="db149-123">The tuner uses this value to select the appropriate frequency table.</span></span> <span data-ttu-id="db149-124">Дополнительные сведения см. в разделе о [назначении страны или региона](country-region-assignments.md) .</span><span class="sxs-lookup"><span data-stu-id="db149-124">See [Country/Region Assignments](country-region-assignments.md) for more information.</span></span>

<span data-ttu-id="db149-125">Чтобы задать канал, вызовите метод [**иамтунер::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) .</span><span class="sxs-lookup"><span data-stu-id="db149-125">To set the channel, call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method.</span></span> <span data-ttu-id="db149-126">Аргумент для этого метода фактически не является номером канала, а индексом в текущей таблицей частоты.</span><span class="sxs-lookup"><span data-stu-id="db149-126">The argument to this method is actually not a channel number, but rather an index into the current frequency table.</span></span> <span data-ttu-id="db149-127">Как было сказано ранее, номер индекса может быть или не соответствовать номеру канала.</span><span class="sxs-lookup"><span data-stu-id="db149-127">As described previously, the index number may or may not correspond to a channel number.</span></span> <span data-ttu-id="db149-128">Метод [**иамтунер:: чаннелминмакс**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) возвращает минимальное и максимальное значения индекса для текущей таблицы частоты.</span><span class="sxs-lookup"><span data-stu-id="db149-128">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method returns the minimum and maximum index values for the current frequency table.</span></span>

<span data-ttu-id="db149-129">Переопределение записей частоты</span><span class="sxs-lookup"><span data-stu-id="db149-129">Overriding Frequency Entries</span></span>

<span data-ttu-id="db149-130">Возможно, некоторые записи в таблицах частоты могут быть неправильными или устаревшими.</span><span class="sxs-lookup"><span data-stu-id="db149-130">It is possible that some entries in the frequency tables might be incorrect or become obsolete.</span></span> <span data-ttu-id="db149-131">Таким образом, для переопределения отдельных записей с помощью разделов реестра предоставляется механизм.</span><span class="sxs-lookup"><span data-stu-id="db149-131">Therefore, a mechanism is provided for overriding individual entries using registry keys.</span></span>

<span data-ttu-id="db149-132">Эти особенности описаны в разделе [Международная Настройка аналогового телевидения](international-analog-tv-tuning.md).</span><span class="sxs-lookup"><span data-stu-id="db149-132">The specifics are explained in the topic [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span> <span data-ttu-id="db149-133">Каждый раздел реестра определяет область настройки, которая содержит один или несколько подразделов.</span><span class="sxs-lookup"><span data-stu-id="db149-133">Each registry key defines a "tuning space" which contains one or more subkeys.</span></span> <span data-ttu-id="db149-134">Каждый подраздел переопределяет одну запись частоты.</span><span class="sxs-lookup"><span data-stu-id="db149-134">Each subkey overrides one frequency entry.</span></span> <span data-ttu-id="db149-135">Чтобы задать текущее пространство настройки, используйте метод [**иамтунер::p UT \_ тунингспаце**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) .</span><span class="sxs-lookup"><span data-stu-id="db149-135">To set the current tuning space, use the [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method.</span></span> <span data-ttu-id="db149-136">Активация пространства настройки переопределяет частоту записей в текущей таблице частоты.</span><span class="sxs-lookup"><span data-stu-id="db149-136">Activating the tuning space overrides the frequency entries in the current frequency table.</span></span> <span data-ttu-id="db149-137">Таким образом, приложение может поддерживать соответствие между областями и странами и регионами настройки.</span><span class="sxs-lookup"><span data-stu-id="db149-137">Therefore, it is up to the application to maintain a correspondence between tuning spaces and countries/regions.</span></span> <span data-ttu-id="db149-138">Лучшим подходом является использование идентификатора страны или региона в качестве имени пространства настройки.</span><span class="sxs-lookup"><span data-stu-id="db149-138">The best approach is simply to use the country/region identifier as the name of the tuning space.</span></span>

<span data-ttu-id="db149-139">Тонкая настройка записей частоты</span><span class="sxs-lookup"><span data-stu-id="db149-139">Fine Tuning the Frequency Entries</span></span>

<span data-ttu-id="db149-140">Частота широковещательной передачи может быть настроена на несколько кГц на станции вещания, чтобы снизить потенциальные помехи с соседними каналами.</span><span class="sxs-lookup"><span data-stu-id="db149-140">Broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span> <span data-ttu-id="db149-141">Учитывая номинальную частоту, плата тюнера может проверять точную частоту.</span><span class="sxs-lookup"><span data-stu-id="db149-141">Given the nominal frequency, the tuner card can scan for the exact frequency.</span></span> <span data-ttu-id="db149-142">Фильтр ТВ-тюнера имеет механизм для сохранения скорректированных частот в реестре.</span><span class="sxs-lookup"><span data-stu-id="db149-142">The TV Tuner filter has a mechanism for saving the adjusted frequencies in the registry.</span></span>

<span data-ttu-id="db149-143">Для каждой записи в таблице Frequency вызовите \_ метод размещения канала, чтобы настроить эту частоту.</span><span class="sxs-lookup"><span data-stu-id="db149-143">For each entry in the frequency table, call the put\_Channel method to tune to that frequency.</span></span> <span data-ttu-id="db149-144">Этот тюнер будет проверять наиболее точную частоту.</span><span class="sxs-lookup"><span data-stu-id="db149-144">The tuner will scan for the most precise frequency.</span></span> <span data-ttu-id="db149-145">Чтобы проверить, достигает ли тюнера горизонтальной блокировки, вызовите [**иамтунер:: сигналпресент**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span><span class="sxs-lookup"><span data-stu-id="db149-145">You can check whether the tuner achieved a horizontal lock by calling [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span></span> <span data-ttu-id="db149-146">Фильтр ТВ-тюнера также сохраняет результаты внутри.</span><span class="sxs-lookup"><span data-stu-id="db149-146">The TV Tuner filter also stores the result internally.</span></span>

<span data-ttu-id="db149-147">После просмотра всех частот вызовите метод [**иамтвтунер:: стореаутотуне**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) , чтобы записать обновленные значения в реестр.</span><span class="sxs-lookup"><span data-stu-id="db149-147">After scanning all of the frequencies, call the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method to write the updated values into the registry.</span></span> <span data-ttu-id="db149-148">Обновленные значения хранятся в записи реестра для текущего пространства настройки.</span><span class="sxs-lookup"><span data-stu-id="db149-148">The updated values are stored under the registry entry for the current tuning space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db149-149">См. также</span><span class="sxs-lookup"><span data-stu-id="db149-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db149-150">Аналоговые телевизоры</span><span class="sxs-lookup"><span data-stu-id="db149-150">Analog Television</span></span>](analog-television.md)
</dt> </dl>

 

 



