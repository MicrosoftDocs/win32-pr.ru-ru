---
description: Функция D3DXSHDot (D3dx9math. h) — подсчитывает скалярное произведение двух сферических гармонических (SH) векторов.
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: Функция D3DXSHDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87f88c7c7b80871a68084607cb99621199dfcc0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093932"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a>Функция D3DXSHDot (D3dx9math. h)

Рассчитывает скалярное произведение двух сферических гармонических (SH) векторов.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Порядок следования* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок вычисления сферического гармонического (SH). Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно. При оценке создается коэффициент порядка ². Степень оценки — Order-1.

</dd> <dt>

*PA* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Указатель на первый вектор SH.

</dd> <dt>

*Pb* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Указатель на второй вектор SH.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)**

Коэффициенты вывода SH.

## <a name="remarks"></a>Remarks

Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:

-   l — это степень базовой функции.
-   m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Предварительно вычисленный перенос Радианце (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
