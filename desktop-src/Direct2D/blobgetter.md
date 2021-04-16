---
title: Блобжеттер (D2d1effecthelpers. h)
description: Вызывает обратный вызов метода получения свойства функции-члена для свойства типа BLOB.
ms.assetid: 55A41BE4-2AAE-480B-A143-86E8E7533210
keywords:
- Блобжеттер Direct2D
topic_type:
- apiref
api_name:
- BlobGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c638501c9c15abc2f895003fd79c481fd0e05b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656935"
---
# <a name="blobgetter"></a>блобжеттер

Вызывает обратный вызов метода получения свойства функции-члена для свойства типа BLOB.

``` syntax
template<typename T, T P, typename I>
HRESULT CALLBACK BlobGetter(
    _In_ const IUnknown *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Direct2D:: Блобсеттер**](blobsetter.md)
</dt> </dl>

 

 





