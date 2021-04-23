---
title: Как работают пакеты загрузки Windows Media (не рекомендуется)
description: Как работают пакеты загрузки Windows Media (не рекомендуется)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Метафайлы Windows Media, пакеты загрузки Windows Media
- Проигрыватель Windows Media, пакеты загрузки Windows Media
- Метафайлы, пакеты загрузки Windows Media
- Windows Media, Загрузка пакетов Windows Media
- Пакеты загрузки Windows Media, сведения
- Пакеты загрузки Windows Media, принципы работы пакетов
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132911"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a><span data-ttu-id="0e1c8-109">Как работают пакеты загрузки Windows Media (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="0e1c8-109">How Windows Media Download Packages Work (deprecated)</span></span>

<span data-ttu-id="0e1c8-110">Эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрывателя Windows Media и Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="0e1c8-111">Пакет загрузки Windows Media запускается с веб-сайта, когда пользователь щелкает ссылку в веб-браузере, например Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-111">A Windows Media Download package is launched from a website when a user clicks a link in a Web browser, such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="0e1c8-112">Это действие открывает проигрыватель Windows Media, а затем скачивает и отменяет упаковку пакета загрузки Windows Media на жестком диске пользователя в папке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-112">This action opens Windows Media Player and then downloads and un-packages the Windows Media Download package on the user's hard disk in a default folder.</span></span>

<span data-ttu-id="0e1c8-113">После извлечения файлов из пакета скачивания Windows Media Player находит список воспроизведения метафайлов Windows Media с расширением. ASX в упакованных файлах.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-113">Once the files have been extracted from the Windows Media Download package, Windows Media Player locates a Windows Media metafile playlist with an .asx file name extension among the packaged files.</span></span> <span data-ttu-id="0e1c8-114">Если такой объект найден, проигрыватель создает список воспроизведения на основе включенного метафайла.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-114">If it finds one, the Player creates a playlist based on the included metafile.</span></span> <span data-ttu-id="0e1c8-115">Файлы, содержащие мультимедийное содержимое, затем добавляются в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-115">Files that contain multimedia content are then added to the library.</span></span>

<span data-ttu-id="0e1c8-116">Проигрыватель Windows Media также ищет элемент **обложки** в метафайле.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-116">Windows Media Player also looks for a **SKIN** element in the metafile.</span></span> <span data-ttu-id="0e1c8-117">Если элемент **Skin** содержит ссылку на файл границы с расширением WMZ, проигрыватель загружает границу **в область текущий** .</span><span class="sxs-lookup"><span data-stu-id="0e1c8-117">If the **SKIN** element contains a reference to a border file with a .wmz file name extension, the Player loads the border into the **Now Playing** pane.</span></span> <span data-ttu-id="0e1c8-118">Затем проигрыватель начинает воспроизводить содержимое, указанное в пакете.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-118">The Player then starts to play the content provided in the package.</span></span>

<span data-ttu-id="0e1c8-119">На следующей схеме показано, как содержимое упаковывается в файл загрузки Windows Media, отправляется на веб-сайт, загружается и воспроизводится на клиентском компьютере с помощью проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-119">The following diagram shows how content is packaged in a Windows Media Download file, posted to a website, downloaded, and played on a client computer using Windows Media Player.</span></span>

![получение и воспроизведение файла загрузки Windows Media.](images/wmd-image.png) <span data-ttu-id="0e1c8-121">Загрузка Windows Media</span><span class="sxs-lookup"><span data-stu-id="0e1c8-121">Windows Media Download</span></span>

<span data-ttu-id="0e1c8-122">В следующей таблице описаны три элемента, которые составляют пакет загрузки Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-122">The following table describes the three elements that make up a Windows Media Download package.</span></span>



| <span data-ttu-id="0e1c8-123">Элемент Package</span><span class="sxs-lookup"><span data-stu-id="0e1c8-123">Package element</span></span>    | <span data-ttu-id="0e1c8-124">Функция</span><span class="sxs-lookup"><span data-stu-id="0e1c8-124">Function</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="0e1c8-125">Расширения имен файлов</span><span class="sxs-lookup"><span data-stu-id="0e1c8-125">File name extensions</span></span>                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="0e1c8-126">Рамка</span><span class="sxs-lookup"><span data-stu-id="0e1c8-126">Border</span></span>             | <span data-ttu-id="0e1c8-127">Фиксированный, настраиваемый пользовательский интерфейс, созданный владельцем содержимого для отображения, связывания и воспроизведения всех файлов мультимедиа, упакованных в пакет загрузки Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-127">A fixed, customized user interface created by the content owner for displaying, linking, and playing all media packaged in the Windows Media Download package.</span></span> <span data-ttu-id="0e1c8-128">Методы, используемые для создания границ, похожи на те, которые используются для создания обложек.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-128">The techniques used to create borders are similar to those used to create skins.</span></span> | <span data-ttu-id="0e1c8-129">.wmz</span><span class="sxs-lookup"><span data-stu-id="0e1c8-129">.wmz</span></span>                                     |
| <span data-ttu-id="0e1c8-130">Список воспроизведения метафайлов</span><span class="sxs-lookup"><span data-stu-id="0e1c8-130">Metafile Playlist</span></span>  | <span data-ttu-id="0e1c8-131">Метафайл Windows Media, который содержит элементы **записи** , сведения о списках воспроизведения и удостоверение элемента **обложки** для файлов содержимого.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-131">A Windows Media metafile that contains **ENTRY** elements, playlist information, and a **SKIN** element identity for content files.</span></span>                                                                                                             | <span data-ttu-id="0e1c8-132">.asx</span><span class="sxs-lookup"><span data-stu-id="0e1c8-132">.asx</span></span>                                     |
| <span data-ttu-id="0e1c8-133">Мультимедийное содержимое</span><span class="sxs-lookup"><span data-stu-id="0e1c8-133">Multimedia Content</span></span> | <span data-ttu-id="0e1c8-134">Файл, содержащий формат аудио или видео, поддерживаемый проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0e1c8-134">A file containing any audio or video format that is supported by Windows Media Player.</span></span>                                                                                                                                                          | <span data-ttu-id="0e1c8-135">. WMA,. WMV,. ASF,. wav,. AVI,. mpg,. mp3</span><span class="sxs-lookup"><span data-stu-id="0e1c8-135">.wma, .wmv, .asf, .wav, .avi, .mpg, .mp3</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0e1c8-136">См. также</span><span class="sxs-lookup"><span data-stu-id="0e1c8-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e1c8-137">**Пакеты загрузки Windows Media (устарели)**</span><span class="sxs-lookup"><span data-stu-id="0e1c8-137">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




