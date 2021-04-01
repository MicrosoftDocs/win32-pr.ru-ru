---
title: Поддержка DRM в DirectShow
description: Поддержка DRM в DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Media Format SDK, поддержка DRM в DirectShow
- Пакет SDK для Windows Media Format, DirectShow
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Расширенный формат систем (ASF), поддержка DRM в DirectShow
- ASF (расширенный формат систем), поддержка DRM в DirectShow
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный формат систем (ASF), управление цифровыми правами (DRM)
- ASF (Расширенный системный формат), управление цифровыми правами (DRM)
- DirectShow, поддержка DRM
- Управление цифровыми правами (DRM), DirectShow
- DRM (Управление цифровыми правами), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987183"
---
# <a name="drm-support-in-directshow"></a><span data-ttu-id="80eda-115">Поддержка DRM в DirectShow</span><span class="sxs-lookup"><span data-stu-id="80eda-115">DRM Support in DirectShow</span></span>

<span data-ttu-id="80eda-116">Чтение и запись файлов, защищенных с помощью DRM, в DirectShow выполняется по сути так же, как при использовании пакета SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="80eda-116">Reading and writing DRM-protected files in DirectShow is done in basically the same way as when you use the Windows Media Format SDK directly.</span></span> <span data-ttu-id="80eda-117">Чтобы начать с, необходима статическая библиотека вмстубдрм, полученная отдельно от корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="80eda-117">To begin with, you need the wmstubdrm static library, which is obtained separately from Microsoft.</span></span> <span data-ttu-id="80eda-118">Кроме того, необходимо реализовать интерфейс **икэйпровидер** , чтобы предоставить приложению доступ к объектам времени выполнения пакета SDK Windows Media Format, когда включена поддержка DRM.</span><span class="sxs-lookup"><span data-stu-id="80eda-118">In addition, you must implement the **IKeyProvider** interface to enable your application to access the Windows Media Format SDK run-time objects when DRM is enabled.</span></span>

<span data-ttu-id="80eda-119">При применении защиты DRM версии 1 используйте интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , который получается, как описано в статье [Чтение ASF-файлов в DirectShow](reading-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="80eda-119">When applying DRM version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which is obtained as described in [Reading ASF Files in DirectShow](reading-asf-files-in-directshow.md).</span></span> <span data-ttu-id="80eda-120">При применении защиты DRM версии 7 получите интерфейс [**ивмдрмвритер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) , вызвав **QueryService** в фильтре [модуля записи WM ASF](wm-asf-writer-filter.md) , как показано в фрагменте кода далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="80eda-120">When applying DRM version 7 protection, obtain the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface by calling **QueryService** on the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the code snippet later in this topic.</span></span>

<span data-ttu-id="80eda-121">Все остальные настройки, зависящие от DRM, точно такие же, как описано в разделе [Включение поддержки DRM](enabling-drm-support.md).</span><span class="sxs-lookup"><span data-stu-id="80eda-121">All other DRM-specific configuration is exactly the same as described in [Enabling DRM Support](enabling-drm-support.md).</span></span> <span data-ttu-id="80eda-122">Используйте **QueryService** для получения интерфейса [**Ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) из фильтра [чтения WM ASF](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="80eda-122">Use **QueryService** to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

<span data-ttu-id="80eda-123">DirectX 9,0 содержит образец, Плайвндасф, приложение DirectShow, поддерживающее DRM, которое демонстрирует получение лицензий DRM версии 1 и версии 7.</span><span class="sxs-lookup"><span data-stu-id="80eda-123">DirectX 9.0 contains a sample, PlayWndASF, a DRM-enabled DirectShow player application that demonstrates DRM version 1 and version 7 license acquisition.</span></span> <span data-ttu-id="80eda-124">Этот пример также включает реализацию класса **ккэйпровидер** , который поддерживает интерфейс **икэйпровидер** .</span><span class="sxs-lookup"><span data-stu-id="80eda-124">This sample also includes an implementation of the **CKeyProvider** class, which supports the **IKeyProvider** interface.</span></span>

 

 




