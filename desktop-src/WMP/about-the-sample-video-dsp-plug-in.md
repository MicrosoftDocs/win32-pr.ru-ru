---
title: О примере подключаемого модуля DSP видео
description: О примере подключаемого модуля DSP видео
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Подключаемые модули проигрывателя Windows Media, примеры
- подключаемые модули, примеры
- подключаемые модули обработки цифровых сигналов, примеры
- Подключаемые модули DSP, примеры
- Подключаемые модули проигрывателя Windows Media, DSP видео
- подключаемые модули, DSP видео
- подключаемые модули обработки цифровых сигналов, образцы видео
- Подключаемые модули DSP, образцы видео
- Примеры, подключаемые модули DSP
- подключаемые модули DSP видео, примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede2eda82c834cefad0e31009805f24941cd4a6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691146"
---
# <a name="about-the-sample-video-dsp-plug-in"></a><span data-ttu-id="22e2b-113">О примере подключаемого модуля DSP видео</span><span class="sxs-lookup"><span data-stu-id="22e2b-113">About the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="22e2b-114">Подключаемый модуль схемы DSP видео — это простая реализация обработки, которая масштабирует насыщенность цвета видео на коэффициент, предоставленный пользователем на странице свойств.</span><span class="sxs-lookup"><span data-stu-id="22e2b-114">The sample video DSP plug-in provides a simple processing implementation that scales the color saturation of the video by a factor provided by the user in the property page.</span></span> <span data-ttu-id="22e2b-115">Подключаемый модуль принимает значения от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="22e2b-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="22e2b-116">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="22e2b-116">The default value is 1.</span></span> <span data-ttu-id="22e2b-117">Значение 1 не влияет на изображение видео; другие коэффициенты масштабирования отменяют насыщенность цвета изображения.</span><span class="sxs-lookup"><span data-stu-id="22e2b-117">A value of 1 has no effect upon the video image; other scale factors desaturate the image color.</span></span> <span data-ttu-id="22e2b-118">Например, значение 0,5 приведет к насыщенности цвета в 50%.</span><span class="sxs-lookup"><span data-stu-id="22e2b-118">For instance, a value of .5 would result in 50 percent color saturation.</span></span> <span data-ttu-id="22e2b-119">Нулевое значение приводит к полутону видео в градациях серого.</span><span class="sxs-lookup"><span data-stu-id="22e2b-119">A value of zero results in grayscale video.</span></span>

<span data-ttu-id="22e2b-120">Пример подключаемого модуля DSP видео работает со следующими видеоформатами:</span><span class="sxs-lookup"><span data-stu-id="22e2b-120">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="22e2b-121">NV12</span><span class="sxs-lookup"><span data-stu-id="22e2b-121">NV12</span></span>
-   <span data-ttu-id="22e2b-122">YV12</span><span class="sxs-lookup"><span data-stu-id="22e2b-122">YV12</span></span>
-   <span data-ttu-id="22e2b-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="22e2b-123">YUY2</span></span>
-   <span data-ttu-id="22e2b-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="22e2b-124">UYVY</span></span>
-   <span data-ttu-id="22e2b-125">RGB32</span><span class="sxs-lookup"><span data-stu-id="22e2b-125">RGB32</span></span>
-   <span data-ttu-id="22e2b-126">RGB24</span><span class="sxs-lookup"><span data-stu-id="22e2b-126">RGB24</span></span>
-   <span data-ttu-id="22e2b-127">RGB555</span><span class="sxs-lookup"><span data-stu-id="22e2b-127">RGB555</span></span>
-   <span data-ttu-id="22e2b-128">RGB565</span><span class="sxs-lookup"><span data-stu-id="22e2b-128">RGB565</span></span>

## <a name="related-topics"></a><span data-ttu-id="22e2b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="22e2b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22e2b-130">**Создание подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="22e2b-130">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




