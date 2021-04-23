---
title: Добавление субтитров к цифровым носителям
description: Добавление субтитров к цифровым носителям
ms.assetid: 0fdd2cdc-32d4-4fda-9596-b050107abd5f
keywords:
- Проигрыватель Windows Media, синхронизированный доступный медиа-обмен (SAMI)
- Объектная модель проигрывателя Windows Media, синхронизированный доступный обмен мультимедийными данными (SAMI)
- Объектная модель, синхронизированный доступный медиа-обмен (SAMI)
- Проигрыватель Windows Media Mobile, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX, синхронизированный доступный медиа-обмен (SAMI)
- Синхронизированный доступный мультимедийный обмен (SAMI), сведения
- SAMI (синхронизированный доступный медиа-обмен), сведения
- Проигрыватель Windows Media, Добавление закрытых субтитров
- Объектная модель проигрывателя Windows Media, Добавление закрытых субтитров
- Объектная модель, Добавление закрытых субтитров
- Проигрыватель Windows Media Mobile, Добавление закрытых субтитров
- Элемент управления ActiveX проигрывателя Windows Media, Добавление закрытых субтитров
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, Добавление закрытых субтитров
- Элемент управления ActiveX, Добавление закрытых субтитров
- Синхронизированный доступный медиа-обмен (SAMI), Добавление закрытых субтитров
- SAMI (синхронизированный доступный медиа-обмен), Добавление закрытых субтитров
- Добавление закрытых субтитров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc464fb879df1c7642cd0a04b319383654bae4aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067646"
---
# <a name="adding-closed-captions-to-digital-media"></a><span data-ttu-id="218c8-122">Добавление субтитров к цифровым носителям</span><span class="sxs-lookup"><span data-stu-id="218c8-122">Adding Closed Captions to Digital Media</span></span>

<span data-ttu-id="218c8-123">Синхронизированный доступный медиа-обмен (SAMI) — это формат файла, предназначенный для предоставления синхронизированного текста, такого как субтитры, субтитры или аудио описания, с цифровым содержимым мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="218c8-123">Synchronized Accessible Media Interchange (SAMI) is a file format designed to deliver synchronized text such as captions, subtitles, or audio descriptions with digital media content.</span></span> <span data-ttu-id="218c8-124">В веб-браузере, использующем объектную модель проигрывателя Windows Media, SAMId способствует специальным возможностям.</span><span class="sxs-lookup"><span data-stu-id="218c8-124">Integrated in a Web browser using the Windows Media Player object model, SAMI promotes accessibility.</span></span> <span data-ttu-id="218c8-125">С помощью SAMI можно создавать мультимедийное содержимое, которое достигает более широкой аудитории.</span><span class="sxs-lookup"><span data-stu-id="218c8-125">By using SAMI, you can create rich media content that reaches a larger, more diverse audience.</span></span>

<span data-ttu-id="218c8-126">В дополнение к стандартным шрифтам саамский SAMId может поддерживать другие стили текста, например различные цвета, размеры или языки, чтобы помочь различным пользователям.</span><span class="sxs-lookup"><span data-stu-id="218c8-126">In addition to standard fonts, SAMI can support other text styles, such as different colors, sizes, or languages to aid a variety of users.</span></span> <span data-ttu-id="218c8-127">Саамский может быть особенно полезным для тех, кто имеет низкую концепцию или слуха.</span><span class="sxs-lookup"><span data-stu-id="218c8-127">SAMI can be particularly useful for individuals who have low vision or those who are deaf or hard-of-hearing.</span></span> <span data-ttu-id="218c8-128">Формат SAMI также может помочь в учебных целях, таких как обучение учащихся на втором языке.</span><span class="sxs-lookup"><span data-stu-id="218c8-128">The SAMI format can also assist in educational purposes, such as teaching students a second language.</span></span>

<span data-ttu-id="218c8-129">Эта статья посвящена использованию SAMId с объектной моделью элемента управления ActiveX проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="218c8-129">This topic focuses on the incorporation of SAMI with the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="218c8-130">Файлы SAMIs существуют независимо от цифровых файлов мультимедиа и не зависят от конкретного видео или звукового формата для работы.</span><span class="sxs-lookup"><span data-stu-id="218c8-130">SAMI files exist independently from digital media files and do not rely on a specific video or audio format to function.</span></span> <span data-ttu-id="218c8-131">Поскольку файлы являются отдельными, элемент управления проигрывателя Windows Media обнаружит, проанализирует, синхронизирует и готовит каждый файл на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="218c8-131">Since the files are separate, the Windows Media Player control will locate, parse, synchronize, and render each file on the client's computer.</span></span> <span data-ttu-id="218c8-132">Это обеспечивает дополнительную гибкость и функциональность, поскольку позволяет редактировать отдельные файлы SAMI, выдает файл SAMI с различными форматами цифрового мультимедиа и хранение файлов SAMI в разных расположениях серверов.</span><span class="sxs-lookup"><span data-stu-id="218c8-132">This provides for added flexibility and functionality because it allows for the editing of individual SAMI files, the incorporation of the SAMI file with different digital media formats, and the storage of SAMI files on different server locations.</span></span>

<span data-ttu-id="218c8-133">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="218c8-133">This topic contains the following sections.</span></span>



| <span data-ttu-id="218c8-134">Section</span><span class="sxs-lookup"><span data-stu-id="218c8-134">Section</span></span>                                                                                                                            | <span data-ttu-id="218c8-135">Описание</span><span class="sxs-lookup"><span data-stu-id="218c8-135">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="218c8-136">О файлах SAMI</span><span class="sxs-lookup"><span data-stu-id="218c8-136">About SAMI Files</span></span>](about-sami-files.md)                                                                                           | <span data-ttu-id="218c8-137">Описывает базовую структуру файлов SAMI.</span><span class="sxs-lookup"><span data-stu-id="218c8-137">Describes the basic structure of SAMI files.</span></span>                                               |
| [<span data-ttu-id="218c8-138">Пример файла SAMI</span><span class="sxs-lookup"><span data-stu-id="218c8-138">SAMI File Example</span></span>](sami-file-example.md)                                                                                         | <span data-ttu-id="218c8-139">Описывает структуру примера файла SAMI.</span><span class="sxs-lookup"><span data-stu-id="218c8-139">Describes the structure of an example SAMI file.</span></span>                                           |
| [<span data-ttu-id="218c8-140">Использование SAMIs с элементом управления проигрывателя Windows Media в браузере</span><span class="sxs-lookup"><span data-stu-id="218c8-140">Using SAMI with the Windows Media Player Control in a Browser</span></span>](using-sami-with-the-windows-media-player-control-in-a-browser.md) | <span data-ttu-id="218c8-141">Описывает использование SAMI в веб-странице с элементом управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="218c8-141">Describes how to use SAMI in a webpage with the Windows Media Player control.</span></span>              |
| [<span data-ttu-id="218c8-142">Об URL-адресах SAMI</span><span class="sxs-lookup"><span data-stu-id="218c8-142">About SAMI URLs</span></span>](about-sami-urls.md)                                                                                             | <span data-ttu-id="218c8-143">Описывает, как с помощью одного URL-адреса можно связать файлы мультимедиа с SAMId.</span><span class="sxs-lookup"><span data-stu-id="218c8-143">Describes how digital media files can be associated with SAMI files by using a single URL.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="218c8-144">См. также</span><span class="sxs-lookup"><span data-stu-id="218c8-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="218c8-145">**Управление проигрывателем**</span><span class="sxs-lookup"><span data-stu-id="218c8-145">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




