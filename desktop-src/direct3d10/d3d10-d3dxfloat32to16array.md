---
description: Преобразует массив из 32-разрядных чисел с плавающей запятой в 16-битные с плавающей запятой.
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Функция D3DXFloat32To16Array (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4c116212be0ffa71ee35939d0a30a40cbb773b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694267"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a>Функция D3DXFloat32To16Array (D3DX10Math. h)

Преобразует массив из 32-разрядных чисел с плавающей запятой в 16-битные с плавающей запятой.

## <a name="syntax"></a>Синтаксис


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Указатель на массив 16-разрядных элементов с плавающей запятой.

</dd> <dt>

*закрепить* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Указатель на массив из 32 разрядов с плавающей запятой.

</dd> <dt>

*n* \[ в\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество элементов в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Указатель на массив 16-разрядных элементов с плавающей запятой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
