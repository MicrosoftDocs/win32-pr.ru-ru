---
description: Определяет метод объявления вершины, который представляет собой предопределенную операцию, выполняемую тесселяцией (или любую процедурную геометрию для данных вершин во время тесселяции).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Перечисление D3DDECLMETHOD (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354383"
---
# <a name="d3ddeclmethod-enumeration"></a><span data-ttu-id="14610-103">Перечисление D3DDECLMETHOD</span><span class="sxs-lookup"><span data-stu-id="14610-103">D3DDECLMETHOD enumeration</span></span>

<span data-ttu-id="14610-104">Определяет метод объявления вершины, который представляет собой предопределенную операцию, выполняемую тесселяцией (или любую процедурную геометрию для данных вершин во время тесселяции).</span><span class="sxs-lookup"><span data-stu-id="14610-104">Defines the vertex declaration method which is a predefined operation performed by the tessellator (or any procedural geometry routine on the vertex data during tessellation).</span></span>

## <a name="syntax"></a><span data-ttu-id="14610-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14610-105">Syntax</span></span>


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a><span data-ttu-id="14610-106">Константы</span><span class="sxs-lookup"><span data-stu-id="14610-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="14610-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="14610-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="14610-108">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14610-108">Default value.</span></span> <span data-ttu-id="14610-109">Тесселяция копирует данные вершин (данные сплайна для исправлений) без дополнительных вычислений.</span><span class="sxs-lookup"><span data-stu-id="14610-109">The tessellator copies the vertex data (spline data for patches) as is, with no additional calculations.</span></span> <span data-ttu-id="14610-110">При использовании тесселяции этот элемент интерполируются.</span><span class="sxs-lookup"><span data-stu-id="14610-110">When the tessellator is used, this element is interpolated.</span></span> <span data-ttu-id="14610-111">В противном случае данные вершин копируются во входной регистр.</span><span class="sxs-lookup"><span data-stu-id="14610-111">Otherwise vertex data is copied into the input register.</span></span> <span data-ttu-id="14610-112">Тип входных и выходных данных может иметь любое значение, но всегда один и тот же тип.</span><span class="sxs-lookup"><span data-stu-id="14610-112">The input and output type can be any value, but are always the same type.</span></span>

</dd> <dt>

<span data-ttu-id="14610-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ партиалу**</span><span class="sxs-lookup"><span data-stu-id="14610-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD\_PARTIALU**</span></span>
</dt> <dd>

<span data-ttu-id="14610-114">Выполняет вычисление тангенса в точке с обновлением прямоугольника или треугольника в направлении U.</span><span class="sxs-lookup"><span data-stu-id="14610-114">Computes the tangent at a point on the rectangle or triangle patch in the U direction.</span></span> <span data-ttu-id="14610-115">Тип входных данных может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="14610-115">The input type can be one of the following:</span></span>

-   <span data-ttu-id="14610-116">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="14610-116">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="14610-117">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="14610-117">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="14610-118">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="14610-118">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="14610-119">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="14610-119">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="14610-120">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="14610-120">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="14610-121">Тип выходных данных всегда D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="14610-121">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="14610-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ партиалв**</span><span class="sxs-lookup"><span data-stu-id="14610-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD\_PARTIALV**</span></span>
</dt> <dd>

<span data-ttu-id="14610-123">Выполняет вычисление тангенса в точке с обновлением прямоугольника или треугольника в направлении V.</span><span class="sxs-lookup"><span data-stu-id="14610-123">Computes the tangent at a point on the rectangle or triangle patch in the V direction.</span></span> <span data-ttu-id="14610-124">Тип входных данных может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="14610-124">The input type can be one of the following:</span></span>

-   <span data-ttu-id="14610-125">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="14610-125">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="14610-126">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="14610-126">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="14610-127">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="14610-127">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="14610-128">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="14610-128">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="14610-129">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="14610-129">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="14610-130">Тип выходных данных всегда D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="14610-130">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="14610-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ кроссув**</span><span class="sxs-lookup"><span data-stu-id="14610-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD\_CROSSUV**</span></span>
</dt> <dd>

<span data-ttu-id="14610-132">Выполняет вычисление нормали в точке на исправлении прямоугольника или треугольника, выполнив перекрестное произведение двух тангенсов.</span><span class="sxs-lookup"><span data-stu-id="14610-132">Computes the normal at a point on the rectangle or triangle patch by taking the cross product of two tangents.</span></span> <span data-ttu-id="14610-133">Тип входных данных может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="14610-133">The input type can be one of the following:</span></span>

-   <span data-ttu-id="14610-134">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="14610-134">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="14610-135">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="14610-135">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="14610-136">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="14610-136">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="14610-137">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="14610-137">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="14610-138">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="14610-138">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="14610-139">Тип выходных данных всегда D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="14610-139">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="14610-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD \_ UV**</span><span class="sxs-lookup"><span data-stu-id="14610-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="14610-141">Скопируйте значения U, V в точку с обновлением прямоугольника или треугольника.</span><span class="sxs-lookup"><span data-stu-id="14610-141">Copy out the U, V values at a point on the rectangle or triangle patch.</span></span> <span data-ttu-id="14610-142">В результате получается 2D с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="14610-142">This results in a 2D float.</span></span> <span data-ttu-id="14610-143">Для типа входных данных должно быть задано значение D3DDECLTYPE не \_ используется.</span><span class="sxs-lookup"><span data-stu-id="14610-143">The input type must be set to D3DDECLTYPE\_UNUSED.</span></span> <span data-ttu-id="14610-144">Тип выходных данных всегда D3DDECLTYPE \_ FLOAT2.</span><span class="sxs-lookup"><span data-stu-id="14610-144">The output data type is always D3DDECLTYPE\_FLOAT2.</span></span> <span data-ttu-id="14610-145">Входной поток и смещение также не являются неиспользуемыми (но должны иметь значение 0).</span><span class="sxs-lookup"><span data-stu-id="14610-145">The input stream and offset are also unused (but must be set to 0).</span></span>

</dd> <dt>

<span data-ttu-id="14610-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD \_ Поиск**</span><span class="sxs-lookup"><span data-stu-id="14610-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD\_LOOKUP**</span></span>
</dt> <dd>

<span data-ttu-id="14610-147">Найдите карту смещения.</span><span class="sxs-lookup"><span data-stu-id="14610-147">Look up a displacement map.</span></span> <span data-ttu-id="14610-148">Тип входных данных может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="14610-148">The input type can be one of the following:</span></span>

-   <span data-ttu-id="14610-149">D3DDECLTYPE \_ FLOAT2</span><span class="sxs-lookup"><span data-stu-id="14610-149">D3DDECLTYPE\_FLOAT2</span></span>
-   <span data-ttu-id="14610-150">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="14610-150">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="14610-151">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="14610-151">D3DDECLTYPE\_FLOAT4</span></span>

<span data-ttu-id="14610-152">Для поиска текстурных карт используются только компоненты x и y.</span><span class="sxs-lookup"><span data-stu-id="14610-152">Only the .x and .y components are used for the texture map lookup.</span></span> <span data-ttu-id="14610-153">Тип выходных данных всегда D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="14610-153">The output type is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="14610-154">Устройство должно поддерживать сопоставление смещений.</span><span class="sxs-lookup"><span data-stu-id="14610-154">The device must support displacement mapping.</span></span> <span data-ttu-id="14610-155">Дополнительные сведения о сопоставлении замещения см. в разделе [сопоставление смещения (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="14610-155">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="14610-156">Эта константа поддерживается только программируемым конвейером для N-патчных данных, если N — исправления включены.</span><span class="sxs-lookup"><span data-stu-id="14610-156">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="14610-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ лукуппресамплед**</span><span class="sxs-lookup"><span data-stu-id="14610-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD\_LOOKUPPRESAMPLED**</span></span>
</dt> <dd>

<span data-ttu-id="14610-158">Поиск предустановленной схемы смещения.</span><span class="sxs-lookup"><span data-stu-id="14610-158">Look up a presampled displacement map.</span></span> <span data-ttu-id="14610-159">Для входного типа необходимо задать значение D3DDECLTYPE не \_ используется; индекс потока и смещение потока должны быть установлены в значение 0.</span><span class="sxs-lookup"><span data-stu-id="14610-159">The input type must be set to D3DDECLTYPE\_UNUSED; the stream index and the stream offset must be set to 0.</span></span> <span data-ttu-id="14610-160">Тип выходных данных для этой операции всегда D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="14610-160">The output type for this operation is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="14610-161">Устройство должно поддерживать сопоставление смещений.</span><span class="sxs-lookup"><span data-stu-id="14610-161">The device must support displacement mapping.</span></span> <span data-ttu-id="14610-162">Дополнительные сведения о сопоставлении замещения см. в разделе [сопоставление смещения (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="14610-162">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="14610-163">Эта константа поддерживается только программируемым конвейером для N-патчных данных, если N — исправления включены.</span><span class="sxs-lookup"><span data-stu-id="14610-163">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span> <span data-ttu-id="14610-164">Этот метод можно использовать только с примером D3DDECLUSAGE \_ .</span><span class="sxs-lookup"><span data-stu-id="14610-164">This method can be used only with D3DDECLUSAGE\_SAMPLE.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14610-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14610-165">Remarks</span></span>

<span data-ttu-id="14610-166">Тесселяция просматривает метод, чтобы определить, какие данные следует вычислить из данных вершин во время тесселяции.</span><span class="sxs-lookup"><span data-stu-id="14610-166">The tessellator looks at the method to determine what data to calculate from the vertex data during tessellation.</span></span> <span data-ttu-id="14610-167">В данных сетки должно использоваться значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14610-167">Mesh data should use the default value.</span></span> <span data-ttu-id="14610-168">Исправления могут использовать любой из других реализованных типов.</span><span class="sxs-lookup"><span data-stu-id="14610-168">Patches can use any of the other implemented types.</span></span>

<span data-ttu-id="14610-169">Данные вершин объявляются с помощью массива структур [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="14610-169">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="14610-170">Каждый элемент массива содержит метод объявления вершины.</span><span class="sxs-lookup"><span data-stu-id="14610-170">Each element in the array contains a vertex declaration method.</span></span>

<span data-ttu-id="14610-171">Помимо использования D3DDECLMETHOD \_ по умолчанию, обычная сетка может использовать методы D3DDECLMETHOD \_ Lookup и D3DDECLMETHOD \_ Лукуппресамплед, если N-патчи включены.</span><span class="sxs-lookup"><span data-stu-id="14610-171">In addition to using D3DDECLMETHOD\_DEFAULT, a normal mesh can use D3DDECLMETHOD\_LOOKUP and D3DDECLMETHOD\_LOOKUPPRESAMPLED methods when N-patches are enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="14610-172">Требования</span><span class="sxs-lookup"><span data-stu-id="14610-172">Requirements</span></span>



| <span data-ttu-id="14610-173">Требование</span><span class="sxs-lookup"><span data-stu-id="14610-173">Requirement</span></span> | <span data-ttu-id="14610-174">Значение</span><span class="sxs-lookup"><span data-stu-id="14610-174">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14610-175">Header</span><span class="sxs-lookup"><span data-stu-id="14610-175">Header</span></span><br/> | <dl> <span data-ttu-id="14610-176"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="14610-176"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14610-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14610-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14610-178">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="14610-178">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




