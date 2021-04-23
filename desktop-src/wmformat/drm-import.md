---
title: Импорт DRM
description: Импорт DRM
ms.assetid: 5e67a721-830b-4d99-9f90-4cb2d7c61104
keywords:
- Windows Media Format SDK, расширенные API клиента DRM
- Пакет SDK для Windows Media Format, расширенные API клиента
- Windows Media Format SDK, расширенные API
- Windows Media Format SDK, API
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Windows Media Format SDK, импорт DRM
- Windows Media Format SDK, импорт
- Windows Media Format SDK, система защиты содержимого (CPS)
- Управление цифровыми правами (DRM), расширенные API клиента
- DRM (Управление цифровыми правами), расширенные API клиента
- Управление цифровыми правами (DRM), расширенные API
- DRM (Управление цифровыми правами), расширенные API
- Управление цифровыми правами (DRM), API
- DRM (Управление цифровыми правами), API
- Управление цифровыми правами (DRM), импорт
- DRM (Управление цифровыми правами), импорт
- Управление цифровыми правами (DRM), система защиты содержимого (CPS)
- DRM (Управление цифровыми правами), система защиты содержимого (CPS)
- Расширенные API клиента DRM, импорт
- Расширенные API клиента, импорт
- Расширенные API клиента DRM, система защиты содержимого (CPS)
- Расширенные API клиента, система защиты содержимого (CPS)
- система защиты содержимого (CPS)
- CPS (система защиты содержимого)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fc20cfd682df975c10a8f39785c0e8d69610d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776664"
---
# <a name="drm-import"></a><span data-ttu-id="e4eb0-127">Импорт DRM</span><span class="sxs-lookup"><span data-stu-id="e4eb0-127">DRM Import</span></span>

<span data-ttu-id="e4eb0-128">В следующих разделах объясняется, как преобразовать мультимедийное содержимое из сторонней системы защиты содержимого (CPS) в Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-128">The following sections explain how to convert media content from a third-party content protection system (CPS) to Windows Media DRM.</span></span> <span data-ttu-id="e4eb0-129">Этот процесс называется импортом DRM и состоит из следующих этапов:</span><span class="sxs-lookup"><span data-stu-id="e4eb0-129">This process is known as DRM Import and consists essentially of the following steps:</span></span>

1.  <span data-ttu-id="e4eb0-130">Создание файла ASF.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-130">Creating the ASF file.</span></span>
2.  <span data-ttu-id="e4eb0-131">Создание лицензии.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-131">Creating the license.</span></span>
3.  <span data-ttu-id="e4eb0-132">При необходимости удалите лицензию.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-132">Optionally deleting the license.</span></span>

<span data-ttu-id="e4eb0-133">Импорт DRM описывается в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-133">DRM Import is explained in the following sections.</span></span>



| <span data-ttu-id="e4eb0-134">Section</span><span class="sxs-lookup"><span data-stu-id="e4eb0-134">Section</span></span>                                                                              | <span data-ttu-id="e4eb0-135">Описание</span><span class="sxs-lookup"><span data-stu-id="e4eb0-135">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4eb0-136">Импорт лицензии и материала ключа</span><span class="sxs-lookup"><span data-stu-id="e4eb0-136">Importing License and Key Material</span></span>](importing-license-and-key-material.md)         | <span data-ttu-id="e4eb0-137">Описывает, как выдавать лицензии локально и импортировать их в Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-137">Describes how to issue licenses locally and import them into Windows Media DRM.</span></span>      |
| [<span data-ttu-id="e4eb0-138">Проверка отзыва сертификата</span><span class="sxs-lookup"><span data-stu-id="e4eb0-138">Checking Certificate Revocation</span></span>](checking-certificate-revocation.md)               | <span data-ttu-id="e4eb0-139">Описывает, как проверить отзыв сертификата.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-139">Describes how to check certificate revocation.</span></span>                                       |
| [<span data-ttu-id="e4eb0-140">Создание лицензии КСМР</span><span class="sxs-lookup"><span data-stu-id="e4eb0-140">Building an XMR License</span></span>](building-an-xmr-license.md)                               | <span data-ttu-id="e4eb0-141">Описывает, как создать лицензию КСМР и передать ее в подсистему DRM.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-141">Describes how to create an XMR license and pass it to the DRM subsystem.</span></span>             |
| [<span data-ttu-id="e4eb0-142">Создание и инициализация модуля записи DRM</span><span class="sxs-lookup"><span data-stu-id="e4eb0-142">Creating and Initializing a DRM Writer</span></span>](creating-and-initializing-a-drm-writer.md) | <span data-ttu-id="e4eb0-143">Описание инициализации объекта модуля записи ASF для подготовки к импорту DRM.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-143">Describes how to initialize an ASF writer object to prepare for DRM Import.</span></span>          |
| [<span data-ttu-id="e4eb0-144">Шифрование и импорт примеров мультимедиа</span><span class="sxs-lookup"><span data-stu-id="e4eb0-144">Encrypting and Importing Media Samples</span></span>](encrypting-and-importing-media-samples.md) | <span data-ttu-id="e4eb0-145">Описывает шифрование и импорт отдельных образцов мультимедиа в Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-145">Describes how to encrypt and import individual media samples into Windows Media DRM.</span></span> |
| [<span data-ttu-id="e4eb0-146">Удаление лицензий</span><span class="sxs-lookup"><span data-stu-id="e4eb0-146">License Deletion</span></span>](license-deletion.md)                                             | <span data-ttu-id="e4eb0-147">Описывает, как удалить локально созданные лицензии.</span><span class="sxs-lookup"><span data-stu-id="e4eb0-147">Describes how to delete locally created licenses.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="e4eb0-148">См. также</span><span class="sxs-lookup"><span data-stu-id="e4eb0-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4eb0-149">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="e4eb0-149">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




