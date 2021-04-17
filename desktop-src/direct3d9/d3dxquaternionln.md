---
description: Вычисляет натуральный логарифм.
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: Функция D3DXQuaternionLn (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b51fcc77da29216acd2bfc1c011a063014da5d69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548047"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a>Функция D3DXQuaternionLn (D3dx9math. h)

Вычисляет натуральный логарифм.

## <a name="syntax"></a>Синтаксис


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.

</dd> <dt>

*pQ* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является естественным логарифмом.

## <a name="remarks"></a>Комментарии

Функция **D3DXQuaternionLn** работает только для единичных кватернионов.


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXQuaternionLn** может использоваться в качестве параметра для другой функции.

Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionExp**](d3dxquaternionexp.md)
</dt> <dt>

[**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
</dt> </dl>

 

 




