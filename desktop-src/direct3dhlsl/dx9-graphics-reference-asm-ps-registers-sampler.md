---
title: Образцы (Direct3D 9 ASM-PS)
description: Образец — это входная псевдо-регистрация для построителя текстуры, которая используется для указания этапа выборки.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Образец, тип (Direct3D 9 ASM-PS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070182"
---
# <a name="sampler-direct3d-9-asm-ps"></a><span data-ttu-id="4c2ec-104">Образцы (Direct3D 9 ASM-PS)</span><span class="sxs-lookup"><span data-stu-id="4c2ec-104">Sampler (Direct3D 9 asm-ps)</span></span>

<span data-ttu-id="4c2ec-105">Образец — это входная псевдо-регистрация для построителя текстуры, которая используется для указания этапа выборки.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-105">A sampler is a input pseudo-register for a pixel shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="4c2ec-106">Регистрируются журналы этапов выборки шейдеров из 16 пикселей: S0 — S15.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-106">There are 16 pixel shader sampling stage registers: s0 to s15.</span></span> <span data-ttu-id="4c2ec-107">Поэтому для одного прохода шейдера можно считать до 16 поверхностей текстуры.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-107">Therefore, up to 16 texture surfaces can be read in a single shader pass.</span></span> <span data-ttu-id="4c2ec-108">В инструкциях, использующих регистр образцов, входят текслд и текслдп.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-108">The instructions that use a sampler register are texld and texldp.</span></span>

<span data-ttu-id="4c2ec-109">Перед использованием инструкции [дкл \_ самплертипе (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) необходимо объявить образец.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-109">Sampler must be declared before use with the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>



| <span data-ttu-id="4c2ec-110">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="4c2ec-110">Pixel shader versions</span></span> | <span data-ttu-id="4c2ec-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="4c2ec-111">1\_1</span></span> | <span data-ttu-id="4c2ec-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="4c2ec-112">1\_2</span></span> | <span data-ttu-id="4c2ec-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4c2ec-113">1\_3</span></span> | <span data-ttu-id="4c2ec-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="4c2ec-114">1\_4</span></span> | <span data-ttu-id="4c2ec-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4c2ec-115">2\_0</span></span> | <span data-ttu-id="4c2ec-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4c2ec-116">2\_sw</span></span> | <span data-ttu-id="4c2ec-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4c2ec-117">2\_x</span></span> | <span data-ttu-id="4c2ec-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4c2ec-118">3\_0</span></span> | <span data-ttu-id="4c2ec-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4c2ec-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="4c2ec-120">Образец</span><span class="sxs-lookup"><span data-stu-id="4c2ec-120">Sampler</span></span>               |      |      |      |      | <span data-ttu-id="4c2ec-121">x</span><span class="sxs-lookup"><span data-stu-id="4c2ec-121">x</span></span>    | <span data-ttu-id="4c2ec-122">x</span><span class="sxs-lookup"><span data-stu-id="4c2ec-122">x</span></span>     | <span data-ttu-id="4c2ec-123">x</span><span class="sxs-lookup"><span data-stu-id="4c2ec-123">x</span></span>    | <span data-ttu-id="4c2ec-124">x</span><span class="sxs-lookup"><span data-stu-id="4c2ec-124">x</span></span>    | <span data-ttu-id="4c2ec-125">x</span><span class="sxs-lookup"><span data-stu-id="4c2ec-125">x</span></span>     |



 

<span data-ttu-id="4c2ec-126">Пробы являются псевдо-регистром, так как вы не можете напрямую считывать их или записывать.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-126">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="4c2ec-127">Единица выборки соответствует этапу выборки текстуры с инкапсуляцией состояния, зависящего от выборки, предоставляемого [**сетсамплерстате**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="4c2ec-127">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="4c2ec-128">Каждая выборка уникально определяет одну текстурную поверхность, которая устанавливается в соответствующий образец с помощью [**сеттекстуре**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="4c2ec-128">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="4c2ec-129">Однако одну и ту же поверхность текстуры можно задать в нескольких пробах.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-129">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="4c2ec-130">Во время рисования текстуру нельзя одновременно задать как цель рендеринга и текстуру на этапе.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-130">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="4c2ec-131">Образец может отображаться в виде единственного аргумента в инструкции загрузки текстуры: [текслдл-PS](texldl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="4c2ec-131">A sampler might appear as the only argument in the texture load instruction: [texldl - ps](texldl---ps.md).</span></span>

<span data-ttu-id="4c2ec-132">В PS \_ 3 \_ 0, если используется образец, его необходимо объявить в начале программы шейдера с помощью инструкции [дкл \_ самплертипе (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="4c2ec-132">In ps\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>

<span data-ttu-id="4c2ec-133">Выборка текстуры с более высоким измерением, чем имеется в координатах текстуры, недопустима.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-133">Sampling a texture with a higher dimension than is present in the texture coordinates is illegal.</span></span> <span data-ttu-id="4c2ec-134">Выборка текстуры с меньшим измерением, чем есть в координатах текстуры, будет игнорировать дополнительные координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="4c2ec-134">Sampling a texture with a lower dimension than is present in the texture coordinates will ignore the extra texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c2ec-135">См. также</span><span class="sxs-lookup"><span data-stu-id="4c2ec-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c2ec-136">Регистры</span><span class="sxs-lookup"><span data-stu-id="4c2ec-136">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 