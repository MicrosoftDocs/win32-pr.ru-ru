---
title: Получение лицензий
description: Получение лицензий
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- Windows Media Format SDK, расширенные API клиента DRM
- Пакет SDK для Windows Media Format, расширенные API клиента
- Windows Media Format SDK, расширенные API
- Windows Media Format SDK, API
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Пакет SDK для Windows Media Format, получение лицензий
- Пакет SDK для Windows Media Format, лицензии
- Управление цифровыми правами (DRM), расширенные API клиента
- DRM (Управление цифровыми правами), расширенные API клиента
- Управление цифровыми правами (DRM), расширенные API
- DRM (Управление цифровыми правами), расширенные API
- Управление цифровыми правами (DRM), API
- DRM (Управление цифровыми правами), API
- Управление цифровыми правами (DRM), получение лицензий
- DRM (Управление цифровыми правами), получение лицензий
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Расширенные API клиента DRM, получение лицензий
- Расширенные API клиента, получение лицензий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410639"
---
# <a name="acquiring-licenses"></a><span data-ttu-id="e302c-122">Получение лицензий</span><span class="sxs-lookup"><span data-stu-id="e302c-122">Acquiring Licenses</span></span>

<span data-ttu-id="e302c-123">Распространенный сценарий для получения лицензий — когда пользователь имеет защищенный файл Windows Media и пытается получить доступ к содержимому в первый раз.</span><span class="sxs-lookup"><span data-stu-id="e302c-123">A common scenario for acquiring licenses is when a user has a protected Windows Media file and tries to access the content for the first time.</span></span> <span data-ttu-id="e302c-124">Поскольку расширенные API клиента DRM Windows Media отличаются от подпрограмм обработки файлов ASF, базовый сценарий приобретения лицензий, поддерживаемый, требует больше вызовов API, чем использование пакета SDK формата Windows Media и пакета SDK для Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e302c-124">Because the Windows Media DRM Client Extended APIs are separate from ASF file handling routines, the basic license acquisition scenario, while supported, requires more API calls than using the Windows Media Format SDK and the Media Foundation SDK.</span></span>

<span data-ttu-id="e302c-125">В этом разделе описывается, как использовать расширенные API клиента DRM Windows Media для получения лицензий, которые хранятся в локальном хранилище лицензий на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="e302c-125">This section describes how to use the Windows Media DRM Client Extended APIs to acquire licenses that are stored in the local license store on a client computer.</span></span> <span data-ttu-id="e302c-126">Он содержит следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="e302c-126">It contains the following topics.</span></span>



| <span data-ttu-id="e302c-127">Раздел</span><span class="sxs-lookup"><span data-stu-id="e302c-127">Topic</span></span>                                                                | <span data-ttu-id="e302c-128">Описание</span><span class="sxs-lookup"><span data-stu-id="e302c-128">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e302c-129">Автоматическое получение лицензий</span><span class="sxs-lookup"><span data-stu-id="e302c-129">Silent License Acquisition</span></span>](silent-license-acquisition.md)         | <span data-ttu-id="e302c-130">Описывает, как получать лицензии без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="e302c-130">Describes how to acquire licenses without user intervention.</span></span>                                                                               |
| [<span data-ttu-id="e302c-131">Получение лицензий без уведомления</span><span class="sxs-lookup"><span data-stu-id="e302c-131">Non-Silent License Acquisition</span></span>](non-silent-license-acquisition.md) | <span data-ttu-id="e302c-132">Описывает, как получить лицензии, если требуется вмешательство пользователя (например, оплата содержимого).</span><span class="sxs-lookup"><span data-stu-id="e302c-132">Describes how to acquire licenses when user intervention (such as paying for the content) is required.</span></span>                                     |
| [<span data-ttu-id="e302c-133">Предварительная Поставка лицензий</span><span class="sxs-lookup"><span data-stu-id="e302c-133">License Pre-Delivery</span></span>](license-pre-delivery.md)                     | <span data-ttu-id="e302c-134">Описывает, как получать лицензии с сервера лицензий на клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="e302c-134">Describes how to pull licenses from a license server to a client computer.</span></span>                                                                 |
| [<span data-ttu-id="e302c-135">Создание лицензий локально</span><span class="sxs-lookup"><span data-stu-id="e302c-135">Creating Licenses Locally</span></span>](creating-licenses-locally.md)           | <span data-ttu-id="e302c-136">Описывает создание собственных лицензий без их загрузки с сервера лицензирования и хранение их в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="e302c-136">Describes how to create your own licenses without downloading them from a license server and how to store them in the local license store.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e302c-137">См. также</span><span class="sxs-lookup"><span data-stu-id="e302c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e302c-138">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="e302c-138">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




