---
title: ДедуЦингвалуесеттер (D2d1effecthelpers. h)
description: Выводит класс и аргументы, а затем вызывает обратный вызов свойства функции-члена для свойства типа значения.
ms.assetid: 4C3D64A8-0CC0-405A-A5B3-627C2DF25EA1
keywords:
- ДедуЦингвалуесеттер Direct2D
topic_type:
- apiref
api_name:
- DeducingValueSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e002c5a36c8ac0b196dfc5fb25e11f7f9d63806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675868"
---
# <a name="deducingvaluesetter"></a><span data-ttu-id="3f3d7-104">дедуЦингвалуесеттер</span><span class="sxs-lookup"><span data-stu-id="3f3d7-104">DeducingValueSetter</span></span>

<span data-ttu-id="3f3d7-105">Выводит класс и аргументы, а затем вызывает обратный вызов свойства функции-члена для свойства типа значения.</span><span class="sxs-lookup"><span data-stu-id="3f3d7-105">Deduces the class and arguments and then calls a member-function property setter callback for a value-type property.</span></span>

> [!Note]  
> <span data-ttu-id="3f3d7-106">ДедуЦингвалуесеттер не следует вызывать напрямую.</span><span class="sxs-lookup"><span data-stu-id="3f3d7-106">DeducingValueSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueSetter(
    _In_ HRESULT (C::*callback)(P),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="3f3d7-107">Требования</span><span class="sxs-lookup"><span data-stu-id="3f3d7-107">Requirements</span></span>



| <span data-ttu-id="3f3d7-108">Требование</span><span class="sxs-lookup"><span data-stu-id="3f3d7-108">Requirement</span></span> | <span data-ttu-id="3f3d7-109">Значение</span><span class="sxs-lookup"><span data-stu-id="3f3d7-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3d7-110">Header</span><span class="sxs-lookup"><span data-stu-id="3f3d7-110">Header</span></span><br/> | <dl> <span data-ttu-id="3f3d7-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f3d7-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f3d7-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f3d7-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f3d7-113">**Direct2D::D ЕдуЦингвалуежеттер**</span><span class="sxs-lookup"><span data-stu-id="3f3d7-113">**Direct2D::DeducingValueGetter**</span></span>](deducingvaluegetter.md)
</dt> </dl>

 

 





