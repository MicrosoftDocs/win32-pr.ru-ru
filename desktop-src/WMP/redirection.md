---
title: Перенаправление
description: Перенаправление
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Списки воспроизведения метафайлов Windows Media, перенаправление
- списки воспроизведения, перенаправление
- списки воспроизведения метафайлов, перенаправление
- Проигрыватель Windows Media, перенаправление
- перенаправление
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328571"
---
# <a name="redirection"></a><span data-ttu-id="3250d-108">Перенаправление</span><span class="sxs-lookup"><span data-stu-id="3250d-108">Redirection</span></span>

<span data-ttu-id="3250d-109">Список воспроизведения перенаправит браузер в проигрыватель Windows Media для воспроизведения указанного потока мультимедиа или файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3250d-109">The playlist will redirect the browser to Windows Media Player to play the designated media stream or media file.</span></span> <span data-ttu-id="3250d-110">Самый простой список воспроизведения метафайлов содержит только универсальный указатель ресурсов (URL-адрес) файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3250d-110">The most basic metafile playlist contains only the Uniform Resource Locator (URL) of a media file.</span></span>

<span data-ttu-id="3250d-111">Чтобы создать базовый список воспроизведения метафайлов, откройте любой текстовый редактор, например Microsoft Notepad, и введите следующий пример кода.</span><span class="sxs-lookup"><span data-stu-id="3250d-111">To create a basic metafile playlist, open your favorite text editor, such as Microsoft Notepad, and type the following example code.</span></span>


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



<span data-ttu-id="3250d-112">Замените допустимый путь к файлу Windows Media, используя синтаксис, приведенный в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3250d-112">Substitute a valid path to your Windows Media file using the syntax in the following table.</span></span>



| <span data-ttu-id="3250d-113">Источник содержимого</span><span class="sxs-lookup"><span data-stu-id="3250d-113">Source of content</span></span>                                                                                 | <span data-ttu-id="3250d-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3250d-114">Syntax</span></span>                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="3250d-115">Содержимое — это файл на сервере Windows Media</span><span class="sxs-lookup"><span data-stu-id="3250d-115">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="3250d-116">mms://ServerName/Path/FileName.wma</span><span class="sxs-lookup"><span data-stu-id="3250d-116">mms://ServerName/Path/FileName.wma</span></span>        |
| <span data-ttu-id="3250d-117">Содержимое — это широковещательная многоадресная рассылка, доступ к которой осуществляется с помощью станции Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3250d-117">Content is a broadcast multicast that is accessed from a Windows Media station</span></span>                    | https://WebServerName/Stations/kxyz.nsc    |
| <span data-ttu-id="3250d-118">Содержимое — это одноадресная рассылка, доступ к которой осуществляется из точки публикации на сервере Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3250d-118">Content is a broadcast unicast that is accessed from a publishing point on a Windows Media server</span></span> | <span data-ttu-id="3250d-119">mms://ServerName/PublishingPointAlias</span><span class="sxs-lookup"><span data-stu-id="3250d-119">mms://ServerName/PublishingPointAlias</span></span>     |
| <span data-ttu-id="3250d-120">Содержимое — это файл на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="3250d-120">Content is a file on a web server</span></span>                                                                 | https://WebServerName/Path/Filename.wma    |
| <span data-ttu-id="3250d-121">Содержимое — это файл на локальном жестком диске</span><span class="sxs-lookup"><span data-stu-id="3250d-121">Content is a file on a local hard disk</span></span>                                                            | <span data-ttu-id="3250d-122">file://c: \\ путь \\ имя_файла. WMA</span><span class="sxs-lookup"><span data-stu-id="3250d-122">file://c:\\Path\\Filename.wma</span></span>             |
| <span data-ttu-id="3250d-123">Содержимое — это файл в общей сетевой папке.</span><span class="sxs-lookup"><span data-stu-id="3250d-123">Content is a file on a network share</span></span>                                                              | <span data-ttu-id="3250d-124">file:// \\ \\ имя_сервера \\ путь \\ имя_файла. WMA</span><span class="sxs-lookup"><span data-stu-id="3250d-124">file://\\\\ServerName\\Path\\Filename.wma</span></span> |
| <span data-ttu-id="3250d-125">Содержимое — это файл на сервере Windows Media</span><span class="sxs-lookup"><span data-stu-id="3250d-125">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="3250d-126">mms://ServerName/Path/FileName.wmv</span><span class="sxs-lookup"><span data-stu-id="3250d-126">mms://ServerName/Path/FileName.wmv</span></span>        |



 

<span data-ttu-id="3250d-127">Сохраните созданный файл с именем файла и расширением, как описано в разделе [расширения имен файлов](file-name-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="3250d-127">Save the file you have created with a file name and extension as described in [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="3250d-128">Дважды щелкните его в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="3250d-128">Double-click it in Windows Explorer.</span></span> <span data-ttu-id="3250d-129">Проигрыватель Windows Media должен открыть и начать потоковую передачу содержимого.</span><span class="sxs-lookup"><span data-stu-id="3250d-129">Windows Media Player should open and start streaming the content.</span></span> <span data-ttu-id="3250d-130">Вы можете сохранить файл на веб-сервере, а также создать ссылку на него с помощью элемента **href** , или внедрить его в страницу с использованием тега **объекта** проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3250d-130">You can save the file to your web server, along with your webpages, and link to it with an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** tag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3250d-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3250d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3250d-132">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="3250d-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="3250d-133">**Использование списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="3250d-133">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="3250d-134">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3250d-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="3250d-135">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3250d-135">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




