---
description: Образец фильтра синтезатора
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Образец фильтра синтезатора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913136"
---
# <a name="synth-filter-sample"></a><span data-ttu-id="2362d-103">Образец фильтра синтезатора</span><span class="sxs-lookup"><span data-stu-id="2362d-103">Synth Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="2362d-104">Описание</span><span class="sxs-lookup"><span data-stu-id="2362d-104">Description</span></span>

<span data-ttu-id="2362d-105">Фильтр синтезатора — это фильтр источника, который создает звуковые волны.</span><span class="sxs-lookup"><span data-stu-id="2362d-105">The Synth filter is a source filter that generates audio waveforms.</span></span>

<span data-ttu-id="2362d-106">Этот фильтр иллюстрирует построение динамического графа.</span><span class="sxs-lookup"><span data-stu-id="2362d-106">This filter illustrates dynamic graph building.</span></span> <span data-ttu-id="2362d-107">Он может переключаться между несжатым звуком PCM и сжатым \_ форматом MS ADPCM (модуляция адаптивного разностного кода Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="2362d-107">It can switch between uncompressed PCM audio and compressed MS\_ADPCM (Microsoft Adaptive Delta Pulse Code Modulation) format.</span></span>

<span data-ttu-id="2362d-108">Этот фильтр отображается в Графедит как "фильтр аудио синтезатора".</span><span class="sxs-lookup"><span data-stu-id="2362d-108">This filter appears in GraphEdit as "Audio Synthesizer Filter."</span></span>

<span data-ttu-id="2362d-109">Дополнительные сведения о построении динамического графа см. в разделе [динамическое построение графа](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="2362d-109">For more information about dynamic graph building, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="usage"></a><span data-ttu-id="2362d-110">Использование</span><span class="sxs-lookup"><span data-stu-id="2362d-110">Usage</span></span>

<span data-ttu-id="2362d-111">Фильтр синтезатора позволяет пользователю задать звук, частоту, количество каналов и другие свойства на странице свойств.</span><span class="sxs-lookup"><span data-stu-id="2362d-111">The Synth filter enables the user to set the waveform, frequency, number of channels, and other properties through the property page.</span></span> <span data-ttu-id="2362d-112">Чтобы задать верхнюю или нижнюю конечную точку диапазона частоты очистка, удерживайте нажатой клавишу SHIFT при настройке ползунка частота.</span><span class="sxs-lookup"><span data-stu-id="2362d-112">To set either the upper or lower endpoint of the swept frequency range, hold down SHIFT while adjusting the frequency slider.</span></span> <span data-ttu-id="2362d-113">Фильтр также поддерживает пользовательский интерфейс ISynth2 для установки этих свойств.</span><span class="sxs-lookup"><span data-stu-id="2362d-113">The filter also supports a custom interface, ISynth2, for setting these properties.</span></span>

<span data-ttu-id="2362d-114">Чтобы продемонстрировать функцию динамического построения графа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2362d-114">To demonstrate the dynamic graph building feature, do the following:</span></span>

1.  <span data-ttu-id="2362d-115">Создайте фильтр и зарегистрируйте его с помощью служебной программы regsvr32.</span><span class="sxs-lookup"><span data-stu-id="2362d-115">Build the filter and register it with the Regsvr32 utility.</span></span>
2.  <span data-ttu-id="2362d-116">Запустите Графедит.</span><span class="sxs-lookup"><span data-stu-id="2362d-116">Launch GraphEdit.</span></span>
3.  <span data-ttu-id="2362d-117">Вставьте фильтр аудио синтезатора.</span><span class="sxs-lookup"><span data-stu-id="2362d-117">Insert the Audio Synthesizer filter.</span></span> <span data-ttu-id="2362d-118">Он отображается в категории фильтры DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2362d-118">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="2362d-119">Отрисовка выходного ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="2362d-119">Render the filter's output pin.</span></span>
5.  <span data-ttu-id="2362d-120">Нажмите кнопку **Воспроизведение** .</span><span class="sxs-lookup"><span data-stu-id="2362d-120">Click the **Play** button.</span></span>
6.  <span data-ttu-id="2362d-121">Откройте страницу свойств фильтра.</span><span class="sxs-lookup"><span data-stu-id="2362d-121">Open the filter's property page.</span></span>
7.  <span data-ttu-id="2362d-122">В области формат вывода выберите PCM или Microsoft ADPCM.</span><span class="sxs-lookup"><span data-stu-id="2362d-122">In the Output Format area, select PCM or Microsoft ADPCM.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="2362d-123">Заметки о программировании</span><span class="sxs-lookup"><span data-stu-id="2362d-123">Programming Notes</span></span>

<span data-ttu-id="2362d-124">Этот пример содержит следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="2362d-124">This sample contains the following files:</span></span>

-   <span data-ttu-id="2362d-125">Dynsrc. h, dynsrc. cpp: содержит два базовых класса для фильтров источников, поддерживающих динамические построения графа, Кдинамиксаурце и Кдинамиксаурцестреам.</span><span class="sxs-lookup"><span data-stu-id="2362d-125">Dynsrc.h, Dynsrc.cpp: Contains two base classes for source filters that support dynamic graph building, CDynamicSource and CDynamicSourceStream.</span></span>
-   <span data-ttu-id="2362d-126">Исинс. h: объявляет пользовательский интерфейс ISynth2 для установки свойств фильтра.</span><span class="sxs-lookup"><span data-stu-id="2362d-126">ISynth.h: Declares the custom ISynth2 interface for setting properties on the filter.</span></span>
-   <span data-ttu-id="2362d-127">Resource. h: содержит константы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2362d-127">Resource.h: Contains resource constants.</span></span>
-   <span data-ttu-id="2362d-128">Синтезатор. def: экспортирует функции DLL, необходимые для библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="2362d-128">Synth.def: Exports the DLL functions needed by the COM library.</span></span>
-   <span data-ttu-id="2362d-129">Синтезатор. h, синтезатор. cpp: содержит класс Каудиосинс, который создает звуковые данные, и класс Ксинсфилтер, который реализует фильтр.</span><span class="sxs-lookup"><span data-stu-id="2362d-129">Synth.h, Synth.cpp: Contains the CAudioSynth class, which generates the audio data, and the CSynthFilter class, which implements the filter.</span></span>
-   <span data-ttu-id="2362d-130">Синтезатор. rc: содержит ресурсы, используемые фильтром.</span><span class="sxs-lookup"><span data-stu-id="2362d-130">Synth.rc: Contains resources used by the filter.</span></span>
-   <span data-ttu-id="2362d-131">Синспрп. h, Синспрп. cpp: реализует страницу свойств фильтра.</span><span class="sxs-lookup"><span data-stu-id="2362d-131">Synthprp.h, Synthprp.cpp: Implements the filter's property page.</span></span>

<span data-ttu-id="2362d-132">Класс Кдинамиксаурце адаптируется от базового класса [**ксаурце**](csource.md) .</span><span class="sxs-lookup"><span data-stu-id="2362d-132">The CDynamicSource class is adapted from the [**CSource**](csource.md) base class.</span></span> <span data-ttu-id="2362d-133">Он использует один или несколько выходных закрепления, производных от класса Кдинамиксаурцестреам.</span><span class="sxs-lookup"><span data-stu-id="2362d-133">It uses one or more output pins derived from the CDynamicSourceStream class.</span></span> <span data-ttu-id="2362d-134">Класс Кдинамиксаурцестреам адаптируется от класса [**ксаурцестреам**](csourcestream.md) , но является производным от класса [**кдинамикаутпутпин**](cdynamicoutputpin.md) , а не класса [**кбасеаутпутпин**](cbaseoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="2362d-134">The CDynamicSourceStream class is adapted from the [**CSourceStream**](csourcestream.md) class, but derives from the [**CDynamicOutputPin**](cdynamicoutputpin.md) class rather than the [**CBaseOutputPin**](cbaseoutputpin.md) class.</span></span>

<span data-ttu-id="2362d-135">Класс Кдинамиксаурце содержит следующие методы, не найденные в [**ксаурце**](csource.md):</span><span class="sxs-lookup"><span data-stu-id="2362d-135">The CDynamicSource class has the following methods not found in [**CSource**](csource.md):</span></span>

-   <span data-ttu-id="2362d-136">Останов: сигнализирует о событии остановки ([**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md)) и завершает работу рабочего потока для всех неподключенных контактов.</span><span class="sxs-lookup"><span data-stu-id="2362d-136">Stop: Signals the stop event ([**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md)), and shuts down the worker thread for all unconnected pins.</span></span> <span data-ttu-id="2362d-137">В подключенном ПИН-коде неактивный метод закрепления завершит работу рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="2362d-137">On a connected pin, the pin's Inactive method will shut down the worker thread.</span></span>
-   <span data-ttu-id="2362d-138">Пауза: сбрасывает событие остановки.</span><span class="sxs-lookup"><span data-stu-id="2362d-138">Pause: Resets the stop event.</span></span>
-   <span data-ttu-id="2362d-139">Жоинфилтерграф: вызывает метод [**кдинамикаутпутпин:: сетконфигинфо**](cdynamicoutputpin-setconfiginfo.md) для каждого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="2362d-139">JoinFilterGraph: Calls the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method on each pin.</span></span>

<span data-ttu-id="2362d-140">Класс Кдинамиксаурцестреам содержит следующие методы, не найденные в [**ксаурцестреам**](csourcestream.md):</span><span class="sxs-lookup"><span data-stu-id="2362d-140">The CDynamicSourceStream class has the following methods not found in [**CSourceStream**](csourcestream.md):</span></span>

-   <span data-ttu-id="2362d-141">Дестройсаурцесреад: завершает работу рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="2362d-141">DestroySourceThread: Shuts down the worker thread.</span></span>
-   <span data-ttu-id="2362d-142">FatalError: сообщает об ошибке диспетчеру графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="2362d-142">FatalError: Signals an error to the filter graph manager.</span></span>
-   <span data-ttu-id="2362d-143">Аутпутпиннидстобереконнектед: сигнализирует, что необходимо повторно подключить ПИН-код вывода.</span><span class="sxs-lookup"><span data-stu-id="2362d-143">OutputPinNeedsToBeReconnected: Signals that the output pin should be reconnected.</span></span> <span data-ttu-id="2362d-144">При вызове этого метода рабочий поток вызывает метод [**кдинамикаутпутпин::D инамикреконнект**](cdynamicoutputpin-dynamicreconnect.md) для повторного подключения ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="2362d-144">When this method is called, the worker thread calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to reconnect the pin.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="2362d-145">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="2362d-145">Downloading the Sample</span></span>

<span data-ttu-id="2362d-146">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2362d-146">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="2362d-147">Этот пример устанавливается по следующему пути: *\[ \] корневой пример пакета SDK* \\ \\ мультимедийные файлы \\ DirectShow \\ фильтры мультимедиа \\ синтезатор.</span><span class="sxs-lookup"><span data-stu-id="2362d-147">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Synth.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2362d-148">См. также</span><span class="sxs-lookup"><span data-stu-id="2362d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2362d-149">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="2362d-149">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



