---
title: ДедуЦингстрингсеттер (D2d1effecthelpers. h)
description: Выводит класс и аргументы, а затем вызывает обратный вызов свойства функции-члена для свойства строкового типа.
ms.assetid: D3075B7B-D253-4F85-9FD2-3487C4207122
keywords:
- ДедуЦингстрингсеттер Direct2D
topic_type:
- apiref
api_name:
- DeducingStringSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7860978fd271b2ff395caae068cd651d3057020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675669"
---
# <a name="deducingstringsetter"></a><span data-ttu-id="6885d-104">дедуЦингстрингсеттер</span><span class="sxs-lookup"><span data-stu-id="6885d-104">DeducingStringSetter</span></span>

<span data-ttu-id="6885d-105">Выводит класс и аргументы, а затем вызывает обратный вызов свойства функции-члена для свойства строкового типа.</span><span class="sxs-lookup"><span data-stu-id="6885d-105">Deduces the class and arguments and then calls a member-function property setter callback for a string-type property.</span></span>

> [!Note]  
> <span data-ttu-id="6885d-106">ДедуЦингстрингсеттер не следует вызывать напрямую.</span><span class="sxs-lookup"><span data-stu-id="6885d-106">DeducingStringSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringSetter(  
    _In_ HRESULT (C::*callback)(PCWSTR string),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="6885d-107">Требования</span><span class="sxs-lookup"><span data-stu-id="6885d-107">Requirements</span></span>



| <span data-ttu-id="6885d-108">Требование</span><span class="sxs-lookup"><span data-stu-id="6885d-108">Requirement</span></span> | <span data-ttu-id="6885d-109">Значение</span><span class="sxs-lookup"><span data-stu-id="6885d-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6885d-110">Header</span><span class="sxs-lookup"><span data-stu-id="6885d-110">Header</span></span><br/> | <dl> <span data-ttu-id="6885d-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="6885d-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6885d-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6885d-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6885d-113">**Direct2D::D ЕдуЦингстрингжеттер**</span><span class="sxs-lookup"><span data-stu-id="6885d-113">**Direct2D::DeducingStringGetter**</span></span>](deducingstringgetter.md)
</dt> </dl>

 

 





