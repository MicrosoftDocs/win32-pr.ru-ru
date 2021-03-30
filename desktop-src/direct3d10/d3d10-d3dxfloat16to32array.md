---
description: Преобразует массив 16-разрядных элементов с плавающей запятой в 32-разрядное число с плавающей запятой.
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: Функция D3DXFloat16To32Array (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a813553234c9e59ad34720da6f380977779e5d96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354990"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a>Функция D3DXFloat16To32Array (D3DX10Math. h)

Преобразует массив 16-разрядных элементов с плавающей запятой в 32-разрядное число с плавающей запятой.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на массив 32-разрядных элементов с плавающей запятой.

</dd> <dt>

*закрепить* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
