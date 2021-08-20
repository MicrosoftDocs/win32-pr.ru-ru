---
description: Функция D3DXFloat16To32Array (D3dx9math. h) — преобразует массив 16-разрядных элементов с плавающей запятой в 32-разрядное число с плавающей запятой.
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: Функция D3DXFloat16To32Array (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c5ce94dcadac8952792e31b51ad84fc2326668500c625728a0af5fd985f1d31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526041"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a>Функция D3DXFloat16To32Array (D3dx9math. h)

Преобразует массив 16-разрядных элементов с плавающей запятой в 32-разрядное число с плавающей запятой.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на массив 32-разрядных элементов с плавающей запятой.

</dd> <dt>

*закрепить* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***

Указатель на массив 16-разрядных элементов с плавающей запятой.

</dd> <dt>

*n* \[ в\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число элементов в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на массив из 32 разрядов с плавающей запятой.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
