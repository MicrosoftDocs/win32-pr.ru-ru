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
ms.openlocfilehash: 8877eece8e33c6508768b22c989e992cf8178823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703841"
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

## <a name="remarks"></a>Комментарии

Эти флаги используются для установки значений следующих состояний отрисовки в перечислимом типе [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) .

-   D3DRS \_ амбиентматериалсаурце
-   D3DRS \_ диффусематериалсаурце
-   D3DRS \_ емиссивематериалсаурце
-   D3DRS \_ спекуларматериалсаурце

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
