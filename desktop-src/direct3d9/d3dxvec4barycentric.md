---
description: Функция D3DXVec4BaryCentric (D3dx9math. h) — возвращает точку в координатах Барицентрик, используя указанные векторы 4D.
ms.assetid: 80d73232-76bf-4f40-add2-dd1bdcc5cd98
title: Функция D3DXVec4BaryCentric (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 643773fe2be45bbae5709dcd7efaeae5fd4b86d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097712"
---
# <a name="d3dxvec4barycentric-function-d3dx9mathh"></a>Функция D3DXVec4BaryCentric (D3dx9math. h)

Возвращает точку в координатах Барицентрик с использованием указанных векторов 4D.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _Out_       D3DXVECTOR4 *pOut,
  _In_  const D3DXVECTOR4 *pV1,
  _In_  const D3DXVECTOR4 *pV2,
  _In_  const D3DXVECTOR4 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.

</dd> <dt>

*pV1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .

</dd> <dt>

*pV2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .

</dd> <dt>

*pV3* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .

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

Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) в координатах барицентрик.

## <a name="remarks"></a>Remarks

Функция **D3DXVec4BaryCentric** предоставляет способ для понимания точек в треугольнике и вокруг него независимо от того, где фактически находится треугольник. Эта функция возвращает результирующую точку, используя следующее уравнение: v1 + f (V2-v1) + g (v3-v1).

Любая точка в плоскости V1V2V3 может быть представлена координатой Барицентрик (f, g). Параметр *f* управляет тем, сколько v2 имеет взвешенный результат, а параметр *g* определяет, сколько единиц измерения v3 будет взвешено по результату. Наконец, 1-f-g определяет, сколько единиц измерения v1 будет взвешено по результату.

Обратите внимание на следующие связи.

-   Если (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), точка находится внутри треугольника V1V2V3.
-   Если (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), точка находится в строке V1V3.
-   Если (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), то точка находится в строке V1V2.
-   Если (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), точка находится в строке V2V3.

Координаты барицентрик — это форма общих координат. В этом контексте использование координат Барицентрик представляет собой изменение в системах координат. Что содержит значение true для декартовых координат, имеет значение true для координат Барицентрик.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXVec4BaryCentric** может использоваться в качестве параметра для другой функции.

Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника. Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
