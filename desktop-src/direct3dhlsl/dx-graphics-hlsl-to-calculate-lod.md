---
title: Калкулателевелофдетаил (объект текстуры DirectX HLSL)
description: Вычисляет уровень детализации.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c59b8da97ff1cbe0bd88d6a49120a0a040cf3c30
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104984092"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a><span data-ttu-id="77e2b-103">Калкулателевелофдетаил (объект текстуры DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77e2b-103">CalculateLevelOfDetail (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="77e2b-104">Вычисляет уровень детализации.</span><span class="sxs-lookup"><span data-stu-id="77e2b-104">Calculates the level of detail.</span></span>



|                                                                 |
|-----------------------------------------------------------------|
| <span data-ttu-id="77e2b-105">RET Object. Калкулателевелофдетаил ( \_ состояние образца S, float x);</span><span class="sxs-lookup"><span data-stu-id="77e2b-105">ret Object.CalculateLevelOfDetail( sampler\_state S, float x );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="77e2b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="77e2b-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77e2b-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="77e2b-107">Item</span></span></th>
<th><span data-ttu-id="77e2b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="77e2b-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77e2b-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em></span><span class="sxs-lookup"><span data-stu-id="77e2b-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="77e2b-110">Любой тип <a href="dx-graphics-hlsl-to-type.md">объекта текстуры</a> (кроме Texture2DMS и Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="77e2b-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77e2b-111"><span id="S"></span><span id="s"></span><em>#D0</em></span><span class="sxs-lookup"><span data-stu-id="77e2b-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="77e2b-112">окне <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Состояние образца</a>.</span><span class="sxs-lookup"><span data-stu-id="77e2b-112">[in] A <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Sampler state</a>.</span></span> <span data-ttu-id="77e2b-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="77e2b-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77e2b-114"><span id="x"></span><span id="X"></span><em>x</em></span><span class="sxs-lookup"><span data-stu-id="77e2b-114"><span id="x"></span><span id="X"></span><em>x</em></span></span><br/></td>
<td><span data-ttu-id="77e2b-115">окне Линейное значение или значения интерполяции, которые являются числом с плавающей запятой в диапазоне от 0,0 до 1,0 включительно.</span><span class="sxs-lookup"><span data-stu-id="77e2b-115">[in] The linear interpolation value or values, which is a floating-point number between 0.0 and 1.0 inclusive.</span></span> <span data-ttu-id="77e2b-116">Количество компонентов зависит от типа объекта «текстура».</span><span class="sxs-lookup"><span data-stu-id="77e2b-116">The number of components is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77e2b-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="77e2b-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="77e2b-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="77e2b-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77e2b-119">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="77e2b-119">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="77e2b-120">float1</span><span class="sxs-lookup"><span data-stu-id="77e2b-120">float1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77e2b-121">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="77e2b-121">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="77e2b-122">float2</span><span class="sxs-lookup"><span data-stu-id="77e2b-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77e2b-123">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="77e2b-123">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="77e2b-124">float3</span><span class="sxs-lookup"><span data-stu-id="77e2b-124">float3</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="77e2b-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77e2b-125">Return Value</span></span>

<span data-ttu-id="77e2b-126">Возвращает вычисленное Лод с одним значением с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="77e2b-126">Returns the calculated LOD, a single floating-point value.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="77e2b-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="77e2b-127">Minimum Shader Model</span></span>

<span data-ttu-id="77e2b-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="77e2b-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="77e2b-129">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77e2b-129">vs\_4\_0</span></span> | <span data-ttu-id="77e2b-130">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77e2b-130">vs\_4\_1</span></span>  | <span data-ttu-id="77e2b-131">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77e2b-131">ps\_4\_0</span></span> | <span data-ttu-id="77e2b-132">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77e2b-132">ps\_4\_1</span></span>  | <span data-ttu-id="77e2b-133">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77e2b-133">gs\_4\_0</span></span> | <span data-ttu-id="77e2b-134">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77e2b-134">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | <span data-ttu-id="77e2b-135">x</span><span class="sxs-lookup"><span data-stu-id="77e2b-135">x</span></span>         |          |           |



 

1.  <span data-ttu-id="77e2b-136">Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="77e2b-136">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="77e2b-137">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="77e2b-137">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77e2b-138">См. также</span><span class="sxs-lookup"><span data-stu-id="77e2b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77e2b-139">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="77e2b-139">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

