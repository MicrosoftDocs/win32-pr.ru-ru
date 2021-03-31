---
title: Экспорт DRM
description: Экспорт DRM
ms.assetid: 0b44f2e5-e63c-4bdb-8123-097a5d5e3756
keywords:
- Windows Media Format SDK, расширенные API клиента DRM
- Пакет SDK для Windows Media Format, расширенные API клиента
- Windows Media Format SDK, расширенные API
- Windows Media Format SDK, API
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Windows Media Format SDK, экспорт DRM
- Пакет Windows Media Format SDK, экспорт
- Управление цифровыми правами (DRM), расширенные API клиента
- DRM (Управление цифровыми правами), расширенные API клиента
- Управление цифровыми правами (DRM), расширенные API
- DRM (Управление цифровыми правами), расширенные API
- Управление цифровыми правами (DRM), API
- DRM (Управление цифровыми правами), API
- Управление цифровыми правами (DRM), экспорт
- DRM (Управление цифровыми правами), экспорт
- Расширенные API клиента DRM, экспорт
- Расширенные API клиента, экспорт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2917cfd0c9042f4547540618b44ed4c2f324edb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330264"
---
# <a name="drm-export"></a><span data-ttu-id="a47f3-120">Экспорт DRM</span><span class="sxs-lookup"><span data-stu-id="a47f3-120">DRM Export</span></span>

<span data-ttu-id="a47f3-121">Функция экспорта DRM в Windows Media позволяет создавать лицензированные приложения, которые расшифровывать содержимое, защищенное с помощью Windows Media DRM, и повторно зашифровать в выходной схеме защиты содержимого (CPS), явно указанной соответствующим издателем лицензии.</span><span class="sxs-lookup"><span data-stu-id="a47f3-121">Windows Media DRM export functionality enables you to create licensed applications that decrypt content protected by Windows Media DRM, and re-encrypt in an output content protection scheme (CPS) explicitly specified by the associated license issuer.</span></span> <span data-ttu-id="a47f3-122">Издатель лицензии явно разрешает экспорт содержимого в конкретный CPS с помощью списка включения.</span><span class="sxs-lookup"><span data-stu-id="a47f3-122">The license issuer explicitly authorizes the export of content to a specific CPS through an inclusion list.</span></span>

> [!Note]  
> <span data-ttu-id="a47f3-123">Чтобы получить доступ к функциям экспорта, необходимо применить к [сертификату приложения для экспорта](export-application-certificate.md) из корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a47f3-123">To access export functionality, you must apply for an [Export Application Certificate](export-application-certificate.md) from Microsoft.</span></span>

 

<span data-ttu-id="a47f3-124">Функции экспорта DRM в Windows Media описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="a47f3-124">Windows Media DRM export functionality is explained in the following sections.</span></span>



| <span data-ttu-id="a47f3-125">Section</span><span class="sxs-lookup"><span data-stu-id="a47f3-125">Section</span></span>                                                                                      | <span data-ttu-id="a47f3-126">Описание</span><span class="sxs-lookup"><span data-stu-id="a47f3-126">Description</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a47f3-127">Экспорт сертификата приложения</span><span class="sxs-lookup"><span data-stu-id="a47f3-127">Export Application Certificate</span></span>](export-application-certificate.md)                         | <span data-ttu-id="a47f3-128">Описывает сертификат приложения экспорта.</span><span class="sxs-lookup"><span data-stu-id="a47f3-128">Describes an export application certificate.</span></span>                                                        |
| [<span data-ttu-id="a47f3-129">Явные списки авторизации и включений</span><span class="sxs-lookup"><span data-stu-id="a47f3-129">Explicit Authorization and Inclusion Lists</span></span>](explicit-authorization-and-inclusion-lists.md) | <span data-ttu-id="a47f3-130">Описание процесса явной авторизации и работы списков включения.</span><span class="sxs-lookup"><span data-stu-id="a47f3-130">Explains the process of explicit authorization, and how inclusions lists work.</span></span>                      |
| [<span data-ttu-id="a47f3-131">Экспорт сжатого содержимого</span><span class="sxs-lookup"><span data-stu-id="a47f3-131">Exporting Compressed Content</span></span>](exporting-compressed-content.md)                             | <span data-ttu-id="a47f3-132">Описывает, как экспортировать сжатое содержимое из защищенного аудио или видео содержимого Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="a47f3-132">Describes how to export compressed content from Windows Media DRM protected audio or video content.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a47f3-133">См. также</span><span class="sxs-lookup"><span data-stu-id="a47f3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a47f3-134">**Явные списки авторизации и включений**</span><span class="sxs-lookup"><span data-stu-id="a47f3-134">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="a47f3-135">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="a47f3-135">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




