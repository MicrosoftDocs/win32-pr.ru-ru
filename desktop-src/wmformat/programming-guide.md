---
title: Справочное руководством по программированию Windows Media Format SDK
description: Справочное руководством по программированию Windows Media Format SDK
ms.assetid: 9b382c88-e4a9-4aed-a250-250fabface44
keywords:
- Windows Media Format SDK, программное обеспеченное программирование
- Windows Media Format SDK, расширенный формат систем (ASF)
- Расширенный системный формат (ASF), программное обеспеченное программирование
- ASF (Расширенный системный формат), программное обеспеченное программирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4ea4f6819a31693d7c9d149717324ef6dcc65a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105701011"
---
# <a name="windows-media-format-sdk-programming-guide"></a><span data-ttu-id="9236c-107">Справочное руководством по программированию Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="9236c-107">Windows Media Format SDK Programming Guide</span></span>

<span data-ttu-id="9236c-108">Руководство по программированию предназначено для того, чтобы научиться использовать пакет средств разработки программного обеспечения (SDK) Microsoft Windows Media для создания приложений, которые работают с файлами в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="9236c-108">The Programming Guide is intended to help you learn how to use the Microsoft Windows Media Format Software Development Kit (SDK) to build applications that work with files using the Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="9236c-109">С помощью пакета SDK для Windows Media Format можно создавать приложения, которые записывают цифровые мультимедийные потоки в файлы ASF и читают их из них.</span><span class="sxs-lookup"><span data-stu-id="9236c-109">You can use the Windows Media Format SDK to create applications that write digital media streams to and read streams from ASF files.</span></span> <span data-ttu-id="9236c-110">Этот пакет SDK также поддерживает редактирование метаданных в файлах ASF.</span><span class="sxs-lookup"><span data-stu-id="9236c-110">This SDK also supports the editing of metadata in ASF files.</span></span> <span data-ttu-id="9236c-111">Кроме того, этот пакет SDK можно использовать для чтения метаданных и управления ими в MP3-файлах.</span><span class="sxs-lookup"><span data-stu-id="9236c-111">In addition, this SDK can be used to read and manipulate metadata in MP3 files.</span></span>

<span data-ttu-id="9236c-112">В следующих разделах подробно описаны шаги, необходимые для записи, чтения и редактирования файлов ASF с помощью этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="9236c-112">The following sections explain in detail the steps required to write, read, and edit ASF files by using this SDK.</span></span>



| <span data-ttu-id="9236c-113">Section</span><span class="sxs-lookup"><span data-stu-id="9236c-113">Section</span></span>                                                                            | <span data-ttu-id="9236c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9236c-114">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9236c-115">Начало работы</span><span class="sxs-lookup"><span data-stu-id="9236c-115">Getting Started</span></span>](getting-started.md)                                             | <span data-ttu-id="9236c-116">Содержит общие сведения о готовности к использованию этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="9236c-116">Provides general information about getting ready to use this SDK.</span></span>                                                 |
| [<span data-ttu-id="9236c-117">Использование методов обратного вызова</span><span class="sxs-lookup"><span data-stu-id="9236c-117">Using the Callback Methods</span></span>](using-the-callback-methods.md)                       | <span data-ttu-id="9236c-118">Описывает методы обратного вызова, используемые в различных задачах.</span><span class="sxs-lookup"><span data-stu-id="9236c-118">Describes the callback methods used in many different tasks.</span></span>                                                      |
| [<span data-ttu-id="9236c-119">Работа с профилями</span><span class="sxs-lookup"><span data-stu-id="9236c-119">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="9236c-120">Описывает использование, изменение и создание профилей.</span><span class="sxs-lookup"><span data-stu-id="9236c-120">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="9236c-121">Запись файлов ASF</span><span class="sxs-lookup"><span data-stu-id="9236c-121">Writing ASF Files</span></span>](writing-asf-files.md)                                         | <span data-ttu-id="9236c-122">Описывает, как использовать объект модуля записи для создания файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="9236c-122">Describes how to use the writer object to create ASF files.</span></span>                                                       |
| [<span data-ttu-id="9236c-123">Чтение файлов ASF</span><span class="sxs-lookup"><span data-stu-id="9236c-123">Reading ASF Files</span></span>](reading-asf-files.md)                                         | <span data-ttu-id="9236c-124">Описывает, как получить содержимое из файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="9236c-124">Describes how to receive content from ASF files.</span></span>                                                                  |
| [<span data-ttu-id="9236c-125">Работа с метаданными</span><span class="sxs-lookup"><span data-stu-id="9236c-125">Working with Metadata</span></span>](working-with-metadata.md)                                 | <span data-ttu-id="9236c-126">Описывает, как управлять содержимым раздела заголовка файла ASF.</span><span class="sxs-lookup"><span data-stu-id="9236c-126">Describes how to manage the contents of the header section of an ASF file.</span></span>                                        |
| [<span data-ttu-id="9236c-127">Работа с индексами</span><span class="sxs-lookup"><span data-stu-id="9236c-127">Working with Indexes</span></span>](working-with-indexes.md)                                   | <span data-ttu-id="9236c-128">Описывает работу с индексами.</span><span class="sxs-lookup"><span data-stu-id="9236c-128">Describes how to work with indexes.</span></span>                                                                               |
| [<span data-ttu-id="9236c-129">Работа с профилями</span><span class="sxs-lookup"><span data-stu-id="9236c-129">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="9236c-130">Описывает использование, изменение и создание профилей.</span><span class="sxs-lookup"><span data-stu-id="9236c-130">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="9236c-131">Использование команд сценария</span><span class="sxs-lookup"><span data-stu-id="9236c-131">Using Script Commands</span></span>](using-script-commands.md)                                 | <span data-ttu-id="9236c-132">Описание использования команд сценариев в файлах ASF.</span><span class="sxs-lookup"><span data-stu-id="9236c-132">Describes how to use script commands in your ASF files.</span></span>                                                           |
| [<span data-ttu-id="9236c-133">Копирование данных из одного файла в другой</span><span class="sxs-lookup"><span data-stu-id="9236c-133">Copying Data from One File to Another</span></span>](copying-data-from-one-file-to-another.md) | <span data-ttu-id="9236c-134">Описывает копирование данных из одного файла ASF в другой без декодирования и кодирования.</span><span class="sxs-lookup"><span data-stu-id="9236c-134">Describes how to copy data from one ASF file to another, with without decoding and encoding.</span></span>                      |
| [<span data-ttu-id="9236c-135">Включение поддержки DRM</span><span class="sxs-lookup"><span data-stu-id="9236c-135">Enabling DRM Support</span></span>](enabling-drm-support.md)                                   | <span data-ttu-id="9236c-136">Описание включения поддержки воспроизведения файлов ASF, защищенных с помощью DRM.</span><span class="sxs-lookup"><span data-stu-id="9236c-136">Describes how to enable support for playback of DRM-protected ASF files.</span></span>                                          |
| [<span data-ttu-id="9236c-137">Реализация функций сети</span><span class="sxs-lookup"><span data-stu-id="9236c-137">Implementing Network Functionality</span></span>](implementing-network-functionality.md)       | <span data-ttu-id="9236c-138">Описание использования этого пакета SDK для выполнения сетевых операций, необходимых для успешной потоковой передачи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9236c-138">Describes the use of this SDK to perform the network operations that are essential to successful streaming media.</span></span> |
| [<span data-ttu-id="9236c-139">Дополнительные разделы</span><span class="sxs-lookup"><span data-stu-id="9236c-139">Advanced Topics</span></span>](advanced-topics.md)                                             | <span data-ttu-id="9236c-140">Описание использования некоторых дополнительных функций этого пакета SDK в приложениях.</span><span class="sxs-lookup"><span data-stu-id="9236c-140">Describes how to use some of the advanced features of this SDK in your applications.</span></span>                              |
| [<span data-ttu-id="9236c-141">DirectShow и Windows Media</span><span class="sxs-lookup"><span data-stu-id="9236c-141">DirectShow and Windows Media</span></span>](directshow-and-windows-media.md)                   | <span data-ttu-id="9236c-142">Описание использования Microsoft DirectShow для создания и чтения файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="9236c-142">Describes how you can use Microsoft DirectShow to create and read ASF files.</span></span>                                      |
| [<span data-ttu-id="9236c-143">Рекомендации по проекту</span><span class="sxs-lookup"><span data-stu-id="9236c-143">Project Considerations</span></span>](project-considerations.md)                               | <span data-ttu-id="9236c-144">Содержит сведения о завершении и распространении приложений.</span><span class="sxs-lookup"><span data-stu-id="9236c-144">Provides details about finishing and distributing your applications.</span></span>                                              |



 

## <a name="related-topics"></a><span data-ttu-id="9236c-145">См. также</span><span class="sxs-lookup"><span data-stu-id="9236c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9236c-146">**О пакете SDK для формата Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9236c-146">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="9236c-147">**Пакет SDK для Windows Media Format 11**</span><span class="sxs-lookup"><span data-stu-id="9236c-147">**Windows Media Format 11 SDK**</span></span>](windows-media-format-11-sdk.md)
</dt> </dl>

 

 




