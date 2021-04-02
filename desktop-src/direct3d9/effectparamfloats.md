---
description: Определяет действующие числа с плавающей запятой. Этот шаблон заменяет шаблон Еффектфлоатс.
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: еффектпарамфлоатс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072201"
---
# <a name="effectparamfloats"></a><span data-ttu-id="c2d52-104">еффектпарамфлоатс</span><span class="sxs-lookup"><span data-stu-id="c2d52-104">EffectParamFloats</span></span>

<span data-ttu-id="c2d52-105">Определяет действующие числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="c2d52-105">Defines effect floating-point numbers.</span></span> <span data-ttu-id="c2d52-106">Этот шаблон заменяет шаблон [**еффектфлоатс**](effectfloats.md) .</span><span class="sxs-lookup"><span data-stu-id="c2d52-106">This template replaces the [**EffectFloats**](effectfloats.md) template.</span></span>

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

<span data-ttu-id="c2d52-107">Где:</span><span class="sxs-lookup"><span data-stu-id="c2d52-107">Where:</span></span>

-   <span data-ttu-id="c2d52-108">ParamName — имя массива чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="c2d52-108">ParamName - Name of the array of floats.</span></span>
-   <span data-ttu-id="c2d52-109">Нфлоатс — число значений с плавающей запятой в массиве.</span><span class="sxs-lookup"><span data-stu-id="c2d52-109">nFloats - Number of floating-point values in the array.</span></span>
-   <span data-ttu-id="c2d52-110">\[ \] Массивы с плавающей запятой нфлоатс.</span><span class="sxs-lookup"><span data-stu-id="c2d52-110">Floats\[nFloats\] - Array of floating-point values.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2d52-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2d52-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d52-112">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="c2d52-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



