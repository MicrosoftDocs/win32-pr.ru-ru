---
title: Создание презентации Хтмлвиев
description: Создание презентации Хтмлвиев
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Списки воспроизведения метафайлов Windows Media, презентации Хтмлвиев
- списки воспроизведения, презентации Хтмлвиев
- списки воспроизведения метафайлов, презентации Хтмлвиев
- Списки воспроизведения метафайлов Windows Media, создание презентаций Хтмлвиев
- списки воспроизведения, создание презентаций Хтмлвиев
- списки воспроизведения метафайлов, создание презентаций Хтмлвиев
- Создание презентаций Хтмлвиев
- Проигрыватель Windows Media, создание презентаций Хтмлвиев
- Проигрыватель Windows Media, Хтмлвиев презентации
- Хтмлвиев, создание презентаций
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411105"
---
# <a name="creating-an-htmlview-presentation"></a><span data-ttu-id="d1038-113">Создание презентации Хтмлвиев</span><span class="sxs-lookup"><span data-stu-id="d1038-113">Creating an HTMLView Presentation</span></span>

<span data-ttu-id="d1038-114">Чтобы создать базовую Хтмлвиев презентацию, требуется по крайней мере три элемента:</span><span class="sxs-lookup"><span data-stu-id="d1038-114">To create a basic HTMLView presentation, you need at least three elements:</span></span>

-   <span data-ttu-id="d1038-115">**Мультимедийное содержимое.**</span><span class="sxs-lookup"><span data-stu-id="d1038-115">**Digital media content.**</span></span> <span data-ttu-id="d1038-116">Это один или несколько звуковых или видеофайлов, которые воспроизводит проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d1038-116">This is one or more audio or video files that Windows Media Player plays.</span></span>
-   <span data-ttu-id="d1038-117">**Веб-страница.**</span><span class="sxs-lookup"><span data-stu-id="d1038-117">**A webpage.**</span></span> <span data-ttu-id="d1038-118">Это веб-содержимое, которое отображается в **воспроизводимой** в данный момент функции пользовательского интерфейса проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="d1038-118">This is the Web-based content that displays in the **Now Playing** feature of the Player UI.</span></span>
-   <span data-ttu-id="d1038-119">**Метафайл Windows Media.**</span><span class="sxs-lookup"><span data-stu-id="d1038-119">**A Windows Media metafile.**</span></span> <span data-ttu-id="d1038-120">Это список воспроизведения метафайлов, который указывает проигрывателю Windows Media объединить мультимедийное содержимое с веб-страницей.</span><span class="sxs-lookup"><span data-stu-id="d1038-120">This is the metafile playlist that directs Windows Media Player to combine the digital media content with the webpage.</span></span>

<span data-ttu-id="d1038-121">ASX-файл — это текстовый файл, содержащий сведения о файловом потоке и его представлении.</span><span class="sxs-lookup"><span data-stu-id="d1038-121">An .asx file is a text file that provides information about a file stream and its presentation.</span></span> <span data-ttu-id="d1038-122">В зависимости от синтаксиса язык XML (XML) ASX-файлы могут содержать множество элементов, каждый из которых определяется тегом с соответствующими атрибутами.</span><span class="sxs-lookup"><span data-stu-id="d1038-122">Based on Extensible Markup Language (XML) syntax, .asx files can contain a variety of elements, each identified by a tag with associated attributes.</span></span> <span data-ttu-id="d1038-123">Элемент **param** предоставляет способ связать пользовательский параметр с определенной записью в списке воспроизведения метафайла или в целом метафайле.</span><span class="sxs-lookup"><span data-stu-id="d1038-123">The **PARAM** element provides a way to associate a custom parameter with either a particular entry in a metafile playlist or the entire metafile.</span></span> <span data-ttu-id="d1038-124">Одно из предопределенных имен параметров, доступных для использования, — "Хтмлвиев".</span><span class="sxs-lookup"><span data-stu-id="d1038-124">One of the predefined parameter names available for your use is "HTMLView".</span></span> <span data-ttu-id="d1038-125">Это параметр, который вызывает отображение веб-страницы, указанной значением URL-адреса, в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d1038-125">This is the parameter that causes the webpage specified by the URL value to be displayed in Windows Media Player.</span></span>

<span data-ttu-id="d1038-126">В следующем примере кода показан файл ASX, объединяющий один файл мультимедиа с одной веб-страницей:</span><span class="sxs-lookup"><span data-stu-id="d1038-126">The following example code shows an .asx file that combines a single digital media file with a single webpage:</span></span>


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="d1038-127">Когда проигрыватель Windows Media открывает ASX-файл в предыдущем примере, он воспроизводит звук из файла с именем content1. WMA и открывает веб-страницу с именем htmlview.htm в **воспроизводимой** функции проигрывателя в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="d1038-127">When Windows Media Player opens the .asx file in the preceding example, it plays the audio from the file named content1.wma and opens the webpage named htmlview.htm in the **Now Playing** feature of the full-mode Player.</span></span> <span data-ttu-id="d1038-128">Пользователь может приостанавливать, искать и останавливать аудио содержимое с помощью элементов управления проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d1038-128">The user can pause, seek, and stop the audio content using the Windows Media Player controls.</span></span>

<span data-ttu-id="d1038-129">Вы можете легко изменить веб-страницу, отображаемую для каждого фрагмента содержимого, связав элемент **param** с каждой записью, как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="d1038-129">You can easily change the webpage that is displayed for each piece of content by associating a **PARAM** element with each entry, as the following code example shows:</span></span>


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="d1038-130">В предыдущем примере проигрыватель Windows Media сначала отображает веб-страницу htmlview1.htm при воспроизведении цифрового звукового файла content1. WMA.</span><span class="sxs-lookup"><span data-stu-id="d1038-130">In the preceding example, Windows Media Player first displays the webpage htmlview1.htm while playing the digital audio file content1.wma.</span></span> <span data-ttu-id="d1038-131">Когда проигрыватель открывает следующую запись в списке воспроизведения content2. WMA, веб-страница, отображаемая в окне **воспроизведения** , изменяется на htmlview2.htm.</span><span class="sxs-lookup"><span data-stu-id="d1038-131">When the Player opens the next entry in the playlist, content2.wma, the webpage displayed in **Now Playing** changes to htmlview2.htm.</span></span> <span data-ttu-id="d1038-132">Таким образом можно указать, какую веб-страницу будет видеть пользователь для каждого фрагмента мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="d1038-132">In this way, you can specify which webpage the user sees for each piece of digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1038-133">См. также</span><span class="sxs-lookup"><span data-stu-id="d1038-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1038-134">**Отображение веб-страниц в проигрывателе Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d1038-134">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="d1038-135">**PARAM, элемент**</span><span class="sxs-lookup"><span data-stu-id="d1038-135">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




