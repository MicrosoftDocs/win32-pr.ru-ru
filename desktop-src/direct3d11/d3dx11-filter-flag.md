---
title: Перечисление D3DX11_FILTER_FLAG (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Флаги фильтрации текстур.
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- Перечисление D3DX11_FILTER_FLAG Direct3D 11
- Указатель перечисления LPD3DX11_FILTER_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_FILTER_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2105970efb7f2ec07464d8a902df49d8f75bc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987221"
---
# <a name="d3dx11_filter_flag-enumeration"></a>\_ \_ Перечисление флагов фильтра D3DX11

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

Флаги фильтрации текстур.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DX11_FILTER_FLAG { 
  D3DX11_FILTER_NONE              = (1 << 0),
  D3DX11_FILTER_POINT             = (2 << 0),
  D3DX11_FILTER_LINEAR            = (3 << 0),
  D3DX11_FILTER_TRIANGLE          = (4 << 0),
  D3DX11_FILTER_BOX               = (5 << 0),
  D3DX11_FILTER_MIRROR_U          = (1 << 16),
  D3DX11_FILTER_MIRROR_V          = (2 << 16),
  D3DX11_FILTER_MIRROR_W          = (4 << 16),
  D3DX11_FILTER_MIRROR            = (7 << 16),
  D3DX11_FILTER_DITHER            = (1 << 19),
  D3DX11_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX11_FILTER_SRGB_IN           = (1 << 21),
  D3DX11_FILTER_SRGB_OUT          = (2 << 21),
  D3DX11_FILTER_SRGB              = (3 << 21)
} D3DX11_FILTER_FLAG, *LPD3DX11_FILTER_FLAG;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**\_Фильтр D3DX11 \_ None**
</dt> <dd>

Масштабирование или фильтрация не выполняются. Пиксели вне границ исходного изображения считаются прозрачными черными.

</dd> <dt>

<span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**\_Точка фильтра \_ D3DX11**
</dt> <dd>

Каждый конечный пиксель вычисляются путем выборки ближайшего пикселя из исходного изображения.

</dd> <dt>

<span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**\_ \_ Линейный фильтр D3DX11**
</dt> <dd>

Каждый конечный пиксель вычисляются путем выборки четырех ближайших пикселей из исходного изображения. Этот фильтр лучше подходит, если масштаб по обеим осям меньше двух.

</dd> <dt>

<span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**\_Треугольник фильтра \_ D3DX11**
</dt> <dd>

Каждый пиксель в исходном изображении одинаково соответствует целевому образу. Это самая медленная из фильтров.

</dd> <dt>

<span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**\_Поле фильтра \_ D3DX11**
</dt> <dd>

Каждый пиксель вычисляются путем усреднения поля 2x2 (x2) пикселей из исходного изображения. Этот фильтр работает только в том случае, если измерения назначения являются половиной значений источника, как в случае с MIP-карты.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**\_Зеркало фильтра \_ D3DX11 \_ U**
</dt> <dd>

Пиксели от края текстуры на оси u должны быть зеркально отображены, а не переноситься в оболочку.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**\_ \_ Зеркальное отображение фильтра D3DX11 \_ V**
</dt> <dd>

Пиксели от края текстуры на оси v должны быть зеркально отображены, а не переноситься в оболочку.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**\_ \_ Зеркальное отображение фильтра D3DX11 \_ W**
</dt> <dd>

Пиксели от края текстуры на оси w должны быть зеркально отражены, а не переноситься в оболочку.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**\_Зеркало фильтра \_ D3DX11**
</dt> <dd>

Задание этого флага аналогично указанию \_ \_ флага зеркального отображения D3DX фильтра \_ U, D3DX \_ Filter \_ \_ V и \_ D3DX \_ фильтр \_ W Mirror.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**\_Дизеринг фильтра \_ D3DX11**
</dt> <dd>

Полученный образ должен отменяться с помощью алгоритма сглаживания 4x4 с упорядочением. Это происходит при преобразовании из одного формата в другой.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**\_ \_ Диффузное сглаживание фильтра D3DX11 \_**
</dt> <dd>

Рассеивание полутонов на изображении при переходе от одного формата к другому.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11 \_ фильтр \_ sRGB \_ в**
</dt> <dd>

Входные данные находятся в стандартном цветовом пространстве RGB (sRGB). См. примечания.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ фильтр \_ sRGB \_**
</dt> <dd>

Выходные данные находятся в стандартном цветовом пространстве RGB (sRGB). См. примечания.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**\_Фильтр D3DX11 \_ sRGB**
</dt> <dd>

Аналогично указанию D3DX \_ Filter \_ sRGB \_ в \| D3DX \_ Filtering \_ sRGB \_ out. См. примечания.

</dd> </dl>

## <a name="remarks"></a>Remarks

D3DX11 автоматически выполняет гамма-коррекцию (для преобразования цветовых данных из пространства RGB в стандартное пространство RGB) при загрузке данных текстуры. Это автоматически выполняется для экземпляра, когда данные RGB загружаются из PNG-файла в текстуру sRGB. Используйте флаги фильтра SRGB, чтобы указать, нужно ли преобразовывать данные в пространство sRGB.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





