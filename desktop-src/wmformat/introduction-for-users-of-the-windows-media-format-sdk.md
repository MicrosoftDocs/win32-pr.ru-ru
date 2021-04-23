---
title: Общие сведения о пользователях пакета SDK Windows Media Format
description: Общие сведения о пользователях пакета SDK Windows Media Format
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows Media Format SDK, расширенные API клиента DRM
- Пакет SDK для Windows Media Format, расширенные API клиента
- Windows Media Format SDK, расширенные API
- Windows Media Format SDK, API
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Управление цифровыми правами (DRM), расширенные API клиента
- DRM (Управление цифровыми правами), расширенные API клиента
- Управление цифровыми правами (DRM), расширенные API
- DRM (Управление цифровыми правами), расширенные API
- Управление цифровыми правами (DRM), API
- DRM (Управление цифровыми правами), API
- Расширенные API клиента DRM, о
- Расширенные API клиента, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410995"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a><span data-ttu-id="09af9-116">Общие сведения о пользователях пакета SDK Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="09af9-116">Introduction for Users of the Windows Media Format SDK</span></span>

<span data-ttu-id="09af9-117">Большая часть функциональных возможностей, обеспечиваемых расширенными API клиента DRM Windows Media, аналогична функциональным возможностям, предоставляемым объектами пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="09af9-117">Much of the functionality provided by the Windows Media DRM Client Extended APIs is the same as the functionality provided by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="09af9-118">Пакет Windows Media Format SDK предоставляет разработчикам объекты, необходимые для создания, доступа и управления файлами мультимедиа, использующими структуру файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="09af9-118">The Windows Media Format SDK provides developers with the objects needed to create, access, and manipulate media files that use the Advanced Systems Format (ASF) file structure.</span></span> <span data-ttu-id="09af9-119">Так как Windows Media DRM предназначена для защиты файлов ASF, клиентские функции DRM были добавлены в пакет SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="09af9-119">Because Windows Media DRM is intended to protect ASF files, client-side DRM functionality was included in the Windows Media Format SDK.</span></span>

<span data-ttu-id="09af9-120">Расширенные API клиента Windows Media DRM выпускаются совместно с платформой цифрового мультимедиа следующего поколения Майкрософт, Microsoft Media Foundationным пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="09af9-120">The Windows Media DRM Client Extended APIs are being released in conjunction with Microsoft's next-generation digital media platform, the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="09af9-121">Media Foundation будет включать функции ASF, которые перекрывают некоторые функции пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="09af9-121">Media Foundation will include ASF functionality that overlaps some of the features of the Windows Media Format SDK.</span></span> <span data-ttu-id="09af9-122">Поскольку теперь существуют два пакета Microsoft SDK для работы с файлами ASF, функциональность DRM на стороне клиента отделяется от Windows Media Format SDK до расширенных API клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="09af9-122">Because there are now two Microsoft SDKs that manipulate ASF files, the client-side DRM functionality is being separated from the Windows Media Format SDK into the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="09af9-123">Доступ к этим API можно получить у пользователей Windows Media Format SDK и Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="09af9-123">These APIs can be accessed by users of both the Windows Media Format SDK and the Media Foundation SDK.</span></span> <span data-ttu-id="09af9-124">В настоящее время эти API-интерфейсы входят в состав установочного пакета пакета SDK Windows Media Format и задокументированы в пакете Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="09af9-124">At present, these APIs are included as part of the Windows Media Format SDK installation package and are documented as part of the Windows Media Format SDK.</span></span> <span data-ttu-id="09af9-125">Однако расширенные API клиента DRM Windows Media реализуются в собственной библиотеке и имеют собственный файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="09af9-125">However, the Windows Media DRM Client Extended APIs are implemented in their own library and have their own header file.</span></span> <span data-ttu-id="09af9-126">После установки пакета SDK для формата Windows Media эти API можно использовать самостоятельно, не включая заголовки или библиотеки пакета SDK Windows Media Format в приложение.</span><span class="sxs-lookup"><span data-stu-id="09af9-126">After installing the Windows Media Format SDK, these APIs can be used one their own, without including any Windows Media Format SDK headers or libraries in your application.</span></span>

<span data-ttu-id="09af9-127">При разработке приложений, использующих пакет SDK для формата Windows Media, необходимо решить, использовать ли функциональные возможности DRM, предоставляемые пакетом SDK, или использовать расширенные API клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="09af9-127">If you develop applications that use the Windows Media Format SDK you must decide whether to use the DRM functionality that SDK provides, or to use the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="09af9-128">Хотя многие функции этих двух пакетов SDK очень похожи, расширенные API клиента DRM Windows Media предлагают следующие функции, недоступные пользователям старых подпрограмм DRM:</span><span class="sxs-lookup"><span data-stu-id="09af9-128">While many of the features of these two SDKs are very similar, the Windows Media DRM Client Extended APIs offer the following features not available to users of the older DRM routines:</span></span>

-   <span data-ttu-id="09af9-129">Возможность импортировать содержимое, защищенное сторонней системой управления правами.</span><span class="sxs-lookup"><span data-stu-id="09af9-129">Ability to import content protected by a third-party rights management system.</span></span>
-   <span data-ttu-id="09af9-130">Возможность экспорта содержимого, защищенного Windows Media DRM, в систему управления правами сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="09af9-130">Ability to export content protected by Windows Media DRM to a third-party rights management system.</span></span>
-   <span data-ttu-id="09af9-131">Прямое перечисление лицензий в хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="09af9-131">Direct enumeration of licenses in the license store.</span></span>
-   <span data-ttu-id="09af9-132">Простой запрос агрегированных прав на основе идентификатора ключа (нет необходимости загружать файл мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="09af9-132">Simple, aggregated rights querying based on key ID (no need to load the media file).</span></span>
-   <span data-ttu-id="09af9-133">Возможность продлить отозванные компоненты с помощью стандартного интерфейса Media Foundation **имфконтентенаблер**.</span><span class="sxs-lookup"><span data-stu-id="09af9-133">Ability to renew revoked components by using the standard Media Foundation interface, **IMFContentEnabler**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09af9-134">См. также</span><span class="sxs-lookup"><span data-stu-id="09af9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09af9-135">**О расширенных API-интерфейсах клиента DRM Windows Media**</span><span class="sxs-lookup"><span data-stu-id="09af9-135">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




