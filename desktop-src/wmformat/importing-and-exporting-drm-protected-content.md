---
title: Импорт и экспорт содержимого, защищенного с использованием DRM
description: Импорт и экспорт содержимого, защищенного с использованием DRM
ms.assetid: 1c0520dd-b698-4174-a70e-32f43e2395b1
keywords:
- Windows Media Format SDK, расширенные API клиента DRM
- Пакет SDK для Windows Media Format, расширенные API клиента
- Windows Media Format SDK, расширенные API
- Windows Media Format SDK, API
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Windows Media Format SDK, импорт
- Пакет Windows Media Format SDK, экспорт
- Управление цифровыми правами (DRM), расширенные API клиента
- DRM (Управление цифровыми правами), расширенные API клиента
- Управление цифровыми правами (DRM), расширенные API
- DRM (Управление цифровыми правами), расширенные API
- Управление цифровыми правами (DRM), API
- DRM (Управление цифровыми правами), API
- Управление цифровыми правами (DRM), импорт защищенного содержимого
- DRM (Управление цифровыми правами), импорт защищенного содержимого
- Управление цифровыми правами (DRM), экспорт защищенного содержимого
- DRM (Управление цифровыми правами), экспорт защищенного содержимого
- Расширенные API клиента DRM, о
- Расширенные API клиента, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f368417b62c9746b6d2c9e331b9cd849455b8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778899"
---
# <a name="importing-and-exporting-drm-protected-content"></a><span data-ttu-id="6dfb9-122">Импорт и экспорт содержимого, защищенного с использованием DRM</span><span class="sxs-lookup"><span data-stu-id="6dfb9-122">Importing and Exporting DRM Protected Content</span></span>

<span data-ttu-id="6dfb9-123">Одна из основных ролей новых расширенных API клиента DRM Windows Media — включение импорта и экспорта содержимого, защищенного с помощью DRM, в сторонние системы управления правами.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-123">One of the primary roles of the new Windows Media DRM Client Extended APIs is to enable the import and export of DRM-protected content to third-party rights management systems.</span></span>

<span data-ttu-id="6dfb9-124">Основная сложность импорта и экспорта защищенных данных в приложении заключается в надежном обмене образцами данных ASF между системой и подсистемой DRM.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-124">The primary challenge of importing and exporting protected data in your application is to robustly share ASF data samples between your system and the DRM subsystem.</span></span> <span data-ttu-id="6dfb9-125">Когда приложение обрабатывает образцы данных, оно должно обеспечить соблюдение определенных стандартов надежности, чтобы избежать возможного обхода механизма защиты.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-125">When your application handles data samples it has to assure that certain robustness standards are met to avoid the potential for the protection mechanism to be circumvented.</span></span> <span data-ttu-id="6dfb9-126">Эти стандарты описаны в правилах надежности и соответствия требованиям, которые вы соглашаетесь соблюдать при лицензировании DRM.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-126">These standards are outlined in the robustness and compliance rules that you agree to when you license DRM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dfb9-127">См. также</span><span class="sxs-lookup"><span data-stu-id="6dfb9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dfb9-128">**О расширенных API-интерфейсах клиента DRM Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6dfb9-128">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




