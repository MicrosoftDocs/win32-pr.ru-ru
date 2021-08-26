---
description: Предоставляет следующие перегрузки операторов и приведения типов для структур D3DXCOLOR.
ms.assetid: 89780c6f-c78b-4ebe-876a-6dbc37b598ef
title: Расширения D3DXCOLOR (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7a07d697192d838298f76205aeb3010fda7bf6a08f58f39fe58893444f604231
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096294"
---
# <a name="d3dxcolor-extensions"></a>Расширения D3DXCOLOR

Предоставляет следующие перегрузки операторов и приведения типов для структур [**D3DXCOLOR**](d3dxcolor.md) .

``` syntax
typedef struct D3DXCOLOR
{
#ifdef __cplusplus
public:
    D3DXCOLOR() {}
    D3DXCOLOR( DWORD argb );
    D3DXCOLOR( CONST FLOAT * );
    D3DXCOLOR( CONST D3DXFLOAT16 * );
    D3DXCOLOR( CONST D3DCOLORVALUE& );
    D3DXCOLOR( FLOAT r, FLOAT g, FLOAT b, FLOAT a );

    // casting
    operator DWORD () const;

    operator FLOAT* ();
    operator CONST FLOAT* () const;

    operator D3DCOLORVALUE* ();
    operator CONST D3DCOLORVALUE* () const;

    operator D3DCOLORVALUE& ();
    operator CONST D3DCOLORVALUE& () const;

    // assignment operators
    D3DXCOLOR& operator += ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator -= ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator *= ( FLOAT );
    D3DXCOLOR& operator /= ( FLOAT );

    // unary operators
    D3DXCOLOR operator + () const;
    D3DXCOLOR operator - () const;

    // binary operators
    D3DXCOLOR operator + ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator - ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator * ( FLOAT ) const;
    D3DXCOLOR operator / ( FLOAT ) const;

    friend D3DXCOLOR operator * ( FLOAT, CONST D3DXCOLOR& );

    BOOL operator == ( CONST D3DXCOLOR& ) const;
    BOOL operator != ( CONST D3DXCOLOR& ) const;

#endif //__cplusplus
    FLOAT r, g, b, a;
} D3DXCOLOR, *LPD3DXCOLOR;
```

Производные типы: \* LPD3DXCOLOR

## <a name="members"></a>Элементы

Дополнительные сведения о членах структуры см. в разделе [**D3DXCOLOR**](d3dxcolor.md).

## <a name="remarks"></a>Remarks

Перегрузки операторов и приведения типов для этой структуры реализуются в d3dx9math. inl.

> [!Note]  
> при запуске конструктора D3DXCOLOR () в режиме отладки в Microsoft Visual Studio 2010 с параметром компилятора " [проверки ошибок во время выполнения" (/RTCc)](/previous-versions/visualstudio/visual-studio-2010/8wtf2dfz(v=vs.100)) происходит сбой во время выполнения.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
