---
title: Структура D3DX11_STATE_BLOCK_MASK (D3dx11effect. h)
description: Указывает состояние устройства.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- D3DX11_STATE_BLOCK_MASK структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41236c541fc251902a7a0a5ad6030a28dd36e3a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355360"
---
# <a name="d3dx11_state_block_mask-structure"></a><span data-ttu-id="4d05f-104">\_ \_ Структура маски блока D3DX11 State \_</span><span class="sxs-lookup"><span data-stu-id="4d05f-104">D3DX11\_STATE\_BLOCK\_MASK structure</span></span>

<span data-ttu-id="4d05f-105">Указывает состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="4d05f-105">Indicates the device state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d05f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d05f-106">Syntax</span></span>


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a><span data-ttu-id="4d05f-107">Участники</span><span class="sxs-lookup"><span data-stu-id="4d05f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d05f-108">**ЛИНЕЙЧАТ**</span><span class="sxs-lookup"><span data-stu-id="4d05f-108">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-109">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-109">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-110">Логическое значение, указывающее, следует ли сохранять состояние шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="4d05f-110">Boolean value indicating whether to save the vertex shader state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-111">**вссамплерс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-111">**VSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-112">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-112">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-113">Массив образцов шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="4d05f-113">Array of vertex-shader samplers.</span></span> <span data-ttu-id="4d05f-114">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.</span><span class="sxs-lookup"><span data-stu-id="4d05f-114">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-115">**всшадерресаурцес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-115">**VSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-116">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-116">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-117">Массив ресурсов шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="4d05f-117">Array of vertex-shader resources.</span></span> <span data-ttu-id="4d05f-118">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d05f-118">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-119">**всконстантбуфферс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-119">**VSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-120">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-120">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-121">Массив константных буферов вершинного шейдера.</span><span class="sxs-lookup"><span data-stu-id="4d05f-121">Array of vertex-shader constant buffers.</span></span> <span data-ttu-id="4d05f-122">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот буфера константы.</span><span class="sxs-lookup"><span data-stu-id="4d05f-122">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-123">**всинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-123">**VSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-124">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-124">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-125">Массив интерфейсов вершинного шейдера.</span><span class="sxs-lookup"><span data-stu-id="4d05f-125">Array of vertex-shader interfaces.</span></span> <span data-ttu-id="4d05f-126">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4d05f-126">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-127">**HS**</span><span class="sxs-lookup"><span data-stu-id="4d05f-127">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-128">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-128">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-129">Логическое значение, указывающее, следует ли сохранять состояние шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="4d05f-129">Boolean value indicating whether to save the hull shader state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-130">**хссамплерс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-130">**HSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-131">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-131">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-132">Массив образцов поверхности-шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4d05f-132">Array of hull-shader samplers.</span></span> <span data-ttu-id="4d05f-133">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.</span><span class="sxs-lookup"><span data-stu-id="4d05f-133">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-134">**хсшадерресаурцес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-134">**HSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-135">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-135">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-136">Массив ресурсов поверхности-шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4d05f-136">Array of hull-shader resources.</span></span> <span data-ttu-id="4d05f-137">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d05f-137">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-138">**хсконстантбуфферс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-138">**HSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-139">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-139">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-140">Массив константных буферов поверхности-шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4d05f-140">Array of hull-shader constant buffers.</span></span> <span data-ttu-id="4d05f-141">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот буфера константы.</span><span class="sxs-lookup"><span data-stu-id="4d05f-141">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-142">**хсинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-142">**HSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-143">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-143">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-144">Массив интерфейсов поверхности-шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4d05f-144">Array of hull-shader interfaces.</span></span> <span data-ttu-id="4d05f-145">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4d05f-145">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-146">**DS**</span><span class="sxs-lookup"><span data-stu-id="4d05f-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-147">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-147">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-148">Логическое значение, указывающее, следует ли сохранять состояние шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="4d05f-148">Boolean value indicating whether to save the domain shader state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-149">**дссамплерс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-149">**DSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-150">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-150">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-151">Массив образцов шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="4d05f-151">Array of domain-shader samplers.</span></span> <span data-ttu-id="4d05f-152">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.</span><span class="sxs-lookup"><span data-stu-id="4d05f-152">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-153">**дсшадерресаурцес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-153">**DSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-154">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-154">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-155">Массив ресурсов шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="4d05f-155">Array of domain-shader resources.</span></span> <span data-ttu-id="4d05f-156">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d05f-156">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-157">**дсконстантбуфферс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-157">**DSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-158">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-158">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-159">Массив константных буферов шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="4d05f-159">Array of domain-shader constant buffers.</span></span> <span data-ttu-id="4d05f-160">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один буферный слот.</span><span class="sxs-lookup"><span data-stu-id="4d05f-160">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-161">**дсинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-161">**DSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-162">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-162">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-163">Массив интерфейсов шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="4d05f-163">Array of domain-shader interfaces.</span></span> <span data-ttu-id="4d05f-164">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4d05f-164">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-165">**GS**</span><span class="sxs-lookup"><span data-stu-id="4d05f-165">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-166">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-166">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-167">Логическое значение, указывающее, следует ли сохранять состояние шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="4d05f-167">Boolean value indicating whether to save the geometry shader state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-168">**гссамплерс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-168">**GSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-169">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-169">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-170">Массив образцов шейдеров Geometry.</span><span class="sxs-lookup"><span data-stu-id="4d05f-170">Array of geometry-shader samplers.</span></span> <span data-ttu-id="4d05f-171">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.</span><span class="sxs-lookup"><span data-stu-id="4d05f-171">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-172">**гсшадерресаурцес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-172">**GSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-173">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-173">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-174">Массив ресурсов с геометрическим шейдером.</span><span class="sxs-lookup"><span data-stu-id="4d05f-174">Array of geometry-shader resources.</span></span> <span data-ttu-id="4d05f-175">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d05f-175">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-176">**гсконстантбуфферс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-176">**GSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-177">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-177">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-178">Массив константных буферов с геометрическим шейдером.</span><span class="sxs-lookup"><span data-stu-id="4d05f-178">Array of geometry-shader constant buffers.</span></span> <span data-ttu-id="4d05f-179">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один буферный слот.</span><span class="sxs-lookup"><span data-stu-id="4d05f-179">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-180">**гсинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-180">**GSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-181">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-181">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-182">Массив интерфейсов Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="4d05f-182">Array of geometry-shader interfaces.</span></span> <span data-ttu-id="4d05f-183">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4d05f-183">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-184">**PS**</span><span class="sxs-lookup"><span data-stu-id="4d05f-184">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-185">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-185">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-186">Логическое значение, указывающее, следует ли сохранять состояние шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="4d05f-186">Boolean value indicating whether to save the pixel shader state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-187">**пссамплерс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-187">**PSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-188">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-188">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-189">Массив образцов построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="4d05f-189">Array of pixel-shader samplers.</span></span> <span data-ttu-id="4d05f-190">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.</span><span class="sxs-lookup"><span data-stu-id="4d05f-190">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-191">**псшадерресаурцес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-191">**PSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-192">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-192">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-193">Массив ресурсов растрового шейдера.</span><span class="sxs-lookup"><span data-stu-id="4d05f-193">Array of pixel-shader resources.</span></span> <span data-ttu-id="4d05f-194">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d05f-194">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-195">**псконстантбуфферс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-195">**PSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-196">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-196">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-197">Массив константных буферов построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="4d05f-197">Array of pixel-shader constant buffers.</span></span> <span data-ttu-id="4d05f-198">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот буфера константы.</span><span class="sxs-lookup"><span data-stu-id="4d05f-198">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-199">**псинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-199">**PSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-200">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-200">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-201">Массив интерфейсов построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="4d05f-201">Array of pixel-shader interfaces.</span></span> <span data-ttu-id="4d05f-202">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4d05f-202">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-203">**псунордередакцессвиевс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-203">**PSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-204">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-204">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-205">Логическое значение, указывающее, следует ли сохранять неупорядоченные представления доступа шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="4d05f-205">Boolean value indicating whether to save the pixel shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-206">**CS**</span><span class="sxs-lookup"><span data-stu-id="4d05f-206">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-207">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-207">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-208">Логическое значение, указывающее, следует ли сохранять состояние шейдера вычислений.</span><span class="sxs-lookup"><span data-stu-id="4d05f-208">Boolean value indicating whether to save the compute shader state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-209">**кссамплерс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-209">**CSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-210">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-210">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-211">Массив пробных шейдеров COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="4d05f-211">Array of compute-shader samplers.</span></span> <span data-ttu-id="4d05f-212">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот пробы.</span><span class="sxs-lookup"><span data-stu-id="4d05f-212">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-213">**ксшадерресаурцес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-213">**CSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-214">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-214">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-215">Массив ресурсов COMPUTE-Shader.</span><span class="sxs-lookup"><span data-stu-id="4d05f-215">Array of compute-shader resources.</span></span> <span data-ttu-id="4d05f-216">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d05f-216">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-217">**ксконстантбуфферс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-217">**CSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-218">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-218">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-219">Массив константных буферов COMPUTE-Shader.</span><span class="sxs-lookup"><span data-stu-id="4d05f-219">Array of compute-shader constant buffers.</span></span> <span data-ttu-id="4d05f-220">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот буфера константы.</span><span class="sxs-lookup"><span data-stu-id="4d05f-220">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-221">**ксинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="4d05f-221">**CSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-222">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-222">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-223">Массив интерфейсов COMPUTE-Shader.</span><span class="sxs-lookup"><span data-stu-id="4d05f-223">Array of compute-shader interfaces.</span></span> <span data-ttu-id="4d05f-224">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4d05f-224">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-225">**ксунордередакцессвиевс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-225">**CSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-226">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-226">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-227">Логическое значение, указывающее, следует ли сохранять неупорядоченные представления доступа "вычисление шейдеров".</span><span class="sxs-lookup"><span data-stu-id="4d05f-227">Boolean value indicating whether to save the compute shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-228">**иавертексбуфферс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-228">**IAVertexBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-229">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-229">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-230">Массив буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="4d05f-230">Array of vertex buffers.</span></span> <span data-ttu-id="4d05f-231">Массив представляет собой многобайтовую битовую маску, где каждый бит представляет один слот ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d05f-231">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-232">**иаиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="4d05f-232">**IAIndexBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-233">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-233">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-234">Логическое значение, указывающее, следует ли сохранять состояние буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="4d05f-234">Boolean value indicating whether to save the index buffer state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-235">**иаинпутлайаут**</span><span class="sxs-lookup"><span data-stu-id="4d05f-235">**IAInputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-236">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-236">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-237">Логическое значение, указывающее, следует ли сохранять состояние макета входных данных.</span><span class="sxs-lookup"><span data-stu-id="4d05f-237">Boolean value indicating whether to save the input layout state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-238">**иапримитиветопологи**</span><span class="sxs-lookup"><span data-stu-id="4d05f-238">**IAPrimitiveTopology**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-239">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-239">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-240">Логическое значение, указывающее, следует ли сохранять состояние простой топологии.</span><span class="sxs-lookup"><span data-stu-id="4d05f-240">Boolean value indicating whether to save the primitive topology state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-241">**омрендертаржетс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-241">**OMRenderTargets**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-242">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-242">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-243">Логическое значение, указывающее, следует ли сохранять состояния целевых объектов рендеринга.</span><span class="sxs-lookup"><span data-stu-id="4d05f-243">Boolean value indicating whether to save the render targets states.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-244">**омдепсстенЦилстате**</span><span class="sxs-lookup"><span data-stu-id="4d05f-244">**OMDepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-245">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-245">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-246">Логическое значение, указывающее, следует ли сохранять состояние шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="4d05f-246">Boolean value indicating whether to save the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-247">**омблендстате**</span><span class="sxs-lookup"><span data-stu-id="4d05f-247">**OMBlendState**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-248">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-248">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-249">Логическое значение, указывающее, следует ли сохранять состояние смешения.</span><span class="sxs-lookup"><span data-stu-id="4d05f-249">Boolean value indicating whether to save the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-250">**рсвиевпортс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-250">**RSViewports**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-251">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-251">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-252">Логическое значение, указывающее, следует ли сохранять состояния окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="4d05f-252">Boolean value indicating whether to save the viewports states.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-253">**рссЦиссорректс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-253">**RSScissorRects**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-254">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-254">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-255">Логическое значение, указывающее, следует ли сохранять состояния прямоугольных прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="4d05f-255">Boolean value indicating whether to save the scissor rectangles states.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-256">**рсрастеризерстате**</span><span class="sxs-lookup"><span data-stu-id="4d05f-256">**RSRasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-257">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-257">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-258">Логическое значение, указывающее, следует ли сохранять состояние средства программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="4d05f-258">Boolean value indicating whether to save the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-259">**собуфферс**</span><span class="sxs-lookup"><span data-stu-id="4d05f-259">**SOBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-260">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-260">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-261">Логическое значение, указывающее, следует ли сохранять состояния буферов потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="4d05f-261">Boolean value indicating whether to save the stream-out buffers states.</span></span>

</dd> <dt>

<span data-ttu-id="4d05f-262">**Предикация**</span><span class="sxs-lookup"><span data-stu-id="4d05f-262">**Predication**</span></span>
</dt> <dd>

<span data-ttu-id="4d05f-263">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d05f-263">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4d05f-264">Логическое значение, указывающее, следует ли сохранять состояние затенения.</span><span class="sxs-lookup"><span data-stu-id="4d05f-264">Boolean value indicating whether to save the predication state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d05f-265">Примечания</span><span class="sxs-lookup"><span data-stu-id="4d05f-265">Remarks</span></span>

<span data-ttu-id="4d05f-266">Маска блока состояния указывает на то, что устройство изменило метод передачи или приема.</span><span class="sxs-lookup"><span data-stu-id="4d05f-266">A state-block mask indicates the device states that a pass or a technique changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d05f-267">Требования</span><span class="sxs-lookup"><span data-stu-id="4d05f-267">Requirements</span></span>



| <span data-ttu-id="4d05f-268">Требование</span><span class="sxs-lookup"><span data-stu-id="4d05f-268">Requirement</span></span> | <span data-ttu-id="4d05f-269">Значение</span><span class="sxs-lookup"><span data-stu-id="4d05f-269">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d05f-270">Header</span><span class="sxs-lookup"><span data-stu-id="4d05f-270">Header</span></span><br/> | <dl> <span data-ttu-id="4d05f-271"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d05f-271"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d05f-272">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d05f-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d05f-273">Эффекты с 11 по структурам</span><span class="sxs-lookup"><span data-stu-id="4d05f-273">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

