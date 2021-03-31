---
description: Предоставляет перегрузки операторов и приведения типов для структур D3DXFLOAT16.
ms.assetid: d287efb5-d15e-46dc-924d-012e1a108efc
title: Расширения D3DXFLOAT16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f97e8917f453e7c2c2db99b8f894d557d7b7909f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081860"
---
# <a name="d3dxfloat16-extensions"></a>Расширения D3DXFLOAT16

Предоставляет перегрузки операторов и приведения типов для структур [**D3DXFLOAT16**](d3dxfloat16.md) .

``` syntax
typedef struct D3DXFLOAT16
{
#ifdef __cplusplus
public:
    D3DXFLOAT16() {};
    D3DXFLOAT16( FLOAT );
    D3DXFLOAT16( CONST D3DXFLOAT16& );

    // casting
    operator FLOAT ();

    // binary operators
    BOOL operator == ( CONST D3DXFLOAT16& ) const;
    BOOL operator != ( CONST D3DXFLOAT16& ) const;

protected:
#endif //__cplusplus
    WORD value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```

Производные типы: \* LPD3DXFLOAT16

## <a name="members"></a>Элементы

Дополнительные сведения о членах структуры см. в разделе D3DXFLOAT16.

## <a name="remarks"></a>Комментарии

Перегрузки операторов и приведения типов для этой структуры реализуются в d3dx9math. inl.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




