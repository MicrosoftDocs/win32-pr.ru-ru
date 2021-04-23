---
title: Границы для проигрывателя Windows Media (не рекомендуется)
description: Границы для проигрывателя Windows Media (не рекомендуется)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Проигрыватель Windows Media, границы
- Обложки проигрывателя Windows Media, границы
- обложки, границы
- границы по сравнению с обложками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329883"
---
# <a name="borders-for-windows-media-player-deprecated"></a><span data-ttu-id="322db-107">Границы для проигрывателя Windows Media (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="322db-107">Borders for Windows Media Player (deprecated)</span></span>

<span data-ttu-id="322db-108">Эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрывателя Windows Media и Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="322db-108">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="322db-109">Рамка похожа на обложку, но вместо замены пользовательского интерфейса для режима сжатия проигрывателя Windows Media рамка внедряется в панель Воспроизведение проигрывателя Windows Media в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="322db-109">A border is similar to a skin, but instead of replacing the user interface for the compact mode of Windows Media Player, a border is embedded in the Now Playing pane of the full mode Windows Media Player.</span></span>

<span data-ttu-id="322db-110">С помощью пакета загрузки Windows Media можно включить содержимое с границей, павинг способ передачи мультимедийных приложений.</span><span class="sxs-lookup"><span data-stu-id="322db-110">By using a Windows Media Download package, you can include content with a border, paving the way to multimedia applications.</span></span>

<span data-ttu-id="322db-111">Пример пакета загрузки Windows Media, который включает в себя обрамление и внедренное содержимое, содержится в каталоге Samples этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="322db-111">A sample Windows Media Download package that includes a border and embedded content is included in the samples directory of this SDK.</span></span>

## <a name="creating-a-border"></a><span data-ttu-id="322db-112">Создание границы</span><span class="sxs-lookup"><span data-stu-id="322db-112">Creating a Border</span></span>

<span data-ttu-id="322db-113">Граница создается таким же образом, как и обложка.</span><span class="sxs-lookup"><span data-stu-id="322db-113">A border is created the same way as a skin.</span></span> <span data-ttu-id="322db-114">Единственное отличие состоит в том, что Обложка встроена **в область текущий** .</span><span class="sxs-lookup"><span data-stu-id="322db-114">The only difference is that the skin is embedded inside the **Now Playing** pane.</span></span> <span data-ttu-id="322db-115">Это означает, что размер обложки не может быть вычислен и все элементы обложки должны быть относительными.</span><span class="sxs-lookup"><span data-stu-id="322db-115">This means that the skin size cannot be calculated and that all skin elements must be relative.</span></span> <span data-ttu-id="322db-116">Если пользователь изменяет размер проигрывателя Windows Media, части границы могут быть обрезаны и не отображаться.</span><span class="sxs-lookup"><span data-stu-id="322db-116">If the user resizes Windows Media Player, portions of the border may be clipped off and not seen.</span></span>

## <a name="loading-a-border"></a><span data-ttu-id="322db-117">Загрузка границы</span><span class="sxs-lookup"><span data-stu-id="322db-117">Loading a Border</span></span>

<span data-ttu-id="322db-118">При загрузке метафайла Windows Media, использующего элемент **Skin** , загружается граница.</span><span class="sxs-lookup"><span data-stu-id="322db-118">A border is loaded when a Windows Media metafile that uses the **SKIN** element is loaded.</span></span> <span data-ttu-id="322db-119">Атрибут **href** элемента **Skin** должен ссылаться на обложку.</span><span class="sxs-lookup"><span data-stu-id="322db-119">The **HREF** attribute of the **SKIN** element must reference a skin.</span></span> <span data-ttu-id="322db-120">Типичный элемент **обложки** будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="322db-120">A typical **SKIN** element would look like this:</span></span>


```C++
<SKIN HREF="myborder.wmz">

```



<span data-ttu-id="322db-121">Дополнительные сведения см. в разделе [элемент Skin (не рекомендуется)](skin-element--deprecated.md).</span><span class="sxs-lookup"><span data-stu-id="322db-121">For more information, see [SKIN Element (deprecated)](skin-element--deprecated.md).</span></span>

## <a name="including-content-with-a-border"></a><span data-ttu-id="322db-122">Включение содержимого с границей</span><span class="sxs-lookup"><span data-stu-id="322db-122">Including Content with a Border</span></span>

<span data-ttu-id="322db-123">Можно включить содержимое с границей с помощью файла загрузки Windows Media (с расширением имени файла WMD).</span><span class="sxs-lookup"><span data-stu-id="322db-123">You can include content with a border by using a Windows Media Download file (with a .wmd file name extension).</span></span> <span data-ttu-id="322db-124">Выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="322db-124">Follow these steps:</span></span>

1.  <span data-ttu-id="322db-125">Создайте границу.</span><span class="sxs-lookup"><span data-stu-id="322db-125">Create the border.</span></span> <span data-ttu-id="322db-126">Постарайтесь создать его таким образом, чтобы изменение размера не насмарку композицию границы.</span><span class="sxs-lookup"><span data-stu-id="322db-126">Take care to create it in such a way that resizing will not ruin the composition of the border.</span></span> <span data-ttu-id="322db-127">Например, не включайте фоновый файл; сделать фон прозрачным, чтобы визуализация выполнялась на его основе.</span><span class="sxs-lookup"><span data-stu-id="322db-127">For example, do not include a background file; make the background transparent so that a visualization could run behind it.</span></span>
2.  <span data-ttu-id="322db-128">Сжатие содержимого обложки (изображений, файлов JScript и файла определения обложки) в файл с расширением WMZ.</span><span class="sxs-lookup"><span data-stu-id="322db-128">Compress the skin contents (art, JScript files, and skin definition file) into a file with a .wmz file name extension.</span></span>
3.  <span data-ttu-id="322db-129">Создайте метафайл Windows Media (с расширением файла. ASX), который ссылается на сжатый файл границ (с расширением WMZ).</span><span class="sxs-lookup"><span data-stu-id="322db-129">Create a Windows Media metafile (with an .asx file name extension) that references the compressed border file (with a .wmz file name extension).</span></span> <span data-ttu-id="322db-130">Метафайл может включать сведения списка воспроизведения с метаданными для иллюстрации и URL-адресов для конкретного содержимого.</span><span class="sxs-lookup"><span data-stu-id="322db-130">The metafile can include playlist information with metadata for art and URLs for specific content.</span></span>
4.  <span data-ttu-id="322db-131">Соберите мультимедийное содержимое.</span><span class="sxs-lookup"><span data-stu-id="322db-131">Assemble the digital media content.</span></span>
5.  <span data-ttu-id="322db-132">Сжатие границы, метафайла и содержимого в один файл и присвоение ему расширения имени файла. WMD.</span><span class="sxs-lookup"><span data-stu-id="322db-132">Compress the border, metafile, and content into one file and give it a .wmd file name extension.</span></span>

## <a name="using-a-border"></a><span data-ttu-id="322db-133">Использование границы</span><span class="sxs-lookup"><span data-stu-id="322db-133">Using a Border</span></span>

<span data-ttu-id="322db-134">После создания файла загрузки Windows Media все, что пользователь должен выполнить, — это дважды щелкнуть его.</span><span class="sxs-lookup"><span data-stu-id="322db-134">After you have created the Windows Media Download file, all that the user has to do is double-click on it.</span></span> <span data-ttu-id="322db-135">Файл будет скачан на компьютер пользователя.</span><span class="sxs-lookup"><span data-stu-id="322db-135">The file will be downloaded to the user's computer.</span></span> <span data-ttu-id="322db-136">Файлы в пакете будут распакованы, список воспроизведения будет добавлен к спискам воспроизведения. Эта граница появится на панели **Воспроизведение** проигрывателя Windows Media в полноэкранном режиме, а первый элемент в новом списке воспроизведения начнет воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="322db-136">The files inside the package will be unpacked, the playlist will be added to the playlists, the border will appear in the **Now Playing** pane of the full mode Windows Media Player, and the first item on the new playlist will begin playing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="322db-137">См. также</span><span class="sxs-lookup"><span data-stu-id="322db-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="322db-138">**О обложках**</span><span class="sxs-lookup"><span data-stu-id="322db-138">**About Skins**</span></span>](about-skins.md)
</dt> <dt>

[<span data-ttu-id="322db-139">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="322db-139">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="322db-140">**Пакеты загрузки Windows Media (устарели)**</span><span class="sxs-lookup"><span data-stu-id="322db-140">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




