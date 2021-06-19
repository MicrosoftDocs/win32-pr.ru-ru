---
title: Типизированное представление неупорядоченного доступа (UAV) загружается
description: Сведения о неупорядоченной нагрузке на представление Access (UAV) в Direct3D 12. Типизированная нагрузка UAV — это способность шейдера считывать из UAV с определенным DXGI_FORMAT.
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128354132a58e0b8648fba2b4e1e6babb95535
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394769"
---
# <a name="typed-unordered-access-view-uav-loads"></a><span data-ttu-id="cecef-104">Типизированное представление неупорядоченного доступа (UAV) загружается</span><span class="sxs-lookup"><span data-stu-id="cecef-104">Typed unordered access view (UAV) loads</span></span>

<span data-ttu-id="cecef-105">Неупорядоченная типизированная Загрузка представления доступа (UAV) — это способность шейдера считывать из UAV с определенным [**\_ форматом DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="cecef-105">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

-   [<span data-ttu-id="cecef-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="cecef-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="cecef-107">Поддерживаемые форматы и вызовы API</span><span class="sxs-lookup"><span data-stu-id="cecef-107">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="cecef-108">Использование типизированных UAV загрузок из HLSL</span><span class="sxs-lookup"><span data-stu-id="cecef-108">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="cecef-109">Использование UNORM и СНОРМ типизированных UAV загружается из HLSL</span><span class="sxs-lookup"><span data-stu-id="cecef-109">Using UNORM and SNORM typed UAV loads from HLSL</span></span>](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="cecef-110">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cecef-110">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="cecef-111">Обзор</span><span class="sxs-lookup"><span data-stu-id="cecef-111">Overview</span></span>

<span data-ttu-id="cecef-112">Представление неупорядоченного доступа (UAV) — это представление неупорядоченного ресурса доступа (которое может включать буферы, текстуры и массивы текстур, но без множественной выборки).</span><span class="sxs-lookup"><span data-stu-id="cecef-112">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="cecef-113">UAV позволяет временно неупорядоченный доступ на чтение и запись из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="cecef-113">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="cecef-114">Это означает, что этот тип ресурса может быть считан и записан одновременно несколькими потоками без создания конфликтов памяти.</span><span class="sxs-lookup"><span data-stu-id="cecef-114">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="cecef-115">Такой одновременный доступ обрабатывается с помощью [атомарных функций](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="cecef-115">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="cecef-116">D3D12 (и D3D 11.3) расширяет список форматов, которые можно использовать с типизированными загрузкой UAV.</span><span class="sxs-lookup"><span data-stu-id="cecef-116">D3D12 (and D3D11.3) expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="cecef-117">Поддерживаемые форматы и вызовы API</span><span class="sxs-lookup"><span data-stu-id="cecef-117">Supported formats and API calls</span></span>

<span data-ttu-id="cecef-118">Ранее в следующих трех форматах поддерживалась типизированная UAV Загрузка и они требовались для оборудования D3D 11.0.</span><span class="sxs-lookup"><span data-stu-id="cecef-118">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="cecef-119">Они поддерживаются для всех устройств D3D 11.3 и D3D12.</span><span class="sxs-lookup"><span data-stu-id="cecef-119">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="cecef-120">R32 \_ float</span><span class="sxs-lookup"><span data-stu-id="cecef-120">R32\_FLOAT</span></span>
-   <span data-ttu-id="cecef-121">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="cecef-121">R32\_UINT</span></span>
-   <span data-ttu-id="cecef-122">R32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="cecef-122">R32\_SINT</span></span>

<span data-ttu-id="cecef-123">Следующие форматы поддерживаются как наборы на оборудовании D3D12 или D3D 11.3, поэтому, если поддерживается любой из них, поддерживаются все.</span><span class="sxs-lookup"><span data-stu-id="cecef-123">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="cecef-124">R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="cecef-124">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="cecef-125">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="cecef-125">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="cecef-126">R32G32B32A32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="cecef-126">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="cecef-127">R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="cecef-127">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="cecef-128">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="cecef-128">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="cecef-129">R16G16B16A16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="cecef-129">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="cecef-130">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="cecef-130">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="cecef-131">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="cecef-131">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="cecef-132">R8G8B8A8 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="cecef-132">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="cecef-133">R16 \_ float</span><span class="sxs-lookup"><span data-stu-id="cecef-133">R16\_FLOAT</span></span>
-   <span data-ttu-id="cecef-134">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="cecef-134">R16\_UINT</span></span>
-   <span data-ttu-id="cecef-135">R16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="cecef-135">R16\_SINT</span></span>
-   <span data-ttu-id="cecef-136">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="cecef-136">R8\_UNORM</span></span>
-   <span data-ttu-id="cecef-137">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="cecef-137">R8\_UINT</span></span>
-   <span data-ttu-id="cecef-138">R8 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="cecef-138">R8\_SINT</span></span>

<span data-ttu-id="cecef-139">Следующие форматы поддерживаются по желанию и по отдельности на оборудовании D3D12 и D3D 11.3, поэтому один запрос должен быть сделан в каждом формате для проверки поддержки.</span><span class="sxs-lookup"><span data-stu-id="cecef-139">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="cecef-140">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="cecef-140">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="cecef-141">R16G16B16A16 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="cecef-141">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="cecef-142">R32G32 \_ float</span><span class="sxs-lookup"><span data-stu-id="cecef-142">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="cecef-143">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="cecef-143">R32G32\_UINT</span></span>
-   <span data-ttu-id="cecef-144">R32G32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="cecef-144">R32G32\_SINT</span></span>
-   <span data-ttu-id="cecef-145">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="cecef-145">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="cecef-146">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="cecef-146">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="cecef-147">R11G11B10 \_ float</span><span class="sxs-lookup"><span data-stu-id="cecef-147">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="cecef-148">R8G8B8A8 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="cecef-148">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="cecef-149">R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="cecef-149">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="cecef-150">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="cecef-150">R16G16\_UNORM</span></span>
-   <span data-ttu-id="cecef-151">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="cecef-151">R16G16\_UINT</span></span>
-   <span data-ttu-id="cecef-152">R16G16 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="cecef-152">R16G16\_SNORM</span></span>
-   <span data-ttu-id="cecef-153">R16G16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="cecef-153">R16G16\_SINT</span></span>
-   <span data-ttu-id="cecef-154">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="cecef-154">R8G8\_UNORM</span></span>
-   <span data-ttu-id="cecef-155">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="cecef-155">R8G8\_UINT</span></span>
-   <span data-ttu-id="cecef-156">R8G8 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="cecef-156">R8G8\_SNORM</span></span>
-   <span data-ttu-id="cecef-157">R8G8 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="cecef-157">R8G8\_SINT</span></span>
-   <span data-ttu-id="cecef-158">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="cecef-158">R16\_UNORM</span></span>
-   <span data-ttu-id="cecef-159">R16 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="cecef-159">R16\_SNORM</span></span>
-   <span data-ttu-id="cecef-160">R8 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="cecef-160">R8\_SNORM</span></span>
-   <span data-ttu-id="cecef-161">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="cecef-161">A8\_UNORM</span></span>
-   <span data-ttu-id="cecef-162">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="cecef-162">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="cecef-163">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="cecef-163">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="cecef-164">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="cecef-164">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="cecef-165">Чтобы определить поддержку для любых дополнительных форматов, вызовите [**чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) с параметром [**D3D12 \_ Data Features \_ \_ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) Structure в качестве первого параметра (см. статью о [запросах возможностей](capability-querying.md)).</span><span class="sxs-lookup"><span data-stu-id="cecef-165">To determine the support for any additional formats, call [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) with the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure as the first parameter (refer to [Capability Querying](capability-querying.md)).</span></span> <span data-ttu-id="cecef-166">Поле *типедуавлоададдитионалформатс* будет установлено, если поддерживается список "Поддерживаемые как наборы" выше.</span><span class="sxs-lookup"><span data-stu-id="cecef-166">The *TypedUAVLoadAdditionalFormats* field will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="cecef-167">Выполните второй вызов **чеккфеатуресуппорт**, используя структуру [**\_ \_ \_ \_ поддержки формата данных о функциях D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (проверка возвращаемой структуры по D3D12 \_ Format \_ SUPPORT2 \_ UAV \_ типизированный \_ элемент Load в [**D3D12 \_ Format \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum), чтобы определить поддержку в списке необязательных поддерживаемых форматов, например:</span><span class="sxs-lookup"><span data-stu-id="cecef-167">Make a second call to **CheckFeatureSupport**, using a [**D3D12\_FEATURE\_DATA\_FORMAT\_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) to determine support in the list of optionally supported formats listed above, for example:</span></span>

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

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="cecef-168">Использование типизированных UAV загрузок из HLSL</span><span class="sxs-lookup"><span data-stu-id="cecef-168">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="cecef-169">Для типизированного Уавс в качестве флага HLSL для \_ шейдера D3D \_ требуется \_ типизированная \_ UAV \_ загрузить \_ Дополнительные \_ форматы.</span><span class="sxs-lookup"><span data-stu-id="cecef-169">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="cecef-170">Ниже приведен пример кода шейдера для обработки типизированной UAV нагрузки:</span><span class="sxs-lookup"><span data-stu-id="cecef-170">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a><span data-ttu-id="cecef-171">Использование UNORM и СНОРМ типизированных UAV загружается из HLSL</span><span class="sxs-lookup"><span data-stu-id="cecef-171">Using UNORM and SNORM typed UAV loads from HLSL</span></span>

<span data-ttu-id="cecef-172">При использовании типизированных UAV загрузок для чтения из ресурса UNORM или СНОРМ необходимо правильно объявить тип элемента объекта HLSL в значение `unorm` или `snorm` .</span><span class="sxs-lookup"><span data-stu-id="cecef-172">When using typed UAV loads to read from a UNORM or SNORM resource, you must properly declare the element type of the HLSL object to be `unorm` or `snorm`.</span></span> <span data-ttu-id="cecef-173">Он задается как неопределенное поведение для несоответствия типа элемента, объявленного в HLSL, с базовым типом данных ресурса.</span><span class="sxs-lookup"><span data-stu-id="cecef-173">It is specified as undefined behavior to mismatch the element type declared in HLSL with the underlying resource data type.</span></span> <span data-ttu-id="cecef-174">Например, если используется типизированная UAV загружается в буферный ресурс с R8 \_ UNORM Data, необходимо объявить тип элемента следующим образом `unorm float` :</span><span class="sxs-lookup"><span data-stu-id="cecef-174">For example, if you are using typed UAV loads on a buffer resource with R8\_UNORM data, then you must declare the element type as `unorm float`:</span></span>

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a><span data-ttu-id="cecef-175">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cecef-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cecef-176">Отрисовка</span><span class="sxs-lookup"><span data-stu-id="cecef-176">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="cecef-177">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="cecef-177">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="cecef-178">Привязка ресурсов в HLSL</span><span class="sxs-lookup"><span data-stu-id="cecef-178">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="cecef-179">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="cecef-179">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="cecef-180">Определение корневых подписей в HLSL</span><span class="sxs-lookup"><span data-stu-id="cecef-180">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 