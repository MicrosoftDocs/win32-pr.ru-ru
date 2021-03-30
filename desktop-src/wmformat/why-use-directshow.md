---
title: Зачем использовать DirectShow
description: Зачем использовать DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Пакет SDK для Windows Media Format, DirectShow
- Windows Media Format SDK, оборудование
- Пакет SDK Windows Media Format, WDM (WDM)
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный системный формат (ASF), оборудование
- ASF (Расширенный системный формат), оборудование
- Расширенный формат систем (ASF), WDM (WDM)
- ASF (Расширенный системный формат), WDM (WDM)
- DirectShow, сведения
- DirectShow, оборудование
- DirectShow, WDM (WDM)
- WDM (WDM)
- WDM (WDM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775908"
---
# <a name="why-use-directshow"></a><span data-ttu-id="96430-117">Зачем использовать DirectShow?</span><span class="sxs-lookup"><span data-stu-id="96430-117">Why Use DirectShow?</span></span>

<span data-ttu-id="96430-118">Существует две основные причины, по которым приложение может использовать DirectShow, а не пакет SDK Windows Media Format, напрямую: для удобства работы с архитектурой потоковой передачи DirectShow и для доступа к оборудованию.</span><span class="sxs-lookup"><span data-stu-id="96430-118">There are two main reasons why an application might use DirectShow rather than the Windows Media Format SDK directly: for the convenience of the DirectShow streaming architecture, and for access to hardware.</span></span>

## <a name="convenience"></a><span data-ttu-id="96430-119">Удобство</span><span class="sxs-lookup"><span data-stu-id="96430-119">Convenience</span></span>

<span data-ttu-id="96430-120">В архитектуре потоковой передачи DirectShow для воспроизведения видеофайлов Windows Media Audio или Windows Media Video требуется всего несколько вызовов метода.</span><span class="sxs-lookup"><span data-stu-id="96430-120">With DirectShow streaming architecture, it takes only a few method calls to play Windows Media Audio or Windows Media Video files.</span></span> <span data-ttu-id="96430-121">Также упрощено создание файлов.</span><span class="sxs-lookup"><span data-stu-id="96430-121">Creating files is also simplified.</span></span> <span data-ttu-id="96430-122">Вы просто указываете профиль с помощью интерфейса **иконфигасфвритер** в фильтре, и DirectShow автоматически загружает необходимые компоненты для подготовки к просмотру или записи потоков, а также предоставляет механизмы для передачи и синхронизации потока данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="96430-122">You simply specify a profile using the **IConfigAsfWriter** interface on the filter, and DirectShow automatically loads the required components for rendering or writing the streams, and provides the mechanisms for transferring and synchronizing the flow of media data.</span></span> <span data-ttu-id="96430-123">DirectShow особенно полезна при преобразовании содержимого из различных форматов в формат Windows Media.</span><span class="sxs-lookup"><span data-stu-id="96430-123">DirectShow is especially useful when converting content from varied formats into Windows Media Format.</span></span> <span data-ttu-id="96430-124">Можно создать графы фильтров DirectShow, которые декодируются разнообразные типы файлов и сжатия, а затем передать декодированные потоки в фильтр [модуля записи WM ASF](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="96430-124">You can create DirectShow filter graphs that decode a wide variety of file and compression types, and then feed the decoded streams into the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span> <span data-ttu-id="96430-125">По сравнению, пример Ункомпавитовмв в этом пакете SDK работает только с несжатыми AVI файлами.</span><span class="sxs-lookup"><span data-stu-id="96430-125">By comparison, the UncompAVItoWMV sample in this SDK works only with uncompressed AVI files.</span></span> <span data-ttu-id="96430-126">Текстовые потоки и произвольные потоки данных также можно создавать и (или) визуализировать с помощью DirectShow, но для этого может потребоваться создать пользовательские фильтры DirectShow для обработки этих потоков.</span><span class="sxs-lookup"><span data-stu-id="96430-126">Text streams and arbitrary data streams can also be created and/or rendered through DirectShow, but this might require you to create custom DirectShow filters for processing those streams.</span></span>

## <a name="access-to-hardware"></a><span data-ttu-id="96430-127">Доступ к оборудованию</span><span class="sxs-lookup"><span data-stu-id="96430-127">Access to Hardware</span></span>

<span data-ttu-id="96430-128">DirectShow — это единственный способ доступа кода приложения к аппаратным устройствам WDM (WDM), таким как 1394 DV-камеры, ТЕЛЕВИЗИОНные тюнеры и USB-камеры.</span><span class="sxs-lookup"><span data-stu-id="96430-128">DirectShow is the only way for application code to access Windows Driver Model (WDM)–based hardware devices such as 1394 DV cameras, TV tuners, and USB webcams.</span></span> <span data-ttu-id="96430-129">Если приложение должно собирать данные непосредственно с аппаратного устройства на основе WDM и перекодировать его в формат Windows Media, а пакет SDK для кодировщика Windows Media не соответствует вашим потребностям, то единственным вариантом является DirectShow.</span><span class="sxs-lookup"><span data-stu-id="96430-129">If your application must capture data directly from a WDM-based hardware device and transcode it to Windows Media Format, and the Windows Media Encoder SDK does not suit your needs, then DirectShow is the only alternative.</span></span> <span data-ttu-id="96430-130">Кроме того, DirectShow можно использовать для доступа к устаревшим устройствам на основе видео для Windows.</span><span class="sxs-lookup"><span data-stu-id="96430-130">DirectShow can also be used to access legacy devices based on Video for Windows.</span></span>

 

 




