---
description: Этот макрос создает значение, используемое при выдаче запроса.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 0c2e7a197612b56eb5ae966da3cd4cc224edd2bd07e3fded3d0b72907f717d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987254"
---
# <a name="d3dissue_end"></a>D3DISSUE \_ конец

Этот макрос создает значение, используемое [**при выдаче запроса**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) .

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a>Параметры





 

## <a name="remarks"></a>Remarks

Этот макрос изменяет состояние запроса на несигнальное.

D3DISSUE \_ End допустимо для следующих типов запросов.

-   D3DQUERYTYPE \_ вкаче
-   D3DQUERYTYPE \_ ResourceManager
-   D3DQUERYTYPE \_ вертексстатс
-   \_Событие D3DQUERYTYPE
-   D3DQUERYTYPE \_ перекрытия

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**\_Начало D3DISSUE**](d3dissue-begin.md)
</dt> <dt>

[**D3DQUERYTYPE**](./d3dquerytype.md)
</dt> </dl>

 

 
