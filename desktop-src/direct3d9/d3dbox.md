---
description: Определяет том.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: Структура D3DBOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9b7e01641348594e962f546a431700db799600a08571bbb7cfaf13396e671036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805517"
---
# <a name="d3dbox-structure"></a>Структура D3DBOX

Определяет том.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a>Члены

<dl> <dt>

**Слева**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Расположение левой стороны поля на оси x.

</dd> <dt>

**Top**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Расположение верхней части бокса на оси y.

</dd> <dt>

**Right**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Расположение правой части бокса на оси x.

</dd> <dt>

**Нижнее**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Расположение нижней части бокса на оси y.

</dd> <dt>

**Front**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Расположение передней части бокса на оси z.

</dd> <dt>

**Назад**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Расположение задней части поля на оси z.

</dd> </dl>

## <a name="remarks"></a>Remarks

**D3DBOX** включает в себя левый, верхний и передний края; Однако правый, нижний и задние края не включены. Например, поле шириной в 100 единиц и начинается с 0 (таким образом, включая точки вплоть до 99) будет выражаться значением 0 для левого элемента и значением 100 для правого члена. Обратите внимание, что для правого члена не используется значение 99.

Для **D3DBOX** наблюдаются ограничения на сторону, расположенные слева направо, сверху вниз и с начала до конца.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
