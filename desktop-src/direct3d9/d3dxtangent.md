---
description: Определяет параметры, используемые для вычислений с использованием сетки касательно.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Перечисление D3DXTANGENT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 5d6e57d2027a7366ec2b82ac7bd82aae4275d489c17f1922684e3ca6232be940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749774"
---
# <a name="d3dxtangent-enumeration"></a>Перечисление D3DXTANGENT

Определяет параметры, используемые для вычислений с использованием сетки касательно.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT в \_ оболочке \_ U**
</dt> <dd>

Значения координат текстуры в направлении u находятся в диапазоне от 0 до 1. В этом случае будет выбран набор координат текстуры, который свертывает периметр треугольника. См. раздел [Перенос текстур (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ переносить \_ V**
</dt> <dd>

Значения координат текстуры в направлении v находятся в диапазоне от 0 до 1. В этом случае будет выбран набор координат текстуры, который свертывает периметр треугольника. См. раздел [Перенос текстур (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ переносить \_ UV**
</dt> <dd>

Значения координат текстуры в обоих направлениях находятся в диапазоне от 0 до 1. В этом случае будет выбран набор координат текстуры, который свертывает периметр треугольника. См. раздел [Перенос текстур (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ не \_ нормализация \_ частичных частей**
</dt> <dd>

Не следует нормализовать частичные производные от относительно координат текстуры. Если не нормализовано, масштаб частичных производных объектов пропорционален масштабу трехмерной модели, деленной на масштабе треугольника в (u, v) пространстве. Это значение шкалы позволяет определить степень растяжения текстуры в заданном направлении. Результирующая Длина вектора является взвешенной суммой длин частичных производных.

</dd> <dt>

<span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ не \_ орсогонализе**
</dt> <dd>

Не преобразуйте координаты текстуры в деортогональные координаты Декарт. Взаимоисключающий с D3DXTANGENT \_ орсогонализе \_ из \_ вас и D3DXTANGENT \_ орсогонализе \_ из \_ V.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ орсогонализе \_ из \_ V**
</dt> <dd>

Вычислите частичные производные с учетом координаты текстуры v независимо для каждой вершины, а затем вычислите частичный производный результат по отношению к вам как перекрестное произведение частичного производного типа относительно v и обычного вектора. Взаимоисключающий с D3DXTANGENT \_ не \_ ОРСОГОНАЛИЗЕ и D3DXTANGENT \_ орсогонализе \_ от \_ U.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ орсогонализе \_ от \_ U**
</dt> <dd>

Вычислите частичные производные с учетом координаты текстуры u независимо для каждой вершины, а затем вычислите частичную производную по отношению к v как перекрестное произведение обычного вектора и частичного производного класса. Взаимоисключающий с D3DXTANGENT \_ не \_ ОРСОГОНАЛИЗЕ и D3DXTANGENT \_ орсогонализе \_ из \_ V.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**\_Вес D3DXTANGENT \_ по \_ областям**
</dt> <dd>

Толщина направления для вычисленного среднего или частичного производного вектора на вершину в соответствии с областями треугольников, присоединенных к этой вершине. Взаимоисключающий с D3DXTANGENTным \_ весом \_ равно.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT \_ вес \_ равен**
</dt> <dd>

Вычислите для каждого треугольника входной сетки Стандартный вектор длины блока. Взаимоисключающий с D3DXTANGENT \_ весом \_ по \_ областям.

</dd> <dt>

<span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ обмотка \_ во вт.**
</dt> <dd>

Вершины упорядочиваются по часовой стрелке вокруг каждого треугольника. Следовательно, вычисленное нормальное векторное направление передается на обратный 180 градусов от направления, вычисленного с помощью порядка вершин против часовой стрелки.

</dd> <dt>

<span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ Вычисление \_ нормальных вычислений**
</dt> <dd>

Вычислите вектор нормали для каждого вершины для каждого треугольника входной сетки и проигнорируйте все обычные векторы, которые уже находятся во входной сетке.

</dd> <dt>

<span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ создать \_ на \_ месте**
</dt> <dd>

Результаты хранятся в исходной входной сетке, а Выходная сетка не используется.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




