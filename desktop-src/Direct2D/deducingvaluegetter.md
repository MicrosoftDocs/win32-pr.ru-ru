---
title: ДедуЦингвалуежеттер (D2d1effecthelpers. h)
description: Выводит класс и аргументы, а затем вызывает обратный вызов метода получения свойства функции-члена для свойства типа значения.
ms.assetid: E2E5CCC3-B112-4D3C-8840-121A55C4F1A2
keywords:
- ДедуЦингвалуежеттер Direct2D
topic_type:
- apiref
api_name:
- DeducingValueGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd6eac823457882513f97557939db884efcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657053"
---
# <a name="deducingvaluegetter"></a><span data-ttu-id="3d6df-104">дедуЦингвалуежеттер</span><span class="sxs-lookup"><span data-stu-id="3d6df-104">DeducingValueGetter</span></span>

<span data-ttu-id="3d6df-105">Выводит класс и аргументы, а затем вызывает обратный вызов метода получения свойства функции-члена для свойства типа значения.</span><span class="sxs-lookup"><span data-stu-id="3d6df-105">Deduces the class and arguments and then calls a member-function property getter callback for a value-type property.</span></span>

> [!Note]  
> <span data-ttu-id="3d6df-106">ДедуЦингвалуежеттер не следует вызывать напрямую.</span><span class="sxs-lookup"><span data-stu-id="3d6df-106">DeducingValueGetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueGetter(
    _In_ P (C::*callback)() const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="3d6df-107">Требования</span><span class="sxs-lookup"><span data-stu-id="3d6df-107">Requirements</span></span>



| <span data-ttu-id="3d6df-108">Требование</span><span class="sxs-lookup"><span data-stu-id="3d6df-108">Requirement</span></span> | <span data-ttu-id="3d6df-109">Значение</span><span class="sxs-lookup"><span data-stu-id="3d6df-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6df-110">Header</span><span class="sxs-lookup"><span data-stu-id="3d6df-110">Header</span></span><br/> | <dl> <span data-ttu-id="3d6df-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d6df-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d6df-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d6df-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d6df-113">**Direct2D::D ЕдуЦингвалуесеттер**</span><span class="sxs-lookup"><span data-stu-id="3d6df-113">**Direct2D::DeducingValueSetter**</span></span>](deducingvaluesetter.md)
</dt> </dl>

 

 





