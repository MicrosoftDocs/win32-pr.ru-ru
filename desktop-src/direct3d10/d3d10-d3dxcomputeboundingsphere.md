---
description: Функция D3DXComputeBoundingSphere (D3DX10math. h) — вычисление ограничивающей сферы для сетки.
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: Функция D3DXComputeBoundingSphere (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88a738c880bcf338e0afafdb40f1d215a8c3aa48712b47180515d36cc24d4c47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730044"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a>Функция D3DXComputeBoundingSphere (D3DX10math. h)

Вычисление ограничивающей сферы для сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфирстпоситион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на первую точку.

</dd> <dt>

*Нумвертицес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число вершин.

</dd> <dt>

*двстриде* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число байтов между векторами позиционирования.

</dd> <dt>

*пцентер* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Структура [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , определяющая центр координат возвращаемой ограничивающей сферы.

</dd> <dt>

*Прадиус* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Радиус возвращаемой ограничивающей сферы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции сетки](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
