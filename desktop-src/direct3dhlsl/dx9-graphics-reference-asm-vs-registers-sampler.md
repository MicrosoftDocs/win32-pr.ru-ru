---
title: Образцы (Direct3D 9 ASM-VS)
description: Образец — это входная псевдо-регистрация для шейдера вершин, которая используется для указания этапа выборки. Есть четыре пробы шейдера вершин с S0 по S3. Для одного прохода шейдера можно считать четыре поверхности текстуры.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Образец, тип (Direct3D 9 ASM-VS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413613"
---
# <a name="sampler-direct3d-9-asm-vs"></a><span data-ttu-id="02a3d-106">Образцы (Direct3D 9 ASM-VS)</span><span class="sxs-lookup"><span data-stu-id="02a3d-106">Sampler (Direct3D 9 asm-vs)</span></span>

<span data-ttu-id="02a3d-107">Образец — это входная псевдо-регистрация для шейдера вершин, которая используется для указания этапа выборки.</span><span class="sxs-lookup"><span data-stu-id="02a3d-107">A sampler is a input pseudo-register for a vertex shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="02a3d-108">Существует четыре пробных шейдера вершин: S0 — S3.</span><span class="sxs-lookup"><span data-stu-id="02a3d-108">There are four vertex shader samplers: s0 to s3.</span></span> <span data-ttu-id="02a3d-109">Для одного прохода шейдера можно считать четыре поверхности текстуры.</span><span class="sxs-lookup"><span data-stu-id="02a3d-109">Four texture surfaces can be read in a single shader pass.</span></span>

<span data-ttu-id="02a3d-110">Образцы (Direct3D 9 ASM-VS) s являются псевдо, так как вы не можете напрямую читать их или записывать.</span><span class="sxs-lookup"><span data-stu-id="02a3d-110">Sampler (Direct3D 9 asm-vs)s are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="02a3d-111">Единица выборки соответствует этапу выборки текстуры с инкапсуляцией состояния, зависящего от выборки, предоставляемого [**сетсамплерстате**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="02a3d-111">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="02a3d-112">Каждая выборка уникально определяет одну текстурную поверхность, которая устанавливается в соответствующий образец с помощью [**сеттекстуре**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="02a3d-112">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="02a3d-113">Однако одну и ту же поверхность текстуры можно задать в нескольких пробах.</span><span class="sxs-lookup"><span data-stu-id="02a3d-113">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="02a3d-114">Во время рисования текстуру нельзя одновременно задать как цель рендеринга и текстуру на этапе.</span><span class="sxs-lookup"><span data-stu-id="02a3d-114">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="02a3d-115">Поскольку существует четыре пробы, можно считывать до четырех поверхностей текстуры из одного прохода шейдера.</span><span class="sxs-lookup"><span data-stu-id="02a3d-115">Because there are four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="02a3d-116">Образец может отображаться в виде единственного аргумента в инструкции загрузки текстуры: [текслдл-VS](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="02a3d-116">A sampler might appear as the only argument in the texture load instruction: [texldl - vs](texldl---vs.md).</span></span>

<span data-ttu-id="02a3d-117">В VS \_ 3 \_ 0, если используется образец, его необходимо объявить в начале программы шейдера с помощью инструкции [дкл \_ самплертипе (SM3-VS ASM)](dcl-samplertype---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="02a3d-117">In vs\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md) instruction.</span></span>



| <span data-ttu-id="02a3d-118">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="02a3d-118">Vertex shader versions</span></span> | <span data-ttu-id="02a3d-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="02a3d-119">1\_1</span></span> | <span data-ttu-id="02a3d-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="02a3d-120">2\_0</span></span> | <span data-ttu-id="02a3d-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="02a3d-121">2\_sw</span></span> | <span data-ttu-id="02a3d-122">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="02a3d-122">2\_x</span></span> | <span data-ttu-id="02a3d-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="02a3d-123">3\_0</span></span> | <span data-ttu-id="02a3d-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="02a3d-124">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="02a3d-125">Образец</span><span class="sxs-lookup"><span data-stu-id="02a3d-125">Sampler</span></span>                |      |      |       |      | <span data-ttu-id="02a3d-126">x</span><span class="sxs-lookup"><span data-stu-id="02a3d-126">x</span></span>    | <span data-ttu-id="02a3d-127">x</span><span class="sxs-lookup"><span data-stu-id="02a3d-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="02a3d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="02a3d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02a3d-129">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="02a3d-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[<span data-ttu-id="02a3d-130">Текстуры вершин в VS \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="02a3d-130">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 