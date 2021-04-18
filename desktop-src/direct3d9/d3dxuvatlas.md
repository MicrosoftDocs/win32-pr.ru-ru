---
description: Определяет параметры для выполнения вычислений геодезические Distance при подсчете текстуры на изогнутую поверхность. Используйте этот флаг, чтобы выбрать между высоким качеством и быстрыми вычислениями при вычислении текстуры Atlas.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Перечисление D3DXUVATLAS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 64cc116199b688fc9dcd8d6fbf331d85da508948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713606"
---
# <a name="d3dxuvatlas-enumeration"></a>Перечисление D3DXUVATLAS

Определяет параметры для выполнения вычислений геодезические Distance при подсчете текстуры на изогнутую поверхность. Используйте этот флаг, чтобы выбрать между высоким качеством и быстрыми вычислениями при вычислении текстуры Atlas.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS \_ по умолчанию**
</dt> <dd>

К сеткам с более чем 25kными лицами будет применяться метод жеодасик Distance, тогда как в сетках с числом лиц, меньшим, чем 25k, вместо них будет использоваться метод повышения качества геодезические.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS \_ геодезические \_ fast**
</dt> <dd>

Использует приближения для повышения скорости построения диаграммы за счет увеличения или увеличения количества диаграмм, выводимых для сетки.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS \_ геодезические \_ качество**
</dt> <dd>

Обеспечивает более качественные диаграммы, но требует больше времени и памяти, чем быстро.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




