---
description: Функция D3DXQuaternionToAxisAngle (D3DX10Math. h) — вычисление оси и угла поворота кватерниона.
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: Функция D3DXQuaternionToAxisAngle (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 51f704aa839ff210b3c2de57767cb32ec609232f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108702"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a>Функция D3DXQuaternionToAxisAngle (D3DX10Math. h)

Выполняет вычисление оси и угла поворота кватерниона.

## <a name="syntax"></a>Синтаксис


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pQ* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Указатель на источник [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).

</dd> <dt>

*паксис* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Эта функция возвращает указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , определяющий ось поворота кватерниона.

</dd> <dt>

*пангле* \[ в, out\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Эта функция возвращает указатель на значение FLOAT, идентифицирующее угол поворота кватерниона в радианах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
