---
description: Определяет расположение, в котором необходимо получить доступ к компоненту цвета или цвета для вычислений освещения.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: Перечисление D3DMATERIALCOLORSOURCE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3c8069fdde062fdc6dea311b40b8614d2165356ff397f0d056c43569f391e02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988894"
---
# <a name="d3dmaterialcolorsource-enumeration"></a>Перечисление D3DMATERIALCOLORSOURCE

Определяет расположение, в котором необходимо получить доступ к компоненту цвета или цвета для вычислений освещения.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**\_Материал D3DMCS**
</dt> <dd>

Использовать цвет из текущего материала.

</dd> <dt>

<span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**
</dt> <dd>

Используйте рассеянный цвет вершины.

</dd> <dt>

<span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**
</dt> <dd>

Используйте цвет отраженной вершины.

</dd> <dt>

<span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эти флаги используются для установки значений следующих состояний отрисовки в перечислимом типе [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) .

-   D3DRS \_ амбиентматериалсаурце
-   D3DRS \_ диффусематериалсаурце
-   D3DRS \_ емиссивематериалсаурце
-   D3DRS \_ спекуларматериалсаурце

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
