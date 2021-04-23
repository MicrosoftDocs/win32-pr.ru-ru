---
title: Программное обеспечении клиента DRM для Microsoft Windows Media
description: Программное обеспечении клиента DRM для Microsoft Windows Media
ms.assetid: e7b179b3-ed14-4ea0-9a00-9d96557a2e2e
keywords:
- Windows Media Format SDK, расширенные API клиента DRM
- Пакет SDK для Windows Media Format, расширенные API клиента
- Windows Media Format SDK, расширенные API
- Windows Media Format SDK, API
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Windows Media Format SDK, программное обеспеченное программирование
- Управление цифровыми правами (DRM), расширенные API клиента
- DRM (Управление цифровыми правами), расширенные API клиента
- Управление цифровыми правами (DRM), расширенные API
- DRM (Управление цифровыми правами), расширенные API
- Управление цифровыми правами (DRM), API
- DRM (Управление цифровыми правами), API
- Управление цифровыми правами (DRM), руководство по программированию
- DRM (Управление цифровыми правами), руководство по программированию
- Расширенные API клиента DRM, о
- Расширенные API клиента, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b338ea6ebd9cb132c8e6b1c76c8e1d7f6c6aa182
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488778"
---
# <a name="microsoft-windows-media-drm-client-programming-guide"></a><span data-ttu-id="9a56b-119">Программное обеспечении клиента DRM для Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="9a56b-119">Microsoft Windows Media DRM Client Programming Guide</span></span>

<span data-ttu-id="9a56b-120">В этом разделе содержатся сведения об использовании функций расширенных API клиента Windows Media DRM в приложениях.</span><span class="sxs-lookup"><span data-stu-id="9a56b-120">This guide provides information about using the features of the Windows Media DRM Client Extended APIs in your applications.</span></span> <span data-ttu-id="9a56b-121">В следующих разделах подробно описаны действия, связанные с реализацией функций DRM.</span><span class="sxs-lookup"><span data-stu-id="9a56b-121">The following sections explain, in detail, the steps involved in implementing DRM features.</span></span>



| <span data-ttu-id="9a56b-122">Section</span><span class="sxs-lookup"><span data-stu-id="9a56b-122">Section</span></span>                                                                                                                          | <span data-ttu-id="9a56b-123">Описание</span><span class="sxs-lookup"><span data-stu-id="9a56b-123">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a56b-124">Начало работы</span><span class="sxs-lookup"><span data-stu-id="9a56b-124">Getting Started</span></span>](drm-getting-started.md)                                                                                       | <span data-ttu-id="9a56b-125">Содержит сведения о настройке проектов C++, использующих расширенные API клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9a56b-125">Provides information about setting up C++ projects that use the Windows Media DRM Client Extended APIs.</span></span>    |
| [<span data-ttu-id="9a56b-126">Получение лицензий</span><span class="sxs-lookup"><span data-stu-id="9a56b-126">Acquiring Licenses</span></span>](acquiring-licenses.md)                                                                                     | <span data-ttu-id="9a56b-127">Описывает, как получить лицензии на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="9a56b-127">Describes how to get licenses on the client computer.</span></span>                                                      |
| [<span data-ttu-id="9a56b-128">Получение сведений из лицензий в локальном хранилище лицензий</span><span class="sxs-lookup"><span data-stu-id="9a56b-128">Getting Information from Licenses in the Local License Store</span></span>](getting-information-from-licenses-in-the-local-license-store.md) | <span data-ttu-id="9a56b-129">Описывает, как получить сведения о правах на защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="9a56b-129">Describes how to get information about rights for protected content.</span></span>                                       |
| [<span data-ttu-id="9a56b-130">Выполнение индивидуальной управления цифровыми правами</span><span class="sxs-lookup"><span data-stu-id="9a56b-130">Performing DRM Individualization</span></span>](performing-drm-individualization.md)                                                         | <span data-ttu-id="9a56b-131">Описывает, как обновить и индивидуализируйте компонент DRM на клиентском компьютере, чтобы сделать его более безопасным.</span><span class="sxs-lookup"><span data-stu-id="9a56b-131">Describes how to update and individualize the DRM component on the client computer to make it more secure.</span></span> |
| [<span data-ttu-id="9a56b-132">Экспорт DRM</span><span class="sxs-lookup"><span data-stu-id="9a56b-132">DRM Export</span></span>](drm-export.md)                                                                                                     | <span data-ttu-id="9a56b-133">Описывает, как экспортировать содержимое, защищенное с помощью Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="9a56b-133">Describes how to export content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="9a56b-134">Импорт DRM</span><span class="sxs-lookup"><span data-stu-id="9a56b-134">DRM Import</span></span>](drm-import.md)                                                                                                     | <span data-ttu-id="9a56b-135">Описывает, как импортировать содержимое, защищенное с помощью Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="9a56b-135">Describes how to import content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="9a56b-136">Отзыв лицензий</span><span class="sxs-lookup"><span data-stu-id="9a56b-136">License Revocation</span></span>](drm-license-revocation.md)                                                                                 | <span data-ttu-id="9a56b-137">Описание удаления лицензий из локального хранилища лицензий.</span><span class="sxs-lookup"><span data-stu-id="9a56b-137">Describes how to remove licenses from the local license store.</span></span>                                             |
| [<span data-ttu-id="9a56b-138">Автоматизированный отзыв и продление компонентов</span><span class="sxs-lookup"><span data-stu-id="9a56b-138">Automated Component Revocation and Renewal</span></span>](automated-component-revocation-and-renewal.md)                                     | <span data-ttu-id="9a56b-139">Описывает автоматизированный отзыв и обновление системы управления цифровыми правами Windows Media с помощью Content созидателями.</span><span class="sxs-lookup"><span data-stu-id="9a56b-139">Describes the Windows Media DRM automated revocation and renewal system using content enablers.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="9a56b-140">См. также</span><span class="sxs-lookup"><span data-stu-id="9a56b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a56b-141">**Расширенные API клиента DRM Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9a56b-141">**Windows Media DRM Client Extended APIs**</span></span>](windows-media-drm-client-extended-apis.md)
</dt> <dt>

<span data-ttu-id="9a56b-142">[Пакет SDK для диспетчера прав Windows Media](/previous-versions/ms986509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9a56b-142">[Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10))</span></span>
</dt> </dl>

 

 
