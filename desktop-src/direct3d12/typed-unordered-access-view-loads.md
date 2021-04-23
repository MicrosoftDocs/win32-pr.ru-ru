---
title: Типизированное представление неупорядоченного доступа (UAV) загружается
description: Неупорядоченная типизированная Загрузка представления доступа (UAV) — это способность шейдера считывать из UAV с определенным \_ форматом DXGI.
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4adfd7511590a43b7f87507c5a1e0a2a87c925b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548962"
---
# <a name="typed-unordered-access-view-uav-loads"></a><span data-ttu-id="023f2-103">Типизированное представление неупорядоченного доступа (UAV) загружается</span><span class="sxs-lookup"><span data-stu-id="023f2-103">Typed unordered access view (UAV) loads</span></span>

<span data-ttu-id="023f2-104">Неупорядоченная типизированная Загрузка представления доступа (UAV) — это способность шейдера считывать из UAV с определенным [**\_ форматом DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="023f2-104">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

-   [<span data-ttu-id="023f2-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="023f2-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="023f2-106">Поддерживаемые форматы и вызовы API</span><span class="sxs-lookup"><span data-stu-id="023f2-106">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="023f2-107">Использование типизированных UAV загрузок из HLSL</span><span class="sxs-lookup"><span data-stu-id="023f2-107">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="023f2-108">Использование UNORM и СНОРМ типизированных UAV загружается из HLSL</span><span class="sxs-lookup"><span data-stu-id="023f2-108">Using UNORM and SNORM typed UAV loads from HLSL</span></span>](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="023f2-109">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="023f2-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="023f2-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="023f2-110">Overview</span></span>

<span data-ttu-id="023f2-111">Представление неупорядоченного доступа (UAV) — это представление неупорядоченного ресурса доступа (которое может включать буферы, текстуры и массивы текстур, но без множественной выборки).</span><span class="sxs-lookup"><span data-stu-id="023f2-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="023f2-112">UAV позволяет временно неупорядоченный доступ на чтение и запись из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="023f2-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="023f2-113">Это означает, что этот тип ресурса может быть считан и записан одновременно несколькими потоками без создания конфликтов памяти.</span><span class="sxs-lookup"><span data-stu-id="023f2-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="023f2-114">Такой одновременный доступ обрабатывается с помощью [атомарных функций](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="023f2-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="023f2-115">D3D12 (и D3D 11.3) расширяет список форматов, которые можно использовать с типизированными загрузкой UAV.</span><span class="sxs-lookup"><span data-stu-id="023f2-115">D3D12 (and D3D11.3) expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="023f2-116">Поддерживаемые форматы и вызовы API</span><span class="sxs-lookup"><span data-stu-id="023f2-116">Supported formats and API calls</span></span>

<span data-ttu-id="023f2-117">Ранее в следующих трех форматах поддерживалась типизированная UAV Загрузка и они требовались для оборудования D3D 11.0.</span><span class="sxs-lookup"><span data-stu-id="023f2-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="023f2-118">Они поддерживаются для всех устройств D3D 11.3 и D3D12.</span><span class="sxs-lookup"><span data-stu-id="023f2-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="023f2-119">R32 \_ float</span><span class="sxs-lookup"><span data-stu-id="023f2-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="023f2-120">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="023f2-120">R32\_UINT</span></span>
-   <span data-ttu-id="023f2-121">R32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="023f2-121">R32\_SINT</span></span>

<span data-ttu-id="023f2-122">Следующие форматы поддерживаются как наборы на оборудовании D3D12 или D3D 11.3, поэтому, если поддерживается любой из них, поддерживаются все.</span><span class="sxs-lookup"><span data-stu-id="023f2-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="023f2-123">R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="023f2-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="023f2-124">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="023f2-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="023f2-125">R32G32B32A32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="023f2-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="023f2-126">R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="023f2-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="023f2-127">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="023f2-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="023f2-128">R16G16B16A16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="023f2-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="023f2-129">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="023f2-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="023f2-130">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="023f2-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="023f2-131">R8G8B8A8 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="023f2-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="023f2-132">R16 \_ float</span><span class="sxs-lookup"><span data-stu-id="023f2-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="023f2-133">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="023f2-133">R16\_UINT</span></span>
-   <span data-ttu-id="023f2-134">R16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="023f2-134">R16\_SINT</span></span>
-   <span data-ttu-id="023f2-135">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="023f2-135">R8\_UNORM</span></span>
-   <span data-ttu-id="023f2-136">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="023f2-136">R8\_UINT</span></span>
-   <span data-ttu-id="023f2-137">R8 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="023f2-137">R8\_SINT</span></span>

<span data-ttu-id="023f2-138">Следующие форматы поддерживаются по желанию и по отдельности на оборудовании D3D12 и D3D 11.3, поэтому один запрос должен быть сделан в каждом формате для проверки поддержки.</span><span class="sxs-lookup"><span data-stu-id="023f2-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="023f2-139">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="023f2-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="023f2-140">R16G16B16A16 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="023f2-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="023f2-141">R32G32 \_ float</span><span class="sxs-lookup"><span data-stu-id="023f2-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="023f2-142">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="023f2-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="023f2-143">R32G32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="023f2-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="023f2-144">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="023f2-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="023f2-145">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="023f2-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="023f2-146">R11G11B10 \_ float</span><span class="sxs-lookup"><span data-stu-id="023f2-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="023f2-147">R8G8B8A8 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="023f2-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="023f2-148">R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="023f2-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="023f2-149">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="023f2-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="023f2-150">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="023f2-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="023f2-151">R16G16 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="023f2-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="023f2-152">R16G16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="023f2-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="023f2-153">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="023f2-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="023f2-154">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="023f2-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="023f2-155">R8G8 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="023f2-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="023f2-156">R8G8 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="023f2-156">R8G8\_SINT</span></span>
-   <span data-ttu-id="023f2-157">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="023f2-157">R16\_UNORM</span></span>
-   <span data-ttu-id="023f2-158">R16 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="023f2-158">R16\_SNORM</span></span>
-   <span data-ttu-id="023f2-159">R8 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="023f2-159">R8\_SNORM</span></span>
-   <span data-ttu-id="023f2-160">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="023f2-160">A8\_UNORM</span></span>
-   <span data-ttu-id="023f2-161">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="023f2-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="023f2-162">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="023f2-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="023f2-163">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="023f2-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="023f2-164">Чтобы определить поддержку для любых дополнительных форматов, вызовите [**чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) с параметром [**D3D12 \_ Data Features \_ \_ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) Structure в качестве первого параметра (см. статью о [запросах возможностей](capability-querying.md)).</span><span class="sxs-lookup"><span data-stu-id="023f2-164">To determine the support for any additional formats, call [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) with the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure as the first parameter (refer to [Capability Querying](capability-querying.md)).</span></span> <span data-ttu-id="023f2-165">Поле *типедуавлоададдитионалформатс* будет установлено, если поддерживается список "Поддерживаемые как наборы" выше.</span><span class="sxs-lookup"><span data-stu-id="023f2-165">The *TypedUAVLoadAdditionalFormats* field will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="023f2-166">Выполните второй вызов **чеккфеатуресуппорт**, используя структуру [**\_ \_ \_ \_ поддержки формата данных о функциях D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (проверка возвращаемой структуры по D3D12 \_ Format \_ SUPPORT2 \_ UAV \_ типизированный \_ элемент Load в [**D3D12 \_ Format \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum), чтобы определить поддержку в списке необязательных поддерживаемых форматов, например:</span><span class="sxs-lookup"><span data-stu-id="023f2-166">Make a second call to **CheckFeatureSupport**, using a [**D3D12\_FEATURE\_DATA\_FORMAT\_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) to determine support in the list of optionally supported formats listed above, for example:</span></span>

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="023f2-167">Использование типизированных UAV загрузок из HLSL</span><span class="sxs-lookup"><span data-stu-id="023f2-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="023f2-168">Для типизированного Уавс в качестве флага HLSL для \_ шейдера D3D \_ требуется \_ типизированная \_ UAV \_ загрузить \_ Дополнительные \_ форматы.</span><span class="sxs-lookup"><span data-stu-id="023f2-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="023f2-169">Ниже приведен пример кода шейдера для обработки типизированной UAV нагрузки:</span><span class="sxs-lookup"><span data-stu-id="023f2-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a><span data-ttu-id="023f2-170">Использование UNORM и СНОРМ типизированных UAV загружается из HLSL</span><span class="sxs-lookup"><span data-stu-id="023f2-170">Using UNORM and SNORM typed UAV loads from HLSL</span></span>

<span data-ttu-id="023f2-171">При использовании типизированных UAV загрузок для чтения из ресурса UNORM или СНОРМ необходимо правильно объявить тип элемента объекта HLSL в значение `unorm` или `snorm` .</span><span class="sxs-lookup"><span data-stu-id="023f2-171">When using typed UAV loads to read from a UNORM or SNORM resource, you must properly declare the element type of the HLSL object to be `unorm` or `snorm`.</span></span> <span data-ttu-id="023f2-172">Он задается как неопределенное поведение для несоответствия типа элемента, объявленного в HLSL, с базовым типом данных ресурса.</span><span class="sxs-lookup"><span data-stu-id="023f2-172">It is specified as undefined behavior to mismatch the element type declared in HLSL with the underlying resource data type.</span></span> <span data-ttu-id="023f2-173">Например, если используется типизированная UAV загружается в буферный ресурс с R8 \_ UNORM Data, необходимо объявить тип элемента следующим образом `unorm float` :</span><span class="sxs-lookup"><span data-stu-id="023f2-173">For example, if you are using typed UAV loads on a buffer resource with R8\_UNORM data, then you must declare the element type as `unorm float`:</span></span>

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a><span data-ttu-id="023f2-174">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="023f2-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="023f2-175">Отрисовка</span><span class="sxs-lookup"><span data-stu-id="023f2-175">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="023f2-176">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="023f2-176">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="023f2-177">Привязка ресурсов в HLSL</span><span class="sxs-lookup"><span data-stu-id="023f2-177">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="023f2-178">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="023f2-178">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="023f2-179">Указание корневых подписей в HLSL</span><span class="sxs-lookup"><span data-stu-id="023f2-179">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 