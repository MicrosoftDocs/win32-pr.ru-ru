---
title: Отзыв лицензий (клиент DRM Microsoft Windows Media)
description: Отзыв лицензий (клиент DRM Microsoft Windows Media)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Пакет SDK для Windows Media Format, лицензии
- Пакет SDK для Windows Media Format, отзыв лицензий
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Управление цифровыми правами (DRM), отзыв лицензий
- DRM (Управление цифровыми правами), отзыв лицензий
- Расширенные API клиента DRM, лицензии
- Расширенные API клиента, лицензии
- Расширенные API клиента DRM, отзыв лицензий
- Расширенные API клиента, отзыв лицензий
- лицензии, отзыв
- Отзыв лицензий, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104273192"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a><span data-ttu-id="acfc0-115">Отзыв лицензий (клиент DRM Microsoft Windows Media)</span><span class="sxs-lookup"><span data-stu-id="acfc0-115">License Revocation (Microsoft Windows Media DRM Client)</span></span>

<span data-ttu-id="acfc0-116">Отзыв лицензии означает удаление лицензий из локального хранилища лицензий.</span><span class="sxs-lookup"><span data-stu-id="acfc0-116">License revocation refers to the removal of licenses from a local license store.</span></span> <span data-ttu-id="acfc0-117">Распространенный сценарий отзыва лицензий возникает, когда поставщик услуг, например служба подписки на музыку, должен отключить службу на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="acfc0-117">A common scenario for license revocation occurs when a service provider, such as a music subscription service, must deactivate the service on a user's computer.</span></span>

<span data-ttu-id="acfc0-118">Процесс отзыва лицензии инициируется службой, предоставленной издателем лицензии.</span><span class="sxs-lookup"><span data-stu-id="acfc0-118">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="acfc0-119">В приложении может размещаться эта служба, или она может быть веб-приложением.</span><span class="sxs-lookup"><span data-stu-id="acfc0-119">Your application can host this service or it can be a Web application.</span></span> <span data-ttu-id="acfc0-120">В любом случае приложение должно иметь возможность получить запрос лицензии, созданный службой.</span><span class="sxs-lookup"><span data-stu-id="acfc0-120">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="acfc0-121">Чтобы удалить лицензии из хранилища лицензий, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="acfc0-121">To remove licenses from the license store, do the following:</span></span>

1.  <span data-ttu-id="acfc0-122">При получении запроса лицензии от издателя лицензии создайте запрос отзыва с помощью метода [**ивмдрмлиценсеманажемент:: креателиценсеревокатиончалленже**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) .</span><span class="sxs-lookup"><span data-stu-id="acfc0-122">Upon receiving a license challenge from the license issuer, create a revocation challenge using the [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) method.</span></span> <span data-ttu-id="acfc0-123">Этот метод выделит буфер, содержащий данные запроса отзыва, который передается в приложение с помощью параметра *ппбчалленжеаутпут* .</span><span class="sxs-lookup"><span data-stu-id="acfc0-123">This method will allocate a buffer containing a revocation challenge data, which is passed to your application through the *ppbChallengeOutput* parameter.</span></span>
2.  <span data-ttu-id="acfc0-124">Отправьте запрос отзыва лицензии службе отзыва лицензий.</span><span class="sxs-lookup"><span data-stu-id="acfc0-124">Send the license revocation challenge to a license revocation service.</span></span> <span data-ttu-id="acfc0-125">Сервер создаст BLOB-объект отзыва лицензий (ЛРБ) в ответе.</span><span class="sxs-lookup"><span data-stu-id="acfc0-125">The server will generate a license revocation BLOB (LRB) in response.</span></span>
3.  <span data-ttu-id="acfc0-126">Удалите лицензию из локального хранилища с помощью метода [**ивмдрмлиценсеманажемент::P роцесслиценсеревокатионреспонсе**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) , передав лрб, возвращенную сервером лицензирования.</span><span class="sxs-lookup"><span data-stu-id="acfc0-126">Remove the license from the local store using the [**IWMDRMLicenseManagement::ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) method, passing the LRB returned by license server.</span></span>
4.  <span data-ttu-id="acfc0-127">Освобождение буфера, выделенного **креателиценсеревокатиончалленже** , с помощью функции **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="acfc0-127">Deallocate the buffer allocated by **CreateLicenseRevocationChallenge** by using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="acfc0-128">Дополнительные сведения о том, как работает отзыв лицензий, а также о том, как создать службу отзыва, см. в разделе [Реализация отзыва лицензий](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span><span class="sxs-lookup"><span data-stu-id="acfc0-128">For more information on how license revocation works or on how to write a revocation service, see [Implementing License Revocation](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="acfc0-129">См. также</span><span class="sxs-lookup"><span data-stu-id="acfc0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acfc0-130">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="acfc0-130">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="acfc0-131">**Локальное хранилище лицензий**</span><span class="sxs-lookup"><span data-stu-id="acfc0-131">**Local License Store**</span></span>](local-license-store.md)
</dt> <dt>

[<span data-ttu-id="acfc0-132">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="acfc0-132">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 