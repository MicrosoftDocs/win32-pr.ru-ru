---
description: Определяет степень переменных в уравнении, описывающее кривую.
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: Перечисление D3DDEGREETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6daacc007438903d3f003a19038b4ea6909814e3a5d024d3df6daa95a0c60602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989054"
---
# <a name="d3ddegreetype-enumeration"></a>Перечисление D3DDEGREETYPE

Определяет степень переменных в уравнении, описывающее кривую.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**\_Линейная D3DDEGREE**
</dt> <dd>

Кривая описывается переменными первого порядка.

</dd> <dt>

<span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE, \_ квадрат**
</dt> <dd>

Кривая описывается переменными второго порядка.

</dd> <dt>

<span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE \_ кубический**
</dt> <dd>

Кривая описывается переменными третьего порядка.

</dd> <dt>

<span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE \_ куинтик**
</dt> <dd>

Кривая описывается с помощью переменных четвертого порядка.

</dd> <dt>

<span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Значения в этом перечислении используются для описания кривых, используемых в обновлениях прямоугольника и треугольника. Дополнительные сведения см. в разделе D3DRS \_ куллмоде.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
