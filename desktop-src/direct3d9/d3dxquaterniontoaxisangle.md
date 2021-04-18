---
description: Выполняет вычисление оси и угла поворота кватерниона.
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: Функция D3DXQuaternionToAxisAngle (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecf8e6d1b1383a6e698f742351ee19ae75fd5bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713615"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a>Функция D3DXQuaternionToAxisAngle (D3dx9math. h)

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

Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .

</dd> <dt>

*паксис* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Эта функция возвращает указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая идентифицирует ось вращения кватернион.

</dd> <dt>

*пангле* \[ в, out\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Эта функция возвращает указатель на значение FLOAT, идентифицирующее угол поворота кватерниона в радианах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
