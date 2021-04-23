---
title: Обработка защищенного содержимого
description: Обработка защищенного содержимого
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Диспетчер устройств Windows Media, сертификаты
- Диспетчер устройств, сертификаты
- Классические приложения, сертификаты
- поставщики услуг, сертификаты
- рекомендации по программированию, сертификаты
- certificates
- Диспетчер устройств Windows Media, поставщик защищенного содержимого (SCP)
- Диспетчер устройств, поставщик защищенного содержимого (SCP)
- Классические приложения, поставщик защищенного содержимого (SCP)
- поставщики услуг, защищенный поставщик содержимого (SCP)
- программное обеспечение, защищенный поставщик содержимого (SCP)
- Поставщик защищенного содержимого (SCP)
- SCP (поставщик защищенного содержимого)
- Диспетчер устройств Windows Media, содержимое, защищенное с использованием DRM
- Диспетчер устройств, содержимое, защищенное с использованием DRM
- Путеводитель по программированию, содержимое, защищенное с использованием DRM
- Классические приложения, содержимое, защищенное с использованием DRM
- поставщики услуг, содержимое, защищенное с использованием DRM
- Содержимое, защищенное DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410809"
---
# <a name="handling-protected-content"></a><span data-ttu-id="224a6-122">Обработка защищенного содержимого</span><span class="sxs-lookup"><span data-stu-id="224a6-122">Handling Protected Content</span></span>

<span data-ttu-id="224a6-123">При создании приложения или поставщика услуг, который будет использовать содержимое, защищенное с помощью системы управления цифровыми правами (DRM) Windows Media, необходимо иметь пару ключ/сертификат, выданную корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="224a6-123">If you are building an application or service provider that will consume content protected by Windows Media digital rights management (DRM), you must have a key/certificate pair issued by Microsoft.</span></span> <span data-ttu-id="224a6-124">Сведения о том, как получить этот сертификат, см. в разделе [средства для разработки](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="224a6-124">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="224a6-125">Если вы не собираетесь работать с защищенным содержимым, вы можете использовать фиктивный ключ и сертификат, предоставляемые с этим пакетом SDK, в файл с именем KEY. c.</span><span class="sxs-lookup"><span data-stu-id="224a6-125">If you do not intend to handle protected content, you can use the dummy key and certificate provided with this SDK in a file named key.c.</span></span>

<span data-ttu-id="224a6-126">Для любого файла, защищенного с помощью технологии DRM, Windows Media диспетчер устройств требует наличия безопасного поставщика содержимого (SCP) для этого формата файлов.</span><span class="sxs-lookup"><span data-stu-id="224a6-126">For any file that is protected by DRM technology, Windows Media Device Manager requires the presence of a secure content provider (SCP) for that file format.</span></span> <span data-ttu-id="224a6-127">Корпорация Майкрософт предоставляет модуль SCP для файлов WMA и WMV.</span><span class="sxs-lookup"><span data-stu-id="224a6-127">Microsoft provides an SCP module for WMA and WMV files.</span></span> <span data-ttu-id="224a6-128">Если приложение или поставщик услуг будет обрабатывать содержимое другого формата, защищенное с помощью DRM, необходимо предоставить собственный модуль SCP.</span><span class="sxs-lookup"><span data-stu-id="224a6-128">If your application or service provider will be handling DRM-protected content of another format, you must provide your own SCP module.</span></span> <span data-ttu-id="224a6-129">Модуль SCP — это COM-объект, который реализует все [интерфейсы для защиты поставщиков содержимого](interfaces-for-secure-content-providers.md).</span><span class="sxs-lookup"><span data-stu-id="224a6-129">An SCP module is a COM object that implements all the [interfaces for Secure Content Providers](interfaces-for-secure-content-providers.md).</span></span>

<span data-ttu-id="224a6-130">Приложение может отсылать содержимое, защищенное с помощью DRM, на устройства, созданные на основе Windows Media DRM 10 для переносных устройств или с переносом DRM для портативных устройств (ПДДРМ).</span><span class="sxs-lookup"><span data-stu-id="224a6-130">An application can send DRM-protected content to devices built on either Windows Media DRM 10 for Portable Devices, or Portable Device DRM (PDDRM).</span></span> <span data-ttu-id="224a6-131">Однако можно создать только поставщика услуг для устройств, построенных на основе ПДДРМ; нельзя создать поставщик услуг для устройств, созданных на основе Windows Media DRM 10 для переносных устройств.</span><span class="sxs-lookup"><span data-stu-id="224a6-131">However, you can only create a service provider for devices built on PDDRM; you cannot create a service provider for devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="224a6-132">Эти последние устройства могут использовать только поставщик услуг MTP, предоставленный корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="224a6-132">These latter devices can only use the Microsoft-provided MTP service provider.</span></span>

<span data-ttu-id="224a6-133">Устройства, созданные на ПДДРМ, могут поддерживать только лицензии на приобретенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="224a6-133">Devices built on PDDRM can only support licenses for purchased content.</span></span> <span data-ttu-id="224a6-134">Лицензии с условиями срока действия поддерживаются только устройствами, созданными на основе Windows Media DRM 10 для переносных устройств, которые имеют особые требования, такие как безопасное время и индивидуальная защита.</span><span class="sxs-lookup"><span data-stu-id="224a6-134">Licenses that have time-expiration conditions are only supported by devices built on Windows Media DRM 10 for Portable Devices, which have special requirements such as a secure clock and individualization.</span></span> <span data-ttu-id="224a6-135">Пакет SDK для Windows Media DRM 10 для переносных устройств предоставляет подробные сведения о требованиях к устройствам для поддержки технологии версии 10.</span><span class="sxs-lookup"><span data-stu-id="224a6-135">Windows Media DRM 10 for Portable Devices SDK gives details on device requirements to support version 10 technology.</span></span>

<span data-ttu-id="224a6-136">Перед отправкой содержимого DRM на устройство приложение должно проверить несколько вещей:</span><span class="sxs-lookup"><span data-stu-id="224a6-136">Before sending DRM content to the device, an application should verify several things:</span></span>

-   <span data-ttu-id="224a6-137">Устройство поддерживает технологию DRM.</span><span class="sxs-lookup"><span data-stu-id="224a6-137">That the device supports DRM technology.</span></span>
-   <span data-ttu-id="224a6-138">Какая версия поддерживаемой технологии DRM (версия 10 или более ранняя).</span><span class="sxs-lookup"><span data-stu-id="224a6-138">What version of DRM technology it supports (version 10 or earlier).</span></span>
-   <span data-ttu-id="224a6-139">Если устройство построено на базе версии 10, все его компоненты будут обновлены (например, безопасное время и любые индивидуальные требования).</span><span class="sxs-lookup"><span data-stu-id="224a6-139">If the device is built on version 10, that all its components are up to date (such as the secure clock and any individualization requirements).</span></span>

<span data-ttu-id="224a6-140">Все вызовы методов, отвечающие на эти вопросы, выполняются клиентом и обрабатываются Windows Media диспетчер устройств и компонентом поставщика безопасного содержимого; поставщик услуг не обрабатывает ни один из этих вызовов.</span><span class="sxs-lookup"><span data-stu-id="224a6-140">All method calls to answer these questions are made by the client and handled by Windows Media Device Manager and the secure content provider component; the service provider does not handle any of these calls.</span></span>

<span data-ttu-id="224a6-141">Если устройство не поддерживает Windows Media DRM 10 для портативных устройств, оно может по-прежнему иметь возможность использовать защищенное содержимое (в зависимости от лицензии на содержимое и структуры устройства), но любое содержимое, отправленное на него, будет иметь упрощенную лицензию на использование с ограниченными правами (например, без истечения срока действия).</span><span class="sxs-lookup"><span data-stu-id="224a6-141">If the device does not support Windows Media DRM 10 for Portable Devices, it might still be able to consume protected content (depending on the content license and the device design), but any content sent to it will have a simplified use license with limited rights (for example, no time expiration).</span></span>

-   <span data-ttu-id="224a6-142">Примеры, демонстрирующие, как приложение проверяет, может ли устройство обрабатывать защищенное содержимое и требуется ли обновлять его компоненты DRM, см. в разделе [Обработка защищенного содержимого в приложении](handling-protected-content-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="224a6-142">For examples demonstrating how an application verifies whether a device can handle protected content, and whether it needs to update its DRM components, see [Handling Protected Content in the Application](handling-protected-content-in-the-application.md).</span></span>
-   <span data-ttu-id="224a6-143">Дополнительные сведения о создании поставщика услуг, который может обрабатывать защищенное содержимое, см. [в разделе Обработка защищенного содержимого в поставщике услуг](handling-protected-content-in-the-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="224a6-143">For more information about building a service provider that can handle protected content, see [Handling Protected Content in the Service Provider](handling-protected-content-in-the-service-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="224a6-144">Многие диспетчер устройств Windows Media, а также права, запрашивающие методы, будут завершаться сбоем (часто с Mysterious значением **HRESULT** ) при обработке файлов, защищенных с помощью DRM, с подключенным отладчиком.</span><span class="sxs-lookup"><span data-stu-id="224a6-144">Many Windows Media Device Manager file transfer or rights requesting methods will fail (often with a mysterious **HRESULT** value) when handling DRM-protected files with a debugger attached.</span></span> <span data-ttu-id="224a6-145">Таким образом, необходимо использовать альтернативные способы отладки кода, такие как вывод журнала в форму Windows или файл журнала.</span><span class="sxs-lookup"><span data-stu-id="224a6-145">Therefore, you must use alternate ways to debug your code, such as logging outputs to a Windows form or a log file.</span></span> <span data-ttu-id="224a6-146">Дополнительные сведения о параметрах ведения журнала см. в разделе [Включение ведения журнала](enabling-logging.md).</span><span class="sxs-lookup"><span data-stu-id="224a6-146">For more information on logging options, see [Enabling Logging](enabling-logging.md).</span></span> <span data-ttu-id="224a6-147">При запуске отладчика для защищенного содержимого метод возвращает один из кодов ошибок, перечисленных в разделе DRM [коды ошибок](error-codes.md)или, возможно, неизвестный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="224a6-147">If you are running a debugger on protected content, a method will return one of the error codes listed in the DRM section [Error Codes](error-codes.md), or possibly an unknown error code.</span></span> <span data-ttu-id="224a6-148">Если при запуске отладчика в защищенном содержимом или методе вы получаете значения **HRESULT** Mysterious, это может быть вызвано защитой DRM.</span><span class="sxs-lookup"><span data-stu-id="224a6-148">If you get mysterious **HRESULT** values when running a debugger on protected content or methods, DRM protection might be the cause.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="224a6-149">См. также</span><span class="sxs-lookup"><span data-stu-id="224a6-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="224a6-150">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="224a6-150">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




