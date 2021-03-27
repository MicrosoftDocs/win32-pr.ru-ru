---
title: Измерения (объект текстуры DirectX HLSL)
description: Возвращает сведения о размере текстуры. Блок синтаксиса показывает все параметры, доступные в объявлении метода. В таблице в разделе "Примечания" показано, какие параметры реализуются для каждого типа объекта текстуры.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103889996"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a><span data-ttu-id="49455-105">Измерения (объект текстуры DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="49455-105">GetDimensions (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="49455-106">Возвращает сведения о размере текстуры.</span><span class="sxs-lookup"><span data-stu-id="49455-106">Gets texture size information.</span></span> <span data-ttu-id="49455-107">Блок синтаксиса показывает все параметры, доступные в объявлении метода.</span><span class="sxs-lookup"><span data-stu-id="49455-107">The syntax block shows all the parameters that are possible in the method declaration.</span></span> <span data-ttu-id="49455-108">В таблице в разделе "Примечания" показано, какие параметры реализуются для каждого типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="49455-108">The table in the Remarks section shows which parameters are implemented for each texture-object type.</span></span>



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49455-109">void Object. GetObject (UINT Миплевел, ширина Типекс, высота Типекс, элементы Типекс, глубина Типекс, Типекс Нумберофлевелс, Типекс Нумберофсамплес);</span><span class="sxs-lookup"><span data-stu-id="49455-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span></span> |



 

<span data-ttu-id="49455-110">Типекс указывает, что существует два возможных типа: **uint** или **float**.</span><span class="sxs-lookup"><span data-stu-id="49455-110">typeX denotes that there are two possible types: **uint** or **float**.</span></span>

## <a name="parameters"></a><span data-ttu-id="49455-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="49455-111">Parameters</span></span>



| <span data-ttu-id="49455-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="49455-112">Item</span></span>                                                                                                                               | <span data-ttu-id="49455-113">Описание</span><span class="sxs-lookup"><span data-stu-id="49455-113">Description</span></span>                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49455-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Объектами*</span><span class="sxs-lookup"><span data-stu-id="49455-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/>                                     | <span data-ttu-id="49455-115">Любой тип [объекта текстуры](dx-graphics-hlsl-to-type.md) , за исключением объекта **буфера** .</span><span class="sxs-lookup"><span data-stu-id="49455-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type except a **Buffer** object.</span></span><br/>                                       |
| <span data-ttu-id="49455-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*миплевел*</span><span class="sxs-lookup"><span data-stu-id="49455-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span></span><br/>                             | <span data-ttu-id="49455-117">\[в \] индексе (с отсчетом от нуля), определяющем уровень mipmap.</span><span class="sxs-lookup"><span data-stu-id="49455-117">\[in\] A zero-based index that identifies the mipmap level.</span></span> <span data-ttu-id="49455-118">Если этот аргумент не используется, предполагается первый MIP уровень.</span><span class="sxs-lookup"><span data-stu-id="49455-118">If this argument is not used, the first mip level is assumed.</span></span><br/> |
| <span data-ttu-id="49455-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Ширина*</span><span class="sxs-lookup"><span data-stu-id="49455-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Width*</span></span><br/>                                         | <span data-ttu-id="49455-120">\[\]Ширина текстуры в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="49455-120">\[out\] The texture width, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="49455-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Равно*</span><span class="sxs-lookup"><span data-stu-id="49455-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Height*</span></span><br/>                                     | <span data-ttu-id="49455-122">\[\]Высота текстуры в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="49455-122">\[out\] The texture height, in texels.</span></span><br/>                                                                                    |
| <span data-ttu-id="49455-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Элементов*</span><span class="sxs-lookup"><span data-stu-id="49455-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elements*</span></span><br/>                             | <span data-ttu-id="49455-124">\[\]количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="49455-124">\[out\] The number of elements in an array.</span></span><br/>                                                                               |
| <span data-ttu-id="49455-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Длина*</span><span class="sxs-lookup"><span data-stu-id="49455-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Depth*</span></span><br/>                                         | <span data-ttu-id="49455-126">\[\]глубина текстуры в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="49455-126">\[out\] The texture depth, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="49455-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*нумберофлевелс*</span><span class="sxs-lookup"><span data-stu-id="49455-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span></span><br/>     | <span data-ttu-id="49455-128">\[\]количество уровней mipmap.</span><span class="sxs-lookup"><span data-stu-id="49455-128">\[out\] The number of mipmap levels.</span></span><br/>                                                                                      |
| <span data-ttu-id="49455-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*нумберофсамплес*</span><span class="sxs-lookup"><span data-stu-id="49455-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span></span><br/> | <span data-ttu-id="49455-130">\[\]количество выборок.</span><span class="sxs-lookup"><span data-stu-id="49455-130">\[out\] The number of samples.</span></span><br/>                                                                                            |



 

## <a name="return-value"></a><span data-ttu-id="49455-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49455-131">Return Value</span></span>

<span data-ttu-id="49455-132">Нет</span><span class="sxs-lookup"><span data-stu-id="49455-132">None</span></span>

## <a name="overloaded-methods"></a><span data-ttu-id="49455-133">Перегруженные методы</span><span class="sxs-lookup"><span data-stu-id="49455-133">Overloaded Methods</span></span>

<span data-ttu-id="49455-134">В этой таблице перечислены все различные версии метода. версии отличаются числом входных параметров.</span><span class="sxs-lookup"><span data-stu-id="49455-134">This table lists all the different versions of the method; versions differs by the number of input parameters.</span></span> <span data-ttu-id="49455-135">Обратите внимание, что для каждого метода, принимающего целочисленные параметры, существует перегруженный метод, принимающий параметры с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="49455-135">Notice that for every method that takes integer parameters, there is an overloaded method that takes floating-point parameters.</span></span>



| <span data-ttu-id="49455-136">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="49455-136">Texture-Object Type</span></span> | <span data-ttu-id="49455-137">Входные параметры</span><span class="sxs-lookup"><span data-stu-id="49455-137">Input Parameters</span></span>                                                               |
|---------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="49455-138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="49455-138">Texture1D</span></span>           | <span data-ttu-id="49455-139">UINT Миплевел, ширина UINT, UINT Нумберофлевелс</span><span class="sxs-lookup"><span data-stu-id="49455-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span></span>                                 |
| <span data-ttu-id="49455-140">Texture1D</span><span class="sxs-lookup"><span data-stu-id="49455-140">Texture1D</span></span>           | <span data-ttu-id="49455-141">Ширина UINT</span><span class="sxs-lookup"><span data-stu-id="49455-141">UINT Width</span></span>                                                                     |
| <span data-ttu-id="49455-142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="49455-142">Texture1D</span></span>           | <span data-ttu-id="49455-143">UINT Миплевел, Width float, float Нумберофлевелс</span><span class="sxs-lookup"><span data-stu-id="49455-143">UINT MipLevel, float Width, float NumberOfLevels</span></span>                               |
| <span data-ttu-id="49455-144">Texture1D</span><span class="sxs-lookup"><span data-stu-id="49455-144">Texture1D</span></span>           | <span data-ttu-id="49455-145">Ширина плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-145">float Width</span></span>                                                                    |
| <span data-ttu-id="49455-146">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="49455-146">Texture1DArray</span></span>      | <span data-ttu-id="49455-147">UINT Миплевел, ширина UINT, элементы UINT, UINT Нумберофлевелс</span><span class="sxs-lookup"><span data-stu-id="49455-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="49455-148">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="49455-148">Texture1DArray</span></span>      | <span data-ttu-id="49455-149">Ширина UINT, элементы UINT</span><span class="sxs-lookup"><span data-stu-id="49455-149">UINT Width, UINT Elements</span></span>                                                      |
| <span data-ttu-id="49455-150">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="49455-150">Texture1DArray</span></span>      | <span data-ttu-id="49455-151">UINT Миплевел, ширина float, элементы с плавающей запятой, Нумберофлевелс с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span></span>               |
| <span data-ttu-id="49455-152">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="49455-152">Texture1DArray</span></span>      | <span data-ttu-id="49455-153">Ширина float, элементы с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-153">float Width, float Elements</span></span>                                                    |
| <span data-ttu-id="49455-154">Texture2D</span><span class="sxs-lookup"><span data-stu-id="49455-154">Texture2D</span></span>           | <span data-ttu-id="49455-155">UINT Миплевел, ширина UINT, высота UINT, UINT Нумберофлевелс</span><span class="sxs-lookup"><span data-stu-id="49455-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="49455-156">Texture2D</span><span class="sxs-lookup"><span data-stu-id="49455-156">Texture2D</span></span>           | <span data-ttu-id="49455-157">Ширина UINT, высота UINT</span><span class="sxs-lookup"><span data-stu-id="49455-157">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="49455-158">Texture2D</span><span class="sxs-lookup"><span data-stu-id="49455-158">Texture2D</span></span>           | <span data-ttu-id="49455-159">UINT Миплевел, ширина float, высота с плавающей запятой, Нумберофлевелс с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span></span>                 |
| <span data-ttu-id="49455-160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="49455-160">Texture2D</span></span>           | <span data-ttu-id="49455-161">Ширина плавающей запятой, высота с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-161">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="49455-162">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="49455-162">Texture2DArray</span></span>      | <span data-ttu-id="49455-163">UINT Миплевел, ширина UINT, высота UINT, элементы UINT, UINT Нумберофлевелс</span><span class="sxs-lookup"><span data-stu-id="49455-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="49455-164">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="49455-164">Texture2DArray</span></span>      | <span data-ttu-id="49455-165">Ширина UINT, высота UINT, элементы UINT</span><span class="sxs-lookup"><span data-stu-id="49455-165">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="49455-166">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="49455-166">Texture2DArray</span></span>      | <span data-ttu-id="49455-167">UINT Миплевел, ширина float, высота с плавающей запятой, элементы с плавающей запятой, Нумберофлевелс с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="49455-168">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="49455-168">Texture2DArray</span></span>      | <span data-ttu-id="49455-169">Ширина float, высота с плавающей запятой, элементы с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-169">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="49455-170">Texture3D</span><span class="sxs-lookup"><span data-stu-id="49455-170">Texture3D</span></span>           | <span data-ttu-id="49455-171">UINT Миплевел, ширина UINT, высота UINT, глубина UINT, UINT Нумберофлевелс</span><span class="sxs-lookup"><span data-stu-id="49455-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span></span>        |
| <span data-ttu-id="49455-172">Texture3D</span><span class="sxs-lookup"><span data-stu-id="49455-172">Texture3D</span></span>           | <span data-ttu-id="49455-173">Ширина UINT, высота UINT, глубина UINT</span><span class="sxs-lookup"><span data-stu-id="49455-173">UINT Width, UINT Height, UINT Depth</span></span>                                            |
| <span data-ttu-id="49455-174">Texture3D</span><span class="sxs-lookup"><span data-stu-id="49455-174">Texture3D</span></span>           | <span data-ttu-id="49455-175">UINT Миплевел, ширина float, высота с плавающей запятой, глубина float, Нумберофлевелс с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span></span>    |
| <span data-ttu-id="49455-176">Texture3D</span><span class="sxs-lookup"><span data-stu-id="49455-176">Texture3D</span></span>           | <span data-ttu-id="49455-177">Ширина плавающей линии, высота с плавающей запятой, глубина плавающего числа</span><span class="sxs-lookup"><span data-stu-id="49455-177">float Width, float Height, float Depth</span></span>                                         |
| <span data-ttu-id="49455-178">TextureCube</span><span class="sxs-lookup"><span data-stu-id="49455-178">TextureCube</span></span>         | <span data-ttu-id="49455-179">UINT Миплевел, ширина UINT, высота UINT, UINT Нумберофлевелс</span><span class="sxs-lookup"><span data-stu-id="49455-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="49455-180">TextureCube</span><span class="sxs-lookup"><span data-stu-id="49455-180">TextureCube</span></span>         | <span data-ttu-id="49455-181">Ширина UINT, высота UINT</span><span class="sxs-lookup"><span data-stu-id="49455-181">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="49455-182">TextureCube</span><span class="sxs-lookup"><span data-stu-id="49455-182">TextureCube</span></span>         | <span data-ttu-id="49455-183">UINT Миплевел, ширина float, высота с плавающей запятой, UINT Нумберофлевелс</span><span class="sxs-lookup"><span data-stu-id="49455-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="49455-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="49455-184">TextureCube</span></span>         | <span data-ttu-id="49455-185">Ширина плавающей запятой, высота с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-185">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="49455-186">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="49455-186">TextureCubeArray</span></span>    | <span data-ttu-id="49455-187">UINT Миплевел, ширина UINT, высота UINT, элементы UINT, UINT Нумберофлевелс</span><span class="sxs-lookup"><span data-stu-id="49455-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="49455-188">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="49455-188">TextureCubeArray</span></span>    | <span data-ttu-id="49455-189">Ширина UINT, высота UINT, элементы UINT</span><span class="sxs-lookup"><span data-stu-id="49455-189">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="49455-190">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="49455-190">TextureCubeArray</span></span>    | <span data-ttu-id="49455-191">UINT Миплевел, ширина float, высота с плавающей запятой, элементы с плавающей запятой, Нумберофлевелс с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="49455-192">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="49455-192">TextureCubeArray</span></span>    | <span data-ttu-id="49455-193">Ширина float, высота с плавающей запятой, элементы с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-193">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="49455-194">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="49455-194">Texture2DMS</span></span>         | <span data-ttu-id="49455-195">Ширина UINT, высота UINT, примеры UINT</span><span class="sxs-lookup"><span data-stu-id="49455-195">UINT Width, UINT Height, UINT Samples</span></span>                                          |
| <span data-ttu-id="49455-196">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="49455-196">Texture2DMS</span></span>         | <span data-ttu-id="49455-197">Ширина float, высота с плавающей запятой, выборка с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-197">float Width, float Height, float Samples</span></span>                                       |
| <span data-ttu-id="49455-198">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="49455-198">Texture2DMSArray</span></span>    | <span data-ttu-id="49455-199">Ширина UINT, высота UINT, элементы UINT, примеры UINT</span><span class="sxs-lookup"><span data-stu-id="49455-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span></span>                           |
| <span data-ttu-id="49455-200">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="49455-200">Texture2DMSArray</span></span>    | <span data-ttu-id="49455-201">Ширина float, высота с плавающей запятой, элементы с плавающей запятой, образцы с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49455-201">float Width, float Height, float Elements, float Samples</span></span>                       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="49455-202">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="49455-202">Minimum Shader Model</span></span>

<span data-ttu-id="49455-203">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="49455-203">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="49455-204">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="49455-204">vs\_4\_0</span></span> | <span data-ttu-id="49455-205">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="49455-205">vs\_4\_1</span></span>  | <span data-ttu-id="49455-206">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="49455-206">ps\_4\_0</span></span> | <span data-ttu-id="49455-207">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="49455-207">ps\_4\_1</span></span>  | <span data-ttu-id="49455-208">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="49455-208">gs\_4\_0</span></span> | <span data-ttu-id="49455-209">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="49455-209">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="49455-210">x</span><span class="sxs-lookup"><span data-stu-id="49455-210">x</span></span>        | <span data-ttu-id="49455-211">x</span><span class="sxs-lookup"><span data-stu-id="49455-211">x</span></span>         | <span data-ttu-id="49455-212">x</span><span class="sxs-lookup"><span data-stu-id="49455-212">x</span></span>        | <span data-ttu-id="49455-213">x</span><span class="sxs-lookup"><span data-stu-id="49455-213">x</span></span>         | <span data-ttu-id="49455-214">x</span><span class="sxs-lookup"><span data-stu-id="49455-214">x</span></span>        | <span data-ttu-id="49455-215">x</span><span class="sxs-lookup"><span data-stu-id="49455-215">x</span></span>         |



 

1.  <span data-ttu-id="49455-216">Возвращает измерения для самого крупного (начальном) уровня mipmap.</span><span class="sxs-lookup"><span data-stu-id="49455-216">Returns dimensions for the largest (zeroth) mipmap level.</span></span>
2.  <span data-ttu-id="49455-217">Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="49455-217">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
3.  <span data-ttu-id="49455-218">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="49455-218">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49455-219">См. также</span><span class="sxs-lookup"><span data-stu-id="49455-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49455-220">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="49455-220">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





