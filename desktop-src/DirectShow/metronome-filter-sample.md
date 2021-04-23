---
description: Образец фильтра метрономе
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Образец фильтра метрономе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682250"
---
# <a name="metronome-filter-sample"></a><span data-ttu-id="45f4c-103">Образец фильтра метрономе</span><span class="sxs-lookup"><span data-stu-id="45f4c-103">Metronome Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="45f4c-104">Описание</span><span class="sxs-lookup"><span data-stu-id="45f4c-104">Description</span></span>

<span data-ttu-id="45f4c-105">В этом образце фильтра показано, как реализовать ссылочное время.</span><span class="sxs-lookup"><span data-stu-id="45f4c-105">This sample filter shows how to implement a reference clock.</span></span> <span data-ttu-id="45f4c-106">Фильтр использует входные микрофона по умолчанию для прослушивания пиковых всплесков (таких как щелчки, руки клапс или каугхс), которые используются для определения тактовой частоты.</span><span class="sxs-lookup"><span data-stu-id="45f4c-106">The filter uses your default microphone input to listen for audio spikes (such as clicks, hand claps, or coughs), which it uses to determine a clock rate.</span></span>

## <a name="usage"></a><span data-ttu-id="45f4c-107">Использование</span><span class="sxs-lookup"><span data-stu-id="45f4c-107">Usage</span></span>

<span data-ttu-id="45f4c-108">Создайте пример проекта и скопируйте файл DLL фильтра (Metronom.ax) в системный каталог Windows.</span><span class="sxs-lookup"><span data-stu-id="45f4c-108">Build the sample project and copy the filter DLL (Metronom.ax) to your Windows system directory.</span></span> <span data-ttu-id="45f4c-109">Запустите файл метроном. reg, чтобы зарегистрировать библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="45f4c-109">Run the Metronom.reg file to register the DLL.</span></span>

<span data-ttu-id="45f4c-110">Чтобы использовать фильтр, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="45f4c-110">To use the filter:</span></span>

1.  <span data-ttu-id="45f4c-111">Создание графа фильтра в Графедит, который визуализирует видео-поток.</span><span class="sxs-lookup"><span data-stu-id="45f4c-111">Build a filter graph in GraphEdit that renders a video stream.</span></span>
2.  <span data-ttu-id="45f4c-112">Удалите все обработанные звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="45f4c-112">Delete any rendered audio streams.</span></span>
3.  <span data-ttu-id="45f4c-113">Добавьте фильтр Метрономе в граф.</span><span class="sxs-lookup"><span data-stu-id="45f4c-113">Add the Metronome filter to the graph.</span></span> <span data-ttu-id="45f4c-114">Он отображается в категории фильтры DirectShow.</span><span class="sxs-lookup"><span data-stu-id="45f4c-114">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="45f4c-115">Запустите граф.</span><span class="sxs-lookup"><span data-stu-id="45f4c-115">Run the graph.</span></span> <span data-ttu-id="45f4c-116">Воспроизведение видео начнется с нормальной скоростью.</span><span class="sxs-lookup"><span data-stu-id="45f4c-116">The video will begin playing at normal speed.</span></span>
5.  <span data-ttu-id="45f4c-117">Рукоплескания свои руки или используйте метрономе, чтобы установить новую скорость.</span><span class="sxs-lookup"><span data-stu-id="45f4c-117">Clap your hands or use a metronome to set a new speed.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="45f4c-118">Заметки о программировании</span><span class="sxs-lookup"><span data-stu-id="45f4c-118">Programming Notes</span></span>

<span data-ttu-id="45f4c-119">Этот фильтр работает только для видео.</span><span class="sxs-lookup"><span data-stu-id="45f4c-119">This filter works only for video.</span></span> <span data-ttu-id="45f4c-120">Модуль подготовки звука не поддерживает синхронизацию с незначительной разностью часов.</span><span class="sxs-lookup"><span data-stu-id="45f4c-120">The audio renderer is not capable of synchronizing to radically different clock rates.</span></span>

<span data-ttu-id="45f4c-121">Если вы рукоплескания 92 раз в минуту (каждые ~ 652 МС), видео будет воспроизводиться по нормальной ставке.</span><span class="sxs-lookup"><span data-stu-id="45f4c-121">If you clap 92 times per minute (once every ~652 ms), the video will play at the normal rate.</span></span> <span data-ttu-id="45f4c-122">Это значение по умолчанию можно изменить путем изменения значения константы `BPM` в метроном. cpp.</span><span class="sxs-lookup"><span data-stu-id="45f4c-122">You can change this default by changing the value of the constant `BPM` in Metronom.cpp.</span></span>

<span data-ttu-id="45f4c-123">Если вы останавливаете аплодисменты в течение определенного периода времени, а затем снова запускаете аплодисменты, необходимо начать заново с примерно такой же скоростью, иначе фильтр пропустит его.</span><span class="sxs-lookup"><span data-stu-id="45f4c-123">If you stop clapping for a period of time and then start clapping again, you must start again at approximately the same speed, or the filter will ignore it.</span></span> <span data-ttu-id="45f4c-124">Кроме того, скорость воспроизведения видео ограничена скоростью ЦП.</span><span class="sxs-lookup"><span data-stu-id="45f4c-124">Also, the video playback rate is limited by the CPU speed.</span></span> <span data-ttu-id="45f4c-125">Если превышено ограничение на период времени, то фильтр перестанет отвечать на запросы на изменение скорости.</span><span class="sxs-lookup"><span data-stu-id="45f4c-125">If you exceed the limit for any length of time, the filter will stop responding to rate changes.</span></span> <span data-ttu-id="45f4c-126">В этом случае закройте граф и перезапустите.</span><span class="sxs-lookup"><span data-stu-id="45f4c-126">If this happens, stop the graph and restart.</span></span>

<span data-ttu-id="45f4c-127">При реализации собственных часов наиболее важными правилами является то, что ссылки на часы не должны идти назад.</span><span class="sxs-lookup"><span data-stu-id="45f4c-127">If you implement your own clock, the most important rules is that reference clocks must not go backward.</span></span> <span data-ttu-id="45f4c-128">То есть они никогда не должны сообщать значение времени, меньшее, чем предыдущее значение времени.</span><span class="sxs-lookup"><span data-stu-id="45f4c-128">That is, they must never report a time value less than the previous time value.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="45f4c-129">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="45f4c-129">Downloading the Sample</span></span>

<span data-ttu-id="45f4c-130">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="45f4c-130">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="45f4c-131">Этот пример устанавливается по следующему пути: *\[ \] корневые примеры SDK* \\ \\ мультимедиа \\ DirectShow \\ фильтры \\ метрономе.</span><span class="sxs-lookup"><span data-stu-id="45f4c-131">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Metronome.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45f4c-132">См. также</span><span class="sxs-lookup"><span data-stu-id="45f4c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45f4c-133">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="45f4c-133">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="45f4c-134">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="45f4c-134">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



