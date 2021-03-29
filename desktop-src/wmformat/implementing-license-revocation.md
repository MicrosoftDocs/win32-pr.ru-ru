---
title: Реализация отзыва лицензий
description: Реализация отзыва лицензий
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- Пакет SDK для Windows Media Format, реализация отзыва лицензий
- Пакет SDK для Windows Media Format, отзыв лицензий
- Windows Media Format SDK, отзыв лицензий
- Расширенный системный формат (ASF), реализация отзыва лицензий
- ASF (Расширенный системный формат), реализация отзыва лицензий
- Расширенный формат систем (ASF), отзыв лицензий
- ASF (расширенный формат систем), отзыв лицензий
- Расширенный формат систем (ASF), отзыв лицензий
- ASF (Расширенный системный формат), отзыв лицензий
- Управление цифровыми правами (DRM), реализация отзыва лицензий
- DRM (Управление цифровыми правами), реализация отзыва лицензий
- Управление цифровыми правами (DRM), отзыв лицензий
- DRM (Управление цифровыми правами), отзыв лицензий
- Управление цифровыми правами (DRM), отзыв лицензий
- DRM (Управление цифровыми правами), отзыв лицензий
- Отзыв лицензий, реализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83bfb1a512b031f5b7c297ecede4ed33fba8f2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788815"
---
# <a name="implementing-license-revocation"></a><span data-ttu-id="72d23-119">Реализация отзыва лицензий</span><span class="sxs-lookup"><span data-stu-id="72d23-119">Implementing License Revocation</span></span>

<span data-ttu-id="72d23-120">Пакет SDK для диспетчера прав Windows Media 10 содержит функцию отзыва лицензий.</span><span class="sxs-lookup"><span data-stu-id="72d23-120">The Windows Media Rights Manager 10 SDK includes a feature called license revocation.</span></span> <span data-ttu-id="72d23-121">Эта функция позволяет серверам лицензий запрашивать удаление лицензий с клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="72d23-121">This feature enables license servers to request that licenses be removed from the client computer.</span></span> <span data-ttu-id="72d23-122">Пакет SDK для формата Windows Media содержит методы, которые обрабатывают сообщения отзыва и удаляют лицензии из локального хранилища лицензий.</span><span class="sxs-lookup"><span data-stu-id="72d23-122">The Windows Media Format SDK provides methods that process revocation messages and remove the licenses from the local license store.</span></span>

<span data-ttu-id="72d23-123">Процесс отзыва лицензии инициируется службой, предоставленной издателем лицензии.</span><span class="sxs-lookup"><span data-stu-id="72d23-123">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="72d23-124">Приложение может размещать эту службу или веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="72d23-124">Your application can host this service, or it can be a Web application.</span></span> <span data-ttu-id="72d23-125">В любом случае приложение должно иметь возможность получить запрос лицензии, созданный службой.</span><span class="sxs-lookup"><span data-stu-id="72d23-125">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="72d23-126">Чтобы удалить лицензии из хранилища лицензий, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="72d23-126">To remove licenses from the license store, perform the following steps:</span></span>

1.  <span data-ttu-id="72d23-127">При получении запроса лицензии от издателя лицензии вызовите функцию [**вмкреателиценсеревокатионажент**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) , чтобы создать объект агента отзыва лицензий и получить указатель на интерфейс [**ивмлиценсеревокатионажент**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .</span><span class="sxs-lookup"><span data-stu-id="72d23-127">Upon receiving a license challenge from the license issuer, call the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function to create a license revocation agent object and obtain a pointer to the [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span>
2.  <span data-ttu-id="72d23-128">Вызовите метод [**ивмлиценсеревокатионажент:: жетлрбчалленже**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) , чтобы создать ответ на запрос.</span><span class="sxs-lookup"><span data-stu-id="72d23-128">Call the [**IWMLicenseRevocationAgent::GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) method to generate the challenge response.</span></span>
3.  <span data-ttu-id="72d23-129">Отправьте ответ на запрос к компоненту службы лицензирования, из которого вы получили запрос.</span><span class="sxs-lookup"><span data-stu-id="72d23-129">Send the challenge response back to the license service component from which you received the challenge.</span></span>
4.  <span data-ttu-id="72d23-130">Компонент службы лицензирования отправляет подписанный BLOB-объект отзыва лицензии (ЛРБ) в приложение.</span><span class="sxs-lookup"><span data-stu-id="72d23-130">The license service component sends a signed license revocation blob (LRB) to your application.</span></span> <span data-ttu-id="72d23-131">Когда вы получите его, вызовите метод [**ивмлиценсеревокатионажент::P роцесслрб**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) .</span><span class="sxs-lookup"><span data-stu-id="72d23-131">When you receive it, call the [**IWMLicenseRevocationAgent::ProcessLRB**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) method.</span></span> <span data-ttu-id="72d23-132">**Процесслрб** создает сообщение подтверждения, которое необходимо отправить обратно в службу лицензирования, чтобы убедиться, что лицензии удалены.</span><span class="sxs-lookup"><span data-stu-id="72d23-132">**ProcessLRB** creates an acknowledgement message that you must send back to the license service to verify that the licenses were removed.</span></span>

> [!Note]  
> <span data-ttu-id="72d23-133">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="72d23-133">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="72d23-134">См. также</span><span class="sxs-lookup"><span data-stu-id="72d23-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72d23-135">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="72d23-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="72d23-136">**Интерфейс Ивмлиценсеревокатионажент**</span><span class="sxs-lookup"><span data-stu-id="72d23-136">**IWMLicenseRevocationAgent Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




