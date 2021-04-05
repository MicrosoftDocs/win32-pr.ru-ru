---
title: Поддержка нескольких языков
description: Поддержка нескольких языков
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Списки воспроизведения метафайлов Windows Media, поддержка нескольких языков
- списки воспроизведения метафайлов, поддержка нескольких языков
- списки воспроизведения, поддержка нескольких языков
- Списки воспроизведения метафайлов Windows Media, поддержка нескольких языков
- списки воспроизведения метафайлов, поддержка нескольких языков
- списки воспроизведения, поддержка нескольких языков
- Списки воспроизведения метафайлов Windows Media, поддержка языков
- списки воспроизведения метафайлов, поддержка языков
- списки воспроизведения, языковая поддержка
- Поддержка нескольких языков
- поддержка нескольких языков
- поддержка языка
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068455"
---
# <a name="support-for-multiple-languages"></a><span data-ttu-id="eb305-115">Поддержка нескольких языков</span><span class="sxs-lookup"><span data-stu-id="eb305-115">Support for Multiple Languages</span></span>

<span data-ttu-id="eb305-116">Проигрыватель Windows Media 9 Series или более поздней версии поддерживает метафайлы Windows Media, созданные с помощью набора символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="eb305-116">Windows Media Player 9 Series or later supports Windows Media metafiles created using the Unicode character set.</span></span> <span data-ttu-id="eb305-117">Это позволяет включать в список воспроизведения метафайлов многоязыковые метаданные.</span><span class="sxs-lookup"><span data-stu-id="eb305-117">This allows you to include multilingual metadata in your metafile playlist.</span></span> <span data-ttu-id="eb305-118">Следующие правила управляют использованием многоязыковых метаданных в метафайлах Windows Media:</span><span class="sxs-lookup"><span data-stu-id="eb305-118">The following rules govern the use of multilingual metadata in Windows Media metafiles:</span></span>

-   <span data-ttu-id="eb305-119">Символы должны быть закодированы с помощью схемы кодировки UTF-8.</span><span class="sxs-lookup"><span data-stu-id="eb305-119">Characters must be encoded using the UTF-8 encoding scheme.</span></span>
-   <span data-ttu-id="eb305-120">Список воспроизведения метафайлов должен включать следующий **параметр** на уровне списка воспроизведения:</span><span class="sxs-lookup"><span data-stu-id="eb305-120">The metafile playlist must include the following **PARAM** at the playlist level:</span></span>
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   <span data-ttu-id="eb305-121">Эта функция поддерживается только в проигрывателе Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="eb305-121">Only Windows Media Player 9 Series or later supports this functionality.</span></span>
-   <span data-ttu-id="eb305-122">Если список воспроизведения метафайлов не сохранен с кодировкой UTF-8 и корректным элементом **param** , он будет проанализирован с помощью кодовой страницы локального компьютера пользователя, используемой по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eb305-122">If the metafile playlist is not saved with UTF-8 encoding and the correct **PARAM** element, it will be parsed using the default system locale code page of the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb305-123">См. также</span><span class="sxs-lookup"><span data-stu-id="eb305-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb305-124">**PARAM, элемент**</span><span class="sxs-lookup"><span data-stu-id="eb305-124">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="eb305-125">**Общие сведения о метафайлах Windows Media**</span><span class="sxs-lookup"><span data-stu-id="eb305-125">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




