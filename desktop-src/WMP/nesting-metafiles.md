---
title: Вложенные метафайлы
description: Вложенные метафайлы
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Метафайлы Windows Media, вложение
- Метафайлы Windows Media, ссылающиеся на другие метафайлы
- вложенные метафайлы
- Метафайлы, вложение
- Метафайлы, ссылки на другие метафайлы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cd5743424858c4bbcd6f66952f4275ea82d947e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328576"
---
# <a name="nesting-metafiles"></a><span data-ttu-id="e5bac-108">Вложенные метафайлы</span><span class="sxs-lookup"><span data-stu-id="e5bac-108">Nesting Metafiles</span></span>

<span data-ttu-id="e5bac-109">Метафайл может ссылаться на другой метафайл.</span><span class="sxs-lookup"><span data-stu-id="e5bac-109">A metafile can reference another metafile.</span></span> <span data-ttu-id="e5bac-110">Чтобы сослаться на другой метафайл, используйте элемент **ентриреф** .</span><span class="sxs-lookup"><span data-stu-id="e5bac-110">To reference another metafile, use the **ENTRYREF** element.</span></span> <span data-ttu-id="e5bac-111">Элемент **ентриреф** в основном метафайле указывает на внешний метафайл.</span><span class="sxs-lookup"><span data-stu-id="e5bac-111">An **ENTRYREF** element in the primary metafile points to an external metafile.</span></span>

<span data-ttu-id="e5bac-112">Элемент управления проигрывателя Windows Media обрабатывает элементы **записи** метафайла, на который указывает ссылка, как если бы они были добавлены в основной метафайл в позиции элемента **ентриреф** .</span><span class="sxs-lookup"><span data-stu-id="e5bac-112">The Windows Media Player control processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="e5bac-113">Однако он пропускает все элементы **записи** в метафайле, на который указывает ссылка, для которого атрибут **СКИПИФРЕФ** имеет значение Да.</span><span class="sxs-lookup"><span data-stu-id="e5bac-113">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="e5bac-114">Проигрыватель Windows Media 7,0, 7,1 и проигрыватель Windows Media для Windows XP игнорируют все элементы **ентриреф** в метафайле, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="e5bac-114">The Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP controls ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="e5bac-115">Таким словами, метафайлы могут быть вложенными только на одном уровне с использованием этих версий.</span><span class="sxs-lookup"><span data-stu-id="e5bac-115">Thus, metafiles can only be nested one level deep using these versions.</span></span> <span data-ttu-id="e5bac-116">Эти версии также игнорируют элемент **ASX** и его атрибуты в файле, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="e5bac-116">These versions also ignore the **ASX** element and its attributes in the referenced file.</span></span> <span data-ttu-id="e5bac-117">Проигрыватель Windows Media 9 Series или более поздней версии поддерживает вложение метафайлов размером до 5 уровней.</span><span class="sxs-lookup"><span data-stu-id="e5bac-117">Windows Media Player 9 Series or later supports nesting metafiles up to 5 deep.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5bac-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e5bac-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5bac-119">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="e5bac-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




