---
title: Создание лицензии КСМР
description: Создание лицензии КСМР
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows Media Format SDK, импорт DRM
- Windows Media Format SDK, импорт
- Пакет SDK для Windows Media Format, лицензии КСМР
- Пакет SDK для Windows Media Format, лицензии
- Windows Media Format SDK, права расширяемых носителей (КСМР)
- Управление цифровыми правами (DRM), импорт
- DRM (Управление цифровыми правами), импорт
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Управление цифровыми правами (DRM), лицензии КСМР
- DRM (Управление цифровыми правами), лицензии КСМР
- Управление цифровыми правами (DRM), права расширяемого носителя (КСМР)
- DRM (Управление цифровыми правами), права расширяемого носителя (КСМР)
- Расширенные API клиента DRM, импорт
- Расширенные API клиента, импорт
- Расширенные API клиента DRM, лицензии КСМР
- Расширенные API клиента, лицензии КСМР
- Расширенные API клиента DRM, лицензии
- Расширенные API клиента, лицензии
- Расширенные API клиента DRM, права расширяемых носителей (КСМР)
- Расширенные API клиента, права расширяемых носителей (КСМР)
- лицензии, КСМР
- Права расширяемых носителей (КСМР)
- КСМР (расширяемые права на носители)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc275419116362c08cabe4dc70aa227687705fdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410620"
---
# <a name="building-an-xmr-license"></a><span data-ttu-id="c9b34-127">Создание лицензии КСМР</span><span class="sxs-lookup"><span data-stu-id="c9b34-127">Building an XMR License</span></span>

<span data-ttu-id="c9b34-128">Чтобы создать лицензию для обработки Windows Media DRM, необходимо использовать двоичную схему КСМР (Extensible Media Rights).</span><span class="sxs-lookup"><span data-stu-id="c9b34-128">To generate a license for Windows Media DRM to process, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="c9b34-129">КСМР — это схема для передачи прав на использование мультимедиа и ограничений, которые должны быть лицензированы отдельно.</span><span class="sxs-lookup"><span data-stu-id="c9b34-129">XMR is a schema for conveying media usage rights and restrictions and needs to be licensed separately.</span></span>

<span data-ttu-id="c9b34-130">Важный материал в лицензии шифруется с помощью открытого ключа в коллекции сертификатов DRM Windows Media, поэтому он доступен только для подсистемы расширенного API клиента Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="c9b34-130">The important material in a license is encrypted using the public key in the Windows Media DRM certificate collection, so it is visible only to the Windows Media DRM Client Extended API subsystem.</span></span> <span data-ttu-id="c9b34-131">.</span><span class="sxs-lookup"><span data-stu-id="c9b34-131">.</span></span>

<span data-ttu-id="c9b34-132">Вы обязаны убедиться, что структура лицензии и параметры политики действительны и согласованы с намерением издателя лицензии и соответствуют правилам соответствия.</span><span class="sxs-lookup"><span data-stu-id="c9b34-132">It is your responsibility to ensure that the license structure and policy settings are valid and consistent with the license issuer's intent, and that they conform to the compliance rules.</span></span>

<span data-ttu-id="c9b34-133">Чтобы узнать полный набор объектов КСМР, которые должны присутствовать в лицензии, ознакомьтесь с разрядом правил соответствия импорта DRM в Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c9b34-133">You should read the Windows Media DRM import compliance rules to learn the complete set of XMR objects that must be present in the license.</span></span>

<span data-ttu-id="c9b34-134">Чтобы передать лицензию КСМР в подсистему DRM, вызовите метод [**ивмдрмлиценсеманажемент:: сторелиценсе**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="c9b34-134">To pass the XMR license to the DRM subsystem, call the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span> <span data-ttu-id="c9b34-135">Используйте следующий формат для передачи лицензии в параметре *бстрлиценсереспонсе* :</span><span class="sxs-lookup"><span data-stu-id="c9b34-135">Use the following format to pass the license in the *bstrLicenseResponse* parameter:</span></span>


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



<span data-ttu-id="c9b34-136">Эта строка должна быть в формате Юникода (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="c9b34-136">This string must be in Unicode format (UTF-16).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9b34-137">См. также</span><span class="sxs-lookup"><span data-stu-id="c9b34-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9b34-138">**Импорт DRM**</span><span class="sxs-lookup"><span data-stu-id="c9b34-138">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




