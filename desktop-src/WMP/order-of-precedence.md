---
title: Очередность выполнения
description: Очередность выполнения
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Метафайлы Windows Media, порядок приоритета
- Метафайлы Windows Media, приоритет
- Метафайлы, порядок приоритетов
- Метафайлы, приоритет
- Windows Media, метафайлы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067627"
---
# <a name="order-of-precedence"></a><span data-ttu-id="473e9-108">Очередность выполнения</span><span class="sxs-lookup"><span data-stu-id="473e9-108">Order of Precedence</span></span>

<span data-ttu-id="473e9-109">Не все атрибуты элемента метафайла создаются равными.</span><span class="sxs-lookup"><span data-stu-id="473e9-109">Not all metafile element attributes are created equal.</span></span> <span data-ttu-id="473e9-110">Некоторые атрибуты элемента метафайла переопределяют другие атрибуты элемента.</span><span class="sxs-lookup"><span data-stu-id="473e9-110">Some metafile element attributes override other element attributes.</span></span> <span data-ttu-id="473e9-111">Атрибуты элементов могут быть переопределены аналогичными атрибутами элементов в зависимости от порядка и расположения.</span><span class="sxs-lookup"><span data-stu-id="473e9-111">Element attributes can be overridden by similar element attributes depending on position and order.</span></span> <span data-ttu-id="473e9-112">Все атрибуты списка воспроизведения метафайлов переопределяют те, которые содержатся в файле Windows Media, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="473e9-112">Any attributes of a metafile playlist override those contained in a referenced Windows Media file.</span></span> <span data-ttu-id="473e9-113">Атрибут, переопределяющий другой, имеет более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="473e9-113">An attribute that overrides another has higher precedence.</span></span>

<span data-ttu-id="473e9-114">В следующей таблице показана иерархия с наивысшим приоритетом «низкий».</span><span class="sxs-lookup"><span data-stu-id="473e9-114">The hierarchy, highest precedence to lowest, is shown in the following table.</span></span> <span data-ttu-id="473e9-115">Элемент с наивысшим приоритетом никогда не переопределяется.</span><span class="sxs-lookup"><span data-stu-id="473e9-115">The highest precedence item is never overridden.</span></span>



| <span data-ttu-id="473e9-116">Область</span><span class="sxs-lookup"><span data-stu-id="473e9-116">Scope</span></span>                    | <span data-ttu-id="473e9-117">Иерархия</span><span class="sxs-lookup"><span data-stu-id="473e9-117">Hierarchy</span></span>                                   |
|--------------------------|---------------------------------------------|
| <span data-ttu-id="473e9-118">"Подписанное содержимое DRM"</span><span class="sxs-lookup"><span data-stu-id="473e9-118">"Signed DRM content"</span></span>     | <span data-ttu-id="473e9-119">Никогда не переопределяется.</span><span class="sxs-lookup"><span data-stu-id="473e9-119">Never overridden.</span></span>                           |
| <span data-ttu-id="473e9-120">Область элемента **ref**</span><span class="sxs-lookup"><span data-stu-id="473e9-120">**REF** element scope</span></span>    | <span data-ttu-id="473e9-121">Переопределено только подписанным содержимым DRM.</span><span class="sxs-lookup"><span data-stu-id="473e9-121">Only overridden by signed DRM content.</span></span>      |
| <span data-ttu-id="473e9-122">Область элемента **entry**</span><span class="sxs-lookup"><span data-stu-id="473e9-122">**ENTRY** element scope</span></span>  | <span data-ttu-id="473e9-123">Переопределяет элементы категорий ниже.</span><span class="sxs-lookup"><span data-stu-id="473e9-123">Overrides elements of the categories below.</span></span> |
| <span data-ttu-id="473e9-124">Область **ASX**</span><span class="sxs-lookup"><span data-stu-id="473e9-124">**ASX** scope</span></span>            | <span data-ttu-id="473e9-125">Переопределяет элементы файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="473e9-125">Overrides media file elements.</span></span>              |
| <span data-ttu-id="473e9-126">Область файла Windows Media</span><span class="sxs-lookup"><span data-stu-id="473e9-126">Windows Media file scope</span></span> | <span data-ttu-id="473e9-127">Переопределено всеми перечисленными выше.</span><span class="sxs-lookup"><span data-stu-id="473e9-127">Overridden by all of the above.</span></span>             |



 

-   <span data-ttu-id="473e9-128">"Подписанное содержимое DRM" — объект цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="473e9-128">"Signed DRM content" - Digital signature object.</span></span>

    <span data-ttu-id="473e9-129">Атрибуты подписанного содержимого DRM будут переопределять все остальные.</span><span class="sxs-lookup"><span data-stu-id="473e9-129">Attributes of Signed DRM content will override all others.</span></span> <span data-ttu-id="473e9-130">Например, информация об авторских правах "подписанное содержимое DRM" не будет переопределена.</span><span class="sxs-lookup"><span data-stu-id="473e9-130">For example, the Copyright information of "Signed DRM content" will not be overridden.</span></span> <span data-ttu-id="473e9-131">Он всегда будет передаваться в потоковом режиме и представлен.</span><span class="sxs-lookup"><span data-stu-id="473e9-131">It will always be streamed and presented.</span></span>

-   <span data-ttu-id="473e9-132">Область элемента **ref**</span><span class="sxs-lookup"><span data-stu-id="473e9-132">**REF** element scope</span></span>

    <span data-ttu-id="473e9-133">Атрибуты элемента **ref** будут переопределять другие атрибуты элемента, но не подписанное содержимое DRM.</span><span class="sxs-lookup"><span data-stu-id="473e9-133">Attributes of the **REF** element will override other element attributes, but not signed DRM content.</span></span>

-   <span data-ttu-id="473e9-134">Область **ввода**</span><span class="sxs-lookup"><span data-stu-id="473e9-134">**ENTRY** scope</span></span>

    <span data-ttu-id="473e9-135">Атрибуты элемента **entry** будут переопределены атрибутом **ref** element, но будут переопределять другие атрибуты элемента.</span><span class="sxs-lookup"><span data-stu-id="473e9-135">Attributes of the **ENTRY** element will be overridden by the **REF** element attribute but will override other element attributes.</span></span> <span data-ttu-id="473e9-136">Метаданные **заголовка** из элемента **entry** отображаются вместо сведений о заголовке из файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="473e9-136">**TITLE** metadata from the **ENTRY** element is displayed instead of the title information from the media file.</span></span>

-   <span data-ttu-id="473e9-137">Область **ASX**</span><span class="sxs-lookup"><span data-stu-id="473e9-137">**ASX** scope</span></span>

    <span data-ttu-id="473e9-138">Все свойства, которые были указаны в метафайле, переопределяют параметры, содержащиеся в файле Windows Media.</span><span class="sxs-lookup"><span data-stu-id="473e9-138">Any properties that are entered in the metafile override those contained in the Windows Media file.</span></span> <span data-ttu-id="473e9-139">Атрибуты элемента **entry** переопределяют атрибуты элемента **ASX** .</span><span class="sxs-lookup"><span data-stu-id="473e9-139">Attributes of the **ENTRY** element override **ASX** element attributes.</span></span> <span data-ttu-id="473e9-140">Во время воспроизведения клипа **мультимедиа, на** который указывает ссылка, метаданные **заголовка** из элемента **entry** отображаются вместо сведений о заголовке из элемента **ASX** .</span><span class="sxs-lookup"><span data-stu-id="473e9-140">While the **ENTRY** element's referenced media clip is playing, **TITLE** metadata from the **ENTRY** element is displayed instead of title information from the **ASX** element.</span></span>

-   <span data-ttu-id="473e9-141">Область файла Windows Media</span><span class="sxs-lookup"><span data-stu-id="473e9-141">Windows Media file scope</span></span>

    <span data-ttu-id="473e9-142">Атрибуты файла Windows Media переопределяются любыми атрибутами метафайлов.</span><span class="sxs-lookup"><span data-stu-id="473e9-142">Attributes of the Windows Media file are overridden by any metafile attributes.</span></span> <span data-ttu-id="473e9-143">Метаданные файлов мультимедиа отображаются, только если для этого элемента в метафайле не определены метаданные.</span><span class="sxs-lookup"><span data-stu-id="473e9-143">Media file metadata is displayed only if there is no metadata defined for that element in the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="473e9-144">См. также</span><span class="sxs-lookup"><span data-stu-id="473e9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="473e9-145">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="473e9-145">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="473e9-146">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="473e9-146">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="473e9-147">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="473e9-147">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="473e9-148">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="473e9-148">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




