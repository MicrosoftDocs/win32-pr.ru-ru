---
title: 'Методы Texture2DArray:: Texture2DArray Гасеркмп'
description: Выборка и сравнение Texture2DArray и возврат всех компонентов.
ms.assetid: 5b2892f0-be62-4fb2-978e-aabb8ae96e67
keywords:
- Методы Гасеркмп HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 760c6313df2fb50ea821495d9f57933aef5bb0cc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104986180"
---
# <a name="texture2darraygathercmp-methods"></a><span data-ttu-id="b7ebe-104">Методы Texture2DArray:: Гасеркмп</span><span class="sxs-lookup"><span data-stu-id="b7ebe-104">Texture2DArray::GatherCmp methods</span></span>

<span data-ttu-id="b7ebe-105">Для четырех шаг текселя значений [**Texture2DArray**](sm5-object-texture2darray.md) , которые будут использоваться в операции линейной фильтрации, возвращает их сравнение со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="b7ebe-105">For four texel values of a [**Texture2DArray**](sm5-object-texture2darray.md) that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

<span data-ttu-id="b7ebe-106">Дополнительные сведения, описывающие базовую инструкцию DXBC, см. в документации по [gather4_c](./gather4-c--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="b7ebe-106">See the documentation on [gather4_c](./gather4-c--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b7ebe-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="b7ebe-107">Overload list</span></span>



| <span data-ttu-id="b7ebe-108">Метод</span><span class="sxs-lookup"><span data-stu-id="b7ebe-108">Method</span></span>                                                                             | <span data-ttu-id="b7ebe-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b7ebe-109">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7ebe-110">**Гасеркмп (S, float, float, int)**</span><span class="sxs-lookup"><span data-stu-id="b7ebe-110">**GatherCmp(S,float,float,int)**</span></span>](sm5-object-texture2darray-gathercmp.md)        | <span data-ttu-id="b7ebe-111">Выборка и сравнение текстуры и возврат всех четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="b7ebe-111">Samples and compares a texture and returns all four components.</span></span><br/>                                       |
| [<span data-ttu-id="b7ebe-112">**Гасеркмп (S, float, float, int, uint)**</span><span class="sxs-lookup"><span data-stu-id="b7ebe-112">**GatherCmp(S,float,float,int,uint)**</span></span>](t2d-gathercmp-s-float-float-int-uint-.md) | <span data-ttu-id="b7ebe-113">Выбирает и сравнивает текстуру и возвращает все четыре компонента вместе с состоянием операции.</span><span class="sxs-lookup"><span data-stu-id="b7ebe-113">Samples and compares a texture and returns all four components along with status about the operation.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7ebe-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7ebe-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ebe-115">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b7ebe-115">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

