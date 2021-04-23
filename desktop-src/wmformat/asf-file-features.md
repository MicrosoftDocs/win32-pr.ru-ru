---
title: Функции файлов ASF
description: Функции файлов ASF
ms.assetid: 6e180f27-69ef-4fe0-b06c-b2ead7be8a05
keywords:
- Windows Media Format SDK, функции файлов ASF
- Windows Media Format SDK, функции
- Расширенный системный формат (ASF), функции файлов
- ASF (Расширенный системный формат), функции файлов
- Расширенный формат систем (ASF), функции
- ASF (Расширенный системный формат), функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871d2986ad85716fe198b9a16e1a3772d1cca5f8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "105700971"
---
# <a name="asf-file-features"></a><span data-ttu-id="09d8b-109">Функции файлов ASF</span><span class="sxs-lookup"><span data-stu-id="09d8b-109">ASF File Features</span></span>

<span data-ttu-id="09d8b-110">Основным назначением пакета SDK для формата Windows Media является предоставление поддержки инкапсуляции цифровых мультимедийных данных в файлы ASF и доставка мультимедиа в клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="09d8b-110">The primary purpose of the Windows Media Format SDK is to provide support for encapsulating digital media data in Advanced Systems Format (ASF) files and delivering the media to a client application.</span></span> <span data-ttu-id="09d8b-111">Сценарии доставки могут сильно различаться в зависимости от приложения, но все они используют структуру файлов ASF между созданием и доставкой.</span><span class="sxs-lookup"><span data-stu-id="09d8b-111">Delivery scenarios can vary widely from application to application, but all use the ASF file structure between authoring and delivery.</span></span> <span data-ttu-id="09d8b-112">Файлы ASF соответствуют хорошо определенной, но очень гибкой структуре.</span><span class="sxs-lookup"><span data-stu-id="09d8b-112">ASF files conform to a well defined but very flexible structure.</span></span> <span data-ttu-id="09d8b-113">Дополнительные сведения о структуре файлов ASF см. в разделе [Обзор формата ASF](overview-of-the-asf-format.md).</span><span class="sxs-lookup"><span data-stu-id="09d8b-113">For more information about the ASF file structure, see [Overview of the ASF Format](overview-of-the-asf-format.md).</span></span>

<span data-ttu-id="09d8b-114">Подробные сведения о данных в файле ASF приведены в спецификации ASF, которую можно загрузить с [веб-сайта корпорации Майкрософт](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span><span class="sxs-lookup"><span data-stu-id="09d8b-114">Detailed information about the data in an ASF file is provided in the ASF specification, which you can download from the [Microsoft Web site](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span></span>

<span data-ttu-id="09d8b-115">Пакет Windows Media Format SDK обеспечивает поддержку функций спецификации ASF в основном через профиль, используемый для создания файла.</span><span class="sxs-lookup"><span data-stu-id="09d8b-115">The Windows Media Format SDK provides support for the features of the ASF specification mostly through the profile that is used to create a file.</span></span> <span data-ttu-id="09d8b-116">Дополнительные сведения о профилях см. в разделе [Профили](profiles.md).</span><span class="sxs-lookup"><span data-stu-id="09d8b-116">For more information about profiles, see [Profiles](profiles.md).</span></span>

<span data-ttu-id="09d8b-117">В этом разделе обсуждаются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="09d8b-117">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="09d8b-118">Потоки аудио и видео</span><span class="sxs-lookup"><span data-stu-id="09d8b-118">Audio and Video Streams</span></span>](audio-and-video-streams.md)
-   [<span data-ttu-id="09d8b-119">Потоки изображений</span><span class="sxs-lookup"><span data-stu-id="09d8b-119">Image Streams</span></span>](image-streams.md)
-   [<span data-ttu-id="09d8b-120">Произвольные потоки</span><span class="sxs-lookup"><span data-stu-id="09d8b-120">Arbitrary Streams</span></span>](arbitrary-streams.md)
-   [<span data-ttu-id="09d8b-121">Команды скриптов</span><span class="sxs-lookup"><span data-stu-id="09d8b-121">Script Commands</span></span>](script-commands.md)
-   [<span data-ttu-id="09d8b-122">Расширения модулей данных</span><span class="sxs-lookup"><span data-stu-id="09d8b-122">Data Unit Extensions</span></span>](data-unit-extensions.md)
-   [<span data-ttu-id="09d8b-123">Поддержка кода времени SMPTE</span><span class="sxs-lookup"><span data-stu-id="09d8b-123">SMPTE Time Code Support</span></span>](smpte-time-code-support.md)
-   [<span data-ttu-id="09d8b-124">Взаимное исключение</span><span class="sxs-lookup"><span data-stu-id="09d8b-124">Mutual Exclusion</span></span>](mutual-exclusion.md)
-   [<span data-ttu-id="09d8b-125">Определение приоритетов потоков</span><span class="sxs-lookup"><span data-stu-id="09d8b-125">Stream Prioritization</span></span>](stream-prioritization.md)
-   [<span data-ttu-id="09d8b-126">Совместное использование пропускной способности</span><span class="sxs-lookup"><span data-stu-id="09d8b-126">Bandwidth Sharing</span></span>](bandwidth-sharing.md)
-   [<span data-ttu-id="09d8b-127">Индексы</span><span class="sxs-lookup"><span data-stu-id="09d8b-127">Indexes</span></span>](indexes.md)
-   [<span data-ttu-id="09d8b-128">Метки</span><span class="sxs-lookup"><span data-stu-id="09d8b-128">Markers</span></span>](markers.md)
-   [<span data-ttu-id="09d8b-129">Ответ читателя на функции ASF</span><span class="sxs-lookup"><span data-stu-id="09d8b-129">Reader Response to ASF Features</span></span>](reader-response-to-asf-features.md)

## <a name="related-topics"></a><span data-ttu-id="09d8b-130">См. также</span><span class="sxs-lookup"><span data-stu-id="09d8b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09d8b-131">**Компоненты**</span><span class="sxs-lookup"><span data-stu-id="09d8b-131">**Features**</span></span>](features.md)
</dt> </dl>

 

 




