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
ms.openlocfilehash: 91e7c918965fc2d7cdf8948806ffffea32f35cafc061ff0d81addd5499c37072
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653264"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Direct2D:: Блобсеттер**](blobsetter.md)
</dt> </dl>

 

 





