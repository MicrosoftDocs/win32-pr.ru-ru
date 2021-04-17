---
title: Использование объявлений
description: Использование объявлений
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Списки воспроизведения метафайлов Windows Media, объявления
- списки воспроизведения, объявления
- списки воспроизведения метафайлов, объявления
- Проигрыватель Windows Media, объявления
- объявления
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700531"
---
# <a name="using-announcements"></a><span data-ttu-id="51aac-108">Использование объявлений</span><span class="sxs-lookup"><span data-stu-id="51aac-108">Using Announcements</span></span>

<span data-ttu-id="51aac-109">Объявление — это файл, содержащий сведения о URL-адресе для потока мультимедиа, включая IP-адрес многоадресной рассылки, порт, формат потока и другие параметры станции.</span><span class="sxs-lookup"><span data-stu-id="51aac-109">An announcement is a file that contains information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> <span data-ttu-id="51aac-110">Объявления создаются администратором Windows Media при создании одноадресного или многоадресного потока публикации.</span><span class="sxs-lookup"><span data-stu-id="51aac-110">Announcements are created by Windows Media Administrator when a unicast or multicast publishing stream is created.</span></span> <span data-ttu-id="51aac-111">Клиент может быстро загрузить файл объявления, а затем перейти к файлу потокового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="51aac-111">The client can quickly load the announcement file, then proceed to access the streaming media file.</span></span>

<span data-ttu-id="51aac-112">Для точки одноадресной рассылки открывается поток мультимедиа пункта публикации.</span><span class="sxs-lookup"><span data-stu-id="51aac-112">For a unicast publishing point, the publishing point media stream is opened.</span></span> <span data-ttu-id="51aac-113">Для точки многоадресной рассылки URL-адрес извлекается из файла станции вещания с расширением NSC, а доступ к потоковой передаче осуществляется.</span><span class="sxs-lookup"><span data-stu-id="51aac-113">For a multicast publishing point, the URL is extracted from a broadcast station file with an .nsc extension, and the streaming media is accessed.</span></span> <span data-ttu-id="51aac-114">В отличие от одноадресного потока сведения о заголовке не содержатся в потоке многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="51aac-114">Unlike a unicast stream, no header information is contained in a multicast stream.</span></span> <span data-ttu-id="51aac-115">Эти сведения поступают из файла станции вещания с расширением NSC.</span><span class="sxs-lookup"><span data-stu-id="51aac-115">That information comes from the broadcast station file with an .nsc extension.</span></span> <span data-ttu-id="51aac-116">Проигрыватель Windows Media обычно сначала открывает файл извещения, который используется для списков воспроизведения метафайлов, указывающий на расположение файла станции вещания.</span><span class="sxs-lookup"><span data-stu-id="51aac-116">Windows Media Player usually first opens an announcement file, which is one use for metafile playlists, that points to the location of the broadcast station file.</span></span>

<span data-ttu-id="51aac-117">Пример кода</span><span class="sxs-lookup"><span data-stu-id="51aac-117">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="51aac-118">См. также</span><span class="sxs-lookup"><span data-stu-id="51aac-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51aac-119">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="51aac-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="51aac-120">**Использование списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="51aac-120">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




