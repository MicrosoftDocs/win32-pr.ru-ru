---
title: Запись непосредственно с устройства в файл ASF (КАСФ)
description: Запись непосредственно с устройства в файл ASF (КАСФ)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- Windows Media Format SDK, запись с устройств в ASF-файлы (КАСФ)
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный формат систем (ASF), захват с устройств (КАСФ)
- ASF (Расширенный системный формат), запись с устройств (КАСФ)
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, запись из устройств в ASF-файлы (КАСФ)
- Windows Media Format SDK, КАСФ
- Расширенный системный формат (ASF), КАСФ
- ASF (Расширенный системный формат), КАСФ
- DirectShow, КАСФ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faaf5ba8df3cffbb2121451d3bd1b456fc994078
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710105"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a><span data-ttu-id="36f49-114">Запись непосредственно с устройства в файл ASF (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="36f49-114">Capturing Directly from a Device to an ASF File (QASF)</span></span>

<span data-ttu-id="36f49-115">При записи аудио или видео непосредственно в ASF-файл граф фильтра выглядит примерно так, как на следующей схеме, в зависимости от типа используемого устройства записи.</span><span class="sxs-lookup"><span data-stu-id="36f49-115">When capturing audio or video directly to an ASF file, the filter graph looks something like the following diagram, depending on the type of capture device being used.</span></span>

![Граф записи веб-камеры в WMV](images/asf-webcam.png)

<span data-ttu-id="36f49-117">В документации по пакету SDK для DirectShow подробно описывается создание графов записи, но при создании графов записи с помощью модуля записи WM ASF необходимо помнить один важный момент: модуль записи WM ASF не будет работать, пока не будут подключены все его ПИН-коды.</span><span class="sxs-lookup"><span data-stu-id="36f49-117">The DirectShow SDK documentation describes in detail how to create capture graphs, but there is one important point to remember when creating capture graphs using the WM ASF Writer: the WM ASF Writer will not run unless all of its pins are connected.</span></span> <span data-ttu-id="36f49-118">Если настроить модуль записи WM ASF с помощью системного профиля по умолчанию (не рекомендуется) или любого профиля с аудио-и видеопотоками, то он создаст входной ПИН-код для каждого потока, и каждый из этих контактов должен быть подключен.</span><span class="sxs-lookup"><span data-stu-id="36f49-118">If you configure the WM ASF Writer with the default system profile (not recommended), or any profile with audio and video streams, then it will create an input pin for each stream and each of those pins must be connected.</span></span> <span data-ttu-id="36f49-119">Если вы не собираетесь записывать звук, например, не забудьте настроить фильтр с помощью профиля только для видео, чтобы не создавался звуковой ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="36f49-119">If you do not intend to capture audio, for example, then be sure to configure the filter with a video-only profile so that no audio pin is created.</span></span>

 

 




