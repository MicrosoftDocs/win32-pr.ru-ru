---
description: Описывает событие анимации.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: Структура D3DXEVENT_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d5569eccd5b99939cd50797ee73593ce5a2bfc8ddd60236e05218ddcca7f4383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731812"
---
# <a name="d3dxevent_desc-structure"></a>\_Структура D3DXEVENT DESC

Описывает событие анимации.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Тип**
</dt> <dd>

Тип: **[ **D3DXEVENT \_ тип**](./d3dxevent-type.md)**

</dd> <dd>

Тип события, как определено [**в \_ типе D3DXEVENT**](./d3dxevent-type.md).

</dd> <dt>

**Track**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Идентификатор трассировки событий.

</dd> <dt>

**StartTime**
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Время начала события в глобальном времени.

</dd> <dt>

**Длительность**
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Длительность события в глобальном времени.

</dd> <dt>

**Переход**
</dt> <dd>

Тип: **[ **D3DXTRANSITION \_ тип**](./d3dxtransition-type.md)**

</dd> <dd>

Стиль перехода для события, как определено в [**\_ типе D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> <dt>

**Weight**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Отслеживание веса для события.

</dd> <dt>

**Скорость**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Скорость записи для события.

</dd> <dt>

**Позиция**
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Отслеживание расположения для события.

</dd> <dt>

**Включить**
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

</dd> <dd>

Включить флаг.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
