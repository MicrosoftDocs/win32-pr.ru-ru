---
description: Масштабирует сферический гармониовый вектор (SH); Иными словами, тоска \[ i \] = PA \[ \] \* , масштабирование.
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: Функция D3DXSHScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1a8cc7c63880876f85969443502db3d5fb3278c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157171"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a>Функция D3DXSHScale (D3dx9math. h)

Масштабирует сферический гармониовый вектор (SH); Иными словами, тоска \[ i \] = PA \[ \] \* , масштабирование.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на коэффициенты вывода в сферическую гармонию (SH). При оценке создается коэффициент порядка ². См. заметки.

</dd> <dt>

*Порядок следования* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок вычисления SH. Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно. При оценке создается коэффициент порядка ². Степень оценки — Order-1.

</dd> <dt>

*закрепить* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Указатель на вектор SH для масштабирования.

</dd> <dt>

*Масштаб* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Указатель на значение шкалы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на коэффициенты вывода SH.

## <a name="remarks"></a>Комментарии

Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:

-   l — это степень базовой функции.
-   m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Предварительно вычисленный перенос Радианце (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
