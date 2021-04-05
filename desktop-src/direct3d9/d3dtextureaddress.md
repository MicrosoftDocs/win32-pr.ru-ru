---
description: Определяет константы, описывающие поддерживаемые режимы адресации текстуры.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: Перечисление D3DTEXTUREADDRESS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081850"
---
# <a name="d3dtextureaddress-enumeration"></a>Перечисление D3DTEXTUREADDRESS

Определяет константы, описывающие поддерживаемые режимы адресации текстуры.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS \_ Перенос**
</dt> <dd>

Мозаичное заполнение текстуры на каждой одноцелочисленной дизъюнкции. Например, для значений в диапазоне от 0 до 3 текстура повторяется три раза; Зеркальное отображение не выполняется.

</dd> <dt>

<span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**\_Зеркальное отображение D3DTADDRESS**
</dt> <dd>

Аналогично D3DTADDRESS \_ переносу, за исключением того, что текстура перемещается на каждое целое число. для значений в диапазоне от 0 до 1, например, текстура обнаправлена обычным образом; в диапазоне от 1 до 2 текстура зеркально отражается (зеркальная); в диапазоне от 2 до 3 текстура является нормальной. и т. д.

</dd> <dt>

<span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESSный \_ срез**
</dt> <dd>

Координаты текстуры за пределами диапазона \[ 0,0, 1,0 \] задаются в качестве цвета текстуры в 0,0 или 1,0 соответственно.

</dd> <dt>

<span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**\_Граница D3DTADDRESS**
</dt> <dd>

Координаты текстуры за пределами диапазона \[ 0,0, 1,0 \] задаются цветом границы.

</dd> <dt>

<span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ мирроронце**
</dt> <dd>

Аналогично \_ зеркальному D3DTADDRESS и D3DTADDRESSному \_ срезу. Принимает абсолютное значение координаты текстуры (то есть зеркальное отображение 0), а затем выполняет фиксацию до максимального значения. Чаще всего используется для текстур томов, где поддержка полного \_ режима адресации ТЕКСТУР D3DTADDRESS мирроронце не требуется, но данные являются симметричными вокруг одной оси.

</dd> <dt>

<span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
