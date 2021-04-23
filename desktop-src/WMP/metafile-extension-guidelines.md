---
title: Рекомендации по расширению метафайлов
description: Рекомендации по расширению метафайлов
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Метафайлы Windows Media, расширения
- Метафайлы Windows Media, расширения имен файлов
- Метафайлы, расширения
- Метафайлы, расширения имен файлов
- Windows Media, метафайлы
- расширения имен файлов для метафайлов Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068548"
---
# <a name="metafile-extension-guidelines"></a><span data-ttu-id="58398-109">Рекомендации по расширению метафайлов</span><span class="sxs-lookup"><span data-stu-id="58398-109">Metafile Extension Guidelines</span></span>

<span data-ttu-id="58398-110">Расширение имени файла предоставляет независимому поставщику программного обеспечения (ISV) сведения о требованиях к отрисовке приложения, использующего расширение, и позволяет авторам содержимого ориентироваться на общие типы игроков.</span><span class="sxs-lookup"><span data-stu-id="58398-110">A file name extension provides an independent software vendor (ISV) with information about the rendering requirements of an application that uses the extension, and enables content authors to target general types of players.</span></span>

<span data-ttu-id="58398-111">Расширения Windows Media Metafile Names используются для задания формата файлов Windows Media, на которые ссылается метафайл.</span><span class="sxs-lookup"><span data-stu-id="58398-111">Windows Media metafile name extensions are used to identify the format of the Windows Media files that a metafile references.</span></span> <span data-ttu-id="58398-112">Метафайлы Windows Media с расширениями. мастика,. ввкс или. ASX имеют справочные файлы с расширениями WMA, WMV и ASF соответственно.</span><span class="sxs-lookup"><span data-stu-id="58398-112">Windows Media metafiles with .wax, .wvx, or .asx extensions reference files with .wma, .wmv, and .asf extensions, respectively.</span></span> <span data-ttu-id="58398-113">Все метафайлы, вне зависимости от используемого расширения имени файла, имеют тег элемента **ASX** в начале файла с указанным атрибутом **Version** .</span><span class="sxs-lookup"><span data-stu-id="58398-113">All metafiles, regardless of the file name extension used, have the **ASX** element tag at the beginning of the file with the **version** attribute specified.</span></span>

<span data-ttu-id="58398-114">В следующей таблице показаны типы файлов мультимедиа, на которые ссылается каждый тип расширения имени файла метафайла.</span><span class="sxs-lookup"><span data-stu-id="58398-114">The following table shows the media file types referenced by each type of metafile file name extension.</span></span> <span data-ttu-id="58398-115">В столбцах перечислены расширения имен файлов мультимедиа, в которых перечислены расширения метафайлов.</span><span class="sxs-lookup"><span data-stu-id="58398-115">The columns list media file name extensions, the rows list metafile name extensions.</span></span> <span data-ttu-id="58398-116">X в столбце указывает тип файла мультимедиа, на который может ссылаться конкретное расширение файла метафайла.</span><span class="sxs-lookup"><span data-stu-id="58398-116">An X in a column indicates a media file type that can be referenced by a particular metafile file name extension.</span></span>



| <span data-ttu-id="58398-117">Расширение</span><span class="sxs-lookup"><span data-stu-id="58398-117">Extension</span></span> | <span data-ttu-id="58398-118">.asf</span><span class="sxs-lookup"><span data-stu-id="58398-118">.asf</span></span> | <span data-ttu-id="58398-119">.wma</span><span class="sxs-lookup"><span data-stu-id="58398-119">.wma</span></span> | <span data-ttu-id="58398-120">.wmv</span><span class="sxs-lookup"><span data-stu-id="58398-120">.wmv</span></span> |
|-----------|------|------|------|
| <span data-ttu-id="58398-121">. ввкс</span><span class="sxs-lookup"><span data-stu-id="58398-121">.wvx</span></span>      | <span data-ttu-id="58398-122">X</span><span class="sxs-lookup"><span data-stu-id="58398-122">X</span></span>    | <span data-ttu-id="58398-123">X</span><span class="sxs-lookup"><span data-stu-id="58398-123">X</span></span>    | <span data-ttu-id="58398-124">X</span><span class="sxs-lookup"><span data-stu-id="58398-124">X</span></span>    |
| <span data-ttu-id="58398-125">. мастика</span><span class="sxs-lookup"><span data-stu-id="58398-125">.wax</span></span>      | <span data-ttu-id="58398-126">X</span><span class="sxs-lookup"><span data-stu-id="58398-126">X</span></span>    | <span data-ttu-id="58398-127">X</span><span class="sxs-lookup"><span data-stu-id="58398-127">X</span></span>    |      |
| <span data-ttu-id="58398-128">.asx</span><span class="sxs-lookup"><span data-stu-id="58398-128">.asx</span></span>      | <span data-ttu-id="58398-129">X</span><span class="sxs-lookup"><span data-stu-id="58398-129">X</span></span>    |      |      |



 

## <a name="related-topics"></a><span data-ttu-id="58398-130">См. также</span><span class="sxs-lookup"><span data-stu-id="58398-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58398-131">**Расширения файлов**</span><span class="sxs-lookup"><span data-stu-id="58398-131">**File Name Extensions**</span></span>](file-name-extensions.md)
</dt> <dt>

[<span data-ttu-id="58398-132">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="58398-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="58398-133">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="58398-133">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




