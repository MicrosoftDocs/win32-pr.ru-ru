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
ms.openlocfilehash: 9e307527f93c153f0f78ce58b4d70ead4f7c1bc4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120559"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a><span data-ttu-id="8fb09-103">Калкулателевелофдетаил (объект текстуры DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8fb09-103">CalculateLevelOfDetail (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="8fb09-104">Вычисляет уровень детализации.</span><span class="sxs-lookup"><span data-stu-id="8fb09-104">Calculates the level of detail.</span></span>

<span data-ttu-id="8fb09-105">RET Object. Калкулателевелофдетаил ( \_ состояние образца S, float x);</span><span class="sxs-lookup"><span data-stu-id="8fb09-105">ret Object.CalculateLevelOfDetail( sampler\_state S, float x );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="8fb09-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fb09-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8fb09-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="8fb09-107">Item</span></span></th>
<th><span data-ttu-id="8fb09-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8fb09-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8fb09-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em></span><span class="sxs-lookup"><span data-stu-id="8fb09-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="8fb09-110">Любой тип <a href="dx-graphics-hlsl-to-type.md">объекта текстуры</a> (кроме Texture2DMS и Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="8fb09-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fb09-111"><span id="S"></span><span id="s"></span><em>#D0</em></span><span class="sxs-lookup"><span data-stu-id="8fb09-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="8fb09-112">окне <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Состояние образца</a>.</span><span class="sxs-lookup"><span data-stu-id="8fb09-112">[in] A <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Sampler state</a>.</span></span> <span data-ttu-id="8fb09-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="8fb09-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8fb09-114"><span id="x"></span><span id="X"></span><em>x</em></span><span class="sxs-lookup"><span data-stu-id="8fb09-114"><span id="x"></span><span id="X"></span><em>x</em></span></span><br/></td>
<td><span data-ttu-id="8fb09-115">окне Линейное значение или значения интерполяции, которые являются числом с плавающей запятой в диапазоне от 0,0 до 1,0 включительно.</span><span class="sxs-lookup"><span data-stu-id="8fb09-115">[in] The linear interpolation value or values, which is a floating-point number between 0.0 and 1.0 inclusive.</span></span> <span data-ttu-id="8fb09-116">Количество компонентов зависит от типа объекта «текстура».</span><span class="sxs-lookup"><span data-stu-id="8fb09-116">The number of components is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8fb09-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="8fb09-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="8fb09-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="8fb09-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8fb09-119">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8fb09-119">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="8fb09-120">float1</span><span class="sxs-lookup"><span data-stu-id="8fb09-120">float1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fb09-121">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8fb09-121">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="8fb09-122">float2</span><span class="sxs-lookup"><span data-stu-id="8fb09-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8fb09-123">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="8fb09-123">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="8fb09-124">float3</span><span class="sxs-lookup"><span data-stu-id="8fb09-124">float3</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="8fb09-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fb09-125">Return Value</span></span>

<span data-ttu-id="8fb09-126">Возвращает вычисленное Лод с одним значением с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="8fb09-126">Returns the calculated LOD, a single floating-point value.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="8fb09-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8fb09-127">Minimum Shader Model</span></span>

<span data-ttu-id="8fb09-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="8fb09-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8fb09-129">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8fb09-129">vs\_4\_0</span></span> | <span data-ttu-id="8fb09-130">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8fb09-130">vs\_4\_1</span></span>  | <span data-ttu-id="8fb09-131">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8fb09-131">ps\_4\_0</span></span> | <span data-ttu-id="8fb09-132">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8fb09-132">ps\_4\_1</span></span>  | <span data-ttu-id="8fb09-133">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8fb09-133">gs\_4\_0</span></span> | <span data-ttu-id="8fb09-134">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8fb09-134">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | <span data-ttu-id="8fb09-135">x</span><span class="sxs-lookup"><span data-stu-id="8fb09-135">x</span></span>         |          |           |



 

1.  <span data-ttu-id="8fb09-136">Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="8fb09-136">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="8fb09-137">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="8fb09-137">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fb09-138">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8fb09-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fb09-139">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="8fb09-139">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

