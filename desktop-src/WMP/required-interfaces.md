---
title: Требуемые интерфейсы (пакет SDK для проигрывателя Windows Media)
description: Сведения о необходимых интерфейсах, реализованных проигрывателем Windows Media в DirectShow или Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Подключаемые модули проигрывателя Windows Media, интерфейсы
- подключаемые модули, интерфейсы
- подключаемые модули обработки цифровых сигналов, интерфейсы
- Подключаемые модули DSP, интерфейсы
- интерфейсы, подключаемые модули DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406097"
---
# <a name="required-interfaces-windows-media-player-sdk"></a><span data-ttu-id="57f69-108">Требуемые интерфейсы (пакет SDK для проигрывателя Windows Media)</span><span class="sxs-lookup"><span data-stu-id="57f69-108">Required Interfaces (Windows Media Player SDK)</span></span>

<span data-ttu-id="57f69-109">Проигрыватель Windows Media визуализирует аудио и видео с помощью одного из следующих конвейеров.</span><span class="sxs-lookup"><span data-stu-id="57f69-109">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="57f69-110">DirectShow</span><span class="sxs-lookup"><span data-stu-id="57f69-110">DirectShow</span></span>
-   <span data-ttu-id="57f69-111">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="57f69-111">Media Foundation</span></span>

<span data-ttu-id="57f69-112">В Microsoft Windows XP и более ранних версиях проигрыватель использует DirectShow.</span><span class="sxs-lookup"><span data-stu-id="57f69-112">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="57f69-113">В Windows Vista проигрыватель иногда использует DirectShow и иногда использует Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="57f69-113">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="57f69-114">Подключаемый модуль DSP реализует некоторые или все из следующих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="57f69-114">A DSP plug-in implements some or all of the following interfaces:</span></span>

-   <span data-ttu-id="57f69-115">**имедиаобжект**</span><span class="sxs-lookup"><span data-stu-id="57f69-115">**IMediaObject**</span></span>
-   <span data-ttu-id="57f69-116">**ивмпплугиненабле**</span><span class="sxs-lookup"><span data-stu-id="57f69-116">**IWMPPluginEnable**</span></span>
-   <span data-ttu-id="57f69-117">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="57f69-117">**IMFTransform**</span></span>
-   <span data-ttu-id="57f69-118">**имфжетсервице**</span><span class="sxs-lookup"><span data-stu-id="57f69-118">**IMFGetService**</span></span>
-   <span data-ttu-id="57f69-119">**испеЦифипропертипажес**</span><span class="sxs-lookup"><span data-stu-id="57f69-119">**ISpecifyPropertyPages**</span></span>

<span data-ttu-id="57f69-120">Подключаемый модуль, реализующий **имедиаобжект** и **ивмпплугиненабле** , может выполняться в конвейере DirectShow.</span><span class="sxs-lookup"><span data-stu-id="57f69-120">A plug-in that implements **IMediaObject** and **IWMPPluginEnable** can run in the DirectShow pipeline.</span></span> <span data-ttu-id="57f69-121">Он также может выполняться в конвейере Media Foundation в оболочке, предоставляемой Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="57f69-121">It can also run in the Media Foundation Pipeline inside a wrapper provided by Media Foundation.</span></span> <span data-ttu-id="57f69-122">Подключаемый модуль этого типа называется объектом мультимедиа Microsoft DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="57f69-122">A plug-in of this type is called a Microsoft DirectX Media Object (DMO).</span></span> <span data-ttu-id="57f69-123">Обычно объект DMO можно рассматривать как аналог объекта Filter в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="57f69-123">It is common to think of a DMO as being analogous to a filter object in DirectShow.</span></span> <span data-ttu-id="57f69-124">Документация по DMO находится в разделе DirectShow Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="57f69-124">The DMO documentation is in the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="57f69-125">Подключаемый модуль, реализующий **имфтрансформ** и **имфжетсервице** , может выполняться изначально (в конвейере Media Foundation не требуется обертки).</span><span class="sxs-lookup"><span data-stu-id="57f69-125">A plug-in that implements **IMFTransform** and **IMFGetService** can run natively (no wrapper required) in the Media Foundation pipeline.</span></span> <span data-ttu-id="57f69-126">Подключаемый модуль этого типа называется Media Foundation преобразованием (MFT).</span><span class="sxs-lookup"><span data-stu-id="57f69-126">A plug-in of this type is called a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="57f69-127">Документация по MFT находится в разделе Media Foundation Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="57f69-127">The MFT documentation is in the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="57f69-128">Подключаемый модуль, который реализует **имедиаобжект**, **ивмпплугиненабле**, **имфтрансформ** и **Имфжетсервице** , может выполняться в конвейере DirectShow и также может выполняться в конвейере Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="57f69-128">A plug-in that implements **IMediaObject**, **IWMPPluginEnable**, **IMFTransform**, and **IMFGetService** can run in the DirectShow pipeline and can also run natively in the Media Foundation pipeline.</span></span> <span data-ttu-id="57f69-129">Этот тип подключаемого модуля, который называется *подключаемым модулем DSP в двойном режиме*, может играть роль DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="57f69-129">This type of plug-in, which is called a *dual-mode DSP plug-in*, can play the role of a DMO or an MFT.</span></span>

<span data-ttu-id="57f69-130">Когда проигрыватель Windows Media использует подключаемый модуль DSP в двойном режиме в Media Foundation конвейере, он сначала запрашивает интерфейс **имфтрансформ** .</span><span class="sxs-lookup"><span data-stu-id="57f69-130">When Windows Media Player uses a dual-mode DSP plug-in in the Media Foundation pipeline, it first queries for the **IMFTransform** interface.</span></span> <span data-ttu-id="57f69-131">В случае сбоя запроса проигрыватель Windows Media запрашивает интерфейс **имедиаобжект** .</span><span class="sxs-lookup"><span data-stu-id="57f69-131">If that query fails, Windows Media Player queries for the **IMediaObject** interface.</span></span> <span data-ttu-id="57f69-132">Если запрос **имедиаобжект** успешно выполнен, подключаемый модуль упаковывается и добавляется в конвейер Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="57f69-132">If the **IMediaObject** query is successful, the plug-in is wrapped and added to the Media Foundation pipeline.</span></span>

<span data-ttu-id="57f69-133">Независимо от конвейера любой подключаемый модуль DSP, который позволяет пользователю задавать свойства, должен реализовывать **испеЦифипропертипажес**.</span><span class="sxs-lookup"><span data-stu-id="57f69-133">Regardless of the pipeline, any DSP plug-in that allows the user to set properties must implement **ISpecifyPropertyPages**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57f69-134">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="57f69-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57f69-135">**Обзор подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="57f69-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="57f69-136">**Подключаемые интерфейсы DSP**</span><span class="sxs-lookup"><span data-stu-id="57f69-136">**DSP Plug-in Interfaces**</span></span>](dsp-plug-in-interfaces.md)
</dt> <dt>

[<span data-ttu-id="57f69-137">**Упаковка подключаемых модулей DSP**</span><span class="sxs-lookup"><span data-stu-id="57f69-137">**DSP Plug-in Packaging**</span></span>](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




