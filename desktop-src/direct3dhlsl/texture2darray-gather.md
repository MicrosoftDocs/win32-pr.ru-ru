---
title: 'Методы сбора Texture2DArray:: Texture2DArray'
description: Примеры Texture2DArray и возвращают все четыре компонента.
ms.assetid: eea1dd00-0061-4601-a218-979eb0ecd36d
keywords:
- HLSL методов сбора данных
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: cd10959490a85583cab01814f9cdb012859317a4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104986172"
---
# <a name="texture2darraygather-methods"></a><span data-ttu-id="23061-104">Методы Texture2DArray:: собрать</span><span class="sxs-lookup"><span data-stu-id="23061-104">Texture2DArray::Gather methods</span></span>

<span data-ttu-id="23061-105">Возвращает четыре значения шаг текселя объекта [**Texture2DArray**](sm5-object-texture2darray.md) , которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="23061-105">Returns the four texel values of a [**Texture2DArray**](sm5-object-texture2darray.md) that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="23061-106">Дополнительные сведения, описывающие базовую инструкцию DXBC, см. в документации по [gather4](./gather4--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="23061-106">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="23061-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="23061-107">Overload list</span></span>



| <span data-ttu-id="23061-108">Метод</span><span class="sxs-lookup"><span data-stu-id="23061-108">Method</span></span>                                                                | <span data-ttu-id="23061-109">Описание</span><span class="sxs-lookup"><span data-stu-id="23061-109">Description</span></span>                                                                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23061-110">**Сбор данных (S, float, int)**</span><span class="sxs-lookup"><span data-stu-id="23061-110">**Gather(S,float,int)**</span></span>](sm5-object-texture2darray-gather.md)        | <span data-ttu-id="23061-111">Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="23061-111">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                 |
| [<span data-ttu-id="23061-112">**Сбор данных (S, float, int, uint)**</span><span class="sxs-lookup"><span data-stu-id="23061-112">**Gather(S,float,int,uint)**</span></span>](t2darray-gather-s-float-int-uint-.md)  | <span data-ttu-id="23061-113">Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="23061-113">Returns the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23061-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23061-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23061-115">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="23061-115">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

