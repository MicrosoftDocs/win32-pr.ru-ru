---
description: Предопределенные наборы состояний конвейера, используемые блоками состояния (см. раздел State Blocks Save and Restore State (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Перечисление D3DSTATEBLOCKTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7780b7ded37ba976f32f4439ab793ae711be2f5790d03555a6a8be4f031571e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850193"
---
# <a name="d3dstateblocktype-enumeration"></a>Перечисление D3DSTATEBLOCKTYPE

Предопределенные наборы состояний конвейера, используемые блоками состояния (см. раздел [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ все**
</dt> <dd>

Запись текущего [состояния устройства](saving-all-device-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ пикселстате**
</dt> <dd>

Захватывает текущее [состояние пикселя](saving-pixel-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ вертексстате**
</dt> <dd>

Захватывает текущее [состояние вершины](saving-vertex-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Не используйте это значение.

</dd> </dl>

## <a name="remarks"></a>Remarks

Как показано на следующей схеме, состояние вершины и пиксела — это оба подмножества состояния устройства.

![Схема состояния устройства с состоянием вершины и состоянием пикселя в качестве подмножества](images/statesets.png)

Существует только несколько состояний, которые считаются состоянием вершины и пикселя. Возможны следующие состояния:

-   Состояние визуализации: D3DRS \_ фогденсити
-   Состояние визуализации: D3DRS \_ фогстарт
-   Состояние визуализации: D3DRS \_ фоженд
-   Состояние текстуры: D3DTSS \_ текскурдиндекс
-   Состояние текстуры: D3DTSS \_ текстуретрансформфлагс

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: Креатестатеблокк**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

**IDirect3DDevice9:: Креатестатеблокк**
</dt> </dl>

 

 
