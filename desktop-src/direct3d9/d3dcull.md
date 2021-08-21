---
description: Определяет поддерживаемые режимы отбора.
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: Перечисление D3DCULL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 062135f1eff43bd568f1b08674985b4744e0835ebf3fa9e78c2756a798f85ccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989064"
---
# <a name="d3dcull-enumeration"></a>Перечисление D3DCULL

Определяет поддерживаемые режимы отбора.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ None**
</dt> <dd>

Не исключать задние грани.

</dd> <dt>

<span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL \_ во вт.**
</dt> <dd>

Исключать грани с отднем по часовой стрелке.

</dd> <dt>

<span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL \_ CCW**
</dt> <dd>

Возврат лицевых сторон с вершинами против часовой стрелки.

</dd> <dt>

<span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Значения в этом перечислимом типе используются \_ состоянием визуализации D3DRS куллмоде. Режимы отбора определяют, каким способом исключаются грани при подготовке к просмотру геометрии.

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

 

 
