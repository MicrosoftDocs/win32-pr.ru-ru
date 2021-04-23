---
title: Проверка отзыва сертификата
description: Проверка отзыва сертификата
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- Windows Media Format SDK, импорт DRM
- Windows Media Format SDK, импорт
- Пакет SDK для формата Windows Media, отзыв сертификата
- Windows Media Format SDK, отзыв сертификатов
- Управление цифровыми правами (DRM), импорт
- DRM (Управление цифровыми правами), импорт
- Управление цифровыми правами (DRM), отзыв сертификата
- DRM (Управление цифровыми правами), отзыв сертификата
- Управление цифровыми правами (DRM), отзыв сертификатов
- DRM (Управление цифровыми правами), отзыв сертификатов
- Расширенные API клиента DRM, импорт
- Расширенные API клиента, импорт
- Расширенные API клиента DRM, отзыв сертификата
- Расширенные API клиента, отзыв сертификатов
- Расширенные API клиента DRM, отзыв сертификатов
- Расширенные API клиента, отзыв сертификатов
- сертификаты, отзыв
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbb72dd52870437ef9b69b30cc36a57725abe09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775770"
---
# <a name="checking-certificate-revocation"></a><span data-ttu-id="bd6e5-120">Проверка отзыва сертификата</span><span class="sxs-lookup"><span data-stu-id="bd6e5-120">Checking Certificate Revocation</span></span>

<span data-ttu-id="bd6e5-121">При импорте содержимого в Windows Media DRM необходимо убедиться, что сертификат в коллекции сертификатов не отозван путем проверки того, что сертификат в коллекции не содержится в списке отзыва.</span><span class="sxs-lookup"><span data-stu-id="bd6e5-121">When importing content into Windows Media DRM, you must ensure that no certificate in a certificate collection has been revoked by verifying that no certificate in the collection is in the revocation list.</span></span> <span data-ttu-id="bd6e5-122">Список отзыва извлекается с помощью метода [**ивмдрмсекурити:: жетревокатиондата**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="bd6e5-122">The revocation list is extracted by using the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>

<span data-ttu-id="bd6e5-123">Затем используйте метод [**ивмдрмсекурити:: чеккцертфорревокатион**](iwmdrmsecurity-checkcertforrevocation.md) , чтобы убедиться, что сертификат не отозван.</span><span class="sxs-lookup"><span data-stu-id="bd6e5-123">You then use the [**IWMDRMSecurity::CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) method to verify that the certificate is not revoked.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd6e5-124">См. также</span><span class="sxs-lookup"><span data-stu-id="bd6e5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd6e5-125">**Импорт DRM**</span><span class="sxs-lookup"><span data-stu-id="bd6e5-125">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




