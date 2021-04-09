---
description: Описывает вектор с двумя компонентами, включая перегрузки операторов и приведения типов. То же, что и D3DXVECTOR2, но он использует 16-разрядные значения с плавающей запятой для x, y и z.
ms.assetid: b410d2e1-a006-4563-928a-c9000f73c224
title: Структура D3DXVECTOR2_16F (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 677f4f8c47cdc70791ad98e18582810bbff23920
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820972"
---
# <a name="d3dxvector2_16f-structure"></a>\_Структура 16F D3DXVECTOR2

Описывает вектор с двумя компонентами, включая перегрузки операторов и приведения типов. То же, что и [**D3DXVECTOR2**](d3d10-d3dxvector2.md), но он использует 16-разрядные значения с плавающей запятой для x, y и z.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXVECTOR2_16F {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2_16F, *LPD3DXVECTOR2_16F;
```



## <a name="members"></a>Члены

<dl> <dt>

**x**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Компонент x.

</dd> <dt>

**y**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Компонент y.

</dd> </dl>

## <a name="remarks"></a>Комментарии

**D3DXVECTOR2 \_ 16F** имеет следующие расширения C++.

### <a name="d3dxvector2_16f-extensions"></a>\_Расширения D3DXVECTOR2 16F


```

typedef struct D3DXVECTOR2_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR2_16F() {};
    D3DXVECTOR2_16F( CONST FLOAT * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR2_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR2_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y;

} D3DXVECTOR2_16F, *LPD3DXVECTOR2_16F;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
