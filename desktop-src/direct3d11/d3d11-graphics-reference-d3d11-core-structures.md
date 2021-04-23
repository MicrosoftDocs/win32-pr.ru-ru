---
title: Базовые структуры Direct3D 11
description: В этом разделе содержатся сведения о базовых структурах.
ms.assetid: 2a45182a-7114-4075-b8b8-147f52fe7aa9
keywords:
- структуры, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7025de822265d86e5da9f1da3855d2542c76abf5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413298"
---
# <a name="direct3d-11-core-structures"></a><span data-ttu-id="c70b3-104">Базовые структуры Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="c70b3-104">Direct3D 11 core structures</span></span>

<span data-ttu-id="c70b3-105">В этом разделе содержатся сведения о базовых структурах.</span><span class="sxs-lookup"><span data-stu-id="c70b3-105">This section contains information about the core structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c70b3-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="c70b3-106">In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c70b3-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="c70b3-107">Topic</span></span></th>
<th><span data-ttu-id="c70b3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c70b3-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c70b3-109"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-109"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-110">Описывает состояние смешения, которое используется при вызове метода <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device:: креатеблендстате</strong></a> для создания объекта состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="c70b3-110">Describes the blend state that you use in a call to <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device::CreateBlendState</strong></a> to create a blend-state object.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-111"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-111"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c70b3-112">Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c70b3-112">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="c70b3-113">Описывает состояние смешения, которое используется при вызове метода <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1:: CreateBlendState1</strong></a> для создания объекта состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="c70b3-113">Describes the blend state that you use in a call to <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1::CreateBlendState1</strong></a> to create a blend-state object.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-114"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-114"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-115">Определяет трехмерное поле.</span><span class="sxs-lookup"><span data-stu-id="c70b3-115">Defines a 3D box.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-116"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-116"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-117">Описывает счетчик.</span><span class="sxs-lookup"><span data-stu-id="c70b3-117">Describes a counter.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-118"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-118"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-119">Сведения о возможностях счетчика производительности видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="c70b3-119">Information about the video card's performance counter capabilities.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-120"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-120"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-121">Описывает состояние трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="c70b3-121">Describes depth-stencil state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-122"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-122"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-123">Операции с наборами элементов, которые могут быть выполнены на основе результатов теста трафарета.</span><span class="sxs-lookup"><span data-stu-id="c70b3-123">Stencil operations that can be performed based on the results of stencil test.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-124"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-124"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-125">Аргументы для нарисованного непрямого индексированного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c70b3-125">Arguments for draw indexed instanced indirect.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-126"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-126"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-127">Аргументы для рисования с непрямыми экземплярами.</span><span class="sxs-lookup"><span data-stu-id="c70b3-127">Arguments for draw instanced indirect.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-128"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-128"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c70b3-129">Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c70b3-129">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="c70b3-130">Описывает сведения об архитектуре адаптера Direct3D 11,1.</span><span class="sxs-lookup"><span data-stu-id="c70b3-130">Describes information about Direct3D 11.1 adapter architecture.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-131"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-131"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c70b3-132">Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c70b3-132">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="c70b3-133">Описание параметров функции Direct3D 9 в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-133">Describes Direct3D 9 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-134"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-134"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-135">Описание параметров функции Direct3D 9 в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-135">Describes Direct3D 9 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-136"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-136"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c70b3-137">Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c70b3-137">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="c70b3-138">Описывает поддержку теневой версии Direct3D 9 в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-138">Describes Direct3D 9 shadow support in the current graphics driver.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-139"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-139"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-140">Описывает, поддерживается ли простой способ создания экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c70b3-140">Describes whether simple instancing is supported.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-141"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-141"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-142">Описывает поддержку шейдера вычислений и необработанных и структурированных буферов в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-142">Describes compute shader and raw and structured buffer support in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-143"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-143"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c70b3-144">Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c70b3-144">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="c70b3-145">Описание параметров функции Direct3D 11,1 в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-145">Describes Direct3D 11.1 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-146"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-146"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-147">Описание параметров функции Direct3D 11,2 в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-147">Describes Direct3D 11.2 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-148"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-148"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-149">Описание параметров функции Direct3D 11,3 в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-149">Describes Direct3D 11.3 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-150"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-150"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-151">Описание параметров функции Direct3D 11,3 в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-151">Describes Direct3D 11.3 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-152"><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-152"><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-153">Описание параметров функции Direct3D 11,4 в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-153">Describes Direct3D 11.4 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-154"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-154"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-155">Описывает уровень поддержки общих ресурсов в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-155">Describes the level of support for shared resources in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-156"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-156"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-157">Описывает поддержку типов данных Double в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-157">Describes double data type support in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-158"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-158"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-159">Описывает, какие ресурсы поддерживаются текущим драйвером графики для заданного формата.</span><span class="sxs-lookup"><span data-stu-id="c70b3-159">Describes which resources are supported by the current graphics driver for a given format.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-160"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-160"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-161">Описание неупорядоченных параметров ресурсов, поддерживаемых текущим графическим драйвером для заданного формата.</span><span class="sxs-lookup"><span data-stu-id="c70b3-161">Describes which unordered resource options are supported by the current graphics driver for a given format.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-162"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-162"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-163">Описание функций, поддерживаемых виртуальным адресом GPU, включая максимальное число битов на ресурс и на процесс.</span><span class="sxs-lookup"><span data-stu-id="c70b3-163">Describes feature data GPU virtual address support, including maximum address bits per resource and per process.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-164"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-164"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-165">Описывает, поддерживается ли метод профилирования GPU.</span><span class="sxs-lookup"><span data-stu-id="c70b3-165">Describes whether a GPU profiling technique is supported.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-166"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-166"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-167">Описывает уровень кэширования шейдера, поддерживаемый в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-167">Describes the level of shader caching supported in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-168"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-168"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c70b3-169">Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c70b3-169">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="c70b3-170">Описывает варианты поддержки точности для шейдеров в текущем графическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="c70b3-170">Describes precision support options for shaders in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-171"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-171"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-172">Описывает функции многопоточности, поддерживаемые текущим драйвером графики.</span><span class="sxs-lookup"><span data-stu-id="c70b3-172">Describes the multi-threading features that are supported by the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-173"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-173"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-174">Описание одного элемента для этапа входного ассемблера.</span><span class="sxs-lookup"><span data-stu-id="c70b3-174">A description of a single element for the input-assembler stage.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-175"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-175"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-176">Запрос сведений о графических-конвейерных действиях между вызовами <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ссылку ID3D11DeviceContext:: Begin</strong></a> и <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ссылку ID3D11DeviceContext:: end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c70b3-176">Query information about graphics-pipeline activity in between calls to <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-177"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-177"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-178">Запрос сведений о количестве потоковых данных, помещенных в поток потока вывода между <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ссылку ID3D11DeviceContext:: Begin</strong></a> и <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ссылку ID3D11DeviceContext:: end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c70b3-178">Query information about the amount of data streamed out to the stream-output buffers in between <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-179"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-179"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-180">Запрос сведений о надежности запроса метки времени.</span><span class="sxs-lookup"><span data-stu-id="c70b3-180">Query information about the reliability of a timestamp query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-181"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-181"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-182">Описывает запрос.</span><span class="sxs-lookup"><span data-stu-id="c70b3-182">Describes a query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-183"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-183"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-184">Описывает запрос.</span><span class="sxs-lookup"><span data-stu-id="c70b3-184">Describes a query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-185"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-185"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-186">Описывает состояние средства отображения программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="c70b3-186">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-187"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-187"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c70b3-188">Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c70b3-188">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="c70b3-189">Описывает состояние средства отображения программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="c70b3-189">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-190"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-190"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-191">Описывает состояние средства отображения программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="c70b3-191">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-192"><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-192"><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-193">D3D11_RECT объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c70b3-193">D3D11_RECT is declared as follows:</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-194"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-194"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-195">Описывает состояние смешения для целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="c70b3-195">Describes the blend state for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-196"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-196"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c70b3-197">Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="c70b3-197">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="c70b3-198">Описывает состояние смешения для целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="c70b3-198">Describes the blend state for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-199"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-199"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-200">Описывает состояние образца.</span><span class="sxs-lookup"><span data-stu-id="c70b3-200">Describes a sampler state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-201"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-201"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-202">Описание элемента вершины в буфере вершин в выходном слоте.</span><span class="sxs-lookup"><span data-stu-id="c70b3-202">Description of a vertex element in a vertex buffer in an output slot.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="c70b3-203"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c70b3-203"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="c70b3-204">Определяет размеры окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="c70b3-204">Defines the dimensions of a viewport.</span></span><br/></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c70b3-205">Кроме того, в D3D11. h определена структура 2D Rectangle.</span><span class="sxs-lookup"><span data-stu-id="c70b3-205">In addition, there's a 2D rectangle structure defined in D3D11.h.</span></span>

```cpp
typedef RECT D3D11_RECT;
```

<span data-ttu-id="c70b3-206">Документацию см. в разделе [Rect](/previous-versions/dd162897%28v%3dvs.85%29) в [Windows GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="c70b3-206">For documentation, see [RECT](/previous-versions/dd162897%28v%3dvs.85%29) in [Windows GDI](../gdi/windows-gdi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c70b3-207">См. также</span><span class="sxs-lookup"><span data-stu-id="c70b3-207">Related topics</span></span>

[<span data-ttu-id="c70b3-208">Справочник по основным</span><span class="sxs-lookup"><span data-stu-id="c70b3-208">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)