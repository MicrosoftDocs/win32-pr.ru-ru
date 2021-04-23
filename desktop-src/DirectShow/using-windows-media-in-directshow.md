---
description: Использование Windows Media в DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Использование Windows Media в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104424126"
---
# <a name="using-windows-media-in-directshow"></a><span data-ttu-id="bf172-103">Использование Windows Media в DirectShow</span><span class="sxs-lookup"><span data-stu-id="bf172-103">Using Windows Media in DirectShow</span></span>

<span data-ttu-id="bf172-104">В этом разделе описывается использование DirectShow для воспроизведения и записи файлов расширенного формата системы (ASF).</span><span class="sxs-lookup"><span data-stu-id="bf172-104">This section describes how to use DirectShow to play and write Advanced Systems Format (ASF) files.</span></span> <span data-ttu-id="bf172-105">Файлы ASF обычно содержат аудио и видео содержимое, закодированное с помощью кодеков аудио и видео Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bf172-105">ASF files commonly contain audio and video content encoded using the Windows Media Audio and Video codecs.</span></span> <span data-ttu-id="bf172-106">Однако ASF может содержать данные любого типа.</span><span class="sxs-lookup"><span data-stu-id="bf172-106">However, ASF can contain any type of data.</span></span>

<span data-ttu-id="bf172-107">Следующие фильтры DirectShow поддерживают чтение и запись файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="bf172-107">The following DirectShow filters support reading and writing ASF files:</span></span>

-   <span data-ttu-id="bf172-108">[Фильтр чтения WM ASF](wm-asf-reader-filter.md).</span><span class="sxs-lookup"><span data-stu-id="bf172-108">[WM ASF Reader Filter](wm-asf-reader-filter.md).</span></span> <span data-ttu-id="bf172-109">Считывает файлы ASF.</span><span class="sxs-lookup"><span data-stu-id="bf172-109">Reads ASF files.</span></span>
-   <span data-ttu-id="bf172-110">[Фильтр модуля записи WM ASF](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="bf172-110">[WM ASF Writer Filter](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="bf172-111">Файлы вртиес ASF.</span><span class="sxs-lookup"><span data-stu-id="bf172-111">Wrties ASF files.</span></span>
-   <span data-ttu-id="bf172-112">[Фильтр оболочки DMO](dmo-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="bf172-112">[DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="bf172-113">Создает оболочку для кодировщика Windows Media и декодера дмос.</span><span class="sxs-lookup"><span data-stu-id="bf172-113">Wraps the Windows Media encoder and decoder DMOs.</span></span>

### <a name="versions"></a><span data-ttu-id="bf172-114">Версии</span><span class="sxs-lookup"><span data-stu-id="bf172-114">Versions</span></span>

<span data-ttu-id="bf172-115">Фильтры модуля записи WM ASF и WM ASF упаковываются в библиотеку DLL с именем qasf.dll, а фильтры совместно называются "компонентами КАСФ".</span><span class="sxs-lookup"><span data-stu-id="bf172-115">The WM ASF Reader and WM ASF Writer filters are packaged in the DLL named qasf.dll, and the filters are collectively named "QASF components."</span></span> <span data-ttu-id="bf172-116">Эти фильтры являются оболочками для пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="bf172-116">These filters are wrappers for the Windows Media Format SDK.</span></span> <span data-ttu-id="bf172-117">Библиотека DLL (qasf.dll) была впервые опубликована в пакете SDK DirectX, но позднее была обновлена в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bf172-117">The DLL (qasf.dll) was first published in the DirectX SDK but was later updated in the Windows Media Format SDK.</span></span> <span data-ttu-id="bf172-118">Ниже приведен журнал версий фильтров КАСФ.</span><span class="sxs-lookup"><span data-stu-id="bf172-118">Here is the version history of the QASF filters:</span></span>

-   <span data-ttu-id="bf172-119">DirectShow 8,1 поддерживает пакет SDK для формата Windows Media версии 7,0.</span><span class="sxs-lookup"><span data-stu-id="bf172-119">DirectShow 8.1 supports Windows Media Format SDK version 7.0.</span></span>
-   <span data-ttu-id="bf172-120">DirectShow 9,0 поддерживает пакет SDK для формата Windows Media версии 7,1.</span><span class="sxs-lookup"><span data-stu-id="bf172-120">DirectShow 9.0 supports Windows Media Format SDK version 7.1.</span></span>
-   <span data-ttu-id="bf172-121">Пакет обновления 2 (SP2) для Windows XP поддерживает пакет SDK Windows Media Format 9.</span><span class="sxs-lookup"><span data-stu-id="bf172-121">Windows XP Service Pack 2 supports Windows Media Format 9 SDK.</span></span>
-   <span data-ttu-id="bf172-122">Windows Vista поддерживает пакет SDK для Windows Media Format 11.</span><span class="sxs-lookup"><span data-stu-id="bf172-122">Windows Vista supports Windows Media Format 11 SDK.</span></span>
-   <span data-ttu-id="bf172-123">Пакет SDK Windows Media Format 9 и более поздние версии содержат соответствующие версии КАСФ.</span><span class="sxs-lookup"><span data-stu-id="bf172-123">Windows Media Format 9 SDK and later contain corresponding versions of QASF.</span></span>

<span data-ttu-id="bf172-124">Для получения последней версии КАСФ всегда Скачайте последнюю версию пакета SDK для Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="bf172-124">To get the latest version of QASF, always download the latest Windows Media Format SDK.</span></span>

### <a name="legacy-windows-media-source-filter"></a><span data-ttu-id="bf172-125">Устаревший фильтр источника Windows Media</span><span class="sxs-lookup"><span data-stu-id="bf172-125">Legacy Windows Media Source Filter</span></span>

<span data-ttu-id="bf172-126">В Windows XP с пакетом обновления 1 (SP1) и более ранних версий фильтр источника по умолчанию для файлов ASF (. ASF,. WMV и. WMA) является устаревшим [фильтром источников Windows Media](windows-media-source-filter.md).</span><span class="sxs-lookup"><span data-stu-id="bf172-126">In Windows XP Service Pack 1 and earlier, the default source filter for ASF files (.asf, .wmv, and .wma file extensions) is the obsolete [Windows Media Source Filter](windows-media-source-filter.md).</span></span> <span data-ttu-id="bf172-127">Это поведение поддерживалось для обеспечения обратной совместимости с приложениями, использующими проигрыватель Windows Media 6,4.</span><span class="sxs-lookup"><span data-stu-id="bf172-127">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="bf172-128">Новые приложения должны использовать более новые версии КАСФ, благодаря которым модуль чтения WM ASF фильтрует фильтр по умолчанию для воспроизведения файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="bf172-128">New applications should use the newer versions of QASF, which make the WM ASF Reader filter the default filter for playing ASF files.</span></span>

<span data-ttu-id="bf172-129">Дополнительные сведения о пакетах средств разработки для Windows Media Suite см. в разделе [аудио и видео](../audio-and-video.md) Библиотеки MDSN.</span><span class="sxs-lookup"><span data-stu-id="bf172-129">For more information on the Windows Media suite of software development kits, see the [Audio and Video](../audio-and-video.md) section of the MDSN Library.</span></span>

<span data-ttu-id="bf172-130">Эта статья содержит следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="bf172-130">This article contains the following topics:</span></span>

-   [<span data-ttu-id="bf172-131">Чтение файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="bf172-131">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
-   [<span data-ttu-id="bf172-132">Создание файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="bf172-132">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="bf172-133">См. также</span><span class="sxs-lookup"><span data-stu-id="bf172-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf172-134">Использование DirectShow</span><span class="sxs-lookup"><span data-stu-id="bf172-134">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 
