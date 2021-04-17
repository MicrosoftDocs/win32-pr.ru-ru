---
description: Определяет набор из двух логических значений, используемых в шаблоне Мешфацеврапс для определения топологии текстуры отдельного лица. Используйте вместо Boolean2d, если координаты текстуры (u, v) охватывают диапазон от 0 до 2 вместо 0 до 1.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: материалврап
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6797719919a4f52421751a5cad008aa8a581089a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710596"
---
# <a name="materialwrap"></a><span data-ttu-id="1dc73-104">материалврап</span><span class="sxs-lookup"><span data-stu-id="1dc73-104">MaterialWrap</span></span>

<span data-ttu-id="1dc73-105">Определяет набор из двух логических значений, используемых в шаблоне [**мешфацеврапс**](meshfacewraps.md) для определения топологии текстуры отдельного лица.</span><span class="sxs-lookup"><span data-stu-id="1dc73-105">Defines a set of two Boolean values used in the [**MeshFaceWraps**](meshfacewraps.md) template to define the texture topology of an individual face.</span></span> <span data-ttu-id="1dc73-106">Используйте вместо [**Boolean2d**](boolean2d.md) , если координаты текстуры (u, v) охватывают диапазон от 0 до 2 вместо 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="1dc73-106">Use instead of [**Boolean2d**](boolean2d.md) when the texture coordinates (u, v) span the range of 0 to 2 instead of 0 to 1.</span></span>

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

<span data-ttu-id="1dc73-107">Где:</span><span class="sxs-lookup"><span data-stu-id="1dc73-107">Where:</span></span>

-   <span data-ttu-id="1dc73-108">u — логическое значение.</span><span class="sxs-lookup"><span data-stu-id="1dc73-108">u - Boolean value.</span></span> <span data-ttu-id="1dc73-109">См. раздел [**Boolean**](boolean.md).</span><span class="sxs-lookup"><span data-stu-id="1dc73-109">See [**Boolean**](boolean.md).</span></span>
-   <span data-ttu-id="1dc73-110">v — логическое значение.</span><span class="sxs-lookup"><span data-stu-id="1dc73-110">v - Boolean value.</span></span> <span data-ttu-id="1dc73-111">См. раздел [**Boolean**](boolean.md).</span><span class="sxs-lookup"><span data-stu-id="1dc73-111">See [**Boolean**](boolean.md).</span></span>

> [!Note]  
> <span data-ttu-id="1dc73-112">Шаблон [**мешфацеврапс**](meshfacewraps.md) больше не используется.</span><span class="sxs-lookup"><span data-stu-id="1dc73-112">The [**MeshFaceWraps**](meshfacewraps.md) template is no longer used.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="1dc73-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1dc73-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc73-114">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="1dc73-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



