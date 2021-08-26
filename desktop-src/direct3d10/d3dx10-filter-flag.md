---
description: Флаги фильтрации текстур.
ms.assetid: bc73d916-fe18-4b15-b507-7954e157ab9a
title: Перечисление D3DX10_FILTER_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FILTER_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 400347efde28133055b97016d877b1bd4148624387ddd7086f4ff185ab87cca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989534"
---
# <a name="d3dx10_filter_flag-enumeration"></a>\_ \_ Перечисление флагов фильтра D3DX10

Флаги фильтрации текстур.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DX10_FILTER_FLAG { 
  D3DX10_FILTER_NONE              = (1 << 0),
  D3DX10_FILTER_POINT             = (2 << 0),
  D3DX10_FILTER_LINEAR            = (3 << 0),
  D3DX10_FILTER_TRIANGLE          = (4 << 0),
  D3DX10_FILTER_BOX               = (5 << 0),
  D3DX10_FILTER_MIRROR_U          = (1 << 16),
  D3DX10_FILTER_MIRROR_V          = (2 << 16),
  D3DX10_FILTER_MIRROR_W          = (4 << 16),
  D3DX10_FILTER_MIRROR            = (7 << 16),
  D3DX10_FILTER_DITHER            = (1 << 19),
  D3DX10_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX10_FILTER_SRGB_IN           = (1 << 21),
  D3DX10_FILTER_SRGB_OUT          = (2 << 21),
  D3DX10_FILTER_SRGB              = (3 << 21)
} D3DX10_FILTER_FLAG, *LPD3DX10_FILTER_FLAG;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**\_Фильтр D3DX10 \_ None**
</dt> <dd>

Масштабирование или фильтрация не выполняются. Пиксели вне границ исходного изображения считаются прозрачными черными.

</dd> <dt>

<span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**\_Точка фильтра \_ D3DX10**
</dt> <dd>

Каждый конечный пиксель вычисляются путем выборки ближайшего пикселя из исходного изображения.

</dd> <dt>

<span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**\_ \_ Линейный фильтр D3DX10**
</dt> <dd>

Каждый конечный пиксель вычисляются путем выборки четырех ближайших пикселей из исходного изображения. Этот фильтр лучше подходит, если масштаб по обеим осям меньше двух.

</dd> <dt>

<span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**\_Треугольник фильтра \_ D3DX10**
</dt> <dd>

Каждый пиксель в исходном изображении одинаково соответствует целевому образу. Это самая медленная из фильтров.

</dd> <dt>

<span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**\_Поле фильтра \_ D3DX10**
</dt> <dd>

Каждый пиксель вычисляются путем усреднения поля 2x2 (x2) пикселей из исходного изображения. Этот фильтр работает только в том случае, если измерения назначения являются половиной значений источника, как в случае с MIP-карты.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**\_Зеркало фильтра \_ D3DX10 \_ U**
</dt> <dd>

Пиксели от края текстуры на оси u должны быть зеркально отображены, а не переноситься в оболочку.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**\_ \_ Зеркальное отображение фильтра D3DX10 \_ V**
</dt> <dd>

Пиксели от края текстуры на оси v должны быть зеркально отображены, а не переноситься в оболочку.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**\_ \_ Зеркальное отображение фильтра D3DX10 \_ W**
</dt> <dd>

Пиксели от края текстуры на оси w должны быть зеркально отражены, а не переноситься в оболочку.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**\_Зеркало фильтра \_ D3DX10**
</dt> <dd>

Задание этого флага аналогично указанию \_ \_ флага зеркального отображения D3DX фильтра \_ U, D3DX \_ Filter \_ \_ V и \_ D3DX \_ фильтр \_ W Mirror.

</dd> <dt>

<span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**\_Дизеринг фильтра \_ D3DX10**
</dt> <dd>

Полученный образ должен отменяться с помощью алгоритма сглаживания 4x4 с упорядочением. Это происходит при преобразовании из одного формата в другой.

</dd> <dt>

<span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**\_ \_ Диффузное сглаживание фильтра D3DX10 \_**
</dt> <dd>

Рассеивание полутонов на изображении при переходе от одного формата к другому.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10 \_ фильтр \_ sRGB \_ в**
</dt> <dd>

Входные данные находятся в стандартном цветовом пространстве RGB (sRGB). См. примечания.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10 \_ фильтр \_ sRGB \_**
</dt> <dd>

Выходные данные находятся в стандартном цветовом пространстве RGB (sRGB). См. примечания.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**\_Фильтр D3DX10 \_ sRGB**
</dt> <dd>

Аналогично указанию D3DX \_ Filter \_ sRGB \_ в \| D3DX \_ Filtering \_ sRGB \_ out. См. примечания.

</dd> </dl>

## <a name="remarks"></a>Remarks

D3DX10 автоматически выполняет гамма-коррекцию (для преобразования цветовых данных из пространства RGB в стандартное пространство RGB) при загрузке данных текстуры. Это автоматически выполняется для экземпляра, когда данные RGB загружаются из файла .png в текстуру sRGB. Используйте флаги фильтра SRGB, чтобы указать, нужно ли преобразовывать данные в пространство sRGB.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




