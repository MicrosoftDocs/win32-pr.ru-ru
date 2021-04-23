---
title: Обработка защищенного содержимого в поставщике услуг
description: Обработка защищенного содержимого в поставщике услуг
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Диспетчер устройств Windows Media, сертификаты
- Диспетчер устройств, сертификаты
- рекомендации по программированию, сертификаты
- поставщики услуг, сертификаты
- Создание поставщиков услуг, сертификаты
- certificates
- Диспетчер устройств Windows Media, содержимое, защищенное с использованием DRM
- Диспетчер устройств, содержимое, защищенное с использованием DRM
- Путеводитель по программированию, содержимое, защищенное с использованием DRM
- поставщики услуг, содержимое, защищенное с использованием DRM
- Создание поставщиков услуг, содержимое, защищенное с использованием DRM
- Содержимое, защищенное DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691178"
---
# <a name="handling-protected-content-in-the-service-provider"></a><span data-ttu-id="fb7a6-115">Обработка защищенного содержимого в поставщике услуг</span><span class="sxs-lookup"><span data-stu-id="fb7a6-115">Handling Protected Content in the Service Provider</span></span>

<span data-ttu-id="fb7a6-116">Вы можете создать поставщик услуг, который может передавать содержимое, защищенное с помощью DRM, на устройство, созданное на основе DRM портативного устройства (ПДДРМ), но нельзя создать поставщик услуг, который может отсылать содержимое, защищенное с помощью DRM, на устройства, созданные на основе Windows Media DRM 10 для портативных устройств.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-116">You can build a service provider that can send DRM-protected content to a device built on Portable Device DRM (PDDRM), but you cannot build a service provider that can send DRM-protected content to devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="fb7a6-117">Эти устройства используют MTP, и вы не можете создать собственный поставщик услуг MTP.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-117">These devices use MTP, and you cannot build your own MTP service provider.</span></span>

<span data-ttu-id="fb7a6-118">Единственным дополнительным шагом, который поставщик услуг должен выполнить для отправки материалов DRM на устройство ПДДРМ, является получение пары «сертификат-ключ», выпущенной корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-118">The only extra step that a service provider must take to send DRM material to a PDDRM device is to get a Microsoft-issued certificate/key pair.</span></span> <span data-ttu-id="fb7a6-119">Сведения о том, где получить этот сертификат или ключ, см. в разделе [средства разработки](tools-for-development.md) .</span><span class="sxs-lookup"><span data-stu-id="fb7a6-119">See [Tools for Development](tools-for-development.md) to learn where to get this certificate/key.</span></span> <span data-ttu-id="fb7a6-120">Лицензии, выданные этим устройствам, будут упрощены, которые поддерживают только простое воспроизведение приобретенного содержимого. они не будут поддерживать лицензии с истечением времени.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-120">The licenses issued to these devices will be simplified licenses that only support simple playback of purchased content; they will not support time-expiring licenses.</span></span> <span data-ttu-id="fb7a6-121">Эта лицензия будет создана поставщиком защищенного содержимого (предоставляемой корпорацией Майкрософт для файлов WMA/WMV) и сохранен в заголовке файла, отправляемого поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-121">This license will be created for you by the secure content provider (provided by Microsoft for WMA/WMV files) and stored in the header of the file sent to the service provider.</span></span> <span data-ttu-id="fb7a6-122">Для защищенных файлов не потребуется предпринимать никаких дополнительных действий.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-122">You will not have to take any special steps for protected files.</span></span>

<span data-ttu-id="fb7a6-123">После отправки защищенного файла Windows Media диспетчер устройств выполнит вызов поставщика услуг, чтобы запросить специальный файл хранилища лицензий на устройстве.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-123">After sending the protected file, Windows Media Device Manager will call the service provider to request a special license storage file from the device.</span></span> <span data-ttu-id="fb7a6-124">Диспетчер устройств Windows Media добавит копию новой лицензии в этот файл и вернет ее поставщику услуг для отправки обратно на устройство.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-124">Windows Media Device Manager will add a copy of the new license to this file, and return it to the service provider to send back to the device.</span></span> <span data-ttu-id="fb7a6-125">Однако даже если поставщик услуг не смог найти или вернуть этот файл, устройство по-прежнему сможет воспроизвести защищенный файл, используя копию лицензии в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-125">However, even if the service provider fails to find or return this file, the device should still be able to play the protected file by using the license copy in the file header.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb7a6-126">См. также</span><span class="sxs-lookup"><span data-stu-id="fb7a6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb7a6-127">**Создание поставщика услуг**</span><span class="sxs-lookup"><span data-stu-id="fb7a6-127">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="fb7a6-128">**Обработка защищенного содержимого**</span><span class="sxs-lookup"><span data-stu-id="fb7a6-128">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 




