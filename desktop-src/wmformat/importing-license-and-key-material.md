---
title: Импорт лицензии и материала ключа
description: Импорт лицензии и материала ключа
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows Media Format SDK, импорт DRM
- Windows Media Format SDK, импорт
- Пакет SDK для Windows Media Format, лицензии
- Управление цифровыми правами (DRM), импорт
- DRM (Управление цифровыми правами), импорт
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Управление цифровыми правами (DRM), материал ключа
- DRM (Управление цифровыми правами), материал ключа
- Расширенные API клиента DRM, импорт
- Расширенные API клиента, импорт
- Расширенные API клиента DRM, лицензии
- Расширенные API клиента, лицензии
- Расширенные API клиента DRM, ключевой материал
- Расширенные API клиента, ключевой материал
- лицензии, импорт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258960"
---
# <a name="importing-license-and-key-material"></a><span data-ttu-id="81297-119">Импорт лицензии и материала ключа</span><span class="sxs-lookup"><span data-stu-id="81297-119">Importing License and Key Material</span></span>

<span data-ttu-id="81297-120">Если у вас есть мультимедийное содержимое, зашифрованное с помощью сторонней системы защиты содержимого, и вы хотите импортировать лицензию и материал ключа в Windows Media DRM, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="81297-120">If you have media content that was encrypted using a third-party content protection system and you want to import the license and key material into Windows Media DRM, follow these steps:</span></span>

1.  <span data-ttu-id="81297-121">Получите коллекцию сертификатов компьютера Windows Media DRM, вызвав метод [**ивмдрмсекурити:: жетмачинецертификате**](iwmdrmsecurity-getmachinecertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="81297-121">Retrieve the Windows Media DRM machine certificate collection by calling the [**IWMDRMSecurity::GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) method.</span></span>
2.  <span data-ttu-id="81297-122">Проанализируйте коллекцию сертификатов, убедившись, что она подписана правильно и проверена на известный корневой открытый ключ Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="81297-122">Parse the certificate collection, ensuring that it is signed correctly and is validated to a known Microsoft root public key.</span></span> <span data-ttu-id="81297-123">Коллекция сертификатов соответствует схеме КСМР.</span><span class="sxs-lookup"><span data-stu-id="81297-123">The certificate collection conforms to the XMR schema.</span></span> <span data-ttu-id="81297-124">Дополнительные сведения см. в разделе [Создание лицензии КСМР](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="81297-124">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>
3.  <span data-ttu-id="81297-125">Необязательно. Извлеките список отзыва, вызвав метод [**ивмдрмсекурити:: жетревокатиондата**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="81297-125">Optional: Extract the revocation list by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
4.  <span data-ttu-id="81297-126">Необязательно. Убедитесь, что сертификат в коллекции не отозван.</span><span class="sxs-lookup"><span data-stu-id="81297-126">Optional: Insure that no certificate in the collection is revoked.</span></span> <span data-ttu-id="81297-127">Дополнительные сведения см. в разделе [Проверка отзыва сертификата](checking-certificate-revocation.md).</span><span class="sxs-lookup"><span data-stu-id="81297-127">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
5.  <span data-ttu-id="81297-128">Создайте лицензию в формате КСМР, который представляет требования политики для импортируемого содержимого и содержит соответствующий материал ключа DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="81297-128">Generate a license in the XMR format that represents the policy requirements for the import content and contains the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="81297-129">Дополнительные сведения см. в разделе [Создание лицензии КСМР](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="81297-129">For more information, see the topic [Building an XMR License](building-an-xmr-license.md).</span></span>
6.  <span data-ttu-id="81297-130">Передайте лицензию КСМР в систему DRM Windows Media для обработки с помощью метода [**ивмдрмлиценсеманажемент:: сторелиценсе**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="81297-130">Pass the XMR license to the Windows Media DRM system for processing, by using the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="81297-131">Сведения о схеме КСМР будут предоставлены вам при лицензировании Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="81297-131">Details about the XMR schema will be provided to you when you license Windows Media DRM.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="81297-132">См. также</span><span class="sxs-lookup"><span data-stu-id="81297-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81297-133">**Проверка отзыва сертификата**</span><span class="sxs-lookup"><span data-stu-id="81297-133">**Checking Certificate Revocation**</span></span>](checking-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="81297-134">**Создание лицензии КСМР**</span><span class="sxs-lookup"><span data-stu-id="81297-134">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="81297-135">**Импорт DRM**</span><span class="sxs-lookup"><span data-stu-id="81297-135">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




