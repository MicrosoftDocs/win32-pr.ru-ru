---
description: В этом разделе описывается, как проверить поддержку формата для оборудования на уровне функций Direct3D с помощью вызовов API.
ms.assetid: 0C40C73E-06F3-41FA-AA27-2C0B730B357B
title: 'Проверка поддержки компонентов оборудования '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b14f0de50c4236c4fce46ceda1896ee32721c3bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990146"
---
# <a name="checking-hardware-feature-support"></a><span data-ttu-id="24dd4-103">Проверка поддержки компонентов оборудования </span><span class="sxs-lookup"><span data-stu-id="24dd4-103">Checking Hardware Feature Support</span></span>

<span data-ttu-id="24dd4-104">В этом разделе описывается, как проверить поддержку формата для оборудования на уровне функций Direct3D с помощью вызовов API.</span><span class="sxs-lookup"><span data-stu-id="24dd4-104">This section covers how to check on Format Support for Direct3D Feature Level Hardware using API calls.</span></span>

<span data-ttu-id="24dd4-105">Для D3D11 используйте [**ID3D11Device:: чеккформатсуппорт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) для программной проверки сведений в предыдущих разделах.</span><span class="sxs-lookup"><span data-stu-id="24dd4-105">For D3D11, use [**ID3D11Device::CheckFormatSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) to programmatically verify the info in the previous sections.</span></span> <span data-ttu-id="24dd4-106">Для D3D12 используйте [**ID3D12:: чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="24dd4-106">For D3D12 use [**ID3D12::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24dd4-107">Формат целевого объекта</span><span class="sxs-lookup"><span data-stu-id="24dd4-107">Format target</span></span></th>
<th><span data-ttu-id="24dd4-108">D3D12</span><span class="sxs-lookup"><span data-stu-id="24dd4-108">D3D12</span></span></th>
<th><span data-ttu-id="24dd4-109">D3D11</span><span class="sxs-lookup"><span data-stu-id="24dd4-109">D3D11</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24dd4-110">Буфер</span><span class="sxs-lookup"><span data-stu-id="24dd4-110">Buffer</span></span></td>
<td><span data-ttu-id="24dd4-111">D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-111">D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-112">D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-112">D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-113">Буфер вершин входного ассемблера</span><span class="sxs-lookup"><span data-stu-id="24dd4-113">Input Assembler Vertex Buffer</span></span></td>
<td><span data-ttu-id="24dd4-114">D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-114">D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-115">D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-115">D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-116">Буфер входного индекса ассемблера</span><span class="sxs-lookup"><span data-stu-id="24dd4-116">Input Assembler Index Buffer</span></span></td>
<td><span data-ttu-id="24dd4-117">D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-117">D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-118">D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-118">D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-119">Потоковый буфер вывода</span><span class="sxs-lookup"><span data-stu-id="24dd4-119">Stream Output Buffer</span></span></td>
<td><span data-ttu-id="24dd4-120">D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-120">D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-121">D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-121">D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-122">Texture1D</span><span class="sxs-lookup"><span data-stu-id="24dd4-122">Texture1D</span></span></td>
<td><span data-ttu-id="24dd4-123">D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-123">D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-124">D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-124">D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-125">Texture2D</span><span class="sxs-lookup"><span data-stu-id="24dd4-125">Texture2D</span></span></td>
<td><span data-ttu-id="24dd4-126">D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-126">D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-127">D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-127">D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-128">Texture3D</span><span class="sxs-lookup"><span data-stu-id="24dd4-128">Texture3D</span></span></td>
<td><span data-ttu-id="24dd4-129">D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-129">D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-130">D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-130">D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="24dd4-131">TextureCube</span></span></td>
<td><span data-ttu-id="24dd4-132">D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-132">D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-133">D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-133">D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-134">Шейдер LD</span><span class="sxs-lookup"><span data-stu-id="24dd4-134">Shader ld</span></span></td>
<td><span data-ttu-id="24dd4-135">D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-135">D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-136">D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-136">D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-137">Пример шейдера (любой фильтр)</span><span class="sxs-lookup"><span data-stu-id="24dd4-137">Shader sample (any filter)</span></span></td>
<td><span data-ttu-id="24dd4-138">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-138">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-139">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-139">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-140">Sample_c шейдера (фильтр сравнения)</span><span class="sxs-lookup"><span data-stu-id="24dd4-140">Shader sample_c (comparison filter)</span></span></td>
<td><span data-ttu-id="24dd4-141">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-141">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-142">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-142">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-143">Пример шейдера (Mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="24dd4-143">Shader sample (mono 1_bit_filter)</span></span></td>
<td><span data-ttu-id="24dd4-144">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-144">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-145">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-145">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-146">Gather4 шейдера</span><span class="sxs-lookup"><span data-stu-id="24dd4-146">Shader gather4</span></span></td>
<td><span data-ttu-id="24dd4-147">D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-147">D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-148">D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-148">D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-149">Gather4_c шейдера</span><span class="sxs-lookup"><span data-stu-id="24dd4-149">Shader gather4_c</span></span></td>
<td><span data-ttu-id="24dd4-150">D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-150">D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-151">D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-151">D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-152">Mipmap</span><span class="sxs-lookup"><span data-stu-id="24dd4-152">Mipmap</span></span></td>
<td><span data-ttu-id="24dd4-153">D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-153">D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-154">D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-154">D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-155">Автоматическое создание mipmap</span><span class="sxs-lookup"><span data-stu-id="24dd4-155">Mipmap Auto-Generation</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="24dd4-156">D3D12 больше не имеет выделенных функций создания mipmap.</span><span class="sxs-lookup"><span data-stu-id="24dd4-156">D3D12 no longer has a dedicated mipmap generation functionality.</span></span> <span data-ttu-id="24dd4-157">Приложения должны реализовывать его самостоятельно с помощью шейдеров.</span><span class="sxs-lookup"><span data-stu-id="24dd4-157">Applications must implement it on their own using shaders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="24dd4-158">D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-158">D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-159">рендертаржет</span><span class="sxs-lookup"><span data-stu-id="24dd4-159">RenderTarget</span></span></td>
<td><span data-ttu-id="24dd4-160">D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-160">D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-161">D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-161">D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-162">Рендертаржет для наложения</span><span class="sxs-lookup"><span data-stu-id="24dd4-162">Blendable RenderTarget</span></span></td>
<td><span data-ttu-id="24dd4-163">D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-163">D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-164">D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-164">D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-165">Выходная операция логики слияния</span><span class="sxs-lookup"><span data-stu-id="24dd4-165">Output Merger Logic Op</span></span></td>
<td><span data-ttu-id="24dd4-166">D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</span><span class="sxs-lookup"><span data-stu-id="24dd4-166">D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</span></span></td>
<td><span data-ttu-id="24dd4-167">D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-167">D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-168">Целевой объект глубины или трафарета</span><span class="sxs-lookup"><span data-stu-id="24dd4-168">Depth/Stencil Target</span></span></td>
<td><span data-ttu-id="24dd4-169">D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-169">D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-170">D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-170">D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-171">Необработанные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="24dd4-171">Raw UAV and SRV</span></span></td>


</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-172">Структурированные UAV и SRV</span><span class="sxs-lookup"><span data-stu-id="24dd4-172">Structured UAV and SRV</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-173">Типизированный UAV</span><span class="sxs-lookup"><span data-stu-id="24dd4-173">Typed UAV</span></span></td>
<td><span data-ttu-id="24dd4-174">D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-174">D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-175">D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-175">D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-176">UAV типизированное хранилище</span><span class="sxs-lookup"><span data-stu-id="24dd4-176">UAV Typed Store</span></span></td>
<td><span data-ttu-id="24dd4-177">D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-177">D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-178">D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-178">D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-179">Типизированная Загрузка UAV</span><span class="sxs-lookup"><span data-stu-id="24dd4-179">UAV Typed Load</span></span></td>
<td><span data-ttu-id="24dd4-180">D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-180">D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-181">D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-181">D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-182">UAV атомарное Добавление</span><span class="sxs-lookup"><span data-stu-id="24dd4-182">UAV Atomic Add</span></span></td>
<td><span data-ttu-id="24dd4-183">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-183">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-184">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-184">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-185">UAV атомарные побитовые операции</span><span class="sxs-lookup"><span data-stu-id="24dd4-185">UAV Atomic Bitwise Ops</span></span></td>
<td><span data-ttu-id="24dd4-186">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-186">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-187">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-187">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-188">UAV атомарный CMP&Store/CMP&</span><span class="sxs-lookup"><span data-stu-id="24dd4-188">UAV Atomic Cmp&Store/ Cmp&Exch</span></span></td>
<td><span data-ttu-id="24dd4-189">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-189">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-190">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-190">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-191">UAV атомарный обмен</span><span class="sxs-lookup"><span data-stu-id="24dd4-191">UAV Atomic Exchange</span></span></td>
<td><span data-ttu-id="24dd4-192">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-192">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-193">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-193">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-194">UAV Atomic со знаком min/max</span><span class="sxs-lookup"><span data-stu-id="24dd4-194">UAV Atomic Signed Min/Max</span></span></td>
<td><span data-ttu-id="24dd4-195">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-195">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-196">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-196">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-197">UAV Atomic неподписанные min/max</span><span class="sxs-lookup"><span data-stu-id="24dd4-197">UAV Atomic Unsigned Min/Max</span></span></td>
<td><span data-ttu-id="24dd4-198">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-198">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-199">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-199">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-200">Блокируемый ЦП</span><span class="sxs-lookup"><span data-stu-id="24dd4-200">CPU Lockable</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="24dd4-201">Только один формат исключает доступ к ЦП (420_OPAQUE).</span><span class="sxs-lookup"><span data-stu-id="24dd4-201">Only a single format precludes cpu access (420_OPAQUE).</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="24dd4-202">D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-202">D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-203">многопримерная Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="24dd4-203">4x Multisample RenderTarget</span></span></td>
<td><span data-ttu-id="24dd4-204">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-204">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-205">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-205">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-206">8X многопримерный Рендертаржет</span><span class="sxs-lookup"><span data-stu-id="24dd4-206">8x Multisample RenderTarget</span></span></td>
<td><span data-ttu-id="24dd4-207">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-207">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-208">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-208">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-209">Другое число с выборке</span><span class="sxs-lookup"><span data-stu-id="24dd4-209">Other Multisample Count RT</span></span></td>
<td><span data-ttu-id="24dd4-210">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-210">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-211">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-211">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-212">Многопримерное разрешение</span><span class="sxs-lookup"><span data-stu-id="24dd4-212">Multisample Resolve</span></span></td>
<td><span data-ttu-id="24dd4-213">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-213">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-214">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-214">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-215">Многовыборочная Загрузка</span><span class="sxs-lookup"><span data-stu-id="24dd4-215">Multisample Load</span></span></td>
<td><span data-ttu-id="24dd4-216">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-216">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-217">D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-217">D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-218">Отображение Scan-Out</span><span class="sxs-lookup"><span data-stu-id="24dd4-218">Display Scan-Out</span></span></td>
<td><span data-ttu-id="24dd4-219">D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-219">D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-220">D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-220">D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-221">Приведение в битовой структуре</span><span class="sxs-lookup"><span data-stu-id="24dd4-221">Cast Within Bit Layout</span></span></td>
<td><span data-ttu-id="24dd4-222">D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-222">D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-223">D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-223">D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-224">Поддержка видеодекодера</span><span class="sxs-lookup"><span data-stu-id="24dd4-224">Video Decoder Support</span></span></td>
<td><span data-ttu-id="24dd4-225">D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-225">D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-226">D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-226">D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-227">Вход обработчика видео</span><span class="sxs-lookup"><span data-stu-id="24dd4-227">Video Processor Input</span></span></td>
<td><span data-ttu-id="24dd4-228">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-228">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-229">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-229">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-230">Выходные данные обработчика видео</span><span class="sxs-lookup"><span data-stu-id="24dd4-230">Video Processor Output</span></span></td>
<td><span data-ttu-id="24dd4-231">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-231">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-232">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-232">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-233">Общий ресурс</span><span class="sxs-lookup"><span data-stu-id="24dd4-233">Shared Resource</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="24dd4-234">Текстуры всех форматов могут быть общими зафиксированными ресурсами или помещены в общие кучи.</span><span class="sxs-lookup"><span data-stu-id="24dd4-234">Textures of all formats may be shared committed resources or be placed in shared heaps.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="24dd4-235">D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-235">D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-236">Переводимая в качестве буфера ввода полная типизация</span><span class="sxs-lookup"><span data-stu-id="24dd4-236">BackBuffer Castable Even Fully Typed</span></span></td>
<td><span data-ttu-id="24dd4-237">D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-237">D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="24dd4-238">Нет доступных API.</span><span class="sxs-lookup"><span data-stu-id="24dd4-238">No API available.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-239">Мозаичный ресурс</span><span class="sxs-lookup"><span data-stu-id="24dd4-239">Tiled Resource</span></span></td>
<td><span data-ttu-id="24dd4-240">D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-240">D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-241">D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-241">D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24dd4-242">Кодировщик видео</span><span class="sxs-lookup"><span data-stu-id="24dd4-242">Video Encoder</span></span></td>
<td><span data-ttu-id="24dd4-243">D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-243">D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER(<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-244">D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-244">D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24dd4-245">Многоплановый оверлей</span><span class="sxs-lookup"><span data-stu-id="24dd4-245">Multiplane Overlay</span></span></td>
<td><span data-ttu-id="24dd4-246">D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-246">D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="24dd4-247">D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="24dd4-247">D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="24dd4-248">См. также</span><span class="sxs-lookup"><span data-stu-id="24dd4-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24dd4-249">Уровни компонентов оборудования D3D12</span><span class="sxs-lookup"><span data-stu-id="24dd4-249">D3D12 Hardware Feature Levels</span></span>](/windows/desktop/direct3d12/hardware-feature-levels)
</dt> <dt>

[<span data-ttu-id="24dd4-250">**\_Формат DXGI**</span><span class="sxs-lookup"><span data-stu-id="24dd4-250">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> <dt>

[<span data-ttu-id="24dd4-251">**\_Поддержка формата \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="24dd4-251">**D3D11\_FORMAT\_SUPPORT**</span></span>](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support)
</dt> <dt>

[<span data-ttu-id="24dd4-252">**\_Формат D3D11 \_ SUPPORT2**</span><span class="sxs-lookup"><span data-stu-id="24dd4-252">**D3D11\_FORMAT\_SUPPORT2**</span></span>](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2)
</dt> <dt>

[<span data-ttu-id="24dd4-253">Руководством по программированию для DXGI</span><span class="sxs-lookup"><span data-stu-id="24dd4-253">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

