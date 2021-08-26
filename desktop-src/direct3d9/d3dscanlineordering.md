---
description: Флаги, указывающие метод, используемый программой растеризации для создания изображения на поверхности.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: Перечисление D3DSCANLINEORDERING (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e5265387973c3c1605ac0022d88df3afa676dda614d7cc238e29a1ddd4a73f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987234"
---
# <a name="d3dscanlineordering-enumeration"></a>Перечисление D3DSCANLINEORDERING

Флаги, указывающие метод, используемый программой растеризации для создания изображения на поверхности.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ прогрессивный**
</dt> <dd>

Изображение создается из первого сканлине к последнему без пропуска.

</dd> <dt>

<span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING с \_ чередованием**
</dt> <dd>

Изображение создается с помощью метода чередования, в котором нечетные нумерованные линии рисуются на нечетных этапах, а даже линии рисуются с четными числами.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это перечисление используется в качестве члена в [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) и [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




