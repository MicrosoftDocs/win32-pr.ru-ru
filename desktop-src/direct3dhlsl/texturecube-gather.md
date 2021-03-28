---
title: 'Методы сбора Текстурекубе:: Текстурекубе'
description: 'Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации. | Методы сбора Текстурекубе:: Текстурекубе'
ms.assetid: 4891A62A-9D54-4F7E-92C2-9CDDF1453671
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
ms.openlocfilehash: ce58acc01ef87e6d53d829a5c84e7c9c0ff6afb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986385"
---
# <a name="texturecubegather-methods"></a><span data-ttu-id="4577e-105">Методы Текстурекубе:: собрать</span><span class="sxs-lookup"><span data-stu-id="4577e-105">TextureCube::Gather methods</span></span>

<span data-ttu-id="4577e-106">Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="4577e-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="4577e-107">Дополнительные сведения, описывающие базовую инструкцию DXBC, см. в документации по [gather4](./gather4--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="4577e-107">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4577e-108">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="4577e-108">Overload list</span></span>



| <span data-ttu-id="4577e-109">Метод</span><span class="sxs-lookup"><span data-stu-id="4577e-109">Method</span></span>                                                     | <span data-ttu-id="4577e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4577e-110">Description</span></span>                                                                                                              |
|:-----------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4577e-111">**Сбор данных (S, float)**</span><span class="sxs-lookup"><span data-stu-id="4577e-111">**Gather(S,float)**</span></span>](dx-graphics-hlsl-to-gather.md)      | <span data-ttu-id="4577e-112">Выбирает текстуру и возвращает четыре образца (только красный компонент), которые используются для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="4577e-112">Samples a texture and returns the four samples (red component only) that are used for bilinear interpolation.</span></span><br/> |
| [<span data-ttu-id="4577e-113">**Сбор данных (S, float, uint)**</span><span class="sxs-lookup"><span data-stu-id="4577e-113">**Gather(S,float,uint)**</span></span>](tcube-gather-s-float-uint-.md) | <span data-ttu-id="4577e-114">Выбирает текстуру и возвращает все четыре компонента вместе с состоянием операции.</span><span class="sxs-lookup"><span data-stu-id="4577e-114">Samples a texture and returns all four components along with status about the operation.</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="4577e-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4577e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4577e-116">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="4577e-116">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

