---
title: Базовые перечисления Direct3D 11
description: В этом разделе содержатся сведения о базовых перечислениях.
ms.assetid: 1641713a-5ac8-4597-900b-1bba54f9f522
keywords:
- перечисления, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b012ae34367ef849bebf3fb25780310fcb924ba9
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104414088"
---
# <a name="direct3d-11-core-enumerations"></a><span data-ttu-id="a99aa-104">Базовые перечисления Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a99aa-104">Direct3D 11 core enumerations</span></span>

<span data-ttu-id="a99aa-105">В этом разделе содержатся сведения о базовых перечислениях.</span><span class="sxs-lookup"><span data-stu-id="a99aa-105">This section contains information about the core enumerations.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a99aa-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="a99aa-106">In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a99aa-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="a99aa-107">Topic</span></span></th>
<th><span data-ttu-id="a99aa-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a99aa-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a99aa-109"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_async_getdata_flag"><strong>D3D11_ASYNC_GETDATA_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-109"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_async_getdata_flag"><strong>D3D11_ASYNC_GETDATA_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-110">Необязательные флаги, управляющие поведением <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-getdata"><strong>ссылку ID3D11DeviceContext:: GetData</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a99aa-110">Optional flags that control the behavior of <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-getdata"><strong>ID3D11DeviceContext::GetData</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-111"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend"><strong>D3D11_BLEND</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-111"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend"><strong>D3D11_BLEND</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-112">Коэффициенты смешения, которые модуляции значений для шейдера пикселей и целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="a99aa-112">Blend factors, which modulate values for the pixel shader and render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-113"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend_op"><strong>D3D11_BLEND_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-113"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend_op"><strong>D3D11_BLEND_OP</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-114">Операция смешения RGB или Alpha.</span><span class="sxs-lookup"><span data-stu-id="a99aa-114">RGB or alpha blending operation.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-115"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_clear_flag"><strong>D3D11_CLEAR_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-115"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_clear_flag"><strong>D3D11_CLEAR_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-116">Указывает части трафарета глубины, которые необходимо очистить.</span><span class="sxs-lookup"><span data-stu-id="a99aa-116">Specifies the parts of the depth stencil to clear.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-117"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_color_write_enable"><strong>D3D11_COLOR_WRITE_ENABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-117"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_color_write_enable"><strong>D3D11_COLOR_WRITE_ENABLE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-118">Определение того, какие компоненты каждого пикселя целевого объекта отрисовки доступны для записи во время смешения.</span><span class="sxs-lookup"><span data-stu-id="a99aa-118">Identify which components of each pixel of a render target are writable during blending.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-119"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_comparison_func"><strong>D3D11_COMPARISON_FUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-119"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_comparison_func"><strong>D3D11_COMPARISON_FUNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-120">Параметры сравнения.</span><span class="sxs-lookup"><span data-stu-id="a99aa-120">Comparison options.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-121"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode"><strong>D3D11_CONSERVATIVE_RASTERIZATION_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-121"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode"><strong>D3D11_CONSERVATIVE_RASTERIZATION_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-122">Определяет, включено ли консервативное растрирование.</span><span class="sxs-lookup"><span data-stu-id="a99aa-122">Identifies whether conservative rasterization is on or off.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-123"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier"><strong>D3D11_CONSERVATIVE_RASTERIZATION_TIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-123"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier"><strong>D3D11_CONSERVATIVE_RASTERIZATION_TIER</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-124">Указывает, поддерживает ли оборудование и драйверы консервативную растрирование и уровень уровня.</span><span class="sxs-lookup"><span data-stu-id="a99aa-124">Specifies if the hardware and driver support conservative rasterization and at what tier level.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-125"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_context_type"><strong>D3D11_CONTEXT_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-125"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_context_type"><strong>D3D11_CONTEXT_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-126">Задает контекст, в котором происходит запрос.</span><span class="sxs-lookup"><span data-stu-id="a99aa-126">Specifies the context in which a query occurs.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-127"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_copy_flags"><strong>D3D11_COPY_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-127"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_copy_flags"><strong>D3D11_COPY_FLAGS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a99aa-128">Это перечисление поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a99aa-128">This enumeration is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="a99aa-129">Указывает способ обработки существующего содержимого ресурса во время операции копирования или обновления региона в этом ресурсе.</span><span class="sxs-lookup"><span data-stu-id="a99aa-129">Specifies how to handle the existing contents of a resource during a copy or update operation of a region within that resource.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-130"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter"><strong>D3D11_COUNTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-130"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter"><strong>D3D11_COUNTER</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-131">Параметры счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="a99aa-131">Options for performance counters.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-132"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter_type"><strong>D3D11_COUNTER_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-132"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter_type"><strong>D3D11_COUNTER_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-133">Тип данных счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="a99aa-133">Data type of a performance counter.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-134"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_create_device_flag"><strong>D3D11_CREATE_DEVICE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-134"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_create_device_flag"><strong>D3D11_CREATE_DEVICE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-135">Описывает параметры, используемые для создания устройства.</span><span class="sxs-lookup"><span data-stu-id="a99aa-135">Describes parameters that are used to create a device.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-136"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag"><strong>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-136"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag"><strong>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-137">Описывает флаги, используемые для создания объекта состояния контекста устройства (<a href="/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a>) с помощью метода <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate"><strong>ID3D11Device1:: креатедевицеконтекстстате</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a99aa-137">Describes flags that are used to create a device context state object (<a href="/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a>) with the <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate"><strong>ID3D11Device1::CreateDeviceContextState</strong></a> method.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-138"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_cull_mode"><strong>D3D11_CULL_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-138"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_cull_mode"><strong>D3D11_CULL_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-139">Показывает, что треугольники, направленные в определенное направление, не рисуются.</span><span class="sxs-lookup"><span data-stu-id="a99aa-139">Indicates triangles facing a particular direction are not drawn.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-140"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_depth_write_mask"><strong>D3D11_DEPTH_WRITE_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-140"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_depth_write_mask"><strong>D3D11_DEPTH_WRITE_MASK</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-141">Определяет часть буфера шаблона глубины для записи данных глубины.</span><span class="sxs-lookup"><span data-stu-id="a99aa-141">Identify the portion of a depth-stencil buffer for writing depth data.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-142"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_device_context_type"><strong>D3D11_DEVICE_CONTEXT_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-142"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_device_context_type"><strong>D3D11_DEVICE_CONTEXT_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-143">Параметры контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="a99aa-143">Device context options.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-144"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-144"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-145">Параметры функции Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="a99aa-145">Direct3D 11 feature options.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-146"><a href="/windows/win32/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag"><strong>D3D11_FENCE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-146"><a href="/windows/win32/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag"><strong>D3D11_FENCE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-147">Задает параметры ограждения.</span><span class="sxs-lookup"><span data-stu-id="a99aa-147">Specifies fence options.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-148"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_fill_mode"><strong>D3D11_FILL_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-148"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_fill_mode"><strong>D3D11_FILL_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-149">Определяет режим заполнения, используемый при отрисовке треугольников.</span><span class="sxs-lookup"><span data-stu-id="a99aa-149">Determines the fill mode to use when rendering triangles.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-150"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter"><strong>D3D11_FILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-150"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter"><strong>D3D11_FILTER</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-151">Параметры фильтрации во время выборки текстуры.</span><span class="sxs-lookup"><span data-stu-id="a99aa-151">Filtering options during texture sampling.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-152"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter_type"><strong>D3D11_FILTER_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-152"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter_type"><strong>D3D11_FILTER_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-153">Типы фильтров "увеличение" или "минификации".</span><span class="sxs-lookup"><span data-stu-id="a99aa-153">Types of magnification or minification sampler filters.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-154"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_filter_reduction_type"><strong>D3D11_FILTER_REDUCTION_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-154"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_filter_reduction_type"><strong>D3D11_FILTER_REDUCTION_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-155">Указывает тип сокращения фильтра образцов.</span><span class="sxs-lookup"><span data-stu-id="a99aa-155">Specifies the type of sampler filter reduction.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-156"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-156"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-157">Какие ресурсы поддерживаются для заданного формата и устройства (см. раздел <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkformatsupport"><strong>ID3D11Device:: чеккформатсуппорт</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: чеккфеатуресуппорт</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="a99aa-157">Which resources are supported for a given format and given device (see <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkformatsupport"><strong>ID3D11Device::CheckFormatSupport</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a>).</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-158"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-158"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-159">Варианты поддержки неупорядоченных ресурсов для ресурса шейдера вычислений (см. <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: чеккфеатуресуппорт</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="a99aa-159">Unordered resource support options for a compute shader resource (see <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a>).</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-160"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_input_classification"><strong>D3D11_INPUT_CLASSIFICATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-160"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_input_classification"><strong>D3D11_INPUT_CLASSIFICATION</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-161">Тип данных, содержащихся во входном слоте.</span><span class="sxs-lookup"><span data-stu-id="a99aa-161">Type of data contained in an input slot.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-162"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_logic_op"><strong>D3D11_LOGIC_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-162"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_logic_op"><strong>D3D11_LOGIC_OP</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a99aa-163">Это перечисление поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a99aa-163">This enumeration is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="a99aa-164">Указывает логические операции, которые необходимо настроить для целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="a99aa-164">Specifies logical operations to configure for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-165"><a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive"><strong>D3D11_PRIMITIVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-165"><a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive"><strong>D3D11_PRIMITIVE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-166">Указывает, как конвейер интерпретирует геометрические или поверхностиные примитивы ввода шейдера.</span><span class="sxs-lookup"><span data-stu-id="a99aa-166">Indicates how the pipeline interprets geometry or hull shader input primitives.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-167"><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)"><strong>D3D11_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-167"><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)"><strong>D3D11_PRIMITIVE_TOPOLOGY</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-168">Способ, с помощью которого конвейер интерпретирует данные вершин, привязанные к этапу ассемблера ввода.</span><span class="sxs-lookup"><span data-stu-id="a99aa-168">How the pipeline interprets vertex data that is bound to the input-assembler stage.</span></span> <span data-ttu-id="a99aa-169">Эти значения примитивной топологии определяют, как данные вершин подготавливаются к просмотру на экране.</span><span class="sxs-lookup"><span data-stu-id="a99aa-169">These primitive topology values determine how the vertex data is rendered on screen.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-170"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query"><strong>D3D11_QUERY</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-170"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query"><strong>D3D11_QUERY</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-171">Типы запросов.</span><span class="sxs-lookup"><span data-stu-id="a99aa-171">Query types.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-172"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query_misc_flag"><strong>D3D11_QUERY_MISC_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-172"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query_misc_flag"><strong>D3D11_QUERY_MISC_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-173">Флаги, описывающие поведение других запросов.</span><span class="sxs-lookup"><span data-stu-id="a99aa-173">Flags that describe miscellaneous query behavior.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-174"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_raise_flag"><strong>D3D11_RAISE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-174"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_raise_flag"><strong>D3D11_RAISE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-175">Параметры для возведения ошибки в непродолжаемое исключение.</span><span class="sxs-lookup"><span data-stu-id="a99aa-175">Option(s) for raising an error to a non-continuable exception.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-176"><a href="https://www.bing.com/search?q=<strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong>"><strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-176"><a href="https://www.bing.com/search?q=<strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong>"><strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-177">Описывает уровень поддержки кэширования шейдеров в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="a99aa-177">Describes the level of support for shader caching in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-178"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_shader_min_precision_support"><strong>D3D11_SHADER_MIN_PRECISION_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-178"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_shader_min_precision_support"><strong>D3D11_SHADER_MIN_PRECISION_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="a99aa-179">Это перечисление поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a99aa-179">This enumeration is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="a99aa-180">Значения, задающих минимальные уровни точности на стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="a99aa-180">Values that specify minimum precision levels at shader stages.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-181"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier"><strong>D3D11_SHARED_RESOURCE_TIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-181"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier"><strong>D3D11_SHARED_RESOURCE_TIER</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-182">Определяет константы, указывающие уровень поддержки общих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a99aa-182">Defines constants that specify a tier for shared resource support.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-183"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_stencil_op"><strong>D3D11_STENCIL_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-183"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_stencil_op"><strong>D3D11_STENCIL_OP</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-184">Операции с наборами элементов, которые могут быть выполнены во время тестирования шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="a99aa-184">The stencil operations that can be performed during depth-stencil testing.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-185"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode"><strong>D3D11_TEXTURE_ADDRESS_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-185"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode"><strong>D3D11_TEXTURE_ADDRESS_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-186">Определение способа разрешения координат текстуры, которые выходят за пределы границ текстуры.</span><span class="sxs-lookup"><span data-stu-id="a99aa-186">Identify a technique for resolving texture coordinates that are outside of the boundaries of a texture.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-187"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texturecube_face"><strong>D3D11_TEXTURECUBE_FACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-187"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texturecube_face"><strong>D3D11_TEXTURECUBE_FACE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-188">Различные грани текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="a99aa-188">The different faces of a cube texture.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="a99aa-189"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier"><strong>D3D11_TILED_RESOURCES_TIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="a99aa-189"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier"><strong>D3D11_TILED_RESOURCES_TIER</strong></a></span></span><br/></td>
<td><span data-ttu-id="a99aa-190">Указывает уровень уровня, на котором поддерживаются мозаичные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a99aa-190">Indicates the tier level at which tiled resources are supported.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="a99aa-191">См. также</span><span class="sxs-lookup"><span data-stu-id="a99aa-191">Related topics</span></span>

[<span data-ttu-id="a99aa-192">Справочник по коду</span><span class="sxs-lookup"><span data-stu-id="a99aa-192">Core reference</span></span>](d3d11-graphics-reference-d3d11-core.md)