---
title: Использование относительных ссылок в метафайлах
description: Использование относительных ссылок в метафайлах
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Списки воспроизведения метафайлов Windows Media, относительные ссылки
- списки воспроизведения, относительные ссылки
- списки воспроизведения метафайлов, относительные ссылки
- Метафайлы, относительные ссылки
- Метафайлы Windows Media, относительные ссылки
- relative links (относительные ссылки).
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888079"
---
# <a name="using-relative-links-in-metafiles"></a><span data-ttu-id="f570c-109">Использование относительных ссылок в метафайлах</span><span class="sxs-lookup"><span data-stu-id="f570c-109">Using Relative Links in Metafiles</span></span>

<span data-ttu-id="f570c-110">Относительные ссылки являются полностью поддерживаемой функцией метафайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f570c-110">Relative links are a fully supported feature of Windows Media metafiles.</span></span> <span data-ttu-id="f570c-111">Можно использовать относительные ссылки в метафайлах во многом аналогично их использованию в HTML-документах.</span><span class="sxs-lookup"><span data-stu-id="f570c-111">You can use relative links in metafiles much like you use them in HTML documents.</span></span> <span data-ttu-id="f570c-112">Использование относительных ссылок позволяет создавать переносимые метафайлы, что означает возможность копирования или перемещения всей структуры каталогов на другой сервер без обновления путей к графическим файлам, используемым в качестве баннеров или атрибутов **href** элементов **мореинфо** (если они ссылаются на файлы на том же веб-сервере, что и сохраненный метафайл).</span><span class="sxs-lookup"><span data-stu-id="f570c-112">The use of relative links enables you to create metafiles that are portable, meaning you can copy or move an entire directory structure to another server without updating the paths to graphic files used as banners or the **HREF** attributes of **MOREINFO** elements (if they reference files on the same web server as the stored metafile).</span></span> <span data-ttu-id="f570c-113">Относительные ссылки работают в любом приложении, которое их поддерживает, поскольку части URL-адреса, не включенные в атрибут **href** элемента, включаются в URL-адрес, отправляемый приложением на сервер при запросе этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f570c-113">Relative links work, in any application that supports them, because the parts of the URL not included in the **HREF** attribute of an element are included in the URL sent by the application to the server when that URL is requested.</span></span> <span data-ttu-id="f570c-114">Это означает, что протокол (например, https://), имя сервера и виртуальный каталог, в котором находится файл, содержащий относительную ссылку, включены в URL-адрес, отправляемый на сервер.</span><span class="sxs-lookup"><span data-stu-id="f570c-114">This means that the protocol (such as https://), the server name, and the virtual directory in which the file containing the relative link is located are all included in the URL that is sent to the server.</span></span> <span data-ttu-id="f570c-115">Если файл мультимедиа или URL-адрес, связанный с использованием относительной ссылки, не находится на том же сервере, что и метафайл, то относительная ссылка является недопустимой.</span><span class="sxs-lookup"><span data-stu-id="f570c-115">If the media file, or URL you link to using a relative link does not reside on the same server as the metafile, the relative link is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="f570c-116">Эти сведения об относительных ссылках верны только при использовании ссылки на метафайлы, открытые в автономном проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f570c-116">This information on relative links is correct only when using a link to metafiles that are opened in the stand-alone Windows Media Player.</span></span> <span data-ttu-id="f570c-117">При использовании встроенного элемента управления проигрывателя Windows Media все ссылки отправляются относительно страницы, на которой размещается элемент управления, если только для перенаправления относительного пути используется **базовый** дочерний элемент элемента **ASX** .</span><span class="sxs-lookup"><span data-stu-id="f570c-117">When you use the embedded Windows Media Player control, all links are relative to the page on which the control is hosted, unless the **BASE** child element of the **ASX** element is used to redirect the relative path.</span></span>

 

<span data-ttu-id="f570c-118">Все относительные ссылки в метафайле должны быть полностью относительными, а не относительно дисками для потоковой передачи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f570c-118">All relative links in the metafile must be fully relative, not drive-relative, for streaming media.</span></span> <span data-ttu-id="f570c-119">Если URL-адрес начинается с \\ символа "", ссылка относится к диску.</span><span class="sxs-lookup"><span data-stu-id="f570c-119">When a URL begins with a "\\" character, the link is drive-relative.</span></span> <span data-ttu-id="f570c-120">Проигрыватель Windows Media пытается открыть файл, связанный с на диске, на котором был открыт метафайл, обычно это веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="f570c-120">Windows Media Player attempts to open the file linked to on the drive where the metafile was opened from, usually a web server.</span></span> <span data-ttu-id="f570c-121">Поскольку веб-серверы используют виртуальные каталоги, проигрыватель Windows Media пытается найти указанный поток или файл мультимедиа в подкаталоге виртуального каталога на веб-сервере, из которого был открыт метафайл.</span><span class="sxs-lookup"><span data-stu-id="f570c-121">Because web servers use virtual directories, Windows Media Player tries to find the specified stream or media file in a subdirectory of a virtual directory on the web server where the metafile was opened from.</span></span> <span data-ttu-id="f570c-122">Пользователь не сможет получить доступ к каталогу сервера.</span><span class="sxs-lookup"><span data-stu-id="f570c-122">A user would not have access to a server directory.</span></span> <span data-ttu-id="f570c-123">В примере в этом разделе показано использование полностью относительных ссылок.</span><span class="sxs-lookup"><span data-stu-id="f570c-123">The example in this section illustrates the use of a fully relative link.</span></span>

<span data-ttu-id="f570c-124">Можно использовать ссылки относительно диска при использовании метафайлов на одном компьютере, где все файлы мультимедиа, связанные с в списке воспроизведения метафайлов, существуют на устройстве хранения на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="f570c-124">You can use drive-relative links when using metafiles on a single computer where all media files linked to in the metafile playlist exist on a storage device in that computer.</span></span> <span data-ttu-id="f570c-125">Однако потоковая передача мультимедиа подобным образом невозможна.</span><span class="sxs-lookup"><span data-stu-id="f570c-125">However, you cannot stream media in this manner.</span></span>

<span data-ttu-id="f570c-126">При использовании ссылки на другой метафайл для разрешения относительных ссылок имя, отображаемое в качестве заголовка Windows Media Player, является названием в исходном метафайле.</span><span class="sxs-lookup"><span data-stu-id="f570c-126">When you use a link to another metafile to allow for relative links, the name displayed as the Title by Windows Media Player is the Title in the original metafile.</span></span>

<span data-ttu-id="f570c-127">Относительные ссылки не могут использоваться для URL-адресов сервера потокового мультимедиа, так как для доступа к потоковой передаче мультимедийного содержимого используются разные протоколы.</span><span class="sxs-lookup"><span data-stu-id="f570c-127">Relative links cannot be used for URLs to a streaming media server because different protocols are used for accessing streaming media content.</span></span>

<span data-ttu-id="f570c-128">В следующем примере списка воспроизведения первый **ентриреф** содержит URL-адрес для другого списка воспроизведения относительно. мастика.</span><span class="sxs-lookup"><span data-stu-id="f570c-128">In the following example playlist, the first **ENTRYREF** contains a URL for another playlist, relative.wax.</span></span>


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



<span data-ttu-id="f570c-129">Ниже приведен пример файла relative. мастика, который содержит относительные ссылки.</span><span class="sxs-lookup"><span data-stu-id="f570c-129">The following example is the file relative.wax, which contains relative links.</span></span>


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="f570c-130">URL-адрес, содержащий ссылку на список воспроизведения, относительный. мастика, может существовать в списке воспроизведения метафайлов в любом месте, доступном пользователю.</span><span class="sxs-lookup"><span data-stu-id="f570c-130">The URL containing the reference to the playlist, relative.wax, can exist in a metafile playlist anywhere that is accessible to the user.</span></span> <span data-ttu-id="f570c-131">Чтобы URL-адрес был успешно обработан, должен существовать веб-сервер с именем «example.microsoft.com».</span><span class="sxs-lookup"><span data-stu-id="f570c-131">For the URL to be processed successfully, there must be a web server named "example.microsoft.com".</span></span> <span data-ttu-id="f570c-132">Этот веб-сервер должен иметь виртуальный каталог, определенный как метафайлы.</span><span class="sxs-lookup"><span data-stu-id="f570c-132">That web server must have a virtual directory defined as "metafiles".</span></span> <span data-ttu-id="f570c-133">На веб-сервере с именем "example.microsoft.com" в виртуальном каталоге "метафайлы" должен присутствовать указанный список воспроизведения, связанный с. мастика.</span><span class="sxs-lookup"><span data-stu-id="f570c-133">The referenced playlist, relative.wax, must exist on the web server named "example.microsoft.com" in the virtual directory "metafiles".</span></span>

<span data-ttu-id="f570c-134">Для файлов мультимедиа, на которые имеются ссылки в списке воспроизведения относительно. мастика для успешного доступа и воспроизведения, необходим каталог с именем "Graphics", который является подкаталогом виртуального каталога сервера "метафайлы".</span><span class="sxs-lookup"><span data-stu-id="f570c-134">For the referenced media files in the playlist relative.wax to be successfully accessed and played, there must be a directory named "Graphics" which is a subdirectory of the server's virtual directory "metafiles".</span></span> <span data-ttu-id="f570c-135">Графический файл Logo1.jpg, на который ссылается элемент **баннера** , должен быть подкаталогом с именем Graphics.</span><span class="sxs-lookup"><span data-stu-id="f570c-135">The graphics file Logo1.jpg, referenced in the **BANNER** element, must be the subdirectory named Graphics.</span></span>

<span data-ttu-id="f570c-136">Аналогичным образом документ с именем Category1.htm должен находиться в подкаталоге с именем Category1.</span><span class="sxs-lookup"><span data-stu-id="f570c-136">Similarly a document named Category1.htm must reside in a subdirectory named Category1.</span></span> <span data-ttu-id="f570c-137">Каталог с именем Category1 должен существовать в виде подкаталога метафайлов виртуального каталога на веб-сервере example.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f570c-137">The directory named Category1 must exist as a subdirectory of the virtual directory "metafiles" on the web server example.microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f570c-138">См. также</span><span class="sxs-lookup"><span data-stu-id="f570c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f570c-139">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="f570c-139">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f570c-140">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="f570c-140">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f570c-141">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f570c-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f570c-142">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f570c-142">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




