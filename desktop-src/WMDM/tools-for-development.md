---
title: Средства для разработки
description: Средства для разработки
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Диспетчер устройств Windows Media, средства разработки
- Диспетчер устройств, средства разработки
- Диспетчер устройств Windows Media, сертификаты
- Диспетчер устройств, сертификаты
- Диспетчер устройств Windows Media, ключи
- Диспетчер устройств, ключи
- Диспетчер устройств Windows Media, библиотеки
- Диспетчер устройств, библиотеки
- Windows Media диспетчер устройств, пакет средств разработки программного обеспечения (SDK)
- Диспетчер устройств, пакет средств разработки программного обеспечения (SDK)
- Windows Media диспетчер устройств SDK
- Пакет SDK для диспетчер устройств
- Пакет SDK для проигрывателя Windows Media
- Пакет SDK для формата Windows Media
- Пакет SDK для диспетчера прав Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "105691700"
---
# <a name="tools-for-development"></a><span data-ttu-id="e1667-118">Средства для разработки</span><span class="sxs-lookup"><span data-stu-id="e1667-118">Tools for Development</span></span>

<span data-ttu-id="e1667-119">В этом разделе описываются различные сертификаты и ключи, библиотеки и пакеты SDK, которые потребуется программировать с помощью Windows Media диспетчер устройств SDK.</span><span class="sxs-lookup"><span data-stu-id="e1667-119">This section describes the various certificates and keys, libraries, and SDKs you will need to program using the Windows Media Device Manager SDK.</span></span>

<span data-ttu-id="e1667-120">Сертификаты и ключи</span><span class="sxs-lookup"><span data-stu-id="e1667-120">Certificates and Keys</span></span>

<span data-ttu-id="e1667-121">Пакет Windows Media диспетчер устройств SDK поставляется с парой тестовых ключей и сертификатов (в файле Key. c), которая может использоваться приложением или поставщиком услуг для использования методов диспетчер устройств Windows Media в незащищенном содержимом.</span><span class="sxs-lookup"><span data-stu-id="e1667-121">The Windows Media Device Manager SDK ships with a test key/certificate pair (in the key.c file) that can be used by an application or a service provider to use Windows Media Device Manager methods on unprotected content.</span></span> <span data-ttu-id="e1667-122">Эта пара ключей и сертификатов позволяет приложению или поставщику служб использовать большинство функциональных возможностей Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="e1667-122">This key/certificate pair allows the application or service provider to use most of the Windows Media Device Manager functionality.</span></span>

<span data-ttu-id="e1667-123">Однако для разработки приложения или поставщика услуг, которые могут работать с содержимым, защищенным с помощью DRM, необходимо запросить один или несколько сертификатов (каждый с ключом) на [странице лицензирования Windows Media](https://www.microsoft.com/licensing/default).</span><span class="sxs-lookup"><span data-stu-id="e1667-123">However, to develop an application or service provider that can handle DRM-protected content, you must request one or more certificates (each with a key) from the [Windows Media Licensing Page](https://www.microsoft.com/licensing/default).</span></span> <span data-ttu-id="e1667-124">Сертификаты необходимы для следующих приложений или объектов:</span><span class="sxs-lookup"><span data-stu-id="e1667-124">Certificates are required for the following applications or objects:</span></span>

-   <span data-ttu-id="e1667-125">Поставщики услуг, которые управляют содержимым, защищенным с помощью DRM, нуждаются в сертификате поставщика службы Windows Media диспетчер устройств (и ключе).</span><span class="sxs-lookup"><span data-stu-id="e1667-125">Service Providers that handle DRM-protected content require a Windows Media Device Manager Service Provider Certificate (and key)</span></span>
-   <span data-ttu-id="e1667-126">Приложениям, которые передают содержимое, защищенное с помощью DRM, требуется сертификат передачи диспетчер устройств Windows Media (и ключ)</span><span class="sxs-lookup"><span data-stu-id="e1667-126">Applications that transfer DRM-protected content require a Windows Media Device Manager Transfer Certificate (and key)</span></span>
-   <span data-ttu-id="e1667-127">Приложениям, которые воспроизводят содержимое, защищенное с помощью DRM, требуется сертификат DRM (и ключ).</span><span class="sxs-lookup"><span data-stu-id="e1667-127">Applications that play DRM-protected content require a DRM Certificate (and key).</span></span>
-   <span data-ttu-id="e1667-128">Для компонентов контроля использования лицензий требуется сертификат отслеживания использования.</span><span class="sxs-lookup"><span data-stu-id="e1667-128">License metering components require a metering certificate.</span></span> <span data-ttu-id="e1667-129">Это обеспечивается службой контроля использования лицензий, созданной на основе пакета SDK Windows Media Rights Manager, который можно запросить на странице лицензирования Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e1667-129">This is provided by a license metering service built on the Windows Media Rights Manager SDK, which can be requested on the Windows Media Licensing Page.</span></span>

<span data-ttu-id="e1667-130">Библиотеки и заголовки</span><span class="sxs-lookup"><span data-stu-id="e1667-130">Libraries and Headers</span></span>

<span data-ttu-id="e1667-131">Помимо библиотек и заголовков, упомянутых в [обязательных файлах библиотек и заголовков для приложения](required-library-and-header-files-for-an-application.md) или [обязательных библиотек и заголовков для поставщика услуг](required-libraries-and-headers-for-a-service-provider.md), любое приложение или подключаемый модуль, которые ранее были связаны с вмдрмсдк. lib для вызова функций пакета SDK Windows Media Format, теперь должны ссылаться на вмдрмсдкстуб. lib.</span><span class="sxs-lookup"><span data-stu-id="e1667-131">In addition to the libraries and headers mentioned in [Required Library and Header Files for an Application](required-library-and-header-files-for-an-application.md) or [Required Libraries and Headers for a Service Provider](required-libraries-and-headers-for-a-service-provider.md), any application or plug-in that formerly linked to WMDRMSDK.lib to call Windows Media Format SDK functions should now instead link to WMDRMSDKStub.Lib.</span></span> <span data-ttu-id="e1667-132">Этот файл библиотеки используется для доступа к файлам, защищенным с использованием DRM.</span><span class="sxs-lookup"><span data-stu-id="e1667-132">This library file is used to access DRM-protected files.</span></span> <span data-ttu-id="e1667-133">Вы также можете запросить эту библиотеку на странице лицензирования Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e1667-133">You can request this library from the Windows Media Licensing Page as well.</span></span>

<span data-ttu-id="e1667-134">Связанные пакеты SDK</span><span class="sxs-lookup"><span data-stu-id="e1667-134">Related SDKs</span></span>

<span data-ttu-id="e1667-135">Следующие пакеты SDK для Microsoft содержат элементы, которые могут потребоваться при проектировании решений для переносных устройств мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e1667-135">The following Microsoft SDKs provide elements you may need in designing solutions for portable media devices.</span></span>



| <span data-ttu-id="e1667-136">Требуется пакет SDK</span><span class="sxs-lookup"><span data-stu-id="e1667-136">SDK Required</span></span>                     | <span data-ttu-id="e1667-137">Требуется для...</span><span class="sxs-lookup"><span data-stu-id="e1667-137">Required for...</span></span>                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1667-138">Windows Media диспетчер устройств SDK</span><span class="sxs-lookup"><span data-stu-id="e1667-138">Windows Media Device Manager SDK</span></span> | <span data-ttu-id="e1667-139">Классические приложения проигрывателя мультимедиа, взаимодействующие с портативными устройствами</span><span class="sxs-lookup"><span data-stu-id="e1667-139">Desktop media player applications that communicate with portable devices</span></span><br/> <span data-ttu-id="e1667-140">Классические приложения, которые могут обмениваться файлами или информацией с портативными устройствами</span><span class="sxs-lookup"><span data-stu-id="e1667-140">Desktop applications that can exchange files or information with portable devices</span></span><br/> <span data-ttu-id="e1667-141">COM-объекты измерения проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="e1667-141">Windows Media Player metering COM objects</span></span><br/> |
| <span data-ttu-id="e1667-142">Пакет SDK для проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="e1667-142">Windows Media Player SDK</span></span>         | <span data-ttu-id="e1667-143">Подключаемые модули проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="e1667-143">Windows Media Player plug-ins</span></span><br/> <span data-ttu-id="e1667-144">COM-объекты измерения проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="e1667-144">Windows Media Player metering COM objects</span></span><br/> <span data-ttu-id="e1667-145">Обложки проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="e1667-145">Windows Media Player skins</span></span><br/>                                                                                                   |
| <span data-ttu-id="e1667-146">Пакет SDK для формата Windows Media</span><span class="sxs-lookup"><span data-stu-id="e1667-146">Windows Media Format SDK</span></span>         | <span data-ttu-id="e1667-147">Звуковые или видеопроигрыватели, которые могут создавать или воспроизводить файлы (особенно файлы ASF)</span><span class="sxs-lookup"><span data-stu-id="e1667-147">Audio or video players that can create or play files (particularly ASF files)</span></span><br/> <span data-ttu-id="e1667-148">Приложения для редактирования аудио или видео</span><span class="sxs-lookup"><span data-stu-id="e1667-148">Audio or video editing applications</span></span><br/>                                                                                               |
| <span data-ttu-id="e1667-149">Пакет SDK для диспетчера прав Windows Media</span><span class="sxs-lookup"><span data-stu-id="e1667-149">Windows Media Rights Manager SDK</span></span> | <span data-ttu-id="e1667-150">Приложения или подключаемые модули, которые воспроизводят счетчики на рабочем столе или устройстве.</span><span class="sxs-lookup"><span data-stu-id="e1667-150">Applications or plug-ins that meter play counts on the desktop or device.</span></span>                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="e1667-151">См. также</span><span class="sxs-lookup"><span data-stu-id="e1667-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1667-152">**начало работы**</span><span class="sxs-lookup"><span data-stu-id="e1667-152">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 





