---
description: Функция D3DXSHRotate (D3dx9math. h) — поворачивает сферическую гармонию (SH) на заданную матрицу.
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: Функция D3DXSHRotate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26505e768a0f8ad48b069cee2cc83876976e0134d8a60a2f93b17b0cb2aad323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298283"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a>Функция D3DXSHRotate (D3dx9math. h)

Поворачивает сферический гармониовый (SH) вектор на заданную матрицу.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на коэффициенты вывода в сферическую гармонию (SH). При оценке создается коэффициент порядка ². Этот указатель не должен иметь псевдоним с *ПИН-кодом*. См. заметки.

</dd> <dt>

*Порядок следования* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок вычисления SH. Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно. При оценке создается коэффициент порядка ². Степень оценки — Order-1.

</dd> <dt>

*пматрикс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на матрицу вращения. Подматрица вращения должна быть ортогональной с определителем единицы.

</dd> <dt>

*закрепить* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Указатель на повернутые коэффициенты SH.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на коэффициенты вывода SH.

## <a name="remarks"></a>Remarks

Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:

-   l — это степень базовой функции.
-   m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Предварительно вычисленный перенос Радианце (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
