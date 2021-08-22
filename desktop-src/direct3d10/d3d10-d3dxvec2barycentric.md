---
description: Функция D3DXVec2BaryCentric (D3DX10Math. h) — возвращает точку в координатах Барицентрик с использованием указанных двумерных векторов.
ms.assetid: 8eceb2c0-26a0-4a7f-9830-85327dcb31ab
title: Функция D3DXVec2BaryCentric (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2BaryCentric
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: be7cf659a3f6c8aeffd07cdc9990e1e705d8b1db84aef019f77c0201961d16a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990744"
---
# <a name="d3dxvec2barycentric-function-d3dx10mathh"></a>Функция D3DXVec2BaryCentric (D3DX10Math. h)

Возвращает точку в координатах Барицентрик с использованием указанных двумерных векторов.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR2* D3DXVec2BaryCentric(
  _In_       D3DXVECTOR2 *pOut,
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2,
  _In_ const D3DXVECTOR2 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , который является результатом операции.

</dd> <dt>

*pV1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на исходную структуру D3DXVECTOR2.

</dd> <dt>

*pV2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на исходную структуру D3DXVECTOR2.

</dd> <dt>

*pV3* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на исходную структуру D3DXVECTOR2.

</dd> <dt>

*f* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Весовой коэффициент. См. заметки.

</dd> <dt>

*g* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Весовой коэффициент. См. заметки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Указатель на структуру D3DXVECTOR2 в координатах Барицентрик.

## <a name="remarks"></a>Remarks

Функция D3DXVec2BaryCentric предоставляет способ для понимания точек в треугольнике и вокруг него независимо от того, где фактически находится треугольник. Эта функция возвращает результирующую точку, используя следующее уравнение: v1 + f (V2-v1) + g (v3-v1).

Любая точка в плоскости V1V2V3 может быть представлена координатой Барицентрик (f, g). Параметр f управляет тем, сколько v2 имеет взвешенный результат, а параметр g определяет, сколько будет иметь взвешенное значение v3 в результате. Наконец, 1-f-g определяет, сколько единиц измерения v1 будет взвешено по результату.

Обратите внимание на следующие связи.

-   Если (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), точка находится внутри треугольника V1V2V3.
-   Если (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), точка находится в строке V1V3.
-   Если (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), то точка находится в строке V1V2.
-   Если (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), точка находится в строке V2V3.

Координаты барицентрик — это форма общих координат. В этом контексте использование координат Барицентрик представляет собой изменение в системах координат. Что содержит значение true для декартовых координат, имеет значение true для координат Барицентрик.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXVec2BaryCentric может использоваться в качестве параметра для другой функции.

Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника. Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
