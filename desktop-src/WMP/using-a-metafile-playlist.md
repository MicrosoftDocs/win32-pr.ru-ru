---
title: Использование списка воспроизведения метафайла
description: Использование списка воспроизведения метафайла
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Списки воспроизведения метафайлов Windows Media с помощью
- списки воспроизведения метафайлов, использование
- списки воспроизведения, использование
- Списки воспроизведения метафайлов Windows Media, сведения
- списки воспроизведения метафайлов, сведения
- списки воспроизведения, сведения
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775386"
---
# <a name="using-a-metafile-playlist"></a><span data-ttu-id="d4f04-109">Использование списка воспроизведения метафайла</span><span class="sxs-lookup"><span data-stu-id="d4f04-109">Using a Metafile Playlist</span></span>

<span data-ttu-id="d4f04-110">Поскольку нельзя напрямую связать веб-страницу с сервером потокового мультимедиа, используются списки воспроизведения метафайлов.</span><span class="sxs-lookup"><span data-stu-id="d4f04-110">Because you cannot link directly from a webpage to a streaming media server, you use metafile playlists.</span></span> <span data-ttu-id="d4f04-111">Списки воспроизведения метафайлов содержат сведения, необходимые для проигрывателя Windows Media и хранятся на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="d4f04-111">The metafile playlists contain the information needed by Windows Media Player and are stored on a web server.</span></span> <span data-ttu-id="d4f04-112">Затем можно связать веб-документ с списком воспроизведения метафайлов.</span><span class="sxs-lookup"><span data-stu-id="d4f04-112">You can then link from the Web document to a metafile playlist.</span></span> <span data-ttu-id="d4f04-113">При открытии списка воспроизведения метафайла Управление передачей в проигрыватель Windows Media, который обрабатывает файл, подключается к серверу потокового мультимедиа и воспроизводит указанное содержимое.</span><span class="sxs-lookup"><span data-stu-id="d4f04-113">When a metafile playlist is opened, control transfers to Windows Media Player, which processes the file, connects to the streaming media server, and plays the specified content.</span></span>

<span data-ttu-id="d4f04-114">Сначала браузер скачивает список воспроизведения метафайлов в каталог кэша пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4f04-114">The browser first downloads the metafile playlist to the user's cache directory.</span></span> <span data-ttu-id="d4f04-115">Так как список воспроизведения метафайлов невелик, это очень быстрое действие.</span><span class="sxs-lookup"><span data-stu-id="d4f04-115">Because the metafile playlist is small, this is a very quick step.</span></span> <span data-ttu-id="d4f04-116">Компьютер пользователя затем находит в таблице сопоставлений файлов, взаимосвязь списка воспроизведения метафайлов с проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d4f04-116">The user's computer then finds in its file associations table the association of the metafile playlist with Windows Media Player.</span></span> <span data-ttu-id="d4f04-117">Проигрыватель Windows Media открывает и интерпретирует скрипты в списке воспроизведения метафайлов, который, помимо прочего, содержит URL-адрес потокового содержимого.</span><span class="sxs-lookup"><span data-stu-id="d4f04-117">Windows Media Player opens and interprets the scripting in the metafile playlist, which contains, among other things, the URL of the streaming content.</span></span> <span data-ttu-id="d4f04-118">Проигрыватель Windows Media использует URL-адрес для нахождение содержимого и инициации потока.</span><span class="sxs-lookup"><span data-stu-id="d4f04-118">Windows Media Player uses the URL to locate the content and initiate the stream.</span></span> <span data-ttu-id="d4f04-119">Затем скрипт списка воспроизведения метафайлов управляет процессом потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="d4f04-119">The metafile playlist scripting then controls the streaming experience.</span></span>

<span data-ttu-id="d4f04-120">Так как списки воспроизведения метафайлов работают через вспомогательное приложение, связанное с типом АСКСМИМЕ (Application/Mplayer2 или Video/x-MS-ASF), они совместимы с любым браузером, поддерживающим вспомогательные приложения.</span><span class="sxs-lookup"><span data-stu-id="d4f04-120">Because metafile playlists work through a helper application associated with the ASXMIME type (application/mplayer2 or video/x-ms-asf), they are compatible with any browser that supports helper applications.</span></span> <span data-ttu-id="d4f04-121">Примеры, приведенные в этом документе, будут работать с Microsoft Internet Explorer 4,0 и более поздней версии, а также с Netscape Navigator 4,0 и более поздней версии на платформах Microsoft Win32® и Apple Macintosh.</span><span class="sxs-lookup"><span data-stu-id="d4f04-121">The examples shown in this document will work with Microsoft Internet Explorer 4.0 and later, and with Netscape Navigator 4.0 and later on Microsoft Win32® and Apple Macintosh platforms.</span></span> <span data-ttu-id="d4f04-122">Во всех примерах необходимо убедиться, что все файлы мультимедиа, на которые имеются ссылки, имеют допустимые пути и имена файлов для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="d4f04-122">In all examples, you will have to be sure that any digital media files referenced have valid paths and file names for your environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4f04-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d4f04-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4f04-124">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d4f04-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="d4f04-125">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d4f04-125">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="d4f04-126">**Общие сведения о метафайлах Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d4f04-126">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




