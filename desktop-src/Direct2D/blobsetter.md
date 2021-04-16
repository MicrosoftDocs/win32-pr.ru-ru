---
title: Блобсеттер (D2d1effecthelpers. h)
description: Вызывает обратный вызов метода задания свойства для функции-члена для свойства типа BLOB.
ms.assetid: 29411D53-1D27-4040-A3C0-B1511E627A32
keywords:
- Блобсеттер Direct2D
topic_type:
- apiref
api_name:
- BlobSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a073db2fb53fa86414ed6081ede0e24c2eb7dcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656933"
---
# <a name="blobsetter"></a><span data-ttu-id="5195d-104">блобсеттер</span><span class="sxs-lookup"><span data-stu-id="5195d-104">BlobSetter</span></span>

<span data-ttu-id="5195d-105">Вызывает обратный вызов метода задания свойства для функции-члена для свойства типа BLOB.</span><span class="sxs-lookup"><span data-stu-id="5195d-105">Calls a member-function property setter callback for a blob-type property.</span></span>

``` syntax
template<typename T, T P, typename I>
HRESULT CALLBACK BlobSetter(
    _In_ IUnknown *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="5195d-106">Требования</span><span class="sxs-lookup"><span data-stu-id="5195d-106">Requirements</span></span>



| <span data-ttu-id="5195d-107">Требование</span><span class="sxs-lookup"><span data-stu-id="5195d-107">Requirement</span></span> | <span data-ttu-id="5195d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5195d-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5195d-109">Header</span><span class="sxs-lookup"><span data-stu-id="5195d-109">Header</span></span><br/> | <dl> <span data-ttu-id="5195d-110"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="5195d-110"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5195d-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5195d-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5195d-112">**Direct2D:: Блобжеттер**</span><span class="sxs-lookup"><span data-stu-id="5195d-112">**Direct2D::BlobGetter**</span></span>](blobgetter.md)
</dt> </dl>

 

 





