---
title: ДедуЦингблобжеттер (D2d1effecthelpers. h)
description: Выводит класс и аргументы, а затем вызывает обратный вызов метода получения свойства функции-члена для свойства типа BLOB.
ms.assetid: 1B8800CB-2AD0-4684-99D7-986F6C53A6F1
keywords:
- ДедуЦингблобжеттер Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7ca5cc37a9fbd79807e258a87a199be7319ce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675920"
---
# <a name="deducingblobgetter"></a><span data-ttu-id="f4832-104">дедуЦингблобжеттер</span><span class="sxs-lookup"><span data-stu-id="f4832-104">DeducingBlobGetter</span></span>

<span data-ttu-id="f4832-105">Выводит класс и аргументы, а затем вызывает обратный вызов метода получения свойства функции-члена для свойства типа BLOB.</span><span class="sxs-lookup"><span data-stu-id="f4832-105">Deduces the class and arguments and then calls a member-function property getter callback for a blob-type property.</span></span>

> [!Note]  
> <span data-ttu-id="f4832-106">ДедуЦингблобжеттер не следует вызывать напрямую.</span><span class="sxs-lookup"><span data-stu-id="f4832-106">DeducingBlobGetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobGetter(  
    _In_ HRESULT (C::*callback)(BYTE *, UINT32, UINT32*) const,  
    _In_ const I *effect,  
    _Out_writes_opt_(dataSize) BYTE *data,  
    UINT32 dataSize,  
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="f4832-107">Требования</span><span class="sxs-lookup"><span data-stu-id="f4832-107">Requirements</span></span>



| <span data-ttu-id="f4832-108">Требование</span><span class="sxs-lookup"><span data-stu-id="f4832-108">Requirement</span></span> | <span data-ttu-id="f4832-109">Значение</span><span class="sxs-lookup"><span data-stu-id="f4832-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4832-110">Header</span><span class="sxs-lookup"><span data-stu-id="f4832-110">Header</span></span><br/> | <dl> <span data-ttu-id="f4832-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4832-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4832-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4832-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4832-113">**Direct2D::D ЕдуЦингблобсеттер**</span><span class="sxs-lookup"><span data-stu-id="f4832-113">**Direct2D::DeducingBlobSetter**</span></span>](deducingblobsetter.md)
</dt> </dl>

 

 





