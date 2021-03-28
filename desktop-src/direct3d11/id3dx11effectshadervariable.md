---
title: Интерфейс ID3DX11EffectShaderVariable (D3dx11effect. h)
description: Интерфейс переменной шейдера обращается к переменной шейдера.
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb011591f715b4bac57dfa34f640ea90278f6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998438"
---
# <a name="id3dx11effectshadervariable-interface"></a><span data-ttu-id="13396-105">Интерфейс ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="13396-105">ID3DX11EffectShaderVariable interface</span></span>

<span data-ttu-id="13396-106">Интерфейс переменной шейдера обращается к переменной шейдера.</span><span class="sxs-lookup"><span data-stu-id="13396-106">A shader-variable interface accesses a shader variable.</span></span>

## <a name="members"></a><span data-ttu-id="13396-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="13396-107">Members</span></span>

<span data-ttu-id="13396-108">Интерфейс **ID3DX11EffectShaderVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="13396-108">The **ID3DX11EffectShaderVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="13396-109">**ID3DX11EffectShaderVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="13396-109">**ID3DX11EffectShaderVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="13396-110">Методы</span><span class="sxs-lookup"><span data-stu-id="13396-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="13396-111">Методы</span><span class="sxs-lookup"><span data-stu-id="13396-111">Methods</span></span>

<span data-ttu-id="13396-112">Интерфейс **ID3DX11EffectShaderVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="13396-112">The **ID3DX11EffectShaderVariable** interface has these methods.</span></span>



| <span data-ttu-id="13396-113">Метод</span><span class="sxs-lookup"><span data-stu-id="13396-113">Method</span></span>                                                                                                           | <span data-ttu-id="13396-114">Описание</span><span class="sxs-lookup"><span data-stu-id="13396-114">Description</span></span>                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="13396-115">**жеткомпутешадер**</span><span class="sxs-lookup"><span data-stu-id="13396-115">**GetComputeShader**</span></span>](id3dx11effectshadervariable-getcomputeshader.md)                                         | <span data-ttu-id="13396-116">Получение шейдера вычислений.</span><span class="sxs-lookup"><span data-stu-id="13396-116">Get a compute shader.</span></span><br/>                       |
| [<span data-ttu-id="13396-117">**жетдомаиншадер**</span><span class="sxs-lookup"><span data-stu-id="13396-117">**GetDomainShader**</span></span>](id3dx11effectshadervariable-getdomainshader.md)                                           | <span data-ttu-id="13396-118">Получите шейдер домена.</span><span class="sxs-lookup"><span data-stu-id="13396-118">Get a domain shader.</span></span><br/>                        |
| [<span data-ttu-id="13396-119">**жетжеометришадер**</span><span class="sxs-lookup"><span data-stu-id="13396-119">**GetGeometryShader**</span></span>](id3dx11effectshadervariable-getgeometryshader.md)                                       | <span data-ttu-id="13396-120">Получение шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="13396-120">Get a geometry shader.</span></span><br/>                      |
| [<span data-ttu-id="13396-121">**жесуллшадер**</span><span class="sxs-lookup"><span data-stu-id="13396-121">**GetHullShader**</span></span>](id3dx11effectshadervariable-gethullshader.md)                                               | <span data-ttu-id="13396-122">Получите шейдер поверхности.</span><span class="sxs-lookup"><span data-stu-id="13396-122">Get a hull shader.</span></span><br/>                          |
| [<span data-ttu-id="13396-123">**жетинпутсигнатурилементдеск**</span><span class="sxs-lookup"><span data-stu-id="13396-123">**GetInputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | <span data-ttu-id="13396-124">Получить описание входной подписи.</span><span class="sxs-lookup"><span data-stu-id="13396-124">Get an input-signature description.</span></span><br/>         |
| [<span data-ttu-id="13396-125">**жетаутпутсигнатурилементдеск**</span><span class="sxs-lookup"><span data-stu-id="13396-125">**GetOutputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | <span data-ttu-id="13396-126">Получение описания выходной подписи.</span><span class="sxs-lookup"><span data-stu-id="13396-126">Get an output-signature description.</span></span><br/>        |
| [<span data-ttu-id="13396-127">**жетпатчконстантсигнатурилементдеск**</span><span class="sxs-lookup"><span data-stu-id="13396-127">**GetPatchConstantSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | <span data-ttu-id="13396-128">Получить описание подписи константы исправлений.</span><span class="sxs-lookup"><span data-stu-id="13396-128">Get a patch constant signature description.</span></span><br/> |
| [<span data-ttu-id="13396-129">**жетпикселшадер**</span><span class="sxs-lookup"><span data-stu-id="13396-129">**GetPixelShader**</span></span>](id3dx11effectshadervariable-getpixelshader.md)                                             | <span data-ttu-id="13396-130">Получение шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="13396-130">Get a pixel shader.</span></span><br/>                         |
| [<span data-ttu-id="13396-131">**жетшадердеск**</span><span class="sxs-lookup"><span data-stu-id="13396-131">**GetShaderDesc**</span></span>](id3dx11effectshadervariable-getshaderdesc.md)                                               | <span data-ttu-id="13396-132">Получение описания шейдера.</span><span class="sxs-lookup"><span data-stu-id="13396-132">Get a shader description.</span></span><br/>                   |
| [<span data-ttu-id="13396-133">**жетвертексшадер**</span><span class="sxs-lookup"><span data-stu-id="13396-133">**GetVertexShader**</span></span>](id3dx11effectshadervariable-getvertexshader.md)                                           | <span data-ttu-id="13396-134">Получение шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="13396-134">Get a vertex shader.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="13396-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="13396-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="13396-136">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="13396-136">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="13396-137">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="13396-137">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="13396-138">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="13396-138">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="13396-139">Требования</span><span class="sxs-lookup"><span data-stu-id="13396-139">Requirements</span></span>



| <span data-ttu-id="13396-140">Требование</span><span class="sxs-lookup"><span data-stu-id="13396-140">Requirement</span></span> | <span data-ttu-id="13396-141">Значение</span><span class="sxs-lookup"><span data-stu-id="13396-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13396-142">Header</span><span class="sxs-lookup"><span data-stu-id="13396-142">Header</span></span><br/>  | <dl> <span data-ttu-id="13396-143"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="13396-143"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="13396-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13396-144">Library</span></span><br/> | <dl> <span data-ttu-id="13396-145"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="13396-145"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13396-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13396-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13396-147">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="13396-147">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="13396-148">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="13396-148">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="13396-149">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="13396-149">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





