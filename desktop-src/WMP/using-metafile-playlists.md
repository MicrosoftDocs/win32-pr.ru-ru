---
title: Использование списков воспроизведения метафайлов
description: Использование списков воспроизведения метафайлов
ms.assetid: f5711a7f-7674-4b92-8262-cee8bac4aa77
keywords:
- Списки воспроизведения метафайлов Windows Media, сведения
- списки воспроизведения, сведения
- списки воспроизведения метафайлов, сведения
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 71f245d1fc1610174f842347a15dfcfaa13286e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887911"
---
# <a name="using-metafile-playlists"></a><span data-ttu-id="927ec-106">Использование списков воспроизведения метафайлов</span><span class="sxs-lookup"><span data-stu-id="927ec-106">Using Metafile Playlists</span></span>

<span data-ttu-id="927ec-107">Списки воспроизведения указывают, как будут воспроизводиться потоковые мультимедиа или мультимедийные файлы и какие метаданные будет отображать проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="927ec-107">Playlists specify how the streaming media or media files will be played and what metadata Windows Media Player will display.</span></span>

<span data-ttu-id="927ec-108">В этом разделе объясняется несколько способов использования списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="927ec-108">This section explains several ways you can use playlists.</span></span> <span data-ttu-id="927ec-109">Раздел состоит из следующих разделов.</span><span class="sxs-lookup"><span data-stu-id="927ec-109">The section is divided into the following topics.</span></span>



| <span data-ttu-id="927ec-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="927ec-110">Topic</span></span>                                                                                              | <span data-ttu-id="927ec-111">Описание</span><span class="sxs-lookup"><span data-stu-id="927ec-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="927ec-112">Изменение экрана</span><span class="sxs-lookup"><span data-stu-id="927ec-112">Modifying the Display</span></span>](modifying-the-display.md)                                                 | <span data-ttu-id="927ec-113">Добавление текста, ссылок и изображений.</span><span class="sxs-lookup"><span data-stu-id="927ec-113">Adding text, links, and images.</span></span>                                                                                                                                |
| [<span data-ttu-id="927ec-114">Перенаправление</span><span class="sxs-lookup"><span data-stu-id="927ec-114">Redirection</span></span>](redirection.md)                                                                     | <span data-ttu-id="927ec-115">Использование списков воспроизведения для перенаправления браузера в проигрыватель Windows Media и указания URL-адреса потока или файла мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="927ec-115">Using playlists to redirect the browser to Windows Media Player and specifying the URL of a stream or media file to play.</span></span>                                      |
| [<span data-ttu-id="927ec-116">Доступ к носителю</span><span class="sxs-lookup"><span data-stu-id="927ec-116">Accessing Media</span></span>](accessing-media.md)                                                             | <span data-ttu-id="927ec-117">Использование элементов Metafile и их дочерних элементов для указания содержимого, к которому необходимо получить доступ, а также порядка и длительности их воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="927ec-117">Using metafile elements and their child elements to specify the content to access, and the order and duration of their playback.</span></span>                               |
| [<span data-ttu-id="927ec-118">Использование динамического переключения потока событий</span><span class="sxs-lookup"><span data-stu-id="927ec-118">Using Live Event Stream Switching</span></span>](using-live-event-stream-switching.md)                         | <span data-ttu-id="927ec-119">Используйте элемент **event** , чтобы указать поток мультимедиа для доступа, а затем возобновить воспроизведение исходного потока.</span><span class="sxs-lookup"><span data-stu-id="927ec-119">Using the **EVENT** element to specify a media stream to access and then resume playing the original stream.</span></span> <span data-ttu-id="927ec-120">Используется для вставки рекламы.</span><span class="sxs-lookup"><span data-stu-id="927ec-120">Used for ad insertion.</span></span>                            |
| [<span data-ttu-id="927ec-121">Использование метафайлов для простого переключения потоков</span><span class="sxs-lookup"><span data-stu-id="927ec-121">Using Metafiles for Seamless Stream Switching</span></span>](using-metafiles-for-seamless-stream-switching.md) | <span data-ttu-id="927ec-122">Использование элемента **event** для предварительной загрузки следующего потока мультимедиа для доступа, чтобы избежать пропусков в презентации.</span><span class="sxs-lookup"><span data-stu-id="927ec-122">Using the **EVENT** element to preload the next media stream to access to avoid gaps in the presentation.</span></span>                                                      |
| [<span data-ttu-id="927ec-123">Использование объявлений</span><span class="sxs-lookup"><span data-stu-id="927ec-123">Using Announcements</span></span>](using-announcements.md)                                                     | <span data-ttu-id="927ec-124">Использование метафайла для предоставления сведений об URL-адресе потока мультимедиа, включая IP-адрес многоадресной рассылки, порт, формат потока и другие параметры станции.</span><span class="sxs-lookup"><span data-stu-id="927ec-124">Using a metafile to provide information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> |
| [<span data-ttu-id="927ec-125">Использование URL-адреса и смены сервера</span><span class="sxs-lookup"><span data-stu-id="927ec-125">Using URL and Server Rollover</span></span>](using-url-and-server-rollover.md)                                 | <span data-ttu-id="927ec-126">Использование списков воспроизведения метафайлов для предоставления средств автоматического перехода к альтернативным источникам содержимого при недоступности или воспроизведении потока.</span><span class="sxs-lookup"><span data-stu-id="927ec-126">Using metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span>             |
| [<span data-ttu-id="927ec-127">Использование пользовательских параметров и команд</span><span class="sxs-lookup"><span data-stu-id="927ec-127">Using Custom Parameters and Commands</span></span>](using-custom-parameters-and-commands.md)                   | <span data-ttu-id="927ec-128">Использование элемента **param** для определения пользовательских элементов для предоставления дополнительных метаданных.</span><span class="sxs-lookup"><span data-stu-id="927ec-128">Using the **PARAM** element to define custom elements to provide additional metadata.</span></span>                                                                          |
| [<span data-ttu-id="927ec-129">Настройка доставки мультимедиа</span><span class="sxs-lookup"><span data-stu-id="927ec-129">Personalizing Media Delivery</span></span>](personalizing-media-delivery.md)                                   | <span data-ttu-id="927ec-130">Использование пользовательских настроек для определения широковещательного содержимого.</span><span class="sxs-lookup"><span data-stu-id="927ec-130">Using user preferences to determine broadcast content.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="927ec-131">См. также</span><span class="sxs-lookup"><span data-stu-id="927ec-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="927ec-132">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="927ec-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="927ec-133">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="927ec-133">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="927ec-134">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="927ec-134">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




