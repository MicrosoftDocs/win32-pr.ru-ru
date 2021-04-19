---
description: Преобразует массив из 32-разрядных чисел с плавающей запятой в 16-битные с плавающей запятой.
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: Функция D3DXFloat32To16Array (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 360aebd5dd1af45fdc6fb5b9c23c514252f0ccf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720892"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a>Функция D3DXFloat32To16Array (D3dx9math. h)

Преобразует массив из 32-разрядных чисел с плавающей запятой в 16-битные с плавающей запятой.

## <a name="syntax"></a>Синтаксис


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***

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

Тип: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***

Указатель на массив 16-разрядных элементов с плавающей запятой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
