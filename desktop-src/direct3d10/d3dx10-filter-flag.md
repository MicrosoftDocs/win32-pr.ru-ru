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
ms.openlocfilehash: f12842cd07c55c33509ecfbb56fc804a6fc3b7c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000488"
---
# <a name="d3dx10_filter_flag-enumeration"></a><span data-ttu-id="b19d6-103">\_ \_ Перечисление флагов фильтра D3DX10</span><span class="sxs-lookup"><span data-stu-id="b19d6-103">D3DX10\_FILTER\_FLAG enumeration</span></span>

<span data-ttu-id="b19d6-104">Флаги фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="b19d6-104">Texture filtering flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="b19d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b19d6-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="b19d6-106">Константы</span><span class="sxs-lookup"><span data-stu-id="b19d6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b19d6-107"><span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**\_Фильтр D3DX10 \_ None**</span><span class="sxs-lookup"><span data-stu-id="b19d6-107"><span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3DX10\_FILTER\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-108">Масштабирование или фильтрация не выполняются.</span><span class="sxs-lookup"><span data-stu-id="b19d6-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="b19d6-109">Пиксели вне границ исходного изображения считаются прозрачными черными.</span><span class="sxs-lookup"><span data-stu-id="b19d6-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-110"><span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**\_Точка фильтра \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="b19d6-110"><span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**D3DX10\_FILTER\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-111">Каждый конечный пиксель вычисляются путем выборки ближайшего пикселя из исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="b19d6-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-112"><span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**\_ \_ Линейный фильтр D3DX10**</span><span class="sxs-lookup"><span data-stu-id="b19d6-112"><span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**D3DX10\_FILTER\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-113">Каждый конечный пиксель вычисляются путем выборки четырех ближайших пикселей из исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="b19d6-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="b19d6-114">Этот фильтр лучше подходит, если масштаб по обеим осям меньше двух.</span><span class="sxs-lookup"><span data-stu-id="b19d6-114">This filter works best when the scale on both axes is less than two.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-115"><span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**\_Треугольник фильтра \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="b19d6-115"><span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**D3DX10\_FILTER\_TRIANGLE**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-116">Каждый пиксель в исходном изображении одинаково соответствует целевому образу.</span><span class="sxs-lookup"><span data-stu-id="b19d6-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="b19d6-117">Это самая медленная из фильтров.</span><span class="sxs-lookup"><span data-stu-id="b19d6-117">This is the slowest of the filters.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-118"><span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**\_Поле фильтра \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="b19d6-118"><span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**D3DX10\_FILTER\_BOX**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-119">Каждый пиксель вычисляются путем усреднения поля 2x2 (x2) пикселей из исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="b19d6-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="b19d6-120">Этот фильтр работает только в том случае, если измерения назначения являются половиной значений источника, как в случае с MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="b19d6-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-121"><span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**\_Зеркало фильтра \_ D3DX10 \_ U**</span><span class="sxs-lookup"><span data-stu-id="b19d6-121"><span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**D3DX10\_FILTER\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-122">Пиксели от края текстуры на оси u должны быть зеркально отображены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="b19d6-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-123"><span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**\_ \_ Зеркальное отображение фильтра D3DX10 \_ V**</span><span class="sxs-lookup"><span data-stu-id="b19d6-123"><span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3DX10\_FILTER\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-124">Пиксели от края текстуры на оси v должны быть зеркально отображены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="b19d6-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-125"><span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**\_ \_ Зеркальное отображение фильтра D3DX10 \_ W**</span><span class="sxs-lookup"><span data-stu-id="b19d6-125"><span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3DX10\_FILTER\_MIRROR\_W**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-126">Пиксели от края текстуры на оси w должны быть зеркально отражены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="b19d6-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-127"><span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**\_Зеркало фильтра \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="b19d6-127"><span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**D3DX10\_FILTER\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-128">Задание этого флага аналогично указанию \_ \_ флага зеркального отображения D3DX фильтра \_ U, D3DX \_ Filter \_ \_ V и \_ D3DX \_ фильтр \_ W Mirror.</span><span class="sxs-lookup"><span data-stu-id="b19d6-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-129"><span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**\_Дизеринг фильтра \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="b19d6-129"><span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**D3DX10\_FILTER\_DITHER**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-130">Полученный образ должен отменяться с помощью алгоритма сглаживания 4x4 с упорядочением.</span><span class="sxs-lookup"><span data-stu-id="b19d6-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span> <span data-ttu-id="b19d6-131">Это происходит при преобразовании из одного формата в другой.</span><span class="sxs-lookup"><span data-stu-id="b19d6-131">This happens when converting from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-132"><span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**\_ \_ Диффузное сглаживание фильтра D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="b19d6-132"><span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**D3DX10\_FILTER\_DITHER\_DIFFUSION**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-133">Рассеивание полутонов на изображении при переходе от одного формата к другому.</span><span class="sxs-lookup"><span data-stu-id="b19d6-133">Do diffuse dithering on the image when changing from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-134"><span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10 \_ фильтр \_ sRGB \_ в**</span><span class="sxs-lookup"><span data-stu-id="b19d6-134"><span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10\_FILTER\_SRGB\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-135">Входные данные находятся в стандартном цветовом пространстве RGB (sRGB).</span><span class="sxs-lookup"><span data-stu-id="b19d6-135">Input data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="b19d6-136">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="b19d6-136">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-137"><span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10 \_ фильтр \_ sRGB \_**</span><span class="sxs-lookup"><span data-stu-id="b19d6-137"><span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10\_FILTER\_SRGB\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-138">Выходные данные находятся в стандартном цветовом пространстве RGB (sRGB).</span><span class="sxs-lookup"><span data-stu-id="b19d6-138">Output data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="b19d6-139">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="b19d6-139">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-140"><span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**\_Фильтр D3DX10 \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="b19d6-140"><span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10\_FILTER\_SRGB**</span></span>
</dt> <dd>

<span data-ttu-id="b19d6-141">Аналогично указанию D3DX \_ Filter \_ sRGB \_ в \| D3DX \_ Filtering \_ sRGB \_ out.</span><span class="sxs-lookup"><span data-stu-id="b19d6-141">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span> <span data-ttu-id="b19d6-142">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="b19d6-142">See remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b19d6-143">Remarks</span><span class="sxs-lookup"><span data-stu-id="b19d6-143">Remarks</span></span>

<span data-ttu-id="b19d6-144">D3DX10 автоматически выполняет гамма-коррекцию (для преобразования цветовых данных из пространства RGB в стандартное пространство RGB) при загрузке данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="b19d6-144">D3DX10 automatically performs gamma correction (to convert color data from RGB space to standard RGB space) when loading texture data.</span></span> <span data-ttu-id="b19d6-145">Это автоматически выполняется для экземпляра, когда данные RGB загружаются из PNG-файла в текстуру sRGB.</span><span class="sxs-lookup"><span data-stu-id="b19d6-145">This is automatically done for instance when RGB data is loaded from a .png file into an sRGB texture.</span></span> <span data-ttu-id="b19d6-146">Используйте флаги фильтра SRGB, чтобы указать, нужно ли преобразовывать данные в пространство sRGB.</span><span class="sxs-lookup"><span data-stu-id="b19d6-146">Use the SRGB filter flags to indicate if the data does not need to be converted into sRGB space.</span></span>

## <a name="requirements"></a><span data-ttu-id="b19d6-147">Требования</span><span class="sxs-lookup"><span data-stu-id="b19d6-147">Requirements</span></span>



| <span data-ttu-id="b19d6-148">Требование</span><span class="sxs-lookup"><span data-stu-id="b19d6-148">Requirement</span></span> | <span data-ttu-id="b19d6-149">Значение</span><span class="sxs-lookup"><span data-stu-id="b19d6-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b19d6-150">Header</span><span class="sxs-lookup"><span data-stu-id="b19d6-150">Header</span></span><br/> | <dl> <span data-ttu-id="b19d6-151"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b19d6-151"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b19d6-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b19d6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b19d6-153">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="b19d6-153">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




