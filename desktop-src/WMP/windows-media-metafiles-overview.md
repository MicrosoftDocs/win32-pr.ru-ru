---
title: Общие сведения о метафайлах Windows Media
description: Общие сведения о метафайлах Windows Media
ms.assetid: 5b7742c0-f416-4bf4-ae03-9554b51fe620
keywords:
- Метафайлы Windows Media, сведения
- Проигрыватель Windows Media, метафайлы
- Проигрыватель Windows Media, метафайлы Windows Media
- Метафайлы, сведения
- Windows Media, метафайлы
- Списки воспроизведения метафайлов Windows Media, сведения
- списки воспроизведения, сведения
- Метафайлы Windows Media, синтаксис
- Метафайлы, синтаксис
- списки воспроизведения метафайлов, сведения
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7ed86cca023103c044f28141e0212542d83d200
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710077"
---
# <a name="windows-media-metafiles-overview"></a><span data-ttu-id="79531-113">Общие сведения о метафайлах Windows Media</span><span class="sxs-lookup"><span data-stu-id="79531-113">Windows Media Metafiles Overview</span></span>

<span data-ttu-id="79531-114">Наиболее важной частью успешного использования метафайлов Windows Media является правильный синтаксис для элементов метафайлов.</span><span class="sxs-lookup"><span data-stu-id="79531-114">The most important part of successfully using Windows Media metafiles is using the correct syntax for the metafile elements.</span></span> <span data-ttu-id="79531-115">Синтаксические ошибки в метафайле Windows Media могут привести к тому, что содержимое одного атрибута будет неизвестным, а метафайл не будет распознан как допустимый и не будет работать.</span><span class="sxs-lookup"><span data-stu-id="79531-115">Syntax errors in a Windows Media metafile can cause anything from a single attribute being overlooked, to the metafile not being recognized as valid and failing to work.</span></span>

<span data-ttu-id="79531-116">Почти так же важно — порядок, в котором элементы отображаются в метафайле Windows Media.</span><span class="sxs-lookup"><span data-stu-id="79531-116">Almost as important is the order in which the elements appear in a Windows Media metafile.</span></span> <span data-ttu-id="79531-117">Атрибуты некоторых элементов временно переопределяют атрибуты похожих элементов в разных разделах метафайла.</span><span class="sxs-lookup"><span data-stu-id="79531-117">The attributes of some elements temporarily override the attributes of similar elements in different sections of the metafile.</span></span> <span data-ttu-id="79531-118">Существует определенный [Порядок приоритета](order-of-precedence.md).</span><span class="sxs-lookup"><span data-stu-id="79531-118">There is a defined [Order of Precedence](order-of-precedence.md).</span></span>

<span data-ttu-id="79531-119">Списки воспроизведения метафайлов Windows Media представляют собой метафайлы Windows Media, которые предоставляют сведения, используемые проигрывателем Windows Media для получения одноадресных потоков, многоадресных потоков и других поддерживаемых носителей из интрасети или Интернета.</span><span class="sxs-lookup"><span data-stu-id="79531-119">Windows Media metafile playlists are Windows Media metafiles that provide information that Windows Media Player uses to receive unicast streams, multicast streams, and other supported media from an intranet or the Internet.</span></span> <span data-ttu-id="79531-120">Список воспроизведения метафайлов, по сути, является ярлыком для мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="79531-120">A metafile playlist is basically a shortcut to media content.</span></span> <span data-ttu-id="79531-121">Список воспроизведения метафайлов можно отправить в виде сообщения электронной почты, который используется в качестве ссылки на веб-страницу, созданной динамически с помощью Active Server страниц (ASP) или существовать как отдельный файл на локальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="79531-121">A metafile playlist can be sent as email, used as a link reference on a webpage, created dynamically using Active Server Pages (ASP), or exist as a stand-alone file on a local disk drive.</span></span> <span data-ttu-id="79531-122">Список воспроизведения метафайлов может ссылаться на другой список воспроизведения метафайлов, страницу ASP или файл станции Windows Media (с расширением имени файла. NSC).</span><span class="sxs-lookup"><span data-stu-id="79531-122">A metafile playlist can reference another metafile playlist, an ASP page, or a Windows Media station file (with an .nsc file name extension).</span></span> <span data-ttu-id="79531-123">NSC-файл используется для определения станции Windows Media в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="79531-123">An .nsc file is used to define a Windows Media station to Windows Media Player.</span></span> <span data-ttu-id="79531-124">Базовый процесс обработки одинаков для каждого случая.</span><span class="sxs-lookup"><span data-stu-id="79531-124">The basic handling process is the same for each case.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79531-125">См. также</span><span class="sxs-lookup"><span data-stu-id="79531-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79531-126">**О метафайлах Windows Media**</span><span class="sxs-lookup"><span data-stu-id="79531-126">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> </dl>

 

 




