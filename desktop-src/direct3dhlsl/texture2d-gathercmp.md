---
title: 'Методы Texture2D:: Texture2D Гасеркмп'
description: Выборка и сравнение Texture2D и возврат всех компонентов.
ms.assetid: d520b113-77af-486e-8d3d-8276f72df18f
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
ms.openlocfilehash: 18455f33ba97c9d5a0180a59e39891cd617a09af
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104986188"
---
# <a name="texture2dgathercmp-methods"></a><span data-ttu-id="94f7a-104">Методы Texture2D:: Гасеркмп</span><span class="sxs-lookup"><span data-stu-id="94f7a-104">Texture2D::GatherCmp methods</span></span>

<span data-ttu-id="94f7a-105">Для четырех шаг текселя значений [**Texture2D**](sm5-object-texture2d.md) , которые будут использоваться в операции линейной фильтрации, возвращает их сравнение со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="94f7a-105">For four texel values of a [**Texture2D**](sm5-object-texture2d.md) that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

<span data-ttu-id="94f7a-106">Дополнительные сведения, описывающие базовую инструкцию DXBC, см. в документации по [gather4_c](./gather4-c--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="94f7a-106">See the documentation on [gather4_c](./gather4-c--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="94f7a-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="94f7a-107">Overload list</span></span>



| <span data-ttu-id="94f7a-108">Метод</span><span class="sxs-lookup"><span data-stu-id="94f7a-108">Method</span></span>                                                                             | <span data-ttu-id="94f7a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="94f7a-109">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94f7a-110">**Гасеркмп (S, float, float, int)**</span><span class="sxs-lookup"><span data-stu-id="94f7a-110">**GatherCmp(S,float,float,int)**</span></span>](sm5-object-texture2d-gathercmp.md)             | <span data-ttu-id="94f7a-111">Выборка и сравнение текстуры и возврат всех четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="94f7a-111">Samples and compares a texture and returns all four components.</span></span><br/>                                       |
| [<span data-ttu-id="94f7a-112">**Гасеркмп (S, float, float, int, uint)**</span><span class="sxs-lookup"><span data-stu-id="94f7a-112">**GatherCmp(S,float,float,int,uint)**</span></span>](t2d-gathercmp-s-float-float-int-uint-.md) | <span data-ttu-id="94f7a-113">Выбирает и сравнивает текстуру и возвращает все четыре компонента вместе с состоянием операции.</span><span class="sxs-lookup"><span data-stu-id="94f7a-113">Samples and compares a texture and returns all four components along with status about the operation.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94f7a-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94f7a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f7a-115">Texture2D</span><span class="sxs-lookup"><span data-stu-id="94f7a-115">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> </dl>

 

