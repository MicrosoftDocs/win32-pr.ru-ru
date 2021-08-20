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
ms.openlocfilehash: 50fdcf97e9df1f77705509a4b93b6936a4c9f7f203ddb16e0b0284630cb42bdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075288"
---
# <a name="deducingstringsetter"></a>дедуЦингстрингсеттер

Выводит класс и аргументы, а затем вызывает обратный вызов свойства функции-члена для свойства строкового типа.

> [!Note]  
> ДедуЦингстрингсеттер не следует вызывать напрямую.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringSetter(  
    _In_ HRESULT (C::*callback)(PCWSTR string),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Direct2D::D ЕдуЦингстрингжеттер**](deducingstringgetter.md)
</dt> </dl>

 

 





