---
title: 10Level9 ID3D11Device методы
description: В этом разделе перечислены различия между каждым уровнем функций 10Level9 и уровнем D3D \_ уровня \_ \_ 11 \_ 0 и более высоким уровнем функций для методов ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413403"
---
# <a name="10level9-id3d11device-methods"></a><span data-ttu-id="dfee2-103">10Level9 ID3D11Device методы</span><span class="sxs-lookup"><span data-stu-id="dfee2-103">10Level9 ID3D11Device Methods</span></span>

<span data-ttu-id="dfee2-104">В этом разделе перечислены различия между каждым уровнем функций 10Level9 и уровнем D3D \_ уровня \_ \_ 11 \_ 0 и более высоким уровнем функций для методов [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="dfee2-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) methods.</span></span>

-   [<span data-ttu-id="dfee2-105">ID3D11Device:: Чекккаунтер</span><span class="sxs-lookup"><span data-stu-id="dfee2-105">ID3D11Device::CheckCounter</span></span>](#id3d11devicecheckcounter)
-   [<span data-ttu-id="dfee2-106">ID3D11Device:: Чеккформатсуппорт</span><span class="sxs-lookup"><span data-stu-id="dfee2-106">ID3D11Device::CheckFormatSupport</span></span>](#id3d11devicecheckformatsupport)
-   [<span data-ttu-id="dfee2-107">ID3D11Device:: Чеккмултисамплекуалитилевелс</span><span class="sxs-lookup"><span data-stu-id="dfee2-107">ID3D11Device::CheckMultisampleQualityLevels</span></span>](#id3d11devicecheckmultisamplequalitylevels)
-   [<span data-ttu-id="dfee2-108">ID3D11Device:: Креатеблендстате</span><span class="sxs-lookup"><span data-stu-id="dfee2-108">ID3D11Device::CreateBlendState</span></span>](#id3d11devicecreateblendstate)
-   [<span data-ttu-id="dfee2-109">ID3D11Device::CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="dfee2-109">ID3D11Device::CreateBlendState1</span></span>](#id3d11devicecreateblendstate1)
-   [<span data-ttu-id="dfee2-110">ID3D11Device:: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="dfee2-110">ID3D11Device::CreateBuffer</span></span>](#id3d11devicecreatebuffer)
-   [<span data-ttu-id="dfee2-111">ID3D11Device:: Креатекаунтер</span><span class="sxs-lookup"><span data-stu-id="dfee2-111">ID3D11Device::CreateCounter</span></span>](#id3d11devicecreatecounter)
-   [<span data-ttu-id="dfee2-112">ID3D11Device:: КреатедепсстенЦилвиев</span><span class="sxs-lookup"><span data-stu-id="dfee2-112">ID3D11Device::CreateDepthStencilView</span></span>](#id3d11devicecreatedepthstencilview)
-   [<span data-ttu-id="dfee2-113">ID3D11Device:: Креатедомаиншадер</span><span class="sxs-lookup"><span data-stu-id="dfee2-113">ID3D11Device::CreateDomainShader</span></span>](#id3d11devicecreatedomainshader)
-   [<span data-ttu-id="dfee2-114">ID3D11Device:: Креатежеометришадер</span><span class="sxs-lookup"><span data-stu-id="dfee2-114">ID3D11Device::CreateGeometryShader</span></span>](#id3d11devicecreategeometryshader)
-   [<span data-ttu-id="dfee2-115">ID3D11Device:: Креатежеометришадервисстреамаутпут</span><span class="sxs-lookup"><span data-stu-id="dfee2-115">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="dfee2-116">ID3D11Device:: Креатехуллшадер</span><span class="sxs-lookup"><span data-stu-id="dfee2-116">ID3D11Device::CreateHullShader</span></span>](#id3d11devicecreatehullshader)
-   [<span data-ttu-id="dfee2-117">ID3D11Device:: Креатеинпутлайаут</span><span class="sxs-lookup"><span data-stu-id="dfee2-117">ID3D11Device::CreateInputLayout</span></span>](#id3d11devicecreateinputlayout)
-   [<span data-ttu-id="dfee2-118">ID3D11Device:: Креатепикселшадер</span><span class="sxs-lookup"><span data-stu-id="dfee2-118">ID3D11Device::CreatePixelShader</span></span>](#id3d11devicecreatepixelshader)
-   [<span data-ttu-id="dfee2-119">ID3D11Device:: Креатепредикате</span><span class="sxs-lookup"><span data-stu-id="dfee2-119">ID3D11Device::CreatePredicate</span></span>](#id3d11devicecreatepredicate)
-   [<span data-ttu-id="dfee2-120">ID3D11Device:: CreateQuery</span><span class="sxs-lookup"><span data-stu-id="dfee2-120">ID3D11Device::CreateQuery</span></span>](#id3d11devicecreatequery)
-   [<span data-ttu-id="dfee2-121">ID3D11Device:: Креатерастеризерстате</span><span class="sxs-lookup"><span data-stu-id="dfee2-121">ID3D11Device::CreateRasterizerState</span></span>](#id3d11devicecreaterasterizerstate)
-   [<span data-ttu-id="dfee2-122">ID3D11Device:: Креатерендертаржетвиев</span><span class="sxs-lookup"><span data-stu-id="dfee2-122">ID3D11Device::CreateRenderTargetView</span></span>](#id3d11devicecreaterendertargetview)
-   [<span data-ttu-id="dfee2-123">ID3D11Device:: Креатесамплерстате</span><span class="sxs-lookup"><span data-stu-id="dfee2-123">ID3D11Device::CreateSamplerState</span></span>](#id3d11devicecreatesamplerstate)
-   [<span data-ttu-id="dfee2-124">ID3D11Device:: Креатешадерресаурцевиев</span><span class="sxs-lookup"><span data-stu-id="dfee2-124">ID3D11Device::CreateShaderResourceView</span></span>](#id3d11devicecreateshaderresourceview)
-   [<span data-ttu-id="dfee2-125">ID3D11Device::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="dfee2-125">ID3D11Device::CreateTexture1D</span></span>](#id3d11devicecreatetexture1d)
-   [<span data-ttu-id="dfee2-126">ID3D11Device::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="dfee2-126">ID3D11Device::CreateTexture2D</span></span>](#id3d11devicecreatetexture2d)
-   [<span data-ttu-id="dfee2-127">ID3D11Device::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="dfee2-127">ID3D11Device::CreateTexture3D</span></span>](#id3d11devicecreatetexture3d)
-   [<span data-ttu-id="dfee2-128">ID3D11Device:: Креатеунордередакцессвиев</span><span class="sxs-lookup"><span data-stu-id="dfee2-128">ID3D11Device::CreateUnorderedAccessView</span></span>](#id3d11devicecreateunorderedaccessview)
-   [<span data-ttu-id="dfee2-129">ID3D11Device:: Креатевертексшадер</span><span class="sxs-lookup"><span data-stu-id="dfee2-129">ID3D11Device::CreateVertexShader</span></span>](#id3d11devicecreatevertexshader)
-   [<span data-ttu-id="dfee2-130">ID3D11Device:: Опеншаредресаурце</span><span class="sxs-lookup"><span data-stu-id="dfee2-130">ID3D11Device::OpenSharedResource</span></span>](#id3d11deviceopensharedresource)
-   [<span data-ttu-id="dfee2-131">См. также</span><span class="sxs-lookup"><span data-stu-id="dfee2-131">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecheckcounter"></a><span data-ttu-id="dfee2-132">ID3D11Device:: Чекккаунтер</span><span class="sxs-lookup"><span data-stu-id="dfee2-132">ID3D11Device::CheckCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-133">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-133">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-134">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-134">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-135">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-135">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-136">Необязательно поддерживаются счетчики, зависящие от устройства.</span><span class="sxs-lookup"><span data-stu-id="dfee2-136">Device-dependent counters are optionally supported.</span></span> <span data-ttu-id="dfee2-137">Для определения поддержки используйте <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device:: чекккаунтеринфо</strong></a> . $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-137">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device::CheckCounterInfo</strong></a> to determine support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-138">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-138">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-139">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-139">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckformatsupport"></a><span data-ttu-id="dfee2-140">ID3D11Device:: Чеккформатсуппорт</span><span class="sxs-lookup"><span data-stu-id="dfee2-140">ID3D11Device::CheckFormatSupport</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-141">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-141">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-142">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-142">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-143">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-143">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-144">См. раздел Поддержка формата по <a href="overviews-direct3d-11-devices-downlevel-intro.md">уровням функций</a>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-144">See format support by <a href="overviews-direct3d-11-devices-downlevel-intro.md">feature level</a>${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-145">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-145">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-146">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-146">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a><span data-ttu-id="dfee2-147">ID3D11Device:: Чеккмултисамплекуалитилевелс</span><span class="sxs-lookup"><span data-stu-id="dfee2-147">ID3D11Device::CheckMultisampleQualityLevels</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-148">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-148">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-149">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-149">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-150">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-150">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-151">Уровни функций не гарантируют поддержку MSAA. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-151">Feature levels make no guarantees concerning MSAA support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-152">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-152">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-153">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-153">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateblendstate"></a><span data-ttu-id="dfee2-154">ID3D11Device:: Креатеблендстате</span><span class="sxs-lookup"><span data-stu-id="dfee2-154">ID3D11Device::CreateBlendState</span></span>



| <span data-ttu-id="dfee2-155">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-155">Feature Level</span></span>              | <span data-ttu-id="dfee2-156">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-156">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfee2-157">D3D \_ \_ уровень возможностей \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-157">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="dfee2-158">Алфатоковеражеенабле должно иметь **значение false**.</span><span class="sxs-lookup"><span data-stu-id="dfee2-158">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="dfee2-159">Первые четыре Бленденаблес должны иметь одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="dfee2-159">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="dfee2-160">D3D11 \_ Blend \_ src \_ алфасат не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dfee2-160">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="dfee2-161">Смешанный цвет смешения цветов не поддерживается (любой Сркбленд или Дестбленд с SRC1 в имени)</span><span class="sxs-lookup"><span data-stu-id="dfee2-161">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="dfee2-162">D3D \_ \_ уровень возможностей \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="dfee2-162">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="dfee2-163">Алфатоковеражеенабле должно иметь **значение false**.</span><span class="sxs-lookup"><span data-stu-id="dfee2-163">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="dfee2-164">Первые четыре Бленденаблес должны иметь одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="dfee2-164">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="dfee2-165">Первые четыре Рендертаржетвритемаскс должны иметь одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="dfee2-165">The first four RenderTargetWriteMasks must all have the same value.</span></span><br/> <span data-ttu-id="dfee2-166">D3D11 \_ Blend \_ src \_ алфасат не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dfee2-166">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="dfee2-167">Смешанный цвет смешения цветов не поддерживается (любой Сркбленд или Дестбленд с SRC1 в имени)</span><span class="sxs-lookup"><span data-stu-id="dfee2-167">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/> |
| <span data-ttu-id="dfee2-168">D3D \_ \_ уровень возможностей \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dfee2-168">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="dfee2-169">Алфатоковеражеенабле должно иметь **значение false**.</span><span class="sxs-lookup"><span data-stu-id="dfee2-169">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="dfee2-170">Первые четыре Бленденаблес должны иметь одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="dfee2-170">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="dfee2-171">D3D11 \_ Blend \_ src \_ алфасат не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dfee2-171">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="dfee2-172">Смешанный цвет смешения цветов не поддерживается (любой Сркбленд или Дестбленд с SRC1 в имени)</span><span class="sxs-lookup"><span data-stu-id="dfee2-172">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="dfee2-173">\_Уровень компонентов \_ D3D \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dfee2-173">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="dfee2-174">Добавляет альфа-в покрытие</span><span class="sxs-lookup"><span data-stu-id="dfee2-174">Adds alpha-to-coverage</span></span>                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a><span data-ttu-id="dfee2-175">ID3D11Device::CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="dfee2-175">ID3D11Device::CreateBlendState1</span></span>



| <span data-ttu-id="dfee2-176">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-176">Feature Level</span></span>              | <span data-ttu-id="dfee2-177">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-177">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfee2-178">D3D \_ \_ уровень возможностей \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-178">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="dfee2-179">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dfee2-179">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="dfee2-180">D3D \_ \_ уровень возможностей \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="dfee2-180">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="dfee2-181">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dfee2-181">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="dfee2-182">D3D \_ \_ уровень возможностей \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dfee2-182">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="dfee2-183">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dfee2-183">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="dfee2-184">\_Уровень компонентов \_ D3D \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dfee2-184">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="dfee2-185">Член *аутпутмержерлогикоп* добавлен в [**\_ \_ \_ \_ Параметры D3D11 данных D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), чтобы определить поддержку логических операций (побитовых логических операций между выходным шейдером пиксельных построителей и содержимым целевого объекта прорисовки), см. в разделе [**D3D11 \_ \_ целевой объект рендеринга \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span><span class="sxs-lookup"><span data-stu-id="dfee2-185">The *OutputMergerLogicOp* member has been added to [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), to determine support for logical operations (bitwise logic operations between pixel shader output and render target contents, refer to [**D3D11\_RENDER\_TARGET\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span></span> |



 

## <a name="id3d11devicecreatebuffer"></a><span data-ttu-id="dfee2-186">ID3D11Device:: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="dfee2-186">ID3D11Device::CreateBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-187">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-187">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-188">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-188">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-189">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-189">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="dfee2-190">Буферы не могут иметь представления целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="dfee2-190">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="dfee2-191">Буферы должны иметь ровно один из D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER или D3D11_BIND_CONSTANT_BUFFER.</span><span class="sxs-lookup"><span data-stu-id="dfee2-191">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="dfee2-192">Разрешает только буферы индексов с форматом DXGI_FORMAT_R16_UINT.</span><span class="sxs-lookup"><span data-stu-id="dfee2-192">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-193">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-193">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="dfee2-194">Буферы не могут иметь представления целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="dfee2-194">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="dfee2-195">Буферы должны иметь ровно один из D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER или D3D11_BIND_CONSTANT_BUFFER.</span><span class="sxs-lookup"><span data-stu-id="dfee2-195">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="dfee2-196">Разрешает буферы индексов с форматами DXGI_FORMAT_R16_UINT и DXGI_FORMAT_R32_UINT, такими как D3D_FEATURE_LEVEL_10_0 и выше.</span><span class="sxs-lookup"><span data-stu-id="dfee2-196">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="dfee2-197">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-197">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-198">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-198">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a><span data-ttu-id="dfee2-199">ID3D11Device:: Креатекаунтер</span><span class="sxs-lookup"><span data-stu-id="dfee2-199">ID3D11Device::CreateCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-200">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-200">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-201">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-201">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-202">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-202">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-203">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-203">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-204">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-204">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-205">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-205">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedepthstencilview"></a><span data-ttu-id="dfee2-206">ID3D11Device:: КреатедепсстенЦилвиев</span><span class="sxs-lookup"><span data-stu-id="dfee2-206">ID3D11Device::CreateDepthStencilView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-207">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-207">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-208">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-208">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-209">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-209">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-210">Не поддерживает двусторонние наборы элементов. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-210">Does not support two-sided stencil.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-211">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-211">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-212">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-212">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedomainshader"></a><span data-ttu-id="dfee2-213">ID3D11Device:: Креатедомаиншадер</span><span class="sxs-lookup"><span data-stu-id="dfee2-213">ID3D11Device::CreateDomainShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-214">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-214">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-215">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-215">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-216">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-216">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="dfee2-217">Не поддерживается на уровне функций 9. \* или 10. \*.</span><span class="sxs-lookup"><span data-stu-id="dfee2-217">Not supported on any 9.\* or 10.\* feature level.</span></span> <span data-ttu-id="dfee2-218">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-218">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-219">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-219">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-220">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-220">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-221">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="dfee2-221">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-222">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-222">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshader"></a><span data-ttu-id="dfee2-223">ID3D11Device:: Креатежеометришадер</span><span class="sxs-lookup"><span data-stu-id="dfee2-223">ID3D11Device::CreateGeometryShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-224">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-224">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-225">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-225">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-226">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-226">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-227">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-227">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-228">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-228">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-229">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-229">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a><span data-ttu-id="dfee2-230">ID3D11Device:: Креатежеометришадервисстреамаутпут</span><span class="sxs-lookup"><span data-stu-id="dfee2-230">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-231">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-231">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-232">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-232">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-233">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-233">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-234">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-234">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-235">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-235">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-236">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-236">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatehullshader"></a><span data-ttu-id="dfee2-237">ID3D11Device:: Креатехуллшадер</span><span class="sxs-lookup"><span data-stu-id="dfee2-237">ID3D11Device::CreateHullShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-238">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-238">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-239">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-239">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-240">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-240">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="dfee2-241">Не поддерживается на уровне функций 9. \* или 10. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-241">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-242">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-242">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-243">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-243">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-244">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="dfee2-244">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-245">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-245">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateinputlayout"></a><span data-ttu-id="dfee2-246">ID3D11Device:: Креатеинпутлайаут</span><span class="sxs-lookup"><span data-stu-id="dfee2-246">ID3D11Device::CreateInputLayout</span></span>



| <span data-ttu-id="dfee2-247">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-247">Feature Level</span></span>             | <span data-ttu-id="dfee2-248">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-248">Behavior Differences</span></span>                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfee2-249">D3D \_ \_ уровень возможностей \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-249">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="dfee2-250">Не поддерживает \_ входные \_ данные D3D11 для каждого \_ экземпляра \_</span><span class="sxs-lookup"><span data-stu-id="dfee2-250">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="dfee2-251">D3D \_ \_ уровень возможностей \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="dfee2-251">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="dfee2-252">Не поддерживает \_ входные \_ данные D3D11 для каждого \_ экземпляра \_</span><span class="sxs-lookup"><span data-stu-id="dfee2-252">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="dfee2-253">D3D \_ \_ уровень возможностей \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dfee2-253">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="dfee2-254">Нулевой поток вершин должен иметь \_ D3D11 \_ Вход \_ на \_ данные вершины, если в потоках есть \_ входные данные D3D11 \_ для \_ \_ данных вершин</span><span class="sxs-lookup"><span data-stu-id="dfee2-254">Vertex stream zero must have D3D11\_INPUT\_PER\_VERTEX\_DATA, if any streams have D3D11\_INPUT\_PER\_VERTEX\_DATA</span></span> |



 

<span data-ttu-id="dfee2-255">Дополнительные сведения о том, какие форматы можно использовать для данных вершин на каждом уровне компонентов, см. в разделе Диаграмма поддержка по [уровням функций](overviews-direct3d-11-devices-downlevel-intro.md) .</span><span class="sxs-lookup"><span data-stu-id="dfee2-255">See the format support by [feature level chart](overviews-direct3d-11-devices-downlevel-intro.md) for details on what formats can be used for vertex data at each feature level.</span></span>

## <a name="id3d11devicecreatepixelshader"></a><span data-ttu-id="dfee2-256">ID3D11Device:: Креатепикселшадер</span><span class="sxs-lookup"><span data-stu-id="dfee2-256">ID3D11Device::CreatePixelShader</span></span>



| <span data-ttu-id="dfee2-257">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-257">Feature Level</span></span>             | <span data-ttu-id="dfee2-258">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-258">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="dfee2-259">D3D \_ \_ уровень возможностей \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-259">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="dfee2-260">Необходимо использовать PS \_ 4 \_ 0 \_ уровня \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-260">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="dfee2-261">D3D \_ \_ уровень возможностей \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="dfee2-261">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="dfee2-262">Необходимо использовать PS \_ 4 \_ 0 \_ уровня \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-262">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="dfee2-263">D3D \_ \_ уровень возможностей \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dfee2-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="dfee2-264">Необходимо использовать PS \_ 4 \_ 0 \_ уровня \_ 9 \_ 3 или PS \_ 4 \_ 0 \_ уровня \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-264">Must use ps\_4\_0\_level\_9\_3 or ps\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11devicecreatepredicate"></a><span data-ttu-id="dfee2-265">ID3D11Device:: Креатепредикате</span><span class="sxs-lookup"><span data-stu-id="dfee2-265">ID3D11Device::CreatePredicate</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-266">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-266">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-267">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-267">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-268">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-268">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-269">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-269">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-270">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-270">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-271">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-271">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatequery"></a><span data-ttu-id="dfee2-272">ID3D11Device:: CreateQuery</span><span class="sxs-lookup"><span data-stu-id="dfee2-272">ID3D11Device::CreateQuery</span></span>



| <span data-ttu-id="dfee2-273">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-273">Feature Level</span></span>             | <span data-ttu-id="dfee2-274">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-274">Behavior Differences</span></span>                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfee2-275">D3D \_ \_ уровень возможностей \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-275">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="dfee2-276">Поддерживаются запросы событий.</span><span class="sxs-lookup"><span data-stu-id="dfee2-276">Event queries are supported.</span></span> <span data-ttu-id="dfee2-277">Запросы меток времени необязательны: вызовите [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) , чтобы определить поддержку.</span><span class="sxs-lookup"><span data-stu-id="dfee2-277">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span>               |
| <span data-ttu-id="dfee2-278">D3D \_ \_ уровень возможностей \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="dfee2-278">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="dfee2-279">Поддерживаются запросы Event и перекрытия.</span><span class="sxs-lookup"><span data-stu-id="dfee2-279">Event and occlusion queries are supported.</span></span> <span data-ttu-id="dfee2-280">Запросы меток времени необязательны: вызовите [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) , чтобы определить поддержку.</span><span class="sxs-lookup"><span data-stu-id="dfee2-280">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |
| <span data-ttu-id="dfee2-281">D3D \_ \_ уровень возможностей \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dfee2-281">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="dfee2-282">Поддерживаются запросы Event и перекрытия.</span><span class="sxs-lookup"><span data-stu-id="dfee2-282">Event and occlusion queries are supported.</span></span> <span data-ttu-id="dfee2-283">Запросы меток времени необязательны: вызовите [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) , чтобы определить поддержку.</span><span class="sxs-lookup"><span data-stu-id="dfee2-283">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |



 

## <a name="id3d11devicecreaterasterizerstate"></a><span data-ttu-id="dfee2-284">ID3D11Device:: Креатерастеризерстате</span><span class="sxs-lookup"><span data-stu-id="dfee2-284">ID3D11Device::CreateRasterizerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-285">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-285">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-286">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-286">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-287">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-287">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-288">Депсклипенабле должно иметь <strong>значение true</strong>.</span><span class="sxs-lookup"><span data-stu-id="dfee2-288">DepthClipEnable must be <strong>TRUE</strong>.</span></span> <span data-ttu-id="dfee2-289">Депсбиаскламп должно иметь значение 0. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-289">DepthBiasClamp must be set to 0.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-290">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-290">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-291">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-291">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreaterendertargetview"></a><span data-ttu-id="dfee2-292">ID3D11Device:: Креатерендертаржетвиев</span><span class="sxs-lookup"><span data-stu-id="dfee2-292">ID3D11Device::CreateRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-293">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-293">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-294">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-294">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-295">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-295">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-296">Поддерживает только целевые представления прорисовки объектов Texture2D. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-296">Can only support render target views of Texture2D objects.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-297">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-297">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-298">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-298">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatesamplerstate"></a><span data-ttu-id="dfee2-299">ID3D11Device:: Креатесамплерстате</span><span class="sxs-lookup"><span data-stu-id="dfee2-299">ID3D11Device::CreateSamplerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-300">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-300">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-301">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-301">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-302">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-302">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="dfee2-303">Фильтр сравнения не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dfee2-303">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="dfee2-304">Цвет границы должен быть в пределах [0, 1]</span><span class="sxs-lookup"><span data-stu-id="dfee2-304">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="dfee2-305">Min Лод не может быть дробной частью</span><span class="sxs-lookup"><span data-stu-id="dfee2-305">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="dfee2-306">Максимальная Лод должна быть FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="dfee2-306">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="dfee2-307">Максимальная анизотропная — 2.</span><span class="sxs-lookup"><span data-stu-id="dfee2-307">Maximum anisotropy is 2.</span></span><br/> <span data-ttu-id="dfee2-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dfee2-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-309">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-309">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="dfee2-310">Фильтр сравнения не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dfee2-310">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="dfee2-311">Цвет границы должен быть в пределах [0, 1]</span><span class="sxs-lookup"><span data-stu-id="dfee2-311">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="dfee2-312">Min Лод не может быть дробной частью</span><span class="sxs-lookup"><span data-stu-id="dfee2-312">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="dfee2-313">Максимальная Лод должна быть FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="dfee2-313">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="dfee2-314">Максимальная анизотропная — 16.</span><span class="sxs-lookup"><span data-stu-id="dfee2-314">Maximum anisotropy is 16.</span></span><br/> <span data-ttu-id="dfee2-315">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-315">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-316">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-316">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a><span data-ttu-id="dfee2-317">ID3D11Device:: Креатешадерресаурцевиев</span><span class="sxs-lookup"><span data-stu-id="dfee2-317">ID3D11Device::CreateShaderResourceView</span></span>



| <span data-ttu-id="dfee2-318">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-318">Feature Level</span></span>             | <span data-ttu-id="dfee2-319">Мостдетаиледмип Plus Миплевелс должен включать наименьший Лод (наименьший подресурс</span><span class="sxs-lookup"><span data-stu-id="dfee2-319">MostDetailedMip plus MipLevels must include lowest LOD (smallest subresource</span></span> | <span data-ttu-id="dfee2-320">Представление должно включать все элементы массива ресурсов</span><span class="sxs-lookup"><span data-stu-id="dfee2-320">View must include all resource array elements</span></span> |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="dfee2-321">D3D \_ \_ уровень возможностей \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-321">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="dfee2-322">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-322">Yes</span></span>                                                                          | <span data-ttu-id="dfee2-323">да</span><span class="sxs-lookup"><span data-stu-id="dfee2-323">yes</span></span>                                           |
| <span data-ttu-id="dfee2-324">D3D \_ \_ уровень возможностей \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="dfee2-324">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="dfee2-325">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-325">Yes</span></span>                                                                          | <span data-ttu-id="dfee2-326">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-326">Yes</span></span>                                           |
| <span data-ttu-id="dfee2-327">D3D \_ \_ уровень возможностей \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dfee2-327">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="dfee2-328">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-328">Yes</span></span>                                                                          | <span data-ttu-id="dfee2-329">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-329">Yes</span></span>                                           |



 

## <a name="id3d11devicecreatetexture1d"></a><span data-ttu-id="dfee2-330">ID3D11Device::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="dfee2-330">ID3D11Device::CreateTexture1D</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-331">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-331">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-332">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-332">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-333">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-333">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-334">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-334">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-335">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-335">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-336">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-336">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatetexture2d"></a><span data-ttu-id="dfee2-337">ID3D11Device::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="dfee2-337">ID3D11Device::CreateTexture2D</span></span>

<span data-ttu-id="dfee2-338">Ресурсы Texture2D имеют ограничения по ширине и высоте, которые отличаются на [уровне функций](overviews-direct3d-11-devices-downlevel-intro.md).</span><span class="sxs-lookup"><span data-stu-id="dfee2-338">Texture2D resources have limits on their width and height that differ across [feature levels](overviews-direct3d-11-devices-downlevel-intro.md).</span></span> <span data-ttu-id="dfee2-339">В уровнях функций 9 \_ 3 гарантируется прыжка, а отдельные реализации могут превысить требования.</span><span class="sxs-lookup"><span data-stu-id="dfee2-339">In feature levels 9\_3, the following are guaranteed minima, and individual implementations may exceed the requirements.</span></span>



| <span data-ttu-id="dfee2-340">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-340">Feature Level</span></span>             | <span data-ttu-id="dfee2-341">Если Мипкаунт > 1, измерения должны быть целыми степенями двух</span><span class="sxs-lookup"><span data-stu-id="dfee2-341">If MipCount > 1, Dimensions must be integral power of two</span></span> | <span data-ttu-id="dfee2-342">Минимальное поддерживаемое измерение текстуры</span><span class="sxs-lookup"><span data-stu-id="dfee2-342">Minimum supported texture dimension</span></span> | <span data-ttu-id="dfee2-343">Измерения текстур Куба должны быть степенью двух</span><span class="sxs-lookup"><span data-stu-id="dfee2-343">Cube textures dimensions must be power of two</span></span> | <span data-ttu-id="dfee2-344">Если \_ задан параметр "Прочие текстурекубе", размера массива имеет следующее значение:</span><span class="sxs-lookup"><span data-stu-id="dfee2-344">If MISC\_TEXTURECUBE is set, the ArraySize is:</span></span> | <span data-ttu-id="dfee2-345">Если параметр \_ "Прочие текстурекубе" не задан, размера массива имеет значение.</span><span class="sxs-lookup"><span data-stu-id="dfee2-345">If MISC\_TEXTURECUBE is not set, the ArraySize is.</span></span> |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="dfee2-346">D3D \_ \_ уровень возможностей \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-346">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="dfee2-347">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-347">Yes</span></span>                                                          | <span data-ttu-id="dfee2-348">2048</span><span class="sxs-lookup"><span data-stu-id="dfee2-348">2048</span></span>                                | <span data-ttu-id="dfee2-349">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-349">Yes</span></span>                                           | <span data-ttu-id="dfee2-350">6</span><span class="sxs-lookup"><span data-stu-id="dfee2-350">6</span></span>                                              | <span data-ttu-id="dfee2-351">1</span><span class="sxs-lookup"><span data-stu-id="dfee2-351">1</span></span>                                                  |
| <span data-ttu-id="dfee2-352">D3D \_ \_ уровень возможностей \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="dfee2-352">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="dfee2-353">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-353">Yes</span></span>                                                          | <span data-ttu-id="dfee2-354">2048</span><span class="sxs-lookup"><span data-stu-id="dfee2-354">2048</span></span>                                | <span data-ttu-id="dfee2-355">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-355">Yes</span></span>                                           | <span data-ttu-id="dfee2-356">6</span><span class="sxs-lookup"><span data-stu-id="dfee2-356">6</span></span>                                              | <span data-ttu-id="dfee2-357">1</span><span class="sxs-lookup"><span data-stu-id="dfee2-357">1</span></span>                                                  |
| <span data-ttu-id="dfee2-358">D3D \_ \_ уровень возможностей \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dfee2-358">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="dfee2-359">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-359">Yes</span></span>                                                          | <span data-ttu-id="dfee2-360">4096</span><span class="sxs-lookup"><span data-stu-id="dfee2-360">4096</span></span>                                | <span data-ttu-id="dfee2-361">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-361">Yes</span></span>                                           | <span data-ttu-id="dfee2-362">6</span><span class="sxs-lookup"><span data-stu-id="dfee2-362">6</span></span>                                              | <span data-ttu-id="dfee2-363">1</span><span class="sxs-lookup"><span data-stu-id="dfee2-363">1</span></span>                                                  |



 

<span data-ttu-id="dfee2-364">В предыдущей таблице полное имя **\_ Текстурекубе** — [**D3D11 \_ Resource \_ \_ текстурекубе**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span><span class="sxs-lookup"><span data-stu-id="dfee2-364">In the previous table, the full name of **MISC\_TEXTURECUBE** is [**D3D11\_RESOURCE\_MISC\_TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span></span>

<span data-ttu-id="dfee2-365">Для всех 9 \_ \* [уровней компонентов](overviews-direct3d-11-devices-downlevel-intro.md)справедливы следующие условия:</span><span class="sxs-lookup"><span data-stu-id="dfee2-365">The following are true for all 9\_\* [feature levels](overviews-direct3d-11-devices-downlevel-intro.md):</span></span>

-   <span data-ttu-id="dfee2-366">При использовании \_ \_ неизменяемого значения по умолчанию D3D11 или D3D11 использование \_ \_ биндфлагс не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="dfee2-366">When using D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>
-   <span data-ttu-id="dfee2-367">При использовании \_ \_ набора элементов глубины привязки D3D11 \_ миплевелс должен быть равен 1.</span><span class="sxs-lookup"><span data-stu-id="dfee2-367">When using D3D11\_BIND\_DEPTH\_STENCIL, MipLevels must be 1.</span></span>
-   <span data-ttu-id="dfee2-368">При использовании \_ \_ ресурса шейдера привязки D3D11 \_ сампледеск. Count должно быть равно 1.</span><span class="sxs-lookup"><span data-stu-id="dfee2-368">When using D3D11\_BIND\_SHADER\_RESOURCE, SampleDesc.Count must be 1.</span></span>
-   <span data-ttu-id="dfee2-369">Если используется \_ Привязка D3D11 \_ , ресурс не может иметь \_ \_ ресурс шейдера D3D11 BIND \_ .</span><span class="sxs-lookup"><span data-stu-id="dfee2-369">When using D3D11\_BIND\_PRESENT, resource cannot have D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
-   <span data-ttu-id="dfee2-370">При использовании \_ \_ общего доступа к ресурсам DDI D3D10 \_ \_ Формат не может иметь формат DXGI \_ \_ R8G8B8A8 \_ UNORM или \_ DXGI \_ R8G8B8A8 \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="dfee2-370">When using D3D10\_DDI\_RESOURCE\_MISC\_SHARED, Format cannot be DXGI\_FORMAT\_R8G8B8A8\_UNORM or DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB.</span></span>

## <a name="id3d11devicecreatetexture3d"></a><span data-ttu-id="dfee2-371">ID3D11Device::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="dfee2-371">ID3D11Device::CreateTexture3D</span></span>



| <span data-ttu-id="dfee2-372">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-372">Feature Level</span></span>             | <span data-ttu-id="dfee2-373">Максимальное измерение (любая ось)</span><span class="sxs-lookup"><span data-stu-id="dfee2-373">Maximum Dimension (any axis)</span></span> | <span data-ttu-id="dfee2-374">Размеры должны быть степенями двух</span><span class="sxs-lookup"><span data-stu-id="dfee2-374">Dimensions must be power of two</span></span> |
|---------------------------|------------------------------|---------------------------------|
| <span data-ttu-id="dfee2-375">D3D \_ \_ уровень возможностей \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-375">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="dfee2-376">256</span><span class="sxs-lookup"><span data-stu-id="dfee2-376">256</span></span>                          | <span data-ttu-id="dfee2-377">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-377">Yes</span></span>                             |
| <span data-ttu-id="dfee2-378">D3D \_ \_ уровень возможностей \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="dfee2-378">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="dfee2-379">512</span><span class="sxs-lookup"><span data-stu-id="dfee2-379">512</span></span>                          | <span data-ttu-id="dfee2-380">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-380">Yes</span></span>                             |
| <span data-ttu-id="dfee2-381">D3D \_ \_ уровень возможностей \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dfee2-381">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="dfee2-382">512</span><span class="sxs-lookup"><span data-stu-id="dfee2-382">512</span></span>                          | <span data-ttu-id="dfee2-383">Да</span><span class="sxs-lookup"><span data-stu-id="dfee2-383">Yes</span></span>                             |



 

<span data-ttu-id="dfee2-384">Если ресурс D3D11 \_ использование \_ по умолчанию или D3D11 \_ использование \_ неизменным, биндфлагс не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="dfee2-384">If resource is D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>

## <a name="id3d11devicecreateunorderedaccessview"></a><span data-ttu-id="dfee2-385">ID3D11Device:: Креатеунордередакцессвиев</span><span class="sxs-lookup"><span data-stu-id="dfee2-385">ID3D11Device::CreateUnorderedAccessView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-386">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-386">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-387">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="dfee2-389">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatevertexshader"></a><span data-ttu-id="dfee2-392">ID3D11Device:: Креатевертексшадер</span><span class="sxs-lookup"><span data-stu-id="dfee2-392">ID3D11Device::CreateVertexShader</span></span>



| <span data-ttu-id="dfee2-393">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-393">Feature Level</span></span>             | <span data-ttu-id="dfee2-394">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-394">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="dfee2-395">D3D \_ \_ уровень возможностей \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-395">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="dfee2-396">Необходимо использовать VS \_ 4 \_ 0 \_ уровня \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-396">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="dfee2-397">D3D \_ \_ уровень возможностей \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="dfee2-397">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="dfee2-398">Необходимо использовать VS \_ 4 \_ 0 \_ уровня \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-398">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="dfee2-399">D3D \_ \_ уровень возможностей \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dfee2-399">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="dfee2-400">Необходимо использовать VS \_ 4 \_ 0 \_ уровня \_ 9 \_ 3 или VS \_ 4 \_ 0 \_ уровня \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dfee2-400">Must use vs\_4\_0\_level\_9\_3 or vs\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11deviceopensharedresource"></a><span data-ttu-id="dfee2-401">ID3D11Device:: Опеншаредресаурце</span><span class="sxs-lookup"><span data-stu-id="dfee2-401">ID3D11Device::OpenSharedResource</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dfee2-402">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="dfee2-402">Feature Level</span></span></th>
<th><span data-ttu-id="dfee2-403">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="dfee2-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfee2-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="dfee2-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="dfee2-405">Используйте <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: чеккфеатуресуппорт</strong></a> со значением <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> и структурой <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> , чтобы определить, можно ли предоставить общий доступ к формату.</span><span class="sxs-lookup"><span data-stu-id="dfee2-405">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a> with the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> value and the <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> structure to determine if a format can be shared.</span></span> <span data-ttu-id="dfee2-406">Если формат можно использовать совместно, <strong>чеккфеатуресуппорт</strong> возвращает флаг <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="dfee2-406">If the format can be shared, <strong>CheckFeatureSupport</strong> returns the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> flag.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dfee2-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/Виндовс/десктоп/АПИ/дксгиформат/не-дксгиформат-dxgi_format) и <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> никогда не являются общими при использовании уровня функции 9, даже если устройство указывает на поддержку дополнительных компонентов для <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span><span class="sxs-lookup"><span data-stu-id="dfee2-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> are never shareable when using feature level 9, even if the device indicates optional feature support for <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span></span> <span data-ttu-id="dfee2-408">Попытка создать общие ресурсы с помощью форматов DXGI <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> и <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> будет завершаться ошибкой, если только уровень компонента не 10_0 или выше.</span><span class="sxs-lookup"><span data-stu-id="dfee2-408">Attempting to create shared resources with DXGI formats <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> will always fail unless the feature level is 10_0 or higher.</span></span>
</blockquote>
<br/> <span data-ttu-id="dfee2-409">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="dfee2-409">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfee2-410">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="dfee2-410">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dfee2-411">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="dfee2-411">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="dfee2-412">См. также</span><span class="sxs-lookup"><span data-stu-id="dfee2-412">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfee2-413">Справочник по 10Level9</span><span class="sxs-lookup"><span data-stu-id="dfee2-413">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

