---
title: Загружаются неупорядоченные представления доступа
description: Неупорядоченная типизированная Загрузка представления доступа (UAV) — это способность шейдера считывать из UAV с определенным \_ форматом DXGI.
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0958b3563ab8001fd7b34ae62c9bcc37ad75c07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337900"
---
# <a name="typed-unordered-access-view-loads"></a><span data-ttu-id="e7539-103">Загружаются неупорядоченные представления доступа</span><span class="sxs-lookup"><span data-stu-id="e7539-103">Typed Unordered Access View Loads</span></span>

<span data-ttu-id="e7539-104">Неупорядоченная типизированная Загрузка представления доступа (UAV) — это способность шейдера считывать из UAV с определенным \_ форматом DXGI.</span><span class="sxs-lookup"><span data-stu-id="e7539-104">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span>

-   [<span data-ttu-id="e7539-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="e7539-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="e7539-106">Поддерживаемые форматы и вызовы API</span><span class="sxs-lookup"><span data-stu-id="e7539-106">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="e7539-107">Использование типизированных UAV загрузок из HLSL</span><span class="sxs-lookup"><span data-stu-id="e7539-107">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="e7539-108">См. также</span><span class="sxs-lookup"><span data-stu-id="e7539-108">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="e7539-109">Обзор</span><span class="sxs-lookup"><span data-stu-id="e7539-109">Overview</span></span>

<span data-ttu-id="e7539-110">Представление неупорядоченного доступа (UAV) — это представление неупорядоченного ресурса доступа (которое может включать буферы, текстуры и массивы текстур, но без множественной выборки).</span><span class="sxs-lookup"><span data-stu-id="e7539-110">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="e7539-111">UAV позволяет временно неупорядоченный доступ на чтение и запись из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="e7539-111">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="e7539-112">Это означает, что этот тип ресурса может быть считан и записан одновременно несколькими потоками без создания конфликтов памяти.</span><span class="sxs-lookup"><span data-stu-id="e7539-112">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="e7539-113">Такой одновременный доступ обрабатывается с помощью [атомарных функций](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="e7539-113">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="e7539-114">D3D12 и D3D 11.3 раскрывает список форматов, которые можно использовать с типизированными загрузкой UAV.</span><span class="sxs-lookup"><span data-stu-id="e7539-114">D3D12 and D3D11.3 expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="e7539-115">Поддерживаемые форматы и вызовы API</span><span class="sxs-lookup"><span data-stu-id="e7539-115">Supported formats and API calls</span></span>

<span data-ttu-id="e7539-116">Ранее в следующих трех форматах поддерживалась типизированная UAV Загрузка и они требовались для оборудования D3D 11.0.</span><span class="sxs-lookup"><span data-stu-id="e7539-116">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="e7539-117">Они поддерживаются для всех устройств D3D 11.3 и D3D12.</span><span class="sxs-lookup"><span data-stu-id="e7539-117">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="e7539-118">R32 \_ float</span><span class="sxs-lookup"><span data-stu-id="e7539-118">R32\_FLOAT</span></span>
-   <span data-ttu-id="e7539-119">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e7539-119">R32\_UINT</span></span>
-   <span data-ttu-id="e7539-120">R32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="e7539-120">R32\_SINT</span></span>

<span data-ttu-id="e7539-121">Следующие форматы поддерживаются как наборы на оборудовании D3D12 или D3D 11.3, поэтому, если поддерживается любой из них, поддерживаются все.</span><span class="sxs-lookup"><span data-stu-id="e7539-121">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="e7539-122">R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="e7539-122">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="e7539-123">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e7539-123">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="e7539-124">R32G32B32A32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="e7539-124">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="e7539-125">R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="e7539-125">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="e7539-126">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e7539-126">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="e7539-127">R16G16B16A16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="e7539-127">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="e7539-128">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e7539-128">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="e7539-129">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e7539-129">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="e7539-130">R8G8B8A8 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="e7539-130">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="e7539-131">R16 \_ float</span><span class="sxs-lookup"><span data-stu-id="e7539-131">R16\_FLOAT</span></span>
-   <span data-ttu-id="e7539-132">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e7539-132">R16\_UINT</span></span>
-   <span data-ttu-id="e7539-133">R16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="e7539-133">R16\_SINT</span></span>
-   <span data-ttu-id="e7539-134">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e7539-134">R8\_UNORM</span></span>
-   <span data-ttu-id="e7539-135">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e7539-135">R8\_UINT</span></span>
-   <span data-ttu-id="e7539-136">R8 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="e7539-136">R8\_SINT</span></span>

<span data-ttu-id="e7539-137">Следующие форматы поддерживаются по желанию и по отдельности на оборудовании D3D12 и D3D 11.3, поэтому один запрос должен быть сделан в каждом формате для проверки поддержки.</span><span class="sxs-lookup"><span data-stu-id="e7539-137">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="e7539-138">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e7539-138">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="e7539-139">R16G16B16A16 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="e7539-139">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="e7539-140">R32G32 \_ float</span><span class="sxs-lookup"><span data-stu-id="e7539-140">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="e7539-141">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e7539-141">R32G32\_UINT</span></span>
-   <span data-ttu-id="e7539-142">R32G32 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="e7539-142">R32G32\_SINT</span></span>
-   <span data-ttu-id="e7539-143">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e7539-143">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="e7539-144">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e7539-144">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="e7539-145">R11G11B10 \_ float</span><span class="sxs-lookup"><span data-stu-id="e7539-145">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="e7539-146">R8G8B8A8 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="e7539-146">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="e7539-147">R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="e7539-147">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="e7539-148">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e7539-148">R16G16\_UNORM</span></span>
-   <span data-ttu-id="e7539-149">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e7539-149">R16G16\_UINT</span></span>
-   <span data-ttu-id="e7539-150">R16G16 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="e7539-150">R16G16\_SNORM</span></span>
-   <span data-ttu-id="e7539-151">R16G16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="e7539-151">R16G16\_SINT</span></span>
-   <span data-ttu-id="e7539-152">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e7539-152">R8G8\_UNORM</span></span>
-   <span data-ttu-id="e7539-153">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e7539-153">R8G8\_UINT</span></span>
-   <span data-ttu-id="e7539-154">R8G8 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="e7539-154">R8G8\_SNORM</span></span>
-   <span data-ttu-id="e7539-155">8G8 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="e7539-155">8G8\_SINT</span></span>
-   <span data-ttu-id="e7539-156">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e7539-156">R16\_UNORM</span></span>
-   <span data-ttu-id="e7539-157">R16 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="e7539-157">R16\_SNORM</span></span>
-   <span data-ttu-id="e7539-158">R8 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="e7539-158">R8\_SNORM</span></span>
-   <span data-ttu-id="e7539-159">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e7539-159">A8\_UNORM</span></span>
-   <span data-ttu-id="e7539-160">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e7539-160">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="e7539-161">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e7539-161">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="e7539-162">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e7539-162">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="e7539-163">Чтобы определить поддержку для любых дополнительных форматов, вызовите [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) с [**функцией D3D11 \_ \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) Structure в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="e7539-163">To determine the support for any additional formats, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure as the first parameter.</span></span> <span data-ttu-id="e7539-164">`TypedUAVLoadAdditionalFormats`Бит будет установлен, если поддерживается список "Поддерживаемые как наборы" выше.</span><span class="sxs-lookup"><span data-stu-id="e7539-164">The `TypedUAVLoadAdditionalFormats` bit will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="e7539-165">Выполните второй вызов **чеккфеатуресуппорт**, используя структуру [**\_ \_ SUPPORT2 D3D11 Data \_ \_ Format**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) (проверка возвращаемой структуры по формату D3D12 \_ \_ SUPPORT2 UAV, \_ \_ типизированному \_ члену D3D11 [**\_ Format \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) SUPPORT2 enum), чтобы определить поддержку в списке поддерживаемых форматов выше, например:</span><span class="sxs-lookup"><span data-stu-id="e7539-165">Make a second call to **CheckFeatureSupport**, using a [**D3D11\_FEATURE\_DATA\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) enum) to determine support in the list of optionally supported formats above, for example:</span></span>

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="e7539-166">Использование типизированных UAV загрузок из HLSL</span><span class="sxs-lookup"><span data-stu-id="e7539-166">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="e7539-167">Для типизированного Уавс в качестве флага HLSL для \_ шейдера D3D \_ требуется \_ типизированная \_ UAV \_ загрузить \_ Дополнительные \_ форматы.</span><span class="sxs-lookup"><span data-stu-id="e7539-167">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="e7539-168">Ниже приведен пример кода шейдера для обработки типизированной UAV нагрузки:</span><span class="sxs-lookup"><span data-stu-id="e7539-168">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a><span data-ttu-id="e7539-169">См. также</span><span class="sxs-lookup"><span data-stu-id="e7539-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7539-170">Функции Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="e7539-170">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="e7539-171">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="e7539-171">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 