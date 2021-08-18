---
description: Функция D3DXQuaternionSlerp (D3DX10Math. h) — выполняет интерполяцию между двумя кватернионами с использованием сферической линейной интерполяции.
ms.assetid: 487e1df1-bf20-49cb-ad14-61fcf1300904
title: Функция D3DXQuaternionSlerp (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eca33eeb67f0c527efe7d0db8b8f17fe901d29dcbe3f2ef3b493463e01d34661
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990974"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a>Функция D3DXQuaternionSlerp (D3DX10Math. h)

Выполняет интерполяцию между двумя кватернионами, используя сферическую линейную интерполяцию.

## <a name="syntax"></a>Синтаксис


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.

</dd> <dt>

*pQ1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Указатель на исходную структуру D3DXQUATERNION.

</dd> <dt>

*pQ2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Указатель на исходную структуру D3DXQUATERNION.

</dd> <dt>

*t* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Параметр, который указывает, насколько проинтерполируются между кватернионми.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Указатель на структуру D3DXQUATERNION, которая является результатом интерполяции.

## <a name="remarks"></a>Remarks

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXQuaternionSlerp может использоваться в качестве параметра для другой функции.

Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
