---
title: Получение сведений из лицензий в локальном хранилище лицензий
description: Получение сведений из лицензий в локальном хранилище лицензий
ms.assetid: dd1abd5e-6536-4d8f-9607-b800c5a16d04
keywords:
- Windows Media Format SDK, расширенные API клиента DRM
- Пакет SDK для Windows Media Format, расширенные API клиента
- Windows Media Format SDK, расширенные API
- Windows Media Format SDK, API
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Пакет SDK Windows Media Format, локальное хранилище лицензий
- Пакет SDK для Windows Media Format, лицензии
- Управление цифровыми правами (DRM), расширенные API клиента
- DRM (Управление цифровыми правами), расширенные API клиента
- Управление цифровыми правами (DRM), расширенные API
- DRM (Управление цифровыми правами), расширенные API
- Управление цифровыми правами (DRM), API
- DRM (Управление цифровыми правами), API
- Управление цифровыми правами (DRM), локальное хранилище лицензий
- DRM (Управление цифровыми правами), локальное хранилище лицензий
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Расширенные API клиента DRM, локальное хранилище лицензий
- Расширенные API клиента, локальное хранилище лицензий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479c7b9351535ba15c75da8a2ee3ddad1b273805
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654226"
---
# <a name="getting-information-from-licenses-in-the-local-license-store"></a><span data-ttu-id="34d8b-122">Получение сведений из лицензий в локальном хранилище лицензий</span><span class="sxs-lookup"><span data-stu-id="34d8b-122">Getting Information from Licenses in the Local License Store</span></span>

<span data-ttu-id="34d8b-123">Расширенные API клиента DRM Windows Media предоставляют несколько способов получения сведений о правах, предоставленных лицензиями в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="34d8b-123">The Windows Media DRM Client Extended APIs provide multiple ways to get information about the rights granted by licenses in the local license store.</span></span> <span data-ttu-id="34d8b-124">В следующих разделах описывается, как получить данные различных типов.</span><span class="sxs-lookup"><span data-stu-id="34d8b-124">The following topics describe how to get these various types of information.</span></span>



| <span data-ttu-id="34d8b-125">Раздел</span><span class="sxs-lookup"><span data-stu-id="34d8b-125">Topic</span></span>                                                                                                  | <span data-ttu-id="34d8b-126">Описание</span><span class="sxs-lookup"><span data-stu-id="34d8b-126">Description</span></span>                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34d8b-127">Запрос сведений о простых правах</span><span class="sxs-lookup"><span data-stu-id="34d8b-127">Querying for Simple Rights Information</span></span>](querying-for-simple-rights-information.md)                   | <span data-ttu-id="34d8b-128">Описание способов получения простых сведений о том, разрешены ли определенные действия для защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="34d8b-128">Describes how to get simple information about whether specific actions are allowed for protected content.</span></span> <span data-ttu-id="34d8b-129">Например, приложение может воспроизвести файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="34d8b-129">For example, can an application play a media file.</span></span>                    |
| [<span data-ttu-id="34d8b-130">Запрос подробных сведений о правах</span><span class="sxs-lookup"><span data-stu-id="34d8b-130">Querying for Detailed Rights Information</span></span>](querying-for-detailed-rights-information.md)               | <span data-ttu-id="34d8b-131">Описание получения подробных обобщенных сведений о правах, предоставленных всеми лицензиями в локальном хранилище лицензий, для элемента защищенного содержимого с помощью идентификатора ключа.</span><span class="sxs-lookup"><span data-stu-id="34d8b-131">Describes how to get detailed aggregated information about the rights granted by all the licenses in the local license store for a piece of protected content using the key ID.</span></span> |
| [<span data-ttu-id="34d8b-132">Перечисление лицензий в локальном хранилище лицензий</span><span class="sxs-lookup"><span data-stu-id="34d8b-132">Enumerating Licenses in the Local License Store</span></span>](enumerating-licenses-in-the-local-license-store.md) | <span data-ttu-id="34d8b-133">Описывает, как получить отдельные лицензии из локального хранилища лицензий.</span><span class="sxs-lookup"><span data-stu-id="34d8b-133">Describes how to get individual licenses from the local license store.</span></span>                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="34d8b-134">См. также</span><span class="sxs-lookup"><span data-stu-id="34d8b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34d8b-135">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="34d8b-135">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




