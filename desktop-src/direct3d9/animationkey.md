---
description: Определяет набор клавиш анимации. Ключ матрицы полезен для наборов данных анимации, которые должны быть представлены как матрицы преобразования.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: аниматионкэй
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701243"
---
# <a name="animationkey"></a><span data-ttu-id="0619d-104">аниматионкэй</span><span class="sxs-lookup"><span data-stu-id="0619d-104">AnimationKey</span></span>

<span data-ttu-id="0619d-105">Определяет набор клавиш анимации.</span><span class="sxs-lookup"><span data-stu-id="0619d-105">Defines a set of animation keys.</span></span> <span data-ttu-id="0619d-106">Ключ матрицы полезен для наборов данных анимации, которые должны быть представлены как матрицы преобразования.</span><span class="sxs-lookup"><span data-stu-id="0619d-106">A matrix key is useful for sets of animation data that need to be represented as transformation matrices.</span></span>

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

<span data-ttu-id="0619d-107">Где:</span><span class="sxs-lookup"><span data-stu-id="0619d-107">Where:</span></span>

-   <span data-ttu-id="0619d-108">keyType — указывает, являются ли ключи ключами вращения, масштабирования, расположения или матрицы (с использованием целых чисел 0, 1, 2 или 3 соответственно).</span><span class="sxs-lookup"><span data-stu-id="0619d-108">keyType - Specifies whether the keys are rotation, scale, position, or matrix keys (using the integers 0, 1, 2, or 3, respectively).</span></span>
-   <span data-ttu-id="0619d-109">Нкэйс — число ключей.</span><span class="sxs-lookup"><span data-stu-id="0619d-109">nKeys - Number of keys.</span></span>
-   <span data-ttu-id="0619d-110">ключи — массив ключей.</span><span class="sxs-lookup"><span data-stu-id="0619d-110">keys - An array of keys.</span></span> <span data-ttu-id="0619d-111">См. [**тимедфлоаткэйс**](timedfloatkeys.md).</span><span class="sxs-lookup"><span data-stu-id="0619d-111">See [**TimedFloatKeys**](timedfloatkeys.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0619d-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0619d-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0619d-113">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="0619d-113">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



