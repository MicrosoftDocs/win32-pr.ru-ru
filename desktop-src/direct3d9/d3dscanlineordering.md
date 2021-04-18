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
ms.openlocfilehash: 2eaed36577f881266c12b0a927cfcdc2494f0d57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714016"
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

## <a name="remarks"></a>Комментарии

Это перечисление используется в качестве члена в [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) и [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




