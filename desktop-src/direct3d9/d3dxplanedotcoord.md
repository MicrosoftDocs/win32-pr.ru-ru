---
description: Вычисление точки в плоскости и трехмерном векторе. Параметр w вектора предполагается равным 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: Функция D3DXPlaneDotCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30f04ec310ce66dc43073e724b08c358cd8fc6f24f0b3840475a1abc61544503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524931"
---
# <a name="d3dxplanedotcoord-function"></a>Функция D3DXPlaneDotCoord

Вычисление точки в плоскости и трехмерном векторе. Параметр w вектора предполагается равным 1.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PP* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXPLANE**](d3dxplane.md) \***

Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)**

Скалярное произведение плоскости и трехмерного вектора.

## <a name="remarks"></a>Remarks

При наличии плоскости (a, b, c, d) и трехмерного вектора (x, y, z) возвращаемое значение этой функции является \* x + b \* y + c \* z + d \* 1. Функция **D3DXPlaneDotCoord** полезна для определения связи плоскости с координатами в трехмерном пространстве.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
