---
title: Создание списков воспроизведения метафайлов
description: Создание списков воспроизведения метафайлов
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Списки воспроизведения метафайлов Windows Media, создание
- списки воспроизведения, создание
- списки воспроизведения метафайлов, создание
- Создание списков воспроизведения метафайлов Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258767"
---
# <a name="creating-metafile-playlists"></a><span data-ttu-id="b7385-107">Создание списков воспроизведения метафайлов</span><span class="sxs-lookup"><span data-stu-id="b7385-107">Creating Metafile Playlists</span></span>

<span data-ttu-id="b7385-108">Список воспроизведения можно создать с помощью любого текстового редактора, например Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="b7385-108">You can create a playlist using any text editor, such as Microsoft Notepad.</span></span> <span data-ttu-id="b7385-109">Откройте текстовый редактор.</span><span class="sxs-lookup"><span data-stu-id="b7385-109">Open your text editor.</span></span> <span data-ttu-id="b7385-110">Введите записи скрипта, которые требуется реализовать.</span><span class="sxs-lookup"><span data-stu-id="b7385-110">Type the script entries you want to implement.</span></span> <span data-ttu-id="b7385-111">После завершения ввода в блокнот сохраните файл с соответствующим именем файла и расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="b7385-111">After you have finished typing into Notepad, save the file with an appropriate file name and file name extension.</span></span> <span data-ttu-id="b7385-112">Дополнительные сведения о расширениях см. в разделе [рекомендации по расширению метафайлов](metafile-extension-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="b7385-112">For more information about extensions, see [Metafile Extension Guidelines](metafile-extension-guidelines.md).</span></span> <span data-ttu-id="b7385-113">Обычно имя файла — это имя файла или потока Windows Media, за которым следует расширение. мастика,. ввкс или. ASX.</span><span class="sxs-lookup"><span data-stu-id="b7385-113">Typically the file name is the name of the Windows Media file or stream followed by an extension of .wax, .wvx, or .asx.</span></span> <span data-ttu-id="b7385-114">Например, если содержимое мультимедиа представляет собой звуковой файл Windows Media с расширением WMA, используйте расширение. мастика при именовании списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b7385-114">For example, if your media content is a Windows Media audio file that has a .wma extension, use the .wax extension when naming the playlist.</span></span> <span data-ttu-id="b7385-115">Списки воспроизведения не должны содержать коды форматирования из текстового редактора, например Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="b7385-115">Playlists must not include any formatting codes from a word processor, such as Microsoft Word.</span></span> <span data-ttu-id="b7385-116">Чтобы не допустить включения в список воспроизведения кодов форматирования, сохраните файл как обычный текстовый или ASCII-файл.</span><span class="sxs-lookup"><span data-stu-id="b7385-116">To be sure no formatting codes are included in the playlist, save the file as a plain text or ASCII file.</span></span>

> [!Note]  
> <span data-ttu-id="b7385-117">Элементы и атрибуты не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="b7385-117">Elements and attributes are not case sensitive.</span></span> <span data-ttu-id="b7385-118">Текст, используемый в списке воспроизведения для определения элемента или атрибута, может быть либо прописной, либо строчной буквой, либо сочетанием обоих типов.</span><span class="sxs-lookup"><span data-stu-id="b7385-118">The text used in the playlist to define an element or attribute can be either uppercase or lowercase, or a mixture of both.</span></span>

 

<span data-ttu-id="b7385-119">Если элемент не имеет дочерних элементов (тех, которые изменяют или содержатся в другом элементе), в конце открывающего тега можно использовать один символ косой черты (/) непосредственно перед ">" вместо закрывающего тега.</span><span class="sxs-lookup"><span data-stu-id="b7385-119">If an element does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag, just before the '>', in place of a closing tag.</span></span> <span data-ttu-id="b7385-120">Дочерние элементы элемента должны находиться между открывающим и закрывающим тегом этого элемента. в противном случае они не являются дочерними элементами для этого элемента и не учитываются или вызывают ошибку в синтаксисе списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b7385-120">Child elements of an element must appear between the opening and closing tag for that element; otherwise they are not child elements for that element, and are ignored or cause an error in the syntax of the playlist.</span></span>

<span data-ttu-id="b7385-121">Первые четыре символа списка воспроизведения должны быть " &lt; ASX".</span><span class="sxs-lookup"><span data-stu-id="b7385-121">The first four characters of a playlist must be "&lt;ASX".</span></span> <span data-ttu-id="b7385-122">Элемент **ASX** используется во всех списках воспроизведения, независимо от того, имеет ли их расширение. мастика,. ввкс или. ASX.</span><span class="sxs-lookup"><span data-stu-id="b7385-122">The **ASX** element is used in all playlists whether their extension is .wax, .wvx, or .asx.</span></span> <span data-ttu-id="b7385-123">В списке воспроизведения должен быть только один элемент **ASX** .</span><span class="sxs-lookup"><span data-stu-id="b7385-123">There must be only one **ASX** element per playlist.</span></span> <span data-ttu-id="b7385-124">Этот элемент определяет файл как список воспроизведения метафайла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b7385-124">This element identifies the file as a Windows Media metafile playlist.</span></span> <span data-ttu-id="b7385-125">Он не указывает тип списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b7385-125">It does not specify the type of playlist.</span></span>

<span data-ttu-id="b7385-126">Элемент **ASX** имеет три возможных атрибута:</span><span class="sxs-lookup"><span data-stu-id="b7385-126">The **ASX** element has three possible attributes:</span></span>

<span data-ttu-id="b7385-127">**VERSION**</span><span class="sxs-lookup"><span data-stu-id="b7385-127">**VERSION**</span></span>

<span data-ttu-id="b7385-128">Атрибут **Version** является обязательным и должен следовать непосредственно после элемента **ASX** , например "<ASX Version =" 3,0 " &gt; ".</span><span class="sxs-lookup"><span data-stu-id="b7385-128">The **VERSION** attribute is required and must follow immediately after the **ASX** element, for example "<ASX version = "3.0"&gt;".</span></span> <span data-ttu-id="b7385-129">Номер текущей версии — 3,0.</span><span class="sxs-lookup"><span data-stu-id="b7385-129">The current version number is 3.0.</span></span> <span data-ttu-id="b7385-130">Проигрыватель Windows Media поддерживает все предыдущие версии.</span><span class="sxs-lookup"><span data-stu-id="b7385-130">Windows Media Player supports all previous versions.</span></span> <span data-ttu-id="b7385-131">Допустимые значения для атрибута **Version** : 3,0 и 3 (без десятичной запятой).</span><span class="sxs-lookup"><span data-stu-id="b7385-131">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="b7385-132">**PREVIEWMODE**</span><span class="sxs-lookup"><span data-stu-id="b7385-132">**PREVIEWMODE**</span></span>

<span data-ttu-id="b7385-133">Атрибут **PREVIEWMODE** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b7385-133">The **PREVIEWMODE** attribute is optional.</span></span> <span data-ttu-id="b7385-134">Он предоставляет еще один механизм для указания времени отрисовки клипа.</span><span class="sxs-lookup"><span data-stu-id="b7385-134">It provides another mechanism for specifying how long to render a clip.</span></span> <span data-ttu-id="b7385-135">Если значение атрибута **PREVIEWMODE** равно Yes, проигрыватель Windows Media выполнит визуализацию каждого клипа в течение времени, указанного в элементе **превиевдуратион**.</span><span class="sxs-lookup"><span data-stu-id="b7385-135">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player will render each clip for the duration specified by the element **PREVIEWDURATION**.</span></span> <span data-ttu-id="b7385-136">Для каждого клипа может быть указан **превиевдуратион** .</span><span class="sxs-lookup"><span data-stu-id="b7385-136">Each clip can have a **PREVIEWDURATION** specified.</span></span>

<span data-ttu-id="b7385-137">**баннербар**</span><span class="sxs-lookup"><span data-stu-id="b7385-137">**BANNERBAR**</span></span>

<span data-ttu-id="b7385-138">Необязательный атрибут **баннербар** определяет, резервирует ли элемент управления проигрывателя Windows Media пространство для изображения баннера.</span><span class="sxs-lookup"><span data-stu-id="b7385-138">The optional **BANNERBAR** attribute defines whether the Windows Media Player control reserves space for a banner graphic.</span></span> <span data-ttu-id="b7385-139">(Используйте элемент **баннера** , чтобы указать изображение для отображения.) Если значение **баннербар** является фиксированным, проигрыватель Windows Media резервирует место для отображения и для каждого клипа, если в списке воспроизведения метафайла указан баннер для отображения или клипа.</span><span class="sxs-lookup"><span data-stu-id="b7385-139">(Use the **BANNER** element to specify the graphic to display.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for the show and for every clip, whether the metafile playlist specifies a banner for the show or clip.</span></span> <span data-ttu-id="b7385-140">При этом размер окна проигрывателя Windows Media будет одинаковым (за исключением изменения размера видео), независимо от отсутствия или наличия изображения баннера.</span><span class="sxs-lookup"><span data-stu-id="b7385-140">This will keep the size of the Windows Media Player window the same (except when the video size changes) regardless of the absence or presence of a banner graphic.</span></span> <span data-ttu-id="b7385-141">Если у представления или клипа нет связанного с ним баннера, то пространство, зарезервированное для одного, является черным.</span><span class="sxs-lookup"><span data-stu-id="b7385-141">If the show or clip does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="b7385-142">Если значение атрибута **баннербар** равно Auto, проигрыватель Windows Media резервирует пространство для баннера только в том случае, если оно включает в себя или клип.</span><span class="sxs-lookup"><span data-stu-id="b7385-142">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the show or clip includes one.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



<span data-ttu-id="b7385-143">Дополнительные сведения о трех атрибутах элемента **ASX** см. в записи справочника по [элементу ASX](asx-element.md).</span><span class="sxs-lookup"><span data-stu-id="b7385-143">For more information about the three attributes of the **ASX** element, see the reference entry for the [ASX Element](asx-element.md).</span></span>

<span data-ttu-id="b7385-144">Элемент **ASX** содержит дочерние элементы **записи** , определяющие сведения о файлах мультимедиа, к которым осуществляется доступ.</span><span class="sxs-lookup"><span data-stu-id="b7385-144">An **ASX** element contains **ENTRY** child elements that define information about the media files to be accessed.</span></span> <span data-ttu-id="b7385-145">Каждый элемент **entry** должен содержать элемент **ref** , указывающий путь к файлу мультимедиа для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="b7385-145">Each **ENTRY** element must contain a **REF** element that specifies the path to the media file to be streamed.</span></span> <span data-ttu-id="b7385-146">В элементе **ASX** должен быть по крайней мере один элемент **entry** или **ентриреф** .</span><span class="sxs-lookup"><span data-stu-id="b7385-146">There must be at least one **ENTRY** or **ENTRYREF** element within an **ASX** element.</span></span>

<span data-ttu-id="b7385-147">Другие элементы, определенные в области элемента **ASX** , такие как **Title** и **Author**, связаны с метаданными, отображаемыми проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b7385-147">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the metadata displayed by Windows Media Player.</span></span>

<span data-ttu-id="b7385-148">Простейшие списки воспроизведения создаются путем добавления нескольких элементов **записи** с одним элементом **ref** в метафайл.</span><span class="sxs-lookup"><span data-stu-id="b7385-148">The simplest playlists are created by adding multiple **ENTRY** elements with a single **REF** element to a metafile.</span></span> <span data-ttu-id="b7385-149">Каждый элемент **entry** в списке воспроизведения метафайлов отображается в том порядке, в котором он отображается в файле, как будто пользователь вручную открывал каждый клип.</span><span class="sxs-lookup"><span data-stu-id="b7385-149">Each **ENTRY** element in a metafile playlist is rendered in the order it appears in the file as though the user had manually opened each clip.</span></span>

<span data-ttu-id="b7385-150">Пример кода</span><span class="sxs-lookup"><span data-stu-id="b7385-150">Example Code</span></span>


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



<span data-ttu-id="b7385-151">Убедитесь, что список воспроизведения работает, дважды щелкнув его в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="b7385-151">Be sure that the playlist is working by double-clicking it in Windows Explorer.</span></span> <span data-ttu-id="b7385-152">Проигрыватель Windows Media должен открыть и начать потоковую передачу содержимого мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b7385-152">Windows Media Player should open and start streaming the media content.</span></span> <span data-ttu-id="b7385-153">После подтверждения того, что список воспроизведения будет работать, сохраните его на веб-сервере вместе со страницами, а затем свяжите с ним с помощью элемента **href** или внедрите его на странице, используя элемент **объекта** проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b7385-153">After you have confirmed that the playlist works, save it to your web server along with your webpages, and link to it by means of an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** element.</span></span>

<span data-ttu-id="b7385-154">Дополнительные сведения содержатся в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="b7385-154">The following sections contain more information:</span></span>

-   [<span data-ttu-id="b7385-155">Вложенные метафайлы</span><span class="sxs-lookup"><span data-stu-id="b7385-155">Nesting Metafiles</span></span>](nesting-metafiles.md)
-   [<span data-ttu-id="b7385-156">Динамическое создание списков воспроизведения метафайлов Windows Media с помощью страниц ASP</span><span class="sxs-lookup"><span data-stu-id="b7385-156">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="b7385-157">См. также</span><span class="sxs-lookup"><span data-stu-id="b7385-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7385-158">**Элемент БАННЕРа**</span><span class="sxs-lookup"><span data-stu-id="b7385-158">**BANNER Element**</span></span>](banner-element.md)
</dt> <dt>

[<span data-ttu-id="b7385-159">**Примеры списков воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="b7385-159">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="b7385-160">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b7385-160">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b7385-161">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b7385-161">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




