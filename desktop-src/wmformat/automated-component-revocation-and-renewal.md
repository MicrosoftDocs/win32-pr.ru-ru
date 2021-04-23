---
title: Автоматизированный отзыв и продление компонентов
description: Автоматизированный отзыв и продление компонентов
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- Windows Media Format SDK, автоматизированный отзыв и продление срока действия
- Пакет SDK Windows Media Format, отзыв
- Windows Media Format SDK, продление
- Управление цифровыми правами (DRM), Автоматический отзыв и продление срока действия
- DRM (Управление цифровыми правами), автоматизированный отзыв и продление срока действия
- Управление цифровыми правами (DRM), отзыв
- DRM (Управление цифровыми правами), отзыв
- Управление цифровыми правами (DRM), продление
- DRM (Управление цифровыми правами), продление
- Расширенные API клиента DRM, Автоматический отзыв и продление срока действия
- Расширенные API клиента, Автоматический отзыв и продление срока действия
- Расширенные API клиента DRM, отзыв
- Расширенные API клиента, отзыв
- Расширенные API клиента DRM, продление
- Расширенные API клиента, продление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338628"
---
# <a name="automated-component-revocation-and-renewal"></a><span data-ttu-id="1fcca-118">Автоматизированный отзыв и продление компонентов</span><span class="sxs-lookup"><span data-stu-id="1fcca-118">Automated Component Revocation and Renewal</span></span>

<span data-ttu-id="1fcca-119">Программные приложения или компоненты, которые считаются скомпрометированными, могут быть отозваны корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1fcca-119">Software applications or components that are considered compromised can be revoked by Microsoft.</span></span> <span data-ttu-id="1fcca-120">Расширенный API клиента формата Windows Media обеспечивает механизм для автоматического отзыва и обновления компонентов.</span><span class="sxs-lookup"><span data-stu-id="1fcca-120">The Windows Media Format Client Extended API provides a mechanism for the automated revocation and renewal of components.</span></span>

<span data-ttu-id="1fcca-121">Отозванные компоненты перечислены в списке отзыва сертификатов, опубликованном корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1fcca-121">Revoked components are listed in a certificate revocation list, which is published by Microsoft.</span></span> <span data-ttu-id="1fcca-122">При отзыве компонента его сертификат добавляется в список отзыва сертификатов, а данные об отзыве (редакция \_ ) обновляются на серверах Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1fcca-122">When a component is revoked, its certificate is added to the certificate revocation list, and the revocation information BLOB (REV\_INFO) is updated on the Microsoft servers.</span></span>

<span data-ttu-id="1fcca-123">Чтобы выполнить автоматический отзыв и продление, когда пользователь пытается обработать защищенное с помощью DRM содержимое Windows Media, приложение должно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1fcca-123">To perform automated revocation and renewal when a user attempts to process Windows Media DRM protected content, your application must do the following:</span></span>

1.  <span data-ttu-id="1fcca-124">Извлеките \_ версию с информацией о версии из лицензии.</span><span class="sxs-lookup"><span data-stu-id="1fcca-124">Extract the REV\_INFO version from the license.</span></span> <span data-ttu-id="1fcca-125">\_Номер версии info находится в следующем расположении в лицензии КСМР:</span><span class="sxs-lookup"><span data-stu-id="1fcca-125">The REV\_INFO version number is located in the following location in an XMR license:</span></span>
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  <span data-ttu-id="1fcca-126">Сравните \_ номер версии лицензии с \_ номером версии сведений в локальном хранилище, вызвав метод [**Ивмдрмсекурити:: жетревокатиондатаверсион**](iwmdrmsecurity-getrevocationdataversion.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcca-126">Compare the REV\_INFO version number of the license with the REV\_INFO version number in the local store by calling the [**IWMDRMSecurity::GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) method.</span></span>
3.  <span data-ttu-id="1fcca-127">Если \_ версия сведений о версии устарела, вызовите метод [**ивмдрмсекурити::P ерформсекуритюпдате**](iwmdrmsecurity-performsecurityupdate.md) , передав в \_ \_ \_ \_ параметр *dwFlags* флаг обновления системы безопасности WMDRM.</span><span class="sxs-lookup"><span data-stu-id="1fcca-127">If the REV\_INFO version is not up to date, call the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, passing the WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH flag in the *dwFlags* parameter.</span></span>
4.  <span data-ttu-id="1fcca-128">Получите список отзыва сертификатов из локального хранилища, вызвав метод [**ивмдрмсекурити:: жетревокатиондата**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcca-128">Retrieve the certificate revocation list from the local store by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
5.  <span data-ttu-id="1fcca-129">Проанализируйте список отзыва и проверьте отзыв Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="1fcca-129">Parse the revocation list, and check for Windows Media DRM revocations.</span></span> <span data-ttu-id="1fcca-130">Дополнительные сведения см. в разделе [Проверка отзыва сертификата](checking-certificate-revocation.md).</span><span class="sxs-lookup"><span data-stu-id="1fcca-130">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
6.  <span data-ttu-id="1fcca-131">При наличии любых отзывов Windows Media DRM:</span><span class="sxs-lookup"><span data-stu-id="1fcca-131">If there are any Windows Media DRM revocations:</span></span>
    1.  <span data-ttu-id="1fcca-132">Создайте модуль включения содержимого для обновления отозванных компонентов, вызвав метод [**ивмдрмсекурити:: жетконтентенаблерсфорревокатионс**](iwmdrmsecurity-getcontentenablersforrevocations.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcca-132">Create a content enabler to renew the revoked components by calling the [**IWMDRMSecurity::GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) method.</span></span>
    2.  <span data-ttu-id="1fcca-133">Вызовите **имфконтентенаблер:: аутоматиценабле** , который направляет пользователя на URL-адрес, содержащий сведения об обновлении компонентов.</span><span class="sxs-lookup"><span data-stu-id="1fcca-133">Call **IMFContentEnabler::AutomaticEnable** which directs the user to a URL that contains component renewal information.</span></span> <span data-ttu-id="1fcca-134">Этот метод описан в [пакете SDK для Media Foundation](../medfound/microsoft-media-foundation-sdk.md) ( https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="1fcca-134">This method is documented in the [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) (https://msdn.microsoft.com/library/ms694197(VS.85).aspx).</span></span>
        > [!Note]  
        > <span data-ttu-id="1fcca-135">Необходимо уточнить этот процесс для пользователя с помощью заявления о конфиденциальности, так как процесс обновления отправляет данные с клиентского компьютера на веб-сайт корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1fcca-135">You must clarify this process to the user through the use of a privacy statement because the update process sends information from the client computer to a Microsoft Web site.</span></span>

         

    3.  <span data-ttu-id="1fcca-136">Если это возможно, пользователь обновит компонент по URL-адресу либо автоматически, либо с помощью указанных инструкций.</span><span class="sxs-lookup"><span data-stu-id="1fcca-136">If possible, the user will renew the component from the URL, either automatically or by following specific instructions.</span></span> <span data-ttu-id="1fcca-137">В некоторых ситуациях компонент не может быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="1fcca-137">There will be some situations in which the component cannot be renewed.</span></span>
    4.  <span data-ttu-id="1fcca-138">Попробуйте получить доступ к содержимому еще раз, пока не будут отменены никакие повторы, или процесс будет остановлен по какой-либо причине.</span><span class="sxs-lookup"><span data-stu-id="1fcca-138">Try to access the content again until there are no more revocations, or the process is halted for some reason.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fcca-139">См. также</span><span class="sxs-lookup"><span data-stu-id="1fcca-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fcca-140">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="1fcca-140">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 