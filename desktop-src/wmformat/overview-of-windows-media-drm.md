---
title: Обзор Windows Media DRM
description: Обзор Windows Media DRM
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Windows Media Format SDK, лицензии DRM
- Пакет SDK для Windows Media Format, лицензии для DRM
- Управление цифровыми правами (DRM), о
- DRM (Управление цифровыми правами), о программе
- Управление цифровыми правами (DRM), Упаковка файлов Windows Media
- DRM (Управление цифровыми правами), Упаковка файлов Windows Media
- Управление цифровыми правами (DRM), лицензирование защищенных файлов
- DRM (Управление цифровыми правами), лицензирование защищенных файлов
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Управление цифровыми правами (DRM), чтение защищенных файлов
- DRM (Управление цифровыми правами), чтение защищенных файлов
- Расширенный формат систем (ASF), управление цифровыми правами (DRM)
- ASF (Расширенный системный формат), управление цифровыми правами (DRM)
- лицензии, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700485"
---
# <a name="overview-of-windows-media-drm"></a><span data-ttu-id="c0018-119">Обзор Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="c0018-119">Overview of Windows Media DRM</span></span>

<span data-ttu-id="c0018-120">Windows Media Digital Rights Management (DRM) — это система защиты содержимого файлов Windows Media, чтобы неавторизованные пользователи не могли получить к ним доступ.</span><span class="sxs-lookup"><span data-stu-id="c0018-120">Windows Media Digital Rights Management (DRM) is a system for protecting the content in Windows Media files so that unauthorized users cannot access it.</span></span> <span data-ttu-id="c0018-121">Базовый цикл DRM состоит из трех этапов: Упаковка, лицензирование и чтение.</span><span class="sxs-lookup"><span data-stu-id="c0018-121">There are three phases to the basic DRM cycle: packaging, licensing, and reading.</span></span>

## <a name="packaging-windows-media-files"></a><span data-ttu-id="c0018-122">Упаковка файлов Windows Media</span><span class="sxs-lookup"><span data-stu-id="c0018-122">Packaging Windows Media Files</span></span>

<span data-ttu-id="c0018-123">Windows Media DRM предназначена для работы с файлами Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c0018-123">Windows Media DRM is designed to work with Windows Media files.</span></span> <span data-ttu-id="c0018-124">Файл Windows Media представляет собой файл, который соответствует спецификации ASF и содержит только аудио-и видеоматериалы, которые были сжаты с помощью аудиокодеков Windows Media Audio и Video.</span><span class="sxs-lookup"><span data-stu-id="c0018-124">A Windows Media file is a file that conforms to the Advanced Systems Format (ASF) specification and only contains Audio and Video that has been compressed by using the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="c0018-125">При упаковке ASF-файла в заголовок добавляется раздел, относящийся к DRM.</span><span class="sxs-lookup"><span data-stu-id="c0018-125">When an ASF file is packaged, a DRM-specific section is added to the header.</span></span> <span data-ttu-id="c0018-126">Заголовок DRM содержит идентификатор ключа, который определяет содержимое в целях лицензирования, и URL-адрес для получения лицензии, который является адресом веб-страницы, которая может выдавать лицензии на чтение защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="c0018-126">The DRM header contains a Key ID, which identifies the content for the purposes of licensing, and a license acquisition URL, which is the address of a Web page that can issue licenses to read the protected content.</span></span> <span data-ttu-id="c0018-127">Существует гораздо больше информации, которую можно разместить в заголовке DRM, но это необязательно.</span><span class="sxs-lookup"><span data-stu-id="c0018-127">There is much more information that can be put in the DRM header, but it is optional.</span></span> <span data-ttu-id="c0018-128">Заголовок DRM подписывается, чтобы можно было проверить упаковщик.</span><span class="sxs-lookup"><span data-stu-id="c0018-128">The DRM header is signed so that the packager can be verified.</span></span>

<span data-ttu-id="c0018-129">Содержимое в ASF-файле шифруется во время процесса упаковки.</span><span class="sxs-lookup"><span data-stu-id="c0018-129">The content in the ASF file is encrypted during the packing process.</span></span> <span data-ttu-id="c0018-130">Однако следующие сведения в упакованном файле доступны даже клиентам, у которых нет лицензии.</span><span class="sxs-lookup"><span data-stu-id="c0018-130">However, the following information in the packaged file is available even to clients that do not have a license:</span></span>

-   <span data-ttu-id="c0018-131">Метаданные, хранящиеся в заголовке ASF.</span><span class="sxs-lookup"><span data-stu-id="c0018-131">Metadata that is stored in the ASF header.</span></span>
-   <span data-ttu-id="c0018-132">Некоторые метаданные, которые хранятся в заголовке DRM (например, всегда можно получить URL-адрес для приобретения лицензии).</span><span class="sxs-lookup"><span data-stu-id="c0018-132">Some metadata that is stored in the DRM header (for example, you can always get the license acquisition URL).</span></span>

## <a name="licensing-protected-files"></a><span data-ttu-id="c0018-133">Лицензированные защищенные файлы</span><span class="sxs-lookup"><span data-stu-id="c0018-133">Licensing Protected Files</span></span>

<span data-ttu-id="c0018-134">Для чтения упакованного файла на клиентский компьютер должна быть выдана лицензия.</span><span class="sxs-lookup"><span data-stu-id="c0018-134">For a packaged file to be read, a license must be issued to the client computer.</span></span> <span data-ttu-id="c0018-135">Лицензия — это набор данных, описывающих условия, при которых данные в защищенных файлах могут быть прочитаны.</span><span class="sxs-lookup"><span data-stu-id="c0018-135">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="c0018-136">Чаще всего для защищенного файла выдается лицензия в ответ на попытку пользователя выполнить какую-либо операцию над файлом.</span><span class="sxs-lookup"><span data-stu-id="c0018-136">Most often, a license is issued for a protected file in response to the user trying to perform some operation on the file.</span></span> <span data-ttu-id="c0018-137">Однако также возможно, что поставщик лицензий доставляет лицензии клиенту, прежде чем он будет явно запрошен.</span><span class="sxs-lookup"><span data-stu-id="c0018-137">It is also possible, however, for a license issuer to deliver licenses to a client before it is explicitly requested.</span></span> <span data-ttu-id="c0018-138">Дополнительные сведения о лицензиях см. в разделе [лицензии](licenses.md).</span><span class="sxs-lookup"><span data-stu-id="c0018-138">For more information about licenses, see [Licenses](licenses.md).</span></span>

## <a name="reading-data-from-protected-files"></a><span data-ttu-id="c0018-139">Чтение данных из защищенных файлов</span><span class="sxs-lookup"><span data-stu-id="c0018-139">Reading Data from Protected Files</span></span>

<span data-ttu-id="c0018-140">Когда пользователь пытается выполнить операцию с защищенным файлом (воспроизведение, запись на компакт-диск, копирование на устройство и т. д.), приложение должно проверить наличие лицензий на содержимое на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="c0018-140">When a user tries to perform an operation on a protected file (play, burn to CD, copy to a device, and so on), the application must check for licenses for the content on the client computer.</span></span> <span data-ttu-id="c0018-141">Если на клиентском компьютере существует действительная лицензия, операция может быть продолжена.</span><span class="sxs-lookup"><span data-stu-id="c0018-141">If a valid license exists on the client computer, the operation can proceed.</span></span> <span data-ttu-id="c0018-142">Если у вас нет лицензии на содержимое или если лицензия на содержимое, установленная на клиентском компьютере, не позволяет выполнить запрошенное действие, необходимо получить лицензию.</span><span class="sxs-lookup"><span data-stu-id="c0018-142">If there isn't a license for the content, or if no license for the content that is on the client computer allows the requested action, then a license must be acquired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0018-143">См. также</span><span class="sxs-lookup"><span data-stu-id="c0018-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0018-144">**О расширенных API-интерфейсах клиента DRM Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c0018-144">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




