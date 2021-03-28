---
title: текслдд-PS
description: Выбор текстуры с дополнительными входными данными градиента.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104412988"
---
# <a name="texldd---ps"></a><span data-ttu-id="cd791-103">текслдд-PS</span><span class="sxs-lookup"><span data-stu-id="cd791-103">texldd - ps</span></span>

<span data-ttu-id="cd791-104">Выбор текстуры с дополнительными входными данными градиента.</span><span class="sxs-lookup"><span data-stu-id="cd791-104">Samples a texture with additional gradient inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd791-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd791-105">Syntax</span></span>



| <span data-ttu-id="cd791-106">текслдд, DST, src0, src1, src2, src3</span><span class="sxs-lookup"><span data-stu-id="cd791-106">texldd, dst, src0, src1, src2, src3</span></span> |
|-------------------------------------|



 

<span data-ttu-id="cd791-107">Где:</span><span class="sxs-lookup"><span data-stu-id="cd791-107">Where:</span></span>

-   <span data-ttu-id="cd791-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="cd791-108">dst is a destination register.</span></span>
-   <span data-ttu-id="cd791-109">src0 — это исходный регистр, предоставляющий координаты текстуры для образца текстуры.</span><span class="sxs-lookup"><span data-stu-id="cd791-109">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="cd791-110">См. раздел [регистрация координат текстуры](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="cd791-110">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="cd791-111">src1 идентифицирует регистры исходного образца \# , где \# указывает, какой номер образца текстуры следует вычислить.</span><span class="sxs-lookup"><span data-stu-id="cd791-111">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="cd791-112">Этот образец связан с текстурой и состоянием элемента управления, определенным перечислением [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (например,</span><span class="sxs-lookup"><span data-stu-id="cd791-112">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (ex.</span></span> <span data-ttu-id="cd791-113">D3DSAMP \_ минфилтер).</span><span class="sxs-lookup"><span data-stu-id="cd791-113">D3DSAMP\_MINFILTER).</span></span>
-   <span data-ttu-id="cd791-114">src2 — это регистр источника входных данных, указывающий градиентный x.</span><span class="sxs-lookup"><span data-stu-id="cd791-114">src2 is an input source register that specifies the x gradient.</span></span>
-   <span data-ttu-id="cd791-115">src3 — это регистр источника входных данных, указывающий градиент по оси y.</span><span class="sxs-lookup"><span data-stu-id="cd791-115">src3 is an input source register that specifies the y gradient.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd791-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="cd791-116">Remarks</span></span>



| <span data-ttu-id="cd791-117">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="cd791-117">Pixel shader versions</span></span> | <span data-ttu-id="cd791-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="cd791-118">1\_1</span></span> | <span data-ttu-id="cd791-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="cd791-119">1\_2</span></span> | <span data-ttu-id="cd791-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="cd791-120">1\_3</span></span> | <span data-ttu-id="cd791-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="cd791-121">1\_4</span></span> | <span data-ttu-id="cd791-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd791-122">2\_0</span></span> | <span data-ttu-id="cd791-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cd791-123">2\_x</span></span> | <span data-ttu-id="cd791-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cd791-124">2\_sw</span></span> | <span data-ttu-id="cd791-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd791-125">3\_0</span></span> | <span data-ttu-id="cd791-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cd791-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="cd791-127">текслдд</span><span class="sxs-lookup"><span data-stu-id="cd791-127">texldd</span></span>                |      |      |      |      |      | <span data-ttu-id="cd791-128">x \*</span><span class="sxs-lookup"><span data-stu-id="cd791-128">x \*</span></span> | <span data-ttu-id="cd791-129">x</span><span class="sxs-lookup"><span data-stu-id="cd791-129">x</span></span>     | <span data-ttu-id="cd791-130">x</span><span class="sxs-lookup"><span data-stu-id="cd791-130">x</span></span>    | <span data-ttu-id="cd791-131">x</span><span class="sxs-lookup"><span data-stu-id="cd791-131">x</span></span>     |



 

<span data-ttu-id="cd791-132">\* Эта инструкция поддерживается только PS \_ 2 \_ a.</span><span class="sxs-lookup"><span data-stu-id="cd791-132">\* This instruction is only supported by ps\_2\_a.</span></span> <span data-ttu-id="cd791-133">Он не поддерживается PS \_ 2 \_ b.</span><span class="sxs-lookup"><span data-stu-id="cd791-133">It is not supported by ps\_2\_b.</span></span> <span data-ttu-id="cd791-134">Дополнительные сведения о профилях см. в разделе [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="cd791-134">For more information about profiles, see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span></span>

<span data-ttu-id="cd791-135">В этой инструкции показана текстура с помощью координат текстуры на src0, образца, определяемого src1, а также градиентов ДСКС и ДСИ, поступающих из src2 и src3.</span><span class="sxs-lookup"><span data-stu-id="cd791-135">This instruction samples a texture using the texture coordinates at src0, the sampler specified by src1, and the gradients DSX and DSY coming from src2 and src3.</span></span> <span data-ttu-id="cd791-136">Значения градиента x и y используются для выбора соответствующего уровня mipmap текстуры для выборки.</span><span class="sxs-lookup"><span data-stu-id="cd791-136">The x and y gradient values are used to select the appropriate mipmap level of the texture for sampling.</span></span>

<span data-ttu-id="cd791-137">Все источники поддерживают произвольный свиззлес.</span><span class="sxs-lookup"><span data-stu-id="cd791-137">All sources support arbitrary swizzles.</span></span>

<span data-ttu-id="cd791-138">Все маски записи допустимы в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="cd791-138">All write masks are valid on the destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd791-139">См. также</span><span class="sxs-lookup"><span data-stu-id="cd791-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd791-140">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="cd791-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 