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
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355083"
---
# <a name="d3dissue_end"></a>D3DISSUE \_ конец

Этот макрос создает значение, используемое [**при выдаче запроса**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) .

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a>Параметры





 

## <a name="remarks"></a>Комментарии

Этот макрос изменяет состояние запроса на несигнальное.

D3DISSUE \_ End допустимо для следующих типов запросов.

-   D3DQUERYTYPE \_ вкаче
-   D3DQUERYTYPE \_ ResourceManager
-   D3DQUERYTYPE \_ вертексстатс
-   \_Событие D3DQUERYTYPE
-   D3DQUERYTYPE \_ перекрытия

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**\_Начало D3DISSUE**](d3dissue-begin.md)
</dt> <dt>

[**D3DQUERYTYPE**](./d3dquerytype.md)
</dt> </dl>

 

 
