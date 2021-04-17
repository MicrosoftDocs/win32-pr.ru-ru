---
description: Определяет предполагаемое использование данных вершин.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Перечисление D3DDECLUSAGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3997aa38a7a97455b9f36d8afbee896ca9ae937
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720879"
---
# <a name="d3ddeclusage-enumeration"></a><span data-ttu-id="00830-103">Перечисление D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="00830-103">D3DDECLUSAGE enumeration</span></span>

<span data-ttu-id="00830-104">Определяет предполагаемое использование данных вершин.</span><span class="sxs-lookup"><span data-stu-id="00830-104">Identifies the intended use of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="00830-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00830-105">Syntax</span></span>


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a><span data-ttu-id="00830-106">Константы</span><span class="sxs-lookup"><span data-stu-id="00830-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="00830-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGEное \_ расположение**</span><span class="sxs-lookup"><span data-stu-id="00830-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="00830-108">Размещение данных в диапазоне от (-1,-1) до (1, 1).</span><span class="sxs-lookup"><span data-stu-id="00830-108">Position data ranging from (-1,-1) to (1,1).</span></span> <span data-ttu-id="00830-109">Используйте D3DDECLUSAGE \_ позиции с индексом использования 0, чтобы указать непреобразованную точку для обработки вершины фиксированной функции и тесселяцию n-patch.</span><span class="sxs-lookup"><span data-stu-id="00830-109">Use D3DDECLUSAGE\_POSITION with a usage index of 0 to specify untransformed position for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="00830-110">Используйте D3DDECLUSAGE \_ позиции с индексом использования, равным 1, чтобы указать непреобразованное расположение в шейдере вершинной функции для анимации вершин.</span><span class="sxs-lookup"><span data-stu-id="00830-110">Use D3DDECLUSAGE\_POSITION with a usage index of 1 to specify untransformed position in the fixed function vertex shader for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="00830-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ блендвеигхт**</span><span class="sxs-lookup"><span data-stu-id="00830-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE\_BLENDWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="00830-112">Данные веса смешения.</span><span class="sxs-lookup"><span data-stu-id="00830-112">Blending weight data.</span></span> <span data-ttu-id="00830-113">Используйте D3DDECLUSAGE \_ блендвеигхт с индексом использования 0, чтобы указать весовые коэффициенты смешения, используемые в индексированном и неиндексированном смешении вершин.</span><span class="sxs-lookup"><span data-stu-id="00830-113">Use D3DDECLUSAGE\_BLENDWEIGHT with a usage index of 0 to specify the blend weights used in indexed and nonindexed vertex blending.</span></span>

</dd> <dt>

<span data-ttu-id="00830-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ блендиндицес**</span><span class="sxs-lookup"><span data-stu-id="00830-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE\_BLENDINDICES**</span></span>
</dt> <dd>

<span data-ttu-id="00830-115">Смешивание данных индексов.</span><span class="sxs-lookup"><span data-stu-id="00830-115">Blending indices data.</span></span> <span data-ttu-id="00830-116">Используйте D3DDECLUSAGE \_ блендиндицес с индексом использования 0, чтобы указать индексы матрицы для выборки с индексированными палитрами.</span><span class="sxs-lookup"><span data-stu-id="00830-116">Use D3DDECLUSAGE\_BLENDINDICES with a usage index of 0 to specify matrix indices for indexed paletted skinning.</span></span>

</dd> <dt>

<span data-ttu-id="00830-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE, \_ Обычная**</span><span class="sxs-lookup"><span data-stu-id="00830-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="00830-118">Нормальные данные вершин.</span><span class="sxs-lookup"><span data-stu-id="00830-118">Vertex normal data.</span></span> <span data-ttu-id="00830-119">Используйте D3DDECLUSAGE \_ нормаль с индексом использования, равным 0, чтобы указать нормали вершин для обработки фиксированной вершины функции и тесселяцию n-patch.</span><span class="sxs-lookup"><span data-stu-id="00830-119">Use D3DDECLUSAGE\_NORMAL with a usage index of 0 to specify vertex normals for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="00830-120">Используйте D3DDECLUSAGE \_ нормаль с индексом использования, равным 1, чтобы указать нормали вершин для обработки фиксированной вершины функции для анимации вершин.</span><span class="sxs-lookup"><span data-stu-id="00830-120">Use D3DDECLUSAGE\_NORMAL with a usage index of 1 to specify vertex normals for fixed function vertex processing for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="00830-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ псизе**</span><span class="sxs-lookup"><span data-stu-id="00830-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE\_PSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="00830-122">Размер точки данных.</span><span class="sxs-lookup"><span data-stu-id="00830-122">Point size data.</span></span> <span data-ttu-id="00830-123">Используйте D3DDECLUSAGE \_ псизе с индексом использования, равным 0, чтобы указать атрибут размера точки, используемый ядром программы установки средства настройки компонента, чтобы расширить точку до четырех элементов для функции "звезда".</span><span class="sxs-lookup"><span data-stu-id="00830-123">Use D3DDECLUSAGE\_PSIZE with a usage index of 0 to specify the point-size attribute used by the setup engine of the rasterizer to expand a point into a quad for the point-sprite functionality.</span></span>

</dd> <dt>

<span data-ttu-id="00830-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ текскурд**</span><span class="sxs-lookup"><span data-stu-id="00830-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE\_TEXCOORD**</span></span>
</dt> <dd>

<span data-ttu-id="00830-125">Данные координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="00830-125">Texture coordinate data.</span></span> <span data-ttu-id="00830-126">Используйте D3DDECLUSAGE \_ текскурд, n для указания координат текстуры в процессе обработки вершин фиксированной функции и в шейдерах пикселей до PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="00830-126">Use D3DDECLUSAGE\_TEXCOORD, n to specify texture coordinates in fixed function vertex processing and in pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="00830-127">Их можно использовать для передачи определяемых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="00830-127">These can be used to pass user defined data.</span></span>

</dd> <dt>

<span data-ttu-id="00830-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE \_ тангенс**</span><span class="sxs-lookup"><span data-stu-id="00830-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE\_TANGENT**</span></span>
</dt> <dd>

<span data-ttu-id="00830-129">Данные касательной вершины.</span><span class="sxs-lookup"><span data-stu-id="00830-129">Vertex tangent data.</span></span>

</dd> <dt>

<span data-ttu-id="00830-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ бинормал**</span><span class="sxs-lookup"><span data-stu-id="00830-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE\_BINORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="00830-131">Данные бинормал вершин.</span><span class="sxs-lookup"><span data-stu-id="00830-131">Vertex binormal data.</span></span>

</dd> <dt>

<span data-ttu-id="00830-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ тессфактор**</span><span class="sxs-lookup"><span data-stu-id="00830-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE\_TESSFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="00830-133">Одиночное положительное значение с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="00830-133">Single positive floating point value.</span></span> <span data-ttu-id="00830-134">Используйте D3DDECLUSAGE \_ тессфактор с индексом использования 0, чтобы указать коэффициент тесселяции, используемый в единице тесселяции для управления частотой тесселяции.</span><span class="sxs-lookup"><span data-stu-id="00830-134">Use D3DDECLUSAGE\_TESSFACTOR with a usage index of 0 to specify a tessellation factor used in the tessellation unit to control the rate of tessellation.</span></span> <span data-ttu-id="00830-135">Дополнительные сведения о типе данных см. в разделе D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="00830-135">For more information about the data type, see D3DDECLTYPE\_FLOAT1.</span></span>

</dd> <dt>

<span data-ttu-id="00830-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE \_ позиций**</span><span class="sxs-lookup"><span data-stu-id="00830-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE\_POSITIONT**</span></span>
</dt> <dd>

<span data-ttu-id="00830-137">Данные вершин содержат преобразованные данные о положении в диапазоне от (0, 0) до (ширина окна просмотра, высота окна просмотра).</span><span class="sxs-lookup"><span data-stu-id="00830-137">Vertex data contains transformed position data ranging from (0,0) to (viewport width, viewport height).</span></span> <span data-ttu-id="00830-138">Используйте D3DDECLUSAGE \_ позиции с индексом использования, равным 0, чтобы указать преобразованное расположение.</span><span class="sxs-lookup"><span data-stu-id="00830-138">Use D3DDECLUSAGE\_POSITIONT with a usage index of 0 to specify transformed position.</span></span> <span data-ttu-id="00830-139">Если задано объявление, содержащее это значение, конвейер не выполняет обработку вершин.</span><span class="sxs-lookup"><span data-stu-id="00830-139">When a declaration containing this is set, the pipeline does not perform vertex processing.</span></span>

</dd> <dt>

<span data-ttu-id="00830-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**\_Цвет D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="00830-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="00830-141">Данные вершин содержат рассеянный или отраженный цвет.</span><span class="sxs-lookup"><span data-stu-id="00830-141">Vertex data contains diffuse or specular color.</span></span> <span data-ttu-id="00830-142">Используйте D3DDECLUSAGE \_ Color с индексом использования, равным 0, чтобы указать рассеянный цвет в предваряющих текстурах в функции и шейдеры пикселей до PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="00830-142">Use D3DDECLUSAGE\_COLOR with a usage index of 0 to specify the diffuse color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="00830-143">Используйте D3DDECLUSAGE \_ Color с индексом использования, равным 1, чтобы указать отражающий цвет в предваряющих текстурах и в шейдерах пикселей перед PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="00830-143">Use D3DDECLUSAGE\_COLOR with a usage index of 1 to specify the specular color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="00830-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE \_ туман**</span><span class="sxs-lookup"><span data-stu-id="00830-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE\_FOG**</span></span>
</dt> <dd>

<span data-ttu-id="00830-145">Данные вершин содержат данные тумана.</span><span class="sxs-lookup"><span data-stu-id="00830-145">Vertex data contains fog data.</span></span> <span data-ttu-id="00830-146">Используйте D3DDECLUSAGE \_ туман с индексом использования, равным 0, чтобы указать значение смешения тумана, используемое после завершения заливки пикселей.</span><span class="sxs-lookup"><span data-stu-id="00830-146">Use D3DDECLUSAGE\_FOG with a usage index of 0 to specify a fog blend value used after pixel shading finishes.</span></span> <span data-ttu-id="00830-147">Это относится к шейдерам пикселей до версии PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="00830-147">This applies to pixel shaders prior to version ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="00830-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**\_Глубина D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="00830-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE\_DEPTH**</span></span>
</dt> <dd>

<span data-ttu-id="00830-149">Данные вершин содержат данные глубины.</span><span class="sxs-lookup"><span data-stu-id="00830-149">Vertex data contains depth data.</span></span>

</dd> <dt>

<span data-ttu-id="00830-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**\_Пример D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="00830-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE\_SAMPLE**</span></span>
</dt> <dd>

<span data-ttu-id="00830-151">Данные вершин содержат данные выборки.</span><span class="sxs-lookup"><span data-stu-id="00830-151">Vertex data contains sampler data.</span></span> <span data-ttu-id="00830-152">Используйте \_ Пример D3DDECLUSAGE с индексом использования, равным 0, чтобы указать значение смещения для поиска.</span><span class="sxs-lookup"><span data-stu-id="00830-152">Use D3DDECLUSAGE\_SAMPLE with a usage index of 0 to specify the displacement value to look up.</span></span> <span data-ttu-id="00830-153">Его можно использовать только с D3DDECLUSAGE \_ лукуппресамплед или D3DDECLUSAGE \_ Lookup.</span><span class="sxs-lookup"><span data-stu-id="00830-153">It can be used only with D3DDECLUSAGE\_LOOKUPPRESAMPLED or D3DDECLUSAGE\_LOOKUP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00830-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00830-154">Remarks</span></span>

<span data-ttu-id="00830-155">Данные вершин объявляются с помощью массива структур [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="00830-155">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="00830-156">Каждый элемент массива содержит тип использования.</span><span class="sxs-lookup"><span data-stu-id="00830-156">Each element in the array contains a usage type.</span></span>

<span data-ttu-id="00830-157">Дополнительные сведения об объявлениях вершин см. в разделе [объявление вершины (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="00830-157">For more information about vertex declarations, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00830-158">Требования</span><span class="sxs-lookup"><span data-stu-id="00830-158">Requirements</span></span>



| <span data-ttu-id="00830-159">Требование</span><span class="sxs-lookup"><span data-stu-id="00830-159">Requirement</span></span> | <span data-ttu-id="00830-160">Значение</span><span class="sxs-lookup"><span data-stu-id="00830-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00830-161">Header</span><span class="sxs-lookup"><span data-stu-id="00830-161">Header</span></span><br/> | <dl> <span data-ttu-id="00830-162"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="00830-162"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00830-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00830-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00830-164">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="00830-164">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="00830-165">Объявление вершины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="00830-165">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 




