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
# <a name="d3dx11_filter_flag-enumeration"></a><span data-ttu-id="b3dff-106">\_ \_ Перечисление флагов фильтра D3DX11</span><span class="sxs-lookup"><span data-stu-id="b3dff-106">D3DX11\_FILTER\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="b3dff-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="b3dff-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="b3dff-108">Флаги фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="b3dff-108">Texture filtering flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3dff-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3dff-109">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="b3dff-110">Константы</span><span class="sxs-lookup"><span data-stu-id="b3dff-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b3dff-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**\_Фильтр D3DX11 \_ None**</span><span class="sxs-lookup"><span data-stu-id="b3dff-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11\_FILTER\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-112">Масштабирование или фильтрация не выполняются.</span><span class="sxs-lookup"><span data-stu-id="b3dff-112">No scaling or filtering will take place.</span></span> <span data-ttu-id="b3dff-113">Пиксели вне границ исходного изображения считаются прозрачными черными.</span><span class="sxs-lookup"><span data-stu-id="b3dff-113">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**\_Точка фильтра \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="b3dff-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**D3DX11\_FILTER\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-115">Каждый конечный пиксель вычисляются путем выборки ближайшего пикселя из исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="b3dff-115">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**\_ \_ Линейный фильтр D3DX11**</span><span class="sxs-lookup"><span data-stu-id="b3dff-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11\_FILTER\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-117">Каждый конечный пиксель вычисляются путем выборки четырех ближайших пикселей из исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="b3dff-117">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="b3dff-118">Этот фильтр лучше подходит, если масштаб по обеим осям меньше двух.</span><span class="sxs-lookup"><span data-stu-id="b3dff-118">This filter works best when the scale on both axes is less than two.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**\_Треугольник фильтра \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="b3dff-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**D3DX11\_FILTER\_TRIANGLE**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-120">Каждый пиксель в исходном изображении одинаково соответствует целевому образу.</span><span class="sxs-lookup"><span data-stu-id="b3dff-120">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="b3dff-121">Это самая медленная из фильтров.</span><span class="sxs-lookup"><span data-stu-id="b3dff-121">This is the slowest of the filters.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**\_Поле фильтра \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="b3dff-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**D3DX11\_FILTER\_BOX**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-123">Каждый пиксель вычисляются путем усреднения поля 2x2 (x2) пикселей из исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="b3dff-123">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="b3dff-124">Этот фильтр работает только в том случае, если измерения назначения являются половиной значений источника, как в случае с MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="b3dff-124">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**\_Зеркало фильтра \_ D3DX11 \_ U**</span><span class="sxs-lookup"><span data-stu-id="b3dff-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11\_FILTER\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-126">Пиксели от края текстуры на оси u должны быть зеркально отображены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="b3dff-126">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**\_ \_ Зеркальное отображение фильтра D3DX11 \_ V**</span><span class="sxs-lookup"><span data-stu-id="b3dff-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11\_FILTER\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-128">Пиксели от края текстуры на оси v должны быть зеркально отображены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="b3dff-128">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**\_ \_ Зеркальное отображение фильтра D3DX11 \_ W**</span><span class="sxs-lookup"><span data-stu-id="b3dff-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**D3DX11\_FILTER\_MIRROR\_W**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-130">Пиксели от края текстуры на оси w должны быть зеркально отражены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="b3dff-130">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**\_Зеркало фильтра \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="b3dff-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**D3DX11\_FILTER\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-132">Задание этого флага аналогично указанию \_ \_ флага зеркального отображения D3DX фильтра \_ U, D3DX \_ Filter \_ \_ V и \_ D3DX \_ фильтр \_ W Mirror.</span><span class="sxs-lookup"><span data-stu-id="b3dff-132">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**\_Дизеринг фильтра \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="b3dff-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**D3DX11\_FILTER\_DITHER**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-134">Полученный образ должен отменяться с помощью алгоритма сглаживания 4x4 с упорядочением.</span><span class="sxs-lookup"><span data-stu-id="b3dff-134">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span> <span data-ttu-id="b3dff-135">Это происходит при преобразовании из одного формата в другой.</span><span class="sxs-lookup"><span data-stu-id="b3dff-135">This happens when converting from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**\_ \_ Диффузное сглаживание фильтра D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="b3dff-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**D3DX11\_FILTER\_DITHER\_DIFFUSION**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-137">Рассеивание полутонов на изображении при переходе от одного формата к другому.</span><span class="sxs-lookup"><span data-stu-id="b3dff-137">Do diffuse dithering on the image when changing from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11 \_ фильтр \_ sRGB \_ в**</span><span class="sxs-lookup"><span data-stu-id="b3dff-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11\_FILTER\_SRGB\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-139">Входные данные находятся в стандартном цветовом пространстве RGB (sRGB).</span><span class="sxs-lookup"><span data-stu-id="b3dff-139">Input data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="b3dff-140">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="b3dff-140">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ фильтр \_ sRGB \_**</span><span class="sxs-lookup"><span data-stu-id="b3dff-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11\_FILTER\_SRGB\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-142">Выходные данные находятся в стандартном цветовом пространстве RGB (sRGB).</span><span class="sxs-lookup"><span data-stu-id="b3dff-142">Output data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="b3dff-143">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="b3dff-143">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b3dff-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**\_Фильтр D3DX11 \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="b3dff-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11\_FILTER\_SRGB**</span></span>
</dt> <dd>

<span data-ttu-id="b3dff-145">Аналогично указанию D3DX \_ Filter \_ sRGB \_ в \| D3DX \_ Filtering \_ sRGB \_ out.</span><span class="sxs-lookup"><span data-stu-id="b3dff-145">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span> <span data-ttu-id="b3dff-146">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="b3dff-146">See remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3dff-147">Remarks</span><span class="sxs-lookup"><span data-stu-id="b3dff-147">Remarks</span></span>

<span data-ttu-id="b3dff-148">D3DX11 автоматически выполняет гамма-коррекцию (для преобразования цветовых данных из пространства RGB в стандартное пространство RGB) при загрузке данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="b3dff-148">D3DX11 automatically performs gamma correction (to convert color data from RGB space to standard RGB space) when loading texture data.</span></span> <span data-ttu-id="b3dff-149">Это автоматически выполняется для экземпляра, когда данные RGB загружаются из PNG-файла в текстуру sRGB.</span><span class="sxs-lookup"><span data-stu-id="b3dff-149">This is automatically done for instance when RGB data is loaded from a .png file into an sRGB texture.</span></span> <span data-ttu-id="b3dff-150">Используйте флаги фильтра SRGB, чтобы указать, нужно ли преобразовывать данные в пространство sRGB.</span><span class="sxs-lookup"><span data-stu-id="b3dff-150">Use the SRGB filter flags to indicate if the data does not need to be converted into sRGB space.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3dff-151">Требования</span><span class="sxs-lookup"><span data-stu-id="b3dff-151">Requirements</span></span>



| <span data-ttu-id="b3dff-152">Требование</span><span class="sxs-lookup"><span data-stu-id="b3dff-152">Requirement</span></span> | <span data-ttu-id="b3dff-153">Значение</span><span class="sxs-lookup"><span data-stu-id="b3dff-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3dff-154">Header</span><span class="sxs-lookup"><span data-stu-id="b3dff-154">Header</span></span><br/> | <dl> <span data-ttu-id="b3dff-155"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3dff-155"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3dff-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3dff-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3dff-157">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="b3dff-157">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





