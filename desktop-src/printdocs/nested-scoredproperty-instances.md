---
description: Экземпляры Скоредпроперти также могут быть вложенными в другие экземпляры Скоредпроперти или как дочерние элементы экземпляра Option.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Вложенные экземпляры Скоредпроперти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a80d291fa59b2f36191f42b2f99ea9d22789a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408607"
---
# <a name="nested-scoredproperty-instances"></a><span data-ttu-id="0e1c0-103">Вложенные экземпляры Скоредпроперти</span><span class="sxs-lookup"><span data-stu-id="0e1c0-103">Nested ScoredProperty Instances</span></span>

<span data-ttu-id="0e1c0-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-104">This topic is not current.</span></span> <span data-ttu-id="0e1c0-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0e1c0-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0e1c0-106">Обратите внимание, что добавление экземпляров Скоредпроперти в качестве дочерних элементов экземпляра параметра не разрешено.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-106">Notice that you are not restricted to adding ScoredProperty instances as child elements of an Option instance.</span></span> <span data-ttu-id="0e1c0-107">Экземпляры Скоредпроперти также могут быть вложенными в другие экземпляры Скоредпроперти.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-107">ScoredProperty instances may also be nested within other ScoredProperty instances.</span></span> <span data-ttu-id="0e1c0-108">Это полезно, когда свойство устройства является сложным и лучше представлено несколькими подсвойствами.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-108">This is useful when a device property is complex and is best represented by multiple subproperties.</span></span> <span data-ttu-id="0e1c0-109">Добавление вложенных свойств в существующее (или открытое) свойство или Скоредпроперти является хорошим способом улучшения параметра, сохраняя при этом переносимость с существующими экземплярами параметров.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-109">Adding subproperties to an existing (or public) Property or ScoredProperty is a good way to enhance an Option, while retaining portability with existing Option instances.</span></span> <span data-ttu-id="0e1c0-110">Например, экземпляры стандартных параметров для функции MediaType содержат Скоредпроперти, описывающий вес носителя как «Light», «средний», «высокий» или «Екстрахеави».</span><span class="sxs-lookup"><span data-stu-id="0e1c0-110">For example, the standard Option instances for the MediaType Feature contain a ScoredProperty describing the weight of the media as Light, Medium, Heavy, or ExtraHeavy.</span></span> <span data-ttu-id="0e1c0-111">Если требуется более точное описание веса, можно добавить подсвойство (GramsPer100Sheets в следующем примере), содержащее фактический вес (в граммах) 100 листов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-111">If you want more precise descriptions of the weight, you can add a subproperty (GramsPer100Sheets in the following example) that contains the actual weight (in grams) of 100 sheets of media.</span></span> <span data-ttu-id="0e1c0-112">Расширенный параметр может выглядеть, как в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-112">The enhanced Option might look like the following example.</span></span>

``` syntax
<!-- Note: The following ScoredProperty is not a Public Print Schema ScoredProperty -->
<!-- This example shows a nested ScoredProperty defined by a Private namespace-->
<!-- It is included for illustration purposes. -->

<psf:ScoredProperty name="FabrikamES500:PaperWeight">
  <psf:Value xsi:type="xs:string">Medium</psf:Value>
  <psf:ScoredProperty name="FabrikamES500:GramsPerSheet">
    <Value xsi:type="decimal">109.5</Value>
  </psf:ScoredProperty>
</psf:ScoredProperty>
```

<span data-ttu-id="0e1c0-113">Сравнение исходного и расширенного параметров обеспечивает близкое к идеальному совпадению, так как расширенный параметр является надмножеством исходного, а расположения и значения каждого из исходных экземпляров Скоредпроперти сохраняются.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-113">A comparison of the original and enhanced Option instances produces a near-perfect match, because the enhanced Option is a superset of the original, and the locations and values of each of the original ScoredProperty instances is preserved.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e1c0-114">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0e1c0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e1c0-115">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="0e1c0-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



