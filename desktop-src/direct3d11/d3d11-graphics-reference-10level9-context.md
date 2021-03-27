---
title: 10Level9 ссылку ID3D11DeviceContext методы
description: В этом разделе перечислены различия между каждым уровнем функций 10Level9 и уровнем D3D \_ уровня \_ \_ 11 \_ 0 и более высоким уровнем функций для методов ссылку ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb3dc46aeeb5d629c4bf50492083d09b34de1b08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067510"
---
# <a name="10level9-id3d11devicecontext-methods"></a><span data-ttu-id="c8567-103">10Level9 ссылку ID3D11DeviceContext методы</span><span class="sxs-lookup"><span data-stu-id="c8567-103">10Level9 ID3D11DeviceContext Methods</span></span>

<span data-ttu-id="c8567-104">В этом разделе перечислены различия между каждым уровнем функций 10Level9 и уровнем D3D \_ уровня \_ \_ 11 \_ 0 и более высоким уровнем функций для методов [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="c8567-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods.</span></span>

-   [<span data-ttu-id="c8567-105">Ссылку ID3D11DeviceContext:: Кописубресаурцерегион</span><span class="sxs-lookup"><span data-stu-id="c8567-105">ID3D11DeviceContext::CopySubresourceRegion</span></span>](#id3d11devicecontextcopysubresourceregion)
-   [<span data-ttu-id="c8567-106">Ссылку ID3D11DeviceContext:: Копиресаурце</span><span class="sxs-lookup"><span data-stu-id="c8567-106">ID3D11DeviceContext::CopyResource</span></span>](#id3d11devicecontextcopyresource)
-   [<span data-ttu-id="c8567-107">Ссылку ID3D11DeviceContext:: Копиструктурекаунт</span><span class="sxs-lookup"><span data-stu-id="c8567-107">ID3D11DeviceContext::CopyStructureCount</span></span>](#id3d11devicecontextcopystructurecount)
-   [<span data-ttu-id="c8567-108">Ссылку ID3D11DeviceContext:: Клеарунордередакцессвиевфлоат</span><span class="sxs-lookup"><span data-stu-id="c8567-108">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [<span data-ttu-id="c8567-109">Ссылку ID3D11DeviceContext:: Клеарунордередакцессвиевуинт</span><span class="sxs-lookup"><span data-stu-id="c8567-109">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>](#id3d11devicecontextclearunorderedaccessviewuint)
-   [<span data-ttu-id="c8567-110">Ссылку ID3D11DeviceContext:: Клеаррендертаржетвиев</span><span class="sxs-lookup"><span data-stu-id="c8567-110">ID3D11DeviceContext::ClearRenderTargetView</span></span>](#id3d11devicecontextclearrendertargetview)
-   [<span data-ttu-id="c8567-111">Ссылку ID3D11DeviceContext:: Кссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-111">ID3D11DeviceContext::CSSetConstantBuffers</span></span>](#id3d11devicecontextcssetconstantbuffers)
-   [<span data-ttu-id="c8567-112">Ссылку ID3D11DeviceContext:: Кссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-112">ID3D11DeviceContext::CSSetSamplers</span></span>](#id3d11devicecontextcssetsamplers)
-   [<span data-ttu-id="c8567-113">Ссылку ID3D11DeviceContext:: Кссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-113">ID3D11DeviceContext::CSSetShader</span></span>](#id3d11devicecontextcssetshader)
-   [<span data-ttu-id="c8567-114">Ссылку ID3D11DeviceContext:: Кссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-114">ID3D11DeviceContext::CSSetShaderResources</span></span>](#id3d11devicecontextcssetshaderresources)
-   [<span data-ttu-id="c8567-115">Ссылку ID3D11DeviceContext:: Кссетунордередакцессвиевс</span><span class="sxs-lookup"><span data-stu-id="c8567-115">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>](#id3d11devicecontextcssetunorderedaccessviews)
-   [<span data-ttu-id="c8567-116">Ссылку ID3D11DeviceContext::D Patch</span><span class="sxs-lookup"><span data-stu-id="c8567-116">ID3D11DeviceContext::Dispatch</span></span>](#id3d11devicecontextdispatch)
-   [<span data-ttu-id="c8567-117">Ссылку ID3D11DeviceContext::D Испатчиндирект</span><span class="sxs-lookup"><span data-stu-id="c8567-117">ID3D11DeviceContext::DispatchIndirect</span></span>](#id3d11devicecontextdispatchindirect)
-   [<span data-ttu-id="c8567-118">ID3D11DeviceContext::Draw</span><span class="sxs-lookup"><span data-stu-id="c8567-118">ID3D11DeviceContext::Draw</span></span>](#id3d11devicecontextdraw)
-   [<span data-ttu-id="c8567-119">ID3D11DeviceContext::DrawAuto</span><span class="sxs-lookup"><span data-stu-id="c8567-119">ID3D11DeviceContext::DrawAuto</span></span>](#id3d11devicecontextdrawauto)
-   [<span data-ttu-id="c8567-120">ID3D11DeviceContext::DrawIndexed</span><span class="sxs-lookup"><span data-stu-id="c8567-120">ID3D11DeviceContext::DrawIndexed</span></span>](#id3d11devicecontextdrawindexed)
-   [<span data-ttu-id="c8567-121">ID3D11DeviceContext::DrawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="c8567-121">ID3D11DeviceContext::DrawIndexedInstanced</span></span>](#id3d11devicecontextdrawindexedinstanced)
-   [<span data-ttu-id="c8567-122">Ссылку ID3D11DeviceContext::D Равиндексединстанцединдирект</span><span class="sxs-lookup"><span data-stu-id="c8567-122">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>](#id3d11devicecontextdrawindexedinstancedindirect)
-   [<span data-ttu-id="c8567-123">ID3D11DeviceContext::DrawInstanced</span><span class="sxs-lookup"><span data-stu-id="c8567-123">ID3D11DeviceContext::DrawInstanced</span></span>](#id3d11devicecontextdrawinstanced)
-   [<span data-ttu-id="c8567-124">Ссылку ID3D11DeviceContext::D Равинстанцединдирект</span><span class="sxs-lookup"><span data-stu-id="c8567-124">ID3D11DeviceContext::DrawInstancedIndirect</span></span>](#id3d11devicecontextdrawinstancedindirect)
-   [<span data-ttu-id="c8567-125">Ссылку ID3D11DeviceContext::D Ссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-125">ID3D11DeviceContext::DSSetConstantBuffers</span></span>](#id3d11devicecontextdssetconstantbuffers)
-   [<span data-ttu-id="c8567-126">Ссылку ID3D11DeviceContext::D Ссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-126">ID3D11DeviceContext::DSSetSamplers</span></span>](#id3d11devicecontextdssetsamplers)
-   [<span data-ttu-id="c8567-127">Ссылку ID3D11DeviceContext::D Ссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-127">ID3D11DeviceContext::DSSetShader</span></span>](#id3d11devicecontextdssetshader)
-   [<span data-ttu-id="c8567-128">Ссылку ID3D11DeviceContext::D Ссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-128">ID3D11DeviceContext::DSSetShaderResources</span></span>](#id3d11devicecontextdssetshaderresources)
-   [<span data-ttu-id="c8567-129">Ссылку ID3D11DeviceContext:: Гссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-129">ID3D11DeviceContext::GSSetConstantBuffers</span></span>](#id3d11devicecontextgssetconstantbuffers)
-   [<span data-ttu-id="c8567-130">Ссылку ID3D11DeviceContext:: Гссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-130">ID3D11DeviceContext::GSSetSamplers</span></span>](#id3d11devicecontextgssetsamplers)
-   [<span data-ttu-id="c8567-131">Ссылку ID3D11DeviceContext:: Гссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-131">ID3D11DeviceContext::GSSetShader</span></span>](#id3d11devicecontextgssetshader)
-   [<span data-ttu-id="c8567-132">Ссылку ID3D11DeviceContext:: Гссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-132">ID3D11DeviceContext::GSSetShaderResources</span></span>](#id3d11devicecontextgssetshaderresources)
-   [<span data-ttu-id="c8567-133">Ссылку ID3D11DeviceContext:: Хссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-133">ID3D11DeviceContext::HSSetConstantBuffers</span></span>](#id3d11devicecontexthssetconstantbuffers)
-   [<span data-ttu-id="c8567-134">Ссылку ID3D11DeviceContext:: Хссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-134">ID3D11DeviceContext::HSSetSamplers</span></span>](#id3d11devicecontexthssetsamplers)
-   [<span data-ttu-id="c8567-135">Ссылку ID3D11DeviceContext:: Хссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-135">ID3D11DeviceContext::HSSetShader</span></span>](#id3d11devicecontexthssetshader)
-   [<span data-ttu-id="c8567-136">Ссылку ID3D11DeviceContext:: Хссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-136">ID3D11DeviceContext::HSSetShaderResources</span></span>](#id3d11devicecontexthssetshaderresources)
-   [<span data-ttu-id="c8567-137">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="c8567-137">ID3D11DeviceContext::IASetIndexBuffer</span></span>](#id3d11devicecontextiasetindexbuffer)
-   [<span data-ttu-id="c8567-138">ID3D11DeviceContext::IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="c8567-138">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>](#id3d11devicecontextiasetprimitivetopology)
-   [<span data-ttu-id="c8567-139">Ссылку ID3D11DeviceContext:: Омсетблендстате</span><span class="sxs-lookup"><span data-stu-id="c8567-139">ID3D11DeviceContext::OMSetBlendState</span></span>](#id3d11devicecontextomsetblendstate)
-   [<span data-ttu-id="c8567-140">Ссылку ID3D11DeviceContext:: Омсетрендертаржетс</span><span class="sxs-lookup"><span data-stu-id="c8567-140">ID3D11DeviceContext::OMSetRenderTargets</span></span>](#id3d11devicecontextomsetrendertargets)
-   [<span data-ttu-id="c8567-141">Ссылку ID3D11DeviceContext:: Омсетрендертаржетсандунордередакцессвиевс</span><span class="sxs-lookup"><span data-stu-id="c8567-141">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [<span data-ttu-id="c8567-142">Ссылку ID3D11DeviceContext::P Ссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-142">ID3D11DeviceContext::PSSetConstantBuffers</span></span>](#id3d11devicecontextpssetconstantbuffers)
-   [<span data-ttu-id="c8567-143">Ссылку ID3D11DeviceContext::P Ссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-143">ID3D11DeviceContext::PSSetSamplers</span></span>](#id3d11devicecontextpssetsamplers)
-   [<span data-ttu-id="c8567-144">Ссылку ID3D11DeviceContext::P Ссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-144">ID3D11DeviceContext::PSSetShader</span></span>](#id3d11devicecontextpssetshader)
-   [<span data-ttu-id="c8567-145">Ссылку ID3D11DeviceContext::P Ссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-145">ID3D11DeviceContext::PSSetShaderResources</span></span>](#id3d11devicecontextpssetshaderresources)
-   [<span data-ttu-id="c8567-146">Ссылку ID3D11DeviceContext:: РссетсЦиссорректс</span><span class="sxs-lookup"><span data-stu-id="c8567-146">ID3D11DeviceContext::RSSetScissorRects</span></span>](#id3d11devicecontextrssetscissorrects)
-   [<span data-ttu-id="c8567-147">Ссылку ID3D11DeviceContext:: Рссетвиевпортс</span><span class="sxs-lookup"><span data-stu-id="c8567-147">ID3D11DeviceContext::RSSetViewports</span></span>](#id3d11devicecontextrssetviewports)
-   [<span data-ttu-id="c8567-148">Ссылку ID3D11DeviceContext:: Сетпредикатион</span><span class="sxs-lookup"><span data-stu-id="c8567-148">ID3D11DeviceContext::SetPredication</span></span>](#id3d11devicecontextsetpredication)
-   [<span data-ttu-id="c8567-149">Ссылку ID3D11DeviceContext:: Сосеттаржетс</span><span class="sxs-lookup"><span data-stu-id="c8567-149">ID3D11DeviceContext::SOSetTargets</span></span>](#id3d11devicecontextsosettargets)
-   [<span data-ttu-id="c8567-150">Ссылку ID3D11DeviceContext:: Вссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-150">ID3D11DeviceContext::VSSetConstantBuffers</span></span>](#id3d11devicecontextvssetconstantbuffers)
-   [<span data-ttu-id="c8567-151">Ссылку ID3D11DeviceContext:: Вссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-151">ID3D11DeviceContext::VSSetSamplers</span></span>](#id3d11devicecontextvssetsamplers)
-   [<span data-ttu-id="c8567-152">Ссылку ID3D11DeviceContext:: Вссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-152">ID3D11DeviceContext::VSSetShader</span></span>](#id3d11devicecontextvssetshader)
-   [<span data-ttu-id="c8567-153">Ссылку ID3D11DeviceContext:: Вссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-153">ID3D11DeviceContext::VSSetShaderResources</span></span>](#id3d11devicecontextvssetshaderresources)
-   [<span data-ttu-id="c8567-154">См. также</span><span class="sxs-lookup"><span data-stu-id="c8567-154">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a><span data-ttu-id="c8567-155">Ссылку ID3D11DeviceContext:: Кописубресаурцерегион</span><span class="sxs-lookup"><span data-stu-id="c8567-155">ID3D11DeviceContext::CopySubresourceRegion</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-156">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-156">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-157">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-157">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-158">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-158">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="c8567-159">В памяти, доступной для GPU, могут копироваться только Texture2D и буферы.</span><span class="sxs-lookup"><span data-stu-id="c8567-159">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="c8567-160">Texture3D не может быть скопирован из памяти, доступной GPU, в память, доступную для ЦП.</span><span class="sxs-lookup"><span data-stu-id="c8567-160">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="c8567-161">Любой ресурс, имеющий только D3D10_BIND_SHADER_RESOURCE, не может быть скопирован из памяти, доступной на GPU, в память, доступную для ЦП.</span><span class="sxs-lookup"><span data-stu-id="c8567-161">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="c8567-162">Копировать текстуры тома мипмаппед нельзя.</span><span class="sxs-lookup"><span data-stu-id="c8567-162">You can't copy mipmapped volume textures.</span></span> <br/> <span data-ttu-id="c8567-163">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c8567-163">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-164">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-164">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-165">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-165">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a><span data-ttu-id="c8567-166">Ссылку ID3D11DeviceContext:: Копиресаурце</span><span class="sxs-lookup"><span data-stu-id="c8567-166">ID3D11DeviceContext::CopyResource</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-167">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-167">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-168">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-168">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-169">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-169">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="c8567-170">В памяти, доступной для GPU, могут копироваться только Texture2D и буферы.</span><span class="sxs-lookup"><span data-stu-id="c8567-170">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="c8567-171">Texture3D не может быть скопирован из памяти, доступной GPU, в память, доступную для ЦП.</span><span class="sxs-lookup"><span data-stu-id="c8567-171">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="c8567-172">Любой ресурс, имеющий только D3D10_BIND_SHADER_RESOURCE, не может быть скопирован из памяти, доступной на GPU, в память, доступную для ЦП.</span><span class="sxs-lookup"><span data-stu-id="c8567-172">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="c8567-173">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c8567-173">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-174">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-174">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-175">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-175">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a><span data-ttu-id="c8567-176">Ссылку ID3D11DeviceContext:: Копиструктурекаунт</span><span class="sxs-lookup"><span data-stu-id="c8567-176">ID3D11DeviceContext::CopyStructureCount</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-177">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-177">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-178">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-178">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-179">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-179">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-180">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-180">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-181">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-181">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-182">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-182">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a><span data-ttu-id="c8567-183">Ссылку ID3D11DeviceContext:: Клеарунордередакцессвиевфлоат</span><span class="sxs-lookup"><span data-stu-id="c8567-183">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-184">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-184">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-185">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-185">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-186">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-186">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-187">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-187">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-188">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-188">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-189">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-189">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a><span data-ttu-id="c8567-190">Ссылку ID3D11DeviceContext:: Клеарунордередакцессвиевуинт</span><span class="sxs-lookup"><span data-stu-id="c8567-190">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-191">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-191">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-192">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-192">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-193">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-193">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-194">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-194">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-195">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-195">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-196">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-196">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a><span data-ttu-id="c8567-197">Ссылку ID3D11DeviceContext:: Клеаррендертаржетвиев</span><span class="sxs-lookup"><span data-stu-id="c8567-197">ID3D11DeviceContext::ClearRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-198">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-198">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-199">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-199">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-200">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-200">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-201">Будет сброшен только первый срез массива.</span><span class="sxs-lookup"><span data-stu-id="c8567-201">Only the first array slice will be cleared.</span></span> <span data-ttu-id="c8567-202">Приложения должны создать представление целевого объекта отрисовки для каждой грани или среза массива, а затем очистить каждое представление по отдельности. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-202">Applications should create a render target view for each face or array slice, then clear each view individually.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-203">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-203">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-204">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-204">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a><span data-ttu-id="c8567-205">Ссылку ID3D11DeviceContext:: Кссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-205">ID3D11DeviceContext::CSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-206">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-206">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-207">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-207">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-208">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-208">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-209">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-209">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-210">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-210">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-211">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-211">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a><span data-ttu-id="c8567-212">Ссылку ID3D11DeviceContext:: Кссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-212">ID3D11DeviceContext::CSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-213">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-213">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-214">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-214">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-215">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-215">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-216">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-216">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-217">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-217">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-218">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-218">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a><span data-ttu-id="c8567-219">Ссылку ID3D11DeviceContext:: Кссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-219">ID3D11DeviceContext::CSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-220">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-220">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-221">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-221">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-222">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-222">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-223">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-223">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-224">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-224">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-225">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-225">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a><span data-ttu-id="c8567-226">Ссылку ID3D11DeviceContext:: Кссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-226">ID3D11DeviceContext::CSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-227">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-227">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-228">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-228">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-229">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-229">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-230">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-230">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-231">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-231">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-232">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-232">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a><span data-ttu-id="c8567-233">Ссылку ID3D11DeviceContext:: Кссетунордередакцессвиевс</span><span class="sxs-lookup"><span data-stu-id="c8567-233">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-234">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-234">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-235">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-235">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-236">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-236">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-237">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-237">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-238">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-238">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-239">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-239">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a><span data-ttu-id="c8567-240">Ссылку ID3D11DeviceContext::D Patch</span><span class="sxs-lookup"><span data-stu-id="c8567-240">ID3D11DeviceContext::Dispatch</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-241">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-241">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-242">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-242">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-243">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-243">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-244">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-244">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-245">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-245">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-246">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-246">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a><span data-ttu-id="c8567-247">Ссылку ID3D11DeviceContext::D Испатчиндирект</span><span class="sxs-lookup"><span data-stu-id="c8567-247">ID3D11DeviceContext::DispatchIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-248">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-248">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-249">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-249">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-250">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-250">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-251">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-251">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-252">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-252">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-253">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-253">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a><span data-ttu-id="c8567-254">ID3D11DeviceContext::Draw</span><span class="sxs-lookup"><span data-stu-id="c8567-254">ID3D11DeviceContext::Draw</span></span>



| <span data-ttu-id="c8567-255">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-255">Feature Level</span></span>             | <span data-ttu-id="c8567-256">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-256">Behavior Differences</span></span>                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8567-257">D3D \_ \_ уровень возможностей \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c8567-257">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="c8567-258">Число примитивов не может превышать 65535.</span><span class="sxs-lookup"><span data-stu-id="c8567-258">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="c8567-259">Текстуры не могут повторяться поверх одного примитива более 128 раз.</span><span class="sxs-lookup"><span data-stu-id="c8567-259">Textures cannot repeat over one primitive more than 128 times.</span></span><br/>    |
| <span data-ttu-id="c8567-260">D3D \_ \_ уровень возможностей \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="c8567-260">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="c8567-261">Число примитивов не может превышать 1048575.</span><span class="sxs-lookup"><span data-stu-id="c8567-261">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="c8567-262">Текстуры не могут повторяться поверх одного примитива более 2048 раз.</span><span class="sxs-lookup"><span data-stu-id="c8567-262">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> |
| <span data-ttu-id="c8567-263">D3D \_ \_ уровень возможностей \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c8567-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="c8567-264">Число примитивов не может превышать 1048575.</span><span class="sxs-lookup"><span data-stu-id="c8567-264">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="c8567-265">Текстуры не могут повторяться поверх одного примитива более 8192 раз.</span><span class="sxs-lookup"><span data-stu-id="c8567-265">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawauto"></a><span data-ttu-id="c8567-266">ID3D11DeviceContext::DrawAuto</span><span class="sxs-lookup"><span data-stu-id="c8567-266">ID3D11DeviceContext::DrawAuto</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-267">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-267">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-268">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-268">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-269">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-269">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-270">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-270">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-271">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-271">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-272">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-272">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a><span data-ttu-id="c8567-273">ID3D11DeviceContext::DrawIndexed</span><span class="sxs-lookup"><span data-stu-id="c8567-273">ID3D11DeviceContext::DrawIndexed</span></span>



| <span data-ttu-id="c8567-274">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-274">Feature Level</span></span>             | <span data-ttu-id="c8567-275">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-275">Behavior Differences</span></span>                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8567-276">D3D \_ \_ уровень возможностей \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c8567-276">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="c8567-277">Число примитивов не может превышать 65535.</span><span class="sxs-lookup"><span data-stu-id="c8567-277">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="c8567-278">Текстуры не могут повторяться поверх одного примитива более 128 раз.</span><span class="sxs-lookup"><span data-stu-id="c8567-278">Textures cannot repeat over one primitive more than 128 times.</span></span><br/> <span data-ttu-id="c8567-279">Значения индекса не могут превышать 65534.</span><span class="sxs-lookup"><span data-stu-id="c8567-279">Index values cannot exceed 65534.</span></span><br/> <span data-ttu-id="c8567-280">Списки индексированных точек не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c8567-280">Indexed point lists not supported.</span></span><br/>      |
| <span data-ttu-id="c8567-281">D3D \_ \_ уровень возможностей \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="c8567-281">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="c8567-282">Число примитивов не может превышать 1048575.</span><span class="sxs-lookup"><span data-stu-id="c8567-282">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="c8567-283">Текстуры не могут повторяться поверх одного примитива более 2048 раз.</span><span class="sxs-lookup"><span data-stu-id="c8567-283">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> <span data-ttu-id="c8567-284">Значения индекса не могут превышать 1048575.</span><span class="sxs-lookup"><span data-stu-id="c8567-284">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="c8567-285">Списки индексированных точек не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c8567-285">Indexed point lists not supported.</span></span><br/> |
| <span data-ttu-id="c8567-286">D3D \_ \_ уровень возможностей \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c8567-286">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="c8567-287">Число примитивов не может превышать 1048575.</span><span class="sxs-lookup"><span data-stu-id="c8567-287">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="c8567-288">Текстуры не могут повторяться поверх одного примитива более 8192 раз.</span><span class="sxs-lookup"><span data-stu-id="c8567-288">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="c8567-289">Значения индекса не могут превышать 1048575.</span><span class="sxs-lookup"><span data-stu-id="c8567-289">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="c8567-290">Списки индексированных точек не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c8567-290">Indexed point lists not supported.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a><span data-ttu-id="c8567-291">ID3D11DeviceContext::DrawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="c8567-291">ID3D11DeviceContext::DrawIndexedInstanced</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-292">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-292">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-293">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-293">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-294">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-294">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="c8567-295">Не поддерживается $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-295">Not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-296">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-296">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-297">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-297">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="c8567-298">Число примитивов не может превышать 1048575.</span><span class="sxs-lookup"><span data-stu-id="c8567-298">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="c8567-299">Текстуры не могут повторяться поверх одного примитива более 8192 раз.</span><span class="sxs-lookup"><span data-stu-id="c8567-299">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="c8567-300">Значения индекса не могут превышать 1048575.</span><span class="sxs-lookup"><span data-stu-id="c8567-300">Index values cannot exceed 1048575.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c8567-301">При вызове метода <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>дравиндексединстанцед</strong></a> с шейдером вершин, привязанным к конвейеру и не импортируя данные каждого экземпляра, некоторые графические аппаратные устройства с Direct3D 9 могут не рисовать ничего.</span><span class="sxs-lookup"><span data-stu-id="c8567-301">When you call the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> method with a vertex shader that is bound to the pipeline and that doesn't import any per-instance data, some Direct3D 9 graphics hardware might not draw anything.</span></span> <span data-ttu-id="c8567-302">В частности, если шейдер вершин не использует данные каждого экземпляра, вызов <strong>дравиндексединстанцед</strong> с 1 экземпляром не эквивалентен вызову <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c8567-302">In particular, if the vertex shader does not use any per-instance data, calling <strong>DrawIndexedInstanced</strong> with 1 instance is not equivalent to calling <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a><span data-ttu-id="c8567-303">Ссылку ID3D11DeviceContext::D Равиндексединстанцединдирект</span><span class="sxs-lookup"><span data-stu-id="c8567-303">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-304">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-304">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-305">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-305">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-306">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-306">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="c8567-307">Не поддерживается на уровне функций 9. \* или 10. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-307">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-308">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-308">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-309">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-309">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c8567-310">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="c8567-310">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-311">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="c8567-311">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a><span data-ttu-id="c8567-312">ID3D11DeviceContext::DrawInstanced</span><span class="sxs-lookup"><span data-stu-id="c8567-312">ID3D11DeviceContext::DrawInstanced</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-313">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-313">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-314">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-314">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-315">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-315">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-316">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-316">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-317">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-317">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-318">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-318">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a><span data-ttu-id="c8567-319">Ссылку ID3D11DeviceContext::D Равинстанцединдирект</span><span class="sxs-lookup"><span data-stu-id="c8567-319">ID3D11DeviceContext::DrawInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-320">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-320">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-321">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-321">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-322">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-322">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="c8567-323">Не поддерживается на уровне функций 9. \* или 10. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-323">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-324">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-324">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-325">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-325">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c8567-326">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="c8567-326">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-327">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="c8567-327">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a><span data-ttu-id="c8567-328">Ссылку ID3D11DeviceContext::D Ссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-328">ID3D11DeviceContext::DSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-329">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-329">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-330">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-330">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-331">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-331">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="c8567-332">Не поддерживается на уровне функций 9. \* или 10. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-332">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-333">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-333">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-334">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-334">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c8567-335">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="c8567-335">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-336">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="c8567-336">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a><span data-ttu-id="c8567-337">Ссылку ID3D11DeviceContext::D Ссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-337">ID3D11DeviceContext::DSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-338">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-338">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-339">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-339">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-340">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-340">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="c8567-341">Не поддерживается на уровне функций 9. \* или 10. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-341">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-342">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-342">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-343">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-343">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c8567-344">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="c8567-344">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-345">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="c8567-345">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a><span data-ttu-id="c8567-346">Ссылку ID3D11DeviceContext::D Ссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-346">ID3D11DeviceContext::DSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-347">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-347">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-348">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-348">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-349">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-349">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="c8567-350">Не поддерживается на уровне функций 9. \* или 10. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-350">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-351">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-351">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-352">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-352">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c8567-353">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="c8567-353">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-354">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="c8567-354">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a><span data-ttu-id="c8567-355">Ссылку ID3D11DeviceContext::D Ссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-355">ID3D11DeviceContext::DSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-356">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-356">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-357">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-357">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-358">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-358">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="c8567-359">Не поддерживается на уровне функций 9. \* или 10. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-359">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-360">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-360">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-361">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-361">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c8567-362">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="c8567-362">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-363">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="c8567-363">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a><span data-ttu-id="c8567-364">Ссылку ID3D11DeviceContext:: Гссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-364">ID3D11DeviceContext::GSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-365">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-365">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-366">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-366">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-367">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-367">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-368">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-368">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-369">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-369">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-370">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-370">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a><span data-ttu-id="c8567-371">Ссылку ID3D11DeviceContext:: Гссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-371">ID3D11DeviceContext::GSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-372">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-372">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-373">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-373">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-374">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-374">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-375">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-375">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-376">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-376">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-377">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-377">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a><span data-ttu-id="c8567-378">Ссылку ID3D11DeviceContext:: Гссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-378">ID3D11DeviceContext::GSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-379">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-379">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-380">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-380">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-381">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-381">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-382">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-382">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-383">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-383">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-384">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-384">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a><span data-ttu-id="c8567-385">Ссылку ID3D11DeviceContext:: Гссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-385">ID3D11DeviceContext::GSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-386">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-386">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-387">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-389">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a><span data-ttu-id="c8567-392">Ссылку ID3D11DeviceContext:: Хссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-392">ID3D11DeviceContext::HSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-393">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-393">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-394">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-394">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-395">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-395">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="c8567-396">Не поддерживается на уровне функций 9. \* или 10. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-396">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-397">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-397">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-398">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-398">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c8567-399">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="c8567-399">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-400">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="c8567-400">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a><span data-ttu-id="c8567-401">Ссылку ID3D11DeviceContext:: Хссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-401">ID3D11DeviceContext::HSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-402">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-402">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-403">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="c8567-405">Не поддерживается на уровне функций 9. \* или 10. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-405">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-406">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-406">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-407">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-407">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c8567-408">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="c8567-408">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-409">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="c8567-409">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a><span data-ttu-id="c8567-410">Ссылку ID3D11DeviceContext:: Хссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-410">ID3D11DeviceContext::HSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-411">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-411">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-412">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-412">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-413">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-413">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="c8567-414">Не поддерживается на уровне функций 9. \* или 10. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-414">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-415">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-415">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-416">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-416">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c8567-417">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="c8567-417">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-418">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="c8567-418">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a><span data-ttu-id="c8567-419">Ссылку ID3D11DeviceContext:: Хссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-419">ID3D11DeviceContext::HSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-420">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-420">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-421">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-421">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-422">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-422">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="c8567-423">Не поддерживается на уровне функций 9. \* или 10. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-423">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-424">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-424">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-425">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-425">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c8567-426">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="c8567-426">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-427">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="c8567-427">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a><span data-ttu-id="c8567-428">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="c8567-428">ID3D11DeviceContext::IASetIndexBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-429">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-429">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-430">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-430">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-431">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-431">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="c8567-432">Формат может отличаться от формата, указанного при создании буфера, но будет дорогостоящим переводом.</span><span class="sxs-lookup"><span data-stu-id="c8567-432">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="c8567-433">Разрешает только буферы индексов с форматом DXGI_FORMAT_R16_UINT.</span><span class="sxs-lookup"><span data-stu-id="c8567-433">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-434">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-434">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="c8567-435">Формат может отличаться от формата, указанного при создании буфера, но будет дорогостоящим переводом.</span><span class="sxs-lookup"><span data-stu-id="c8567-435">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="c8567-436">Разрешает буферы индексов с форматами DXGI_FORMAT_R16_UINT и DXGI_FORMAT_R32_UINT, такими как D3D_FEATURE_LEVEL_10_0 и выше.</span><span class="sxs-lookup"><span data-stu-id="c8567-436">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="c8567-437">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c8567-437">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-438">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-438">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a><span data-ttu-id="c8567-439">ID3D11DeviceContext::IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="c8567-439">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-440">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-440">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-441">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-441">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-442">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-442">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-443">Примитивные топологии с соседями не поддерживаются $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-443">Primitive topologies with adjacency are not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-444">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-444">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-445">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-445">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a><span data-ttu-id="c8567-446">Ссылку ID3D11DeviceContext:: Омсетблендстате</span><span class="sxs-lookup"><span data-stu-id="c8567-446">ID3D11DeviceContext::OMSetBlendState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-447">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-447">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-448">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-448">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-449">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-449">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-450">Самплемаск не может быть нулевым $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-450">SampleMask cannot be zero${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-451">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-451">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-452">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-452">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a><span data-ttu-id="c8567-453">Ссылку ID3D11DeviceContext:: Омсетрендертаржетс</span><span class="sxs-lookup"><span data-stu-id="c8567-453">ID3D11DeviceContext::OMSetRenderTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-454">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-454">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-455">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-455">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-456">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-456">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="c8567-457">Поддерживается только один целевой объект прорисовки $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-457">Only one render target supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-458">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-458">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-459">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-459">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="c8567-460">Поддерживаются только четыре целевого объекта отрисовки, и все связанные ресурсы должны иметь одинаковую глубину.</span><span class="sxs-lookup"><span data-stu-id="c8567-460">Only four render targets supported, and all bound resources must have same bit depth.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a><span data-ttu-id="c8567-461">Ссылку ID3D11DeviceContext:: Омсетрендертаржетсандунордередакцессвиевс</span><span class="sxs-lookup"><span data-stu-id="c8567-461">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-462">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-462">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-463">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-463">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-464">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-464">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-465">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-465">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-466">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-466">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-467">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-467">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a><span data-ttu-id="c8567-468">Ссылку ID3D11DeviceContext::P Ссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-468">ID3D11DeviceContext::PSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-469">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-469">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-470">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-470">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-471">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-471">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-472">См. раздел уровень компонентов 10,0, но общее число констант, используемых шейдером, не может превышать 32 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-472">See feature level 10.0, but total number of constants used by shader cannot exceed 32${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-473">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-473">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-474">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-474">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a><span data-ttu-id="c8567-475">Ссылку ID3D11DeviceContext::P Ссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-475">ID3D11DeviceContext::PSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-476">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-476">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-477">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-477">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-478">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-478">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-479">Можно привязать не более 16 пробных выдолженстей $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-479">No more than 16 samplers can be bound${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-480">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-480">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-481">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-481">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a><span data-ttu-id="c8567-482">Ссылку ID3D11DeviceContext::P Ссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-482">ID3D11DeviceContext::PSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-483">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-483">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-484">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-484">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-485">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-485">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="c8567-486">Только ps_4_0_level_9_1 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-486">Only ps_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-487">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-487">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-488">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-488">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="c8567-489">Только ps_4_0_level_9_3 или ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-489">Only ps_4_0_level_9_3 or ps_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a><span data-ttu-id="c8567-490">Ссылку ID3D11DeviceContext::P Ссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-490">ID3D11DeviceContext::PSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-491">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-491">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-492">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-492">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-493">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-493">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-494">Не более 8 одновременно привязанных ресурсов шейдера $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-494">No more than 8 simultaneously bound shader resources${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-495">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-495">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-496">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-496">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a><span data-ttu-id="c8567-497">Ссылку ID3D11DeviceContext:: РссетсЦиссорректс</span><span class="sxs-lookup"><span data-stu-id="c8567-497">ID3D11DeviceContext::RSSetScissorRects</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-498">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-498">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-499">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-499">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-500">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-500">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-501">Доступен только начальном-прямоугольный прямоугольник $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-501">Only the zeroth scissor rect is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-502">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-502">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-503">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-503">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a><span data-ttu-id="c8567-504">Ссылку ID3D11DeviceContext:: Рссетвиевпортс</span><span class="sxs-lookup"><span data-stu-id="c8567-504">ID3D11DeviceContext::RSSetViewports</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-505">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-505">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-506">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-506">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-507">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-507">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-508">Доступно только окно просмотра начальном $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-508">Only the zeroth viewport is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-509">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-509">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-510">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-510">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="c8567-511">Даже если вы указали значения float для элементов структуры [**\_ окна просмотра D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) для массива *Пвиевпортс* в вызове [**ссылку ID3D11DeviceContext:: рссетвиевпортс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) для [уровней компонентов](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, **рссетвиевпортс** использует DWORD внутри.</span><span class="sxs-lookup"><span data-stu-id="c8567-511">Even though you specify float values to the members of the [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) structure for the *pViewports* array in a call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9\_x, **RSSetViewports** uses DWORDs internally.</span></span> <span data-ttu-id="c8567-512">Из-за такого поведения при использовании отрицательного верхнего левого угла для окна просмотра, вызов **рссетвиевпортс** для уровней компонентов 9 \_ x завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c8567-512">Because of this behavior, when you use a negative top left corner for the viewport, the call to **RSSetViewports** for feature levels 9\_x fails.</span></span> <span data-ttu-id="c8567-513">Эта ошибка возникает из-за того, что **рссетвиевпортс** для 9 \_ x приводит значения с плавающей запятой к целым числам без знака, не выполняя проверку, что приводит к переполнению целого числа.</span><span class="sxs-lookup"><span data-stu-id="c8567-513">This failure occurs because **RSSetViewports** for 9\_x casts the floating point values into unsigned integers without validation, which results in integer overflow.</span></span>

<span data-ttu-id="c8567-514">Вызов [**ссылку ID3D11DeviceContext:: рссетвиевпортс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) для [уровней компонентов](overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ x и 11 \_ x работает так, как вы ожидаете, даже если для окна просмотра используется отрицательный верхний левый угол.</span><span class="sxs-lookup"><span data-stu-id="c8567-514">The call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10\_x and 11\_x works as you expect even when you use a negative top left corner for the viewport.</span></span>

## <a name="id3d11devicecontextsetpredication"></a><span data-ttu-id="c8567-515">Ссылку ID3D11DeviceContext:: Сетпредикатион</span><span class="sxs-lookup"><span data-stu-id="c8567-515">ID3D11DeviceContext::SetPredication</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-516">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-516">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-517">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-517">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-518">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-518">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-519">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-519">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-520">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-520">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-521">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-521">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a><span data-ttu-id="c8567-522">Ссылку ID3D11DeviceContext:: Сосеттаржетс</span><span class="sxs-lookup"><span data-stu-id="c8567-522">ID3D11DeviceContext::SOSetTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-523">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-523">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-524">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-524">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-525">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-525">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-526">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-526">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-527">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-527">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-528">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-528">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a><span data-ttu-id="c8567-529">Ссылку ID3D11DeviceContext:: Вссетконстантбуфферс</span><span class="sxs-lookup"><span data-stu-id="c8567-529">ID3D11DeviceContext::VSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-530">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-530">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-531">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-531">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-532">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-532">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-533">См. раздел уровень компонентов 10,0, но общее число констант, используемых шейдером, не может превышать 255 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-533">See feature level 10.0, but total number of constants used by shader cannot exceed 255${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-534">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-534">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-535">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-535">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a><span data-ttu-id="c8567-536">Ссылку ID3D11DeviceContext:: Вссетсамплерс</span><span class="sxs-lookup"><span data-stu-id="c8567-536">ID3D11DeviceContext::VSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-537">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-537">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-538">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-538">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-539">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-539">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-540">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-540">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-541">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-541">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-542">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-542">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a><span data-ttu-id="c8567-543">Ссылку ID3D11DeviceContext:: Вссетшадер</span><span class="sxs-lookup"><span data-stu-id="c8567-543">ID3D11DeviceContext::VSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-544">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-544">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-545">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-545">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-546">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-546">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="c8567-547">Только vs_4_0_level_9_1 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-547">Only vs_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-548">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-548">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-549">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-549">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="c8567-550">Только vs_4_0_level_9_3 или vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-550">Only vs_4_0_level_9_3 or vs_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a><span data-ttu-id="c8567-551">Ссылку ID3D11DeviceContext:: Вссетшадерресаурцес</span><span class="sxs-lookup"><span data-stu-id="c8567-551">ID3D11DeviceContext::VSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8567-552">Уровень компонентов</span><span class="sxs-lookup"><span data-stu-id="c8567-552">Feature Level</span></span></th>
<th><span data-ttu-id="c8567-553">Различия в поведении</span><span class="sxs-lookup"><span data-stu-id="c8567-553">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8567-554">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="c8567-554">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="c8567-555">Не поддерживается на уровне функций 9. \*. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c8567-555">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8567-556">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="c8567-556">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c8567-557">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="c8567-557">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c8567-558">См. также</span><span class="sxs-lookup"><span data-stu-id="c8567-558">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8567-559">Справочник по 10Level9</span><span class="sxs-lookup"><span data-stu-id="c8567-559">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





