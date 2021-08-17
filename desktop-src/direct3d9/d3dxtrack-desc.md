---
description: Описывает анимацию и задает толщину, скорость и позиции смешения для записи в заданный момент времени.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: Структура D3DXTRACK_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: cddabb3ea79951e35831c2cdc32e11baeb5c7c1c4ce174fd29d9382edb391953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731121"
---
# <a name="d3dxtrack_desc-structure"></a>\_Структура D3DXTRACK DESC

Описывает анимацию и задает толщину, скорость и позиции смешения для записи в заданный момент времени.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Приоритет**
</dt> <dd>

Тип: **[ **D3DXPRIORITY \_ тип**](./d3dxpriority-type.md)**

</dd> <dd>

Тип приоритета, как определено в [**\_ типе D3DXPRIORITY**](./d3dxpriority-type.md).

</dd> <dt>

**Weight**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Значение веса. Вес определяет долю этой дорожки для смешения с другими дорожками.

</dd> <dt>

**Скорость**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Значение скорости. Он используется аналогично множителю для масштабирования периода курса.

</dd> <dt>

**Позиция**
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Время, на которое ведется трассировка, в локальной временной области текущего набора анимации.

</dd> <dt>

**Включить**
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

</dd> <dd>

Следите за включением и отключением. Чтобы включить, установите значение **true**. Чтобы отключить, задайте для параметра значение **false**.

</dd> </dl>

## <a name="remarks"></a>Remarks

Курсы с одинаковым приоритетом смешиваются друг с другом, а два результирующих значения смешиваются с использованием коэффициента смешения приоритетов. С дорожкой должен быть связан набор анимации (хранящийся отдельно).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
