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
# <a name="blobsetter"></a>блобсеттер

Вызывает обратный вызов метода задания свойства для функции-члена для свойства типа BLOB.

``` syntax
template<typename T, T P, typename I>
HRESULT CALLBACK BlobSetter(
    _In_ IUnknown *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Direct2D:: Блобжеттер**](blobgetter.md)
</dt> </dl>

 

 





